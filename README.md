# Novel View Synthesis Using NeRF


 <div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/novel-view-synthesis/blob/master/Novel_View_Synthesis_Using_NeRF.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
 </div>


Legend has it that the artificial neural network (ANN) is infamously known as the universal approximator, which can fit any existing function. By exploiting this fact, we can build a network that approximates a function that maps spatial positions (_x_, _y_, _z_) and camera rays (these rays are acquired through calculation involving viewing directions (_θ_ (rotating along _y_ axis), _ϕ_ (rotating along _x_ axis)) and the spatial positions) to RGB pixels. Such a network, called the Neural Radiance Field, or NeRF in short, can be used to solve a problem of novel view synthesis of a scene. The network is coerced to overfit the function, which generates an RGB image. These generated images from multiple angles are then collected, rendering the 3D representation of a certain object. In this project, a buildozer from the Tiny NeRF dataset is used.


## Experiment


This [notebook](https://github.com/reshalfahsi/novel-view-synthesis/blob/master/Novel_View_Synthesis_Using_NeRF.ipynb) contains the implementation of this project.


## Result


<p align="center"> <img src="https://github.com/reshalfahsi/novel-view-synthesis/blob/master/assets/training_process.gif" alt="training_process" > <br /> The visualization of the training process. </p>



## Quantitative Result

The table below reports quantitative results of the implemented NeRF.

Metrics | Test Dataset |
------------ | ------------- |
PSNR | 17.486 |
SSIM | 0.381 |


## Evaluation Metrics Curve


<p align="center"> <img src="https://github.com/reshalfahsi/novel-view-synthesis/blob/master/assets/loss_curve.png" alt="loss_curve" > <br /> The loss curve on the train set and the validation set. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/novel-view-synthesis/blob/master/assets/psnr_curve.png" alt="psnr_curve" > <br /> PSNR curve on the train set and the validation set. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/novel-view-synthesis/blob/master/assets/ssim_curve.png" alt="ssim_curve" > <br /> SSIM curve on the train set and the validation set. </p>


## Qualitative Result

This GIF shows the qualitative result of the NeRF.

<p align="center"> <img src="https://github.com/reshalfahsi/novel-view-synthesis/blob/master/assets/qualitative_result.gif" alt="qualitative_result" > <br /> The 3D view of a buildozer viewed from _z_ = 3.5, _ϕ_ = -15°, and _θ_ = 0° to 360°. </p>


## Credit

- [3D volumetric rendering with NeRF](https://keras.io/examples/vision/nerf)
- [NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis](https://arxiv.org/pdf/2003.08934.pdf)
- [TinyNeRF dataset](https://cseweb.ucsd.edu/~viscomp/projects/LF/papers/ECCV20/nerf/tiny_nerf_data.npz)
- [PyTorch NeRF and pixelNeRF](https://github.com/airalcorn2/pytorch-nerf)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
