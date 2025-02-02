## EER Results

* Setup: fbank80, num_frms200, ArcMargin, aug_prob0.6, speed_perturb (no spec_aug)

| Model | Params | vox1-O(%)    | vox1-E(%)   | vox1-H(%)     |
|:------|--------|-----------|----------|------------|
| XVEC-TSTP-emb512 | 4.61M | 1.941   | 1.896    | 3.314    |
| ECAPA_TDNN_GLOB_c512-ASTP-emb192 | 6.19M | 1.090    | 1.207    | 2.280    |
| ECAPA_TDNN_GLOB_c1024-ASTP-emb192 | 20.76M | 1.010    | 1.070    | 1.997    |
| ResNet34-TSTP-emb256 | 6.70M | 1.000    | 1.067    | 1.990    |
| ResNet101-TSTP-emb256 | 15.95M | **0.739**    | **0.863**    | **1.562**    |

* Comparison among different augmentation methods based on ResNet34-TSTP-emb256 model

| Aug method | vox1-O(%)    | vox1-E(%)   | vox1-H(%)     |
|:------|-----------|----------|------------|
| no aug  | 1.329   | 1.354    | 2.335    |
| kaldi aug | 1.165    | 1.238    | 2.208    |
| wenet online aug | **1.000**    | **1.067**    | **1.990**    |
