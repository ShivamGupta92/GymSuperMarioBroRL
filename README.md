# GymSuperMarioBroRL Agent

This project uses reinforcement learning to train an AI agent to play **Super Mario Bros** using **Stable-Baselines3** and **OpenAI Gym**. The agent is trained using Proximal Policy Optimization (PPO) on the **gym-super-mario-bros** environment.

## Installation

To set up the project, follow these steps:

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/super-mario-rl-agent.git
cd super-mario-rl-agent
```

### 2. Create a Python virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Running the Project
```bash
Python script will train an agent using PPO on the Super Mario Bros environment.
```

### 5. Monitor the training process with TensorBoard
```bash
tensorboard --logdir=./logs/
```

### 6. Test the trained model
Once the model is trained, you can run the following Python code to see how well your agent performs in the game:

# Load the trained model
### 7. Monitor the training process with TensorBoard
```python
model = PPO.load('thisisatestmodel')

# Start testing the trained model
state = env.reset()
while True:
    action, _ = model.predict(state)
    state, reward, done, info = env.step(action)
    if done:
        state = env.reset()
    env.render()
```  
License
This project is licensed under the MIT License - see the LICENSE file for details.
