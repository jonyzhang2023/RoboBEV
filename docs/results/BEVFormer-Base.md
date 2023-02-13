<img src="../figs/logo.png" align="right" width="10%">

# RoboDet Benchmark

The official [nuScenes metric](https://www.nuscenes.org/object-detection/?externalData=all&mapData=all&modalities=Any) are considered in our benchmark:

- **Average Translation Error (ATE)** is the Euclidean center distance in 2D (units in meters). 
- **Average Scale Error (ASE)** is the 3D intersection-over-union (IoU) after aligning orientation and translation (1 − IoU).
- **Average Orientation Error (AOE)** is the smallest yaw angle difference between prediction and ground truth (radians). All angles are measured on a full 360-degree period except for barriers where they are measured on a 180-degree period.
- **Average Velocity Error (AVE)** is the absolute velocity error as the L2 norm of the velocity differences in 2D (m/s).
- **Average Attribute Error (AAE)** is defined as 1 minus attribute classification accuracy (1 − acc).
- **nuScenes Detection Score (NDS)**: $$\text{NDS} = \frac{1}{10} [5\text{mAP}+\sum_{\text{mTP}\in\mathbb{TP}} (1-\min(1, \text{mTP}))]$$

## BEVFormer-Base

| **Corruption** | **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- |------- | ------- | ------- |------- | ------- | ------- |
| **Clean** |  0.5174    | 0.4164    | 0.6726     | 0.2734     | 0.3704     | 0.3941     | 0.1974     |
| **Motion Blur** | 0.2695    | 0.1531    | 0.8739     | 0.3236     | 0.6941     | 0.9334     | 0.2592     |
| **Color Quant** | 0.3509    | 0.2393    | 0.8294     | 0.2953     | 0.5200     | 0.8079     | 0.2350     |
| **Frame Lost** | 0.3017    | 0.1307    | 0.8359     | 0.3053     | 0.5262     | 0.7364     | 0.2328     |
| **Camera Crash** | 0.3154    | 0.1545    | 0.8015     | 0.2975     | 0.5031     | 0.7865     | 0.2301     |
| **Brightness** | 0.4184    | 0.3312    | 0.7457     | 0.2832     | 0.4721     | 0.7686     | 0.2024     |
| **Low Light** | 0.2961    | 0.1866    | 0.8343     | 0.3101     | 0.6297     | 0.9348     | 0.2644     |
| **Fog** | 0.4069    | 0.3141    | 0.7627     | 0.2837     | 0.4711     | 0.7798     | 0.2046     |
| **Snow** | 0.1857    | 0.0739    | 0.9405     | 0.3966     | 0.7806     | 1.0880     | 0.3951     |

## Experiment Log

Time: Sun Feb 12 21:42:23 2023

### Evaluating MotionBlur

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3918    | 0.2968    | 0.7602     | 0.2859     | 0.5047     | 0.7998     | 0.2152     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2311    | 0.1022    | 0.8999     | 0.3276     | 0.7440     | 0.9607     | 0.2679     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.1855    | 0.0603    | 0.9615     | 0.3574     | 0.8336     | 1.0397     | 0.2944     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2695    | 0.1531    | 0.8739     | 0.3236     | 0.6941     | 0.9334     | 0.2592     |

### Evaluating Fog

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.4207    | 0.3318    | 0.7545     | 0.2806     | 0.4608     | 0.7595     | 0.1968     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.4092    | 0.3175    | 0.7601     | 0.2827     | 0.4703     | 0.7770     | 0.2051     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3906    | 0.2930    | 0.7734     | 0.2879     | 0.4822     | 0.8029     | 0.2120     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.4069    | 0.3141    | 0.7627     | 0.2837     | 0.4711     | 0.7798     | 0.2046     |

### Evaluating Snow

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2296    | 0.1060    | 0.9212     | 0.3424     | 0.6615     | 1.0302     | 0.3087     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.1702    | 0.0621    | 0.9353     | 0.4245     | 0.8143     | 1.0902     | 0.4346     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.1572    | 0.0536    | 0.9649     | 0.4229     | 0.8661     | 1.1435     | 0.4419     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.1857    | 0.0739    | 0.9405     | 0.3966     | 0.7806     | 1.0880     | 0.3951     |

### Evaluating ColorQuant

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.4323    | 0.3447    | 0.7454     | 0.2780     | 0.4292     | 0.7385     | 0.2088     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3651    | 0.2544    | 0.8038     | 0.2862     | 0.5050     | 0.7943     | 0.2318     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2553    | 0.1189    | 0.9389     | 0.3217     | 0.6257     | 0.8908     | 0.2643     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3509    | 0.2393    | 0.8294     | 0.2953     | 0.5200     | 0.8079     | 0.2350     |

### Evaluating Brightness

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.4466    | 0.3656    | 0.7313     | 0.2793     | 0.4288     | 0.7224     | 0.2001     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.4201    | 0.3316    | 0.7444     | 0.2840     | 0.4664     | 0.7612     | 0.2009     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3885    | 0.2965    | 0.7614     | 0.2862     | 0.5212     | 0.8222     | 0.2061     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.4184    | 0.3312    | 0.7457     | 0.2832     | 0.4721     | 0.7686     | 0.2024     |

### Evaluating LowLight

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3161    | 0.2098    | 0.8198     | 0.3035     | 0.6155     | 0.9016     | 0.2482     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3178    | 0.2098    | 0.8138     | 0.3028     | 0.6042     | 0.9008     | 0.2498     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2543    | 0.1402    | 0.8692     | 0.3239     | 0.6695     | 1.0020     | 0.2952     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2961    | 0.1866    | 0.8343     | 0.3101     | 0.6297     | 0.9348     | 0.2644     |

### Evaluating CameraCrash

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3719    | 0.2324    | 0.7753     | 0.2883     | 0.4503     | 0.7161     | 0.2127     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3100    | 0.1370    | 0.8431     | 0.2965     | 0.4819     | 0.7323     | 0.2315     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2643    | 0.0941    | 0.7862     | 0.3077     | 0.5772     | 0.9110     | 0.2460     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3154    | 0.1545    | 0.8015     | 0.2975     | 0.5031     | 0.7865     | 0.2301     |

### Evaluating FrameLost

#### Severity easy

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3818    | 0.2552    | 0.7683     | 0.2843     | 0.4490     | 0.7455     | 0.2110     |

#### Severity mid

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2878    | 0.1037    | 0.8411     | 0.3056     | 0.4982     | 0.7616     | 0.2345     |

#### Severity hard

Evaluating Results

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.2355    | 0.0331    | 0.8983     | 0.3259     | 0.6314     | 0.7021     | 0.2528     |

#### Average

| **NDS** | **mAP** | **mATE** | **mASE** | **mAOE** | **mAVE** | **mAAE** |
| ------- | ------- | -------- | -------- | -------- | -------- | -------- |
| 0.3017    | 0.1307    | 0.8359     | 0.3053     | 0.5262     | 0.7364     | 0.2328     |