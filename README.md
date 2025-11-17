## Installation

```bash
conda create -n humanoid-gym python=3.8
conda activate humanoid-gym
pip install -e ../isaacgym/python
pip install -e .
```

## Usage Guide

#### Examples

```bash
python scripts/train.py --task=roban_s2_ppo --run_name v1 --num_envs 4096
python scripts/play.py --task=roban_s2_ppo --run_name v1
```
## Resuming Training and Play Specified '.pt' Version

#### Examples

```bash
python scripts/train.py --task=roban_s2_ppo --run_name v1 --num_envs 4096 --load_run --checkpoint
python scripts/play.py --task=roban_s2_ppo --run_name v1 --load_run --checkpoint
```

## Reward Visualization
```bash
tensorboard --logdir=
```

## Sim2Sim in Mujoco
```bash
python scripts/play_mujoco.py $onnx_model_path
```

## Test push disturbance in Mujoco
```bash
python scripts/test_push_disturbance.py $onnx_model_path
```