# PyTorch WMT14 DE-EN

Patch for PyTorch's machine translation dataset (WMT14 DE-EN). WMT14 From [Hugging Face](https://huggingface.co/datasets/wmt/wmt14)

用WMT14的数据"冒充Multi30k。

Train samples: 228000  
Validation samples: 3000  
Test samples: 3003  

To fix this, add these lines before using the dataset:

```python
from torchtext.datasets import multi30k

multi30k.URL['train'] = 'https://raw.githubusercontent.com/A11MiND/pytorch-wmt14/main/training.tar.gz'
multi30k.URL['valid'] = 'https://raw.githubusercontent.com/A11MiND/pytorch-wmt14/main/validation.tar.gz'
multi30k.URL['test'] = 'https://raw.githubusercontent.com/A11MiND/pytorch-wmt14/main/test.tar.gz'
```

### Disclaimer: All rights belong to the authors of the original dataset under the original license.
