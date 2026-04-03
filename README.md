# PreACT_Training_Curve

The provided learning curves from the Cooperative Navigation (N=7) scenario empirically validate the dynamic consensus-building process.

- Early Training (Establishing Anchors): In the first 1M steps, both the Message Reconstruction Loss and Value Function Loss drop rapidly. This confirms that agents quickly learn to broadcast faithful, credible proposals, and the critic begins to evaluate states effectively.

- Exploration Phase: Despite the early stabilization of messages, the Action Distribution Entropy remains remarkably high (above 1.2) for the first 2.5M to 3M steps. This visualizes the entropy-dominated phase where agents actively explore different final action combinations conditioned on their teammates' credible proposals.

- Exploitation and Consensus: As training progresses past 3M steps, the growing advantage scale overtakes the entropy bonus. The Action Distribution Entropy drops precipitously (down to ~0.5), indicating that agents have discovered the optimal convention and are now confidently exploiting it. This transition directly correlates with the Team Reward, which climbs steadily during the exploration phase and smoothly plateaus as the optimal cooperative strategies are learned.
