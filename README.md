<div align="center">  
  
# Physically sound, self-learning digital twins for sloshing fluids
[![Paper](https://img.shields.io/badge/Paper-PDF-red)]()


</div>

## Abstract   

We present a learning strategy to build digital twins that emulate the sloshing dynamics of a fluid in realtime. We train a physically sound integrator from pseudo-experimental data obtained from Abaqus simulations. The model is implemented to interact online with a real glass, and presents the results of the virtual fluid with augmented reality. Realtime calculations are perfomed in a low dimensional space reached through the use of a-posteriori model order reduction techniques (k-PCA in this case). In addition, the have trained a random forest classificator from the whole dataset the learn to classidy our fluids and be able to distinguish the real liquid perceived from a few video frames. 


## Software  
_Note that off-line processing has been performed with MATLAB2017b

## Downloads
The dataset of each fluid consists of the state variables obtained from Abaqus simulations of the sloshing dynamics under different initial conditions. Four sloshing cases have been simulated for each fluid. 


- [Water](https://drive.google.com/file/d/16VxiqHZsu-Onss1g3itF0lVUy53-5mxF/view?usp=sharing)
- [Glycerine](https://drive.google.com/file/d/1UrRnkg5RcEogywZ0CgXibueb7dbP6oI5/view?usp=sharing)
- [Butter](https://drive.google.com/file/d/1-RUsZhv3NkhGE2Akui-jc2ft8MWtWz79/view?usp=sharing)
- [Blood](https://drive.google.com/file/d/1RxAaNmIPaKmEEVIXbtJU0VELjVsbf5ph/view?usp=sharing)
- [Honey](https://drive.google.com/file/d/1la4zFFemThU_f2cC4C4cSuhTCi2fSilN/view?usp=sharing)
- [Chocolate](https://drive.google.com/file/d/1o0tyFcG2meyTmgRUThGB85Njnzdk-7_w/view?usp=sharing)
- [Mayonnaise](https://drive.google.com/file/d/1hkeRwkoFSikpHhDFPxLprasyRtYyAo8Y/view?usp=sharing)



## Training the model

We have performed simulations aplying the smooth particle hydrodynamics theory. Each column vector of the matrices available corresponds to the state variables that we employ in the model at discrete time steps. These state variables are the 3D position, the 3D velocity, the internal energy, and the stress tensor evaluated at each particle. Since the fluid has been discretized in 2134 particles, the full dimensionality of the problem is 27742.


### For training each fluid's simulator

The data base is projected to a low-order manifold where we learn the GENERIC structure of the problem to perform machine learning that fulfills the first and second laws of thermodynamics.

<img width="1265" alt="video_water" src="https://user-images.githubusercontent.com/65158632/81586504-e515db80-93b5-11ea-8d11-93c700ab0f5f.png">

### For training the classificator

In this case, model order reduction techniques are applied over the whole dataset to learn a random forest classificator. 


## Results 

Please, follow the [link](https://www.youtube.com/watch?v=d1JyhPNkLkU) to the  see results video of the implementation of the digital twin.

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/65158632/81592142-c582b100-93bd-11ea-9cc8-1a781a1dd2ea.gif)

</div>

## Citation   
If you found this information useful please cite our work as:
```
@article{moya2019learning,
  title={Learning slosh dynamics by means of data},
  author={Moya, Beatriz and Gonz{\'a}lez, David and Alfaro, Ic{\'\i}ar and Chinesta, Francisco and Cueto, E},
  journal={Computational Mechanics},
  volume={64},
  number={2},
  pages={511--523},
  year={2019},
  publisher={Springer}
}
```   
