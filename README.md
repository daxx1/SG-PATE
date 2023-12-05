# SG-PATE
This is the code for our paper:
《Squeezing More Utility on Privacy-Preserving Scalable Generator》
### Training 

```shell script
python main.py --checkpoint_dir [checkpoint_dir] --dataset [dataset_name] --train
```

Example of one of our best commands on MNIST:

Given eps=1, default use Fashion_mnist as  non-sensitive auxiliary data (NAD).

Default

including:

  The number of samples in NAD:2000.
  
  The anchar subspace B=20x784.
  
  The threshold of iterations Tβ (use PCA): 40.
  
  The number of  threshold W:20.
  
  The threshold q:40.
  
```shell script
python main.py --checkpoint_dir mnist_teacher_4000_z_dim_50_c_5e-5/ --teachers_batch 40 --batch_teachers 100 --dataset mnist --train --sigma_thresh 3000 --sigma 1000 --step_size 5e-5 --max_eps 1 --nopretrain --z_dim 50 --batch_size 64
```

it will generate 100,000 DP samples.
