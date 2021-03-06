# trajectory2vec

Simulation in "Trajectory clustering via deep representation learning"

## Required Packages:

Tested for following versions (Should be compatible for many lower versions):
```
Tensorflow = 2.2.0
pandas = 1.0.3, 
sklearn = 0.22.1
traj_dist = https://github.com/maikol-solis/trajectory_distance (for python2)
traj_dist = https://github.com/THinnerichs/trajectory_distance (for python3)

```


## Useage:
### simulate_data.py: 
Generating the synthetic trajectories ```'sim_trajectories'``` in ```/simulated_data/```.
Here, we only generate 30 trajectories as the sample.
### tmb2vec.py: 
Embed each trajectory to a fixed-length vector utilizing our framework. 
Five files is generated in /simulated_data/
* ```sim_trajectories_complete``` : Trajectories after attributes completion.
* ```sim_trajectories_feas``` : Elementary features computed by each pair of continuous records
* ```sim_behavior_sequences``` : Behavior sequence generated sliding windows and Feature Extraction Layer
* ```sim_normal_behavior_sequences``` : Moving behavior sequence after normalizaion
* ```sim_traj_vec_normal_reverse``` : Vector of trajectories generated by Seq2Seq Auto-Encoder Layer

### compared_methods.py:
Four distance based trajectory clustering methods(DTW, EDR, LCSS, Hausdorff) were compared with our framwork.
After compution, distance matrices are generated in ```/distances/```.

## Reference:
Besse P, Guillouet B, Loubes J M, et al. Review and perspective for
distance based trajectory clustering[J]. arXiv preprint arXiv:1508.04904, 2015.

## Citing trajectory2vec
"Yao, D., Zhang, C., Zhu, Z., Huang, J., & Bi, J. (2017, May). Trajectory clustering via deep representation learning. In Neural Networks (IJCNN), 2017 International Joint Conference on (pp. 3880-3887). IEEE."

## Update
Updated this repo to fit python3 and some other SOTA modules. 
