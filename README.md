# ReinforcementLearning
## Reinforcement Learning Course
## Docker - RL & openAI Gym
### Description:
A docker environment for RL in python 3 including the OpenAI Gym toolkit
INcludes:
1. Basics: NumPy, Pandas, Scipy, Jupyter, Matplotlib
2. Deep Learning: Tensorflow, Keras
3. Reinforcement Learning: Keras-RL, baselines, TensorForce
4. Environments: AI Gym
5. Others: ipywidgets, h5py

### Docker Hub
You can directly pull the built image from Docker Hub by running

```
docker pull jaimeps/rl-gym
```

### Rendering on Jupyter notebook
The virtual frame buffer allows the video from the gym environments to be rendered on jupyter notebooks. Simple example with Breakout:

```
import gym
from IPython import display
import matplotlib.pyplot as plt
%matplotlib inline

env = gym.make('Breakout-v0')
env.reset()
for _ in range(1000):
  plt.imshow(env.render(mode='rgb_array'))
  display.clear_output(wait=True)
  display.display(plt.gcf())
  env.step(env.action_space.sample())
```

### Reference
github : https://github.com/jaimeps/docker-rl-gym
