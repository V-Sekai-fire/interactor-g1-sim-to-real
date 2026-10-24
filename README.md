# interactor-g1-sim-to-real

The G1 humanoid sim-to-real environment: a MuJoCo rig, its joint-range envelope, and a PPO task whose policy exports to GGUF.

## What it is for

It trains and checks locomotion policies for the G1 robot model before anything runs on hardware. The task family, the range-of-motion calibration, the convex hull pipeline and the policy export live here. RFD66606-2238 owns the design, and RFD66606-2276 builds on it.

## Build and run

The environment is declared in `pixi.toml`. `pixi install` sets it up, and the scripts run inside it with `pixi run python <script>`. Training needs a GPU the pinned torch build supports. The editable dependencies expect the workspace layout the goal manifest checks out.

## Licence

The code is Apache-2.0 (`LICENSE`). The G1 model files are BSD-3-Clause, from the MuJoCo Menagerie copy that `CITATION.cff` names.
