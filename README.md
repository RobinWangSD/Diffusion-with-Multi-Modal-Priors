
# Diffusion-with-Multi-Modal-Priors

This repository contains the source code for the following paper:

[**Controllable Motion Generation via Diffusion Modal Coupling**](https://arxiv.org/abs/2503.02353v1)

Training and evaluation code will be released soon. Stay tuned!

## Validation dataset with annotated action labels
The validation dataset is located at:

```
/Diffusion-with-Multi-Modal-Priors/scenario_with_action_label/scenario_action_combo.pkl
```

This dataset accompanies the Waymo Open Motion Dataset (validation subset) and contains labeled vehicle actions. The key columns are:

- **scenario_id**  
  A unique identifier for a driving scenario in the Waymo Open Motion Dataset (validation subset).

- **speed_action_label**  
  Integer label for the vehicle’s speed behavior:
  - 1 – Accelerate
  - 2 – Decelerate
  - 3 – Maintain speed

- **steer_action_label**  
  Integer label for the vehicle’s steering behavior:
  - 0 – Go straight
  - 1 – Turn left
  - 2 – Turn right

## Getting Started

Below is a simple code snippet to help you load and explore the dataset.
```
import pickle

with open('/Diffusion-with-Multi-Modal-Priors/scenario_with_action_label/scenario_action_combo.pkl', 'rb') as f:
    scenario_data = pickle.load(f)

print(f"Loaded {len(scenario_data)} scenario tuples.")
print("Example tuple:", scenario_data[0])
```



