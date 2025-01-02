# Reinforcement Learning Magnetic Resonance Operators

Transformer based RL (PPO) for dynamic decoupling with fixed discrete action space composed of rotation operators. Prior experience with MLP and RNN (e.g., LSTM) based PPO has shown that this is a challenging problem for machine agents to learn. Moving to a transformer-based architecture may make sense in order to incorporate local and global observation space context. 

# Transformer-based PPO

`input_shape`: The shape of the input data representing the environment's state (e.g., `(observation_dim,)`).

`num_actions`: The number of possible discrete actions the agent can take. Can be obtained from gym env. This determines the size of the output layer (which will correspond to the probability or logits of taking the action).

`num_heads`: The number of attention heads in the Multi-Head Attention layer. Each attention head performs its own scaled dot-product attention, and the outputs of all the attention heads are concatenated and then projected through a linear transformation.

`num_layers`: The number of transformer layers (each layer contains Multi-Head Attention and Layer Normalization).

`units`: The dimensionality of the key and value vectors in the attention mechanism. Note, this isn't necessarily the same as the size of the observations (raw inputs): The attention mechanism requires transforming the observation space into a higher-dimensional feature space, allowing the model to focus on important features and relationships, which wouldn't be possible if Q and K were restricted to the same dimensionality as the observation space. It’s also the number of units in the hidden layers. 


This repo is a reduced edition of previous work co-written by Dionisio C., Lisando B., and Carlos M., and Keith C.
