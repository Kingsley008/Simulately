---
sidebar_position: 1
---

# Overall Comparison

Here is a table including a brief summary for physics simulators:

|  Simulator  |           Physics Engine            |          Rendering           | Sensor(CHECK) |        Dynamics        | Parallelization | Vectorization | OpenSource |
|:-----------:|:-----------------------------------:|:----------------------------:|:-------------:|:----------------------:|:---------------:|:-------------:|:----------:|
|  IsaacSim   |               PhysX 5               |  Rasterization; RayTracing   |     RGBD;     | Rigid;Soft;Cloth;Fluid |        ✔        |     GPU🟡     |     ✘      |
|  IsaacGym   |            PhysX 5, Flex            |        Rasterization;        |     RGBD;     |    Rigid;Soft;Cloth    |        ✔        |    CPU;GPU    |     ✘      |
|   SAPIEN    |            PhysX 5, Warp            | Rasterization; RayTracing⭐️; |     RGBD;     |    Rigid;Soft;Fluid    |        ✔        |     CPU;      |     ✔      |
|  Pybullet   |               Bullet                |        Rasterization;        |     RGBD;     |    Rigid;Soft;Cloth    |        ✘        |     CPU;      |     ✔      |
|   MuJoCo    |               MuJoCo                |        Rasterization;        |     RGBD;     |    Rigid;Soft;Cloth    |        ✘        |     CPU;      |     ✔      |
| CoppeliaSim | MuJoCo; Bullet; ODE; Newton; Vortex | Rasterization; RayTracing🔶; |     RGBD;     |    Rigid;Soft;Cloth    |        ✘        |     CPU;      |     ✔      |
|   Gazebo    |     Bullet; ODE; DART; Simbody      |        Rasterization;        |     RGBD;     |    Rigid;Soft;Cloth    |        ✘        |     CPU;      |     ✔      |
|   Blender   |               Bullet                |  Rasterization; RayTracing   |     RGBD;     | Rigid;Soft;Cloth;Fluid |        ✘        |     CPU;      |     ✔      |

🟡: GPU only, RTX series is required.

⭐️: RayTracing is currently not available in parallel gym-like envs.

🔶: Supported but Limited: CoppeliaSim has built-in functionality for simulating ray-tracing effects to a certain extent.
For example, it can perform ray-casting operations, which are useful for sensor simulations and collision detections.
However, this is not the same as full-fledged ray tracing for photorealistic rendering.

# Rendering

### Comparison of Rendering Speed

We build up the same environment with all the simulators. Here are the rendered images

<div style="display: flex; justify-content: center;">
  <img src="../../code/rendering/sapien/color.png" alt="Image 1" style="margin-right: 10px;">
  <img src="../../code/rendering/isaacgym/color.png" alt="Image 1" style="margin-right: 10px;">
  <img src="../../code/rendering/pybullet/color.png" alt="Image 1" style="margin-right: 10px;">
</div>


|     Simulator      | SAPIEN | IsaacGym | IsaacSim | Pybullet | MuJoCo | CoppeliaSim | Gazebo | Blender |
|:------------------:|:------:|:--------:|:--------:|:--------:|:------:|:-----------:|:------:|:-------:|
|     RGB @ FPS      | 292.16 |  785.30  |          |          |        |             |        |         |
|    Depth @ FPS     | 260.03 |  788.34  |          |          |        |             |        |         |
| Segmentation @ FPS | 279.87 |  800.20  |          |          |        |             |        |         |

### Comparison of Rendering Performance

pending...

# Parallelization

pending...

# Popularity

pending...