<div align="center">  
  
# Physically sound, self-learning digital twins for sloshing fluids
[![Paper](https://img.shields.io/badge/Paper-PDF-red)]()


</div>

## Abstract   

We present a learning strategy to build digital twins that emulate the sloshing dynamics of a fluid in realtime. We train a physically sound integrator from pseudo-experimental data obtained from Abaqus simulations. The model is implemented to interact online with a real glass, and present the results of the virtual fluid with augmented reality. Realtime calculations are perfomed in a low dimensional space reached through the use of a-posteriori model order reduction techniques (k-PCA).


## Software  
_Note that off-line processing has been performed with MATLAB2017b

## Downloads
The dataset of each fluid consists of the state variables measured obtained from the Abaqus simulation of the sloshing dynamics under different initial conditions. Four sloshing cases have been simulated for each fluid. 


- [Water](https://drive.google.com/file/d/16VxiqHZsu-Onss1g3itF0lVUy53-5mxF/view?usp=sharing)
- [Glycerine](https://drive.google.com/file/d/1UrRnkg5RcEogywZ0CgXibueb7dbP6oI5/view?usp=sharing)
- [Butter](https://drive.google.com/file/d/1-RUsZhv3NkhGE2Akui-jc2ft8MWtWz79/view?usp=sharing)
- [Blood](https://drive.google.com/file/d/1RxAaNmIPaKmEEVIXbtJU0VELjVsbf5ph/view?usp=sharing)
- [Honey](https://drive.google.com/file/d/1la4zFFemThU_f2cC4C4cSuhTCi2fSilN/view?usp=sharing)
- [Chocolate](https://drive.google.com/file/d/1o0tyFcG2meyTmgRUThGB85Njnzdk-7_w/view?usp=sharing)
- [Mayonnaise](https://drive.google.com/file/d/1hkeRwkoFSikpHhDFPxLprasyRtYyAo8Y/view?usp=sharing)



## Training the model

We have performed simulations aplying the smooth particle hydrodynamics theory. Each column vector of the matrices available corresponds to the state variables that we employ in the model at a discrete time step. 

Since the fluid has been discretized in 2134 particles, the full dimensionality of the problem is 27742.


### For training each fluid's simulator

The data base is projected to a low-order manifold where we learn the GENERIC structure of the problem to perform machine learning that 

### For training the classificator

In this case, MOR techniques are applied over the whole dataset. 


## Results 



[![IMAGE ALT TEXT HERE](https://www.youtube.com/watch?v=d1JyhPNkLkU
v=YOUTUBE_VIDEO_ID_HERE)



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
