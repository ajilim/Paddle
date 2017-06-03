# Audio data augmentation proces: Design doc

we are planning add audio data augmentation process to audio data provider，we augment our training data by adding noise to increase the effective size of our training data and to improve our robustness to noisy speech.

## methods
We roughly break down the agumentation methods into 6:
1. volume_change
2. speed perturbation
3. resample
4. online bayesian normalization
5. impulse response
6. walla noise

### difference
| methods | other audio |
| ------- | ----------- |
| volume change |  no   |
| speed perturbation | no |
| resample | no         |
| online bayesian | no  |
| impulse response | need |
| walla noise | need     |

## Implementation
1） audio 
   type：class
   params： samples， sample_rate
   fuction:
       augmentation function: eg. noise_add()
       read audio file: eg. wav, pcm
2) augmentation
   type: class
   abstract clase: augmentation , funciton: __init__() and transform_audio()
   6 Inheritance class ： eg. walla_noise




