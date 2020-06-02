# 3DOCT 6DoF Pose Dataset

![png](https://raw.githubusercontent.com/mlaves/3doct-pose-dataset/master/oct_datset.png)
Figure: Example image from OCT data set showing arg max projections of a surgical needle tip acquired by optical coherence tomography.

If you use this data set in your work, please cite  
*Laves, MH., Ihler, S., Fast, JF., Kahrs, LA., Ortmaier, T. Well-Calibrated Regression Uncertainty in Medical Imaging with Deep Learning. Medical Imaging with Deep Learning (MIDL), 2020.*  
[https://openreview.net/forum?id=CecZ_0t79q](https://openreview.net/forum?id=CecZ_0t79q)

## Description

This data set was created by attaching a surgical needle to a high-precision six-axis hexapod robot (H-826, Physik Instrumente GmbH & Co. KG, Germany) and observing the needle tip with 3D optical coherence tomography (OCS1300SS, Thorlabs Inc., USA). The data set consists of 5,000 OCT acquisitions with 64 × 64 × 512 voxels, covering a volume of 3 approx. 3 × 3 × 3 mm. Each acquisition is taken at a different robot configuration and labeled with the corresponding 6DoF pose. The data are characterized by a high amount of speckle noise, which is a typical phenomenon in optical coherence tomography.

You can read the data using the following Python code:

```python
import numpy as np

f = np.load("1565077565.9816186.npz")
img = f['data']
pos = f['pos']
img = img.transpose(2, 0, 1)  # permute data as it is in FORTRAN order
```

## Contact

Max-Heinrich Laves  
[laves@imes.uni-hannover.de](mailto:laves@imes.uni-hannover.de)  
[@MaxLaves](https://twitter.com/MaxLaves)

Institute of Mechatronic Systems  
Leibniz Universität Hannover  
An der Universität 1, 30823 Garbsen, Germany
