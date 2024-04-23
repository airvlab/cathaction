# CathAction PyTorch Dataset

A PyTorch Dataset for the **CathAction** datasets.

In particular, it handles **frames** and **features** (the latter provided by the RULSTM repo [[link](https://github.com/fpv-iplab/rulstm)]) for both the **Action Recognition** and the **Action Anticipation** tasks.


# Action Recognition Usage Example

```python
# Imports
from torchvision import transforms
from input_loaders import ActionRecognitionSampler, FramesLoader, FeaturesLoader, PipeLoaders
from utils import get_cath_annotation

# Create clip samples and clip loader
sampler = ActionRecognitionSampler(sample_mode='center', num_frames_per_action=16)
loader = PipeLoaders([
    FramesLoader(sampler, 'path/to/frames', fps=5.0, transform_frame=transforms.ToTensor()),
    FeaturesLoader(sampler, 'path/to/features', fps=5.0, input_name='rgb'),
])
csv = get_cath_annotation(partition='train') # Load annotations (dataframe)
ds =  CathDataset(csv, partition='train', loader=loader, task='recognition') # Create the Cath dataset

# Get sample
sample = next(iter(ds))

"""
sample['uid'] -> int
sample['frame'] -> tensor of shape [C, T, H, W]
sample['action_class'] -> int
"""

```

# Action Anticipation Usage Example

```python
# Imports
from torchvision import transforms
from input_loaders import ActionAnticipationSampler, FramesLoader, FeaturesLoader, PipeLoaders
from utils import get_cath_annotation

# Create clip samples and clip loader
sampler = ActionAnticipationSampler(t_buffer=3.5, t_ant=1.0, fps=5.0)
loader = PipeLoaders([
    FramesLoader(sampler, 'path/to/frames', fps=5.0, transform_frame=transforms.ToTensor()),
    FeaturesLoader(sampler, 'path/to/features', fps=5.0, input_name='rgb'),
])
csv = get_cath_annotation(partition='train', use_rulstm_splits=True) # Load annotations (dataframe)
ds = CathDataset(csv, partition='train', loader=loader, task='recognition') # Create the Cath dataset

# Get sample
sample = next(iter(ds))

"""
sample['uid'] -> int
sample['frame'] -> tensor of shape [C, T, H, W]
sample['action_class'] -> int
"""

```