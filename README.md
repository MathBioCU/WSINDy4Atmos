# WSINDy4Atmos <br> (Under construction!)
Weak SINDy model discovery for atmospheric data.

![changing_scales_fine](https://github.com/user-attachments/assets/ae67286a-1e1b-443a-b71c-bfdc63f2483c)

Code accompanying the pre-print paper ["Learning Weather Models from Data with Weak SINDy"](https://arxiv.org/abs/2501.00738), currently available on the ArXiV:
```
@misc{minor2025learningweathermodelsdata,
      title={Learning Weather Models from Data with WSINDy}, 
      author={Seth Minor and Daniel A. Messenger and Vanja Dukic and David M. Bortz},
      year={2025},
      eprint={2501.00738},
      archivePrefix={arXiv},
      primaryClass={physics.geo-ph},
      url={https://arxiv.org/abs/2501.00738}}
```

- See [the tutorials and examples located here](https://github.com/SethMinor/PyWSINDy-for-PDEs) for instructions on how to use the codebase.
- To recreate results in the paper, see the `wsindy_for_weather_examples.ipynb` and `full_globe_wsindy.ipynb` notebooks.

**Note:** unfortunately, our examples data files are too large host on GitHub.
Luckily, they are all publicly-available! Interested readers are directed towards the following locations:
- `barotropic`: [this PyQG example](https://pyqg.readthedocs.io/en/latest/examples/barotropic.html)
- `swe_wsindy`: [this Dedalus example](https://dedalus-project.readthedocs.io/en/latest/pages/examples/ivp_sphere_shallow_water.html)
- `stratified`: [this JHTDB simulation](https://turbulence.idies.jhu.edu/datasets/geophysicalTurbulence/sabl)
- `full_globe`: [this ERA5 data store](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-pressure-levels?tab=overview)

###### This algorithm uses the following dependencies:
```python
import torch
import scipy
import numpy as np
import itertools
import symengine as sp

import torch.linalg as la
from scipy.signal import convolve
from scipy.special import factorial
import matplotlib.pyplot as plt
from tqdm import tqdm
```
