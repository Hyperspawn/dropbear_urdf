# Dropbear URDF Repo

#### This repos contains 2 URDFs of Dropbear humanoid robot - high-fidelity and modular.

---

## Repository Structure

```
dropbear_urdf/
├── dropbear_modular_urdf/
│   ├── meshes/
│   ├── urdf/
│   ├── launch/
│   └── rviz/
├── dropbear_granular_urdf/
│   ├── meshes/
│   ├── urdf/
│   ├── launch/
│   ├── config/
│   └── rviz/
└── README.md
```

---

## Package Descriptions

### `dropbear_modular_urdf`
A clean, organized representation of Dropbear using a modular approach.
- ✅ Easier to edit or replace limbs or sections.
- ✅ Suitable for structured control and component testing.
- Includes:
  - `urdf/` with modular `.xacro` files for arms, legs, torso, etc.
  - `meshes/` with STL files
  - `launch/` for basic visualization using RViz or integration into larger systems

### `dropbear_granular_urdf`
A more granular and realistic URDF of the robot:
- ✅ Includes additional parts like internal mechanical structure and adapters
- ✅ Closer to the actual CAD model structure
- ✅ Useful for high-fidelity simulation, sim2real workflows
- Includes:
  - Fine-tuned joint definitions and inertias
  - Detailed naming convention matching internal components
  - Realistic joint placements and motor constraints

---

## 🚀 Usage

### Clone:
```bash
git clone https://github.com/Hyperspawn/dropbear_urdf
cd dropbear_urdf
```

### Build:
```bash
colcon build
source install/setup.sh
```

### Visualization in RViz:
```bash
ros2 launch dropbear_modular_urdf display.launch.py
# or
ros2 launch dropbear_granular_urdf display.launch.py
```

---

## 🧠 Applications

These URDFs for Dropbear are pretty important to get into development on the Dropbear platfrom. You can use them for:

- ✅ Reinforcement learning (Isaac Gym, Mujoco via MJCF conversion)
- ✅ Sim-to-real calibration with actual hardware
- ✅ ROS 2 controller interfacing and testing
- ✅ Motion planning (MoveIt 2 integration)
- ✅ Integration with Isaac Sim (Omniverse)
- ✅ Unity or Unreal Engine import via conversion pipelines
- ✅ Mesh editing, collision checking, kinematic tuning
  (Let me know what else you use it for)

---

## 🧰 Notes

- Both packages use consistent link naming, allowing drop-in replacement depending on use-case.
- STL meshes are scaled to meters and aligned to robot link frames.
- Inertial parameters in some links of the granular URDF may not be realistic.
- Modular version is ideal for beginner setups and fast iterations.

---

## 🔗 License

MIT License — use freely and contribute back if you make improvements!
