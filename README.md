# Awesome Robot Teleoperation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of hardware, software, data formats, datasets, papers, platforms, services and job boards for teleoperating robot arms, humanoids, mobile robots and drones, and for turning those sessions into robot-learning data.

Maintained by RoboPilots, a managed teleoperation provider; we list competitors and alternatives on equal terms.

Entries are listed for what they do, not for who made them. No affiliate links. Every link was checked on 2026-11-09. Corrections and additions are welcome: see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [Teleoperation interfaces and leader arms](#teleoperation-interfaces-and-leader-arms)
  - [Leader arms and exoskeletons](#leader-arms-and-exoskeletons)
  - [Handheld and wearable capture](#handheld-and-wearable-capture)
  - [VR, XR and phone teleoperation](#vr-xr-and-phone-teleoperation)
  - [Humanoid whole-body teleoperation](#humanoid-whole-body-teleoperation)
- [Software and frameworks](#software-and-frameworks)
- [Data formats and tooling](#data-formats-and-tooling)
- [Datasets](#datasets)
- [Papers](#papers)
- [Fleet teleoperation platforms](#fleet-teleoperation-platforms)
- [Managed teleoperation and data-collection services](#managed-teleoperation-and-data-collection-services)
- [Jobs and careers](#jobs-and-careers)
- [Tools and guides](#tools-and-guides)
- [Related lists](#related-lists)

## Teleoperation interfaces and leader arms

### Leader arms and exoskeletons

- [GELLO](https://wuphilipp.github.io/gello_site/) - Low-cost 3D-printed leader arms that copy the follower's kinematics, with designs for UR5, Franka and xArm ([code](https://github.com/wuphilipp/gello_software), [paper](https://arxiv.org/abs/2309.13037)).
- [ALOHA](https://tonyzhaozh.github.io/aloha/) - Bimanual leader-follower rig on ViperX and WidowX arms, the hardware behind ACT ([code](https://github.com/tonyzhaozh/aloha), [Trossen docs](https://docs.trossenrobotics.com/aloha_docs/)).
- [ALOHA 2](https://aloha-2.github.io/) - Revised ALOHA hardware with better grippers, ergonomics and durability, plus a MuJoCo model ([paper](https://arxiv.org/abs/2405.02292)).
- [Mobile ALOHA](https://mobile-aloha.github.io/) - ALOHA on a wheeled base, with the operator tethered for whole-body teleoperation ([code](https://github.com/MarkFzp/mobile-aloha)).
- [SO-ARM100 and SO-101](https://github.com/TheRobotStudio/SO-ARM100) - Open-source low-cost follower arm with a matching leader arm, the default hardware in LeRobot tutorials ([LeRobot SO-101 guide](https://huggingface.co/docs/lerobot/so101)).
- [Koch v1.1](https://github.com/jess-moss/koch-v1-1) - Low-cost leader-follower arm pair on Dynamixel servos, supported in LeRobot.
- [AirExo](https://airexo.github.io/) - Low-cost whole-arm exoskeleton for teleoperation and for collecting demonstrations in the wild ([paper](https://arxiv.org/abs/2309.14975)).
- [ACE](https://ace-teleop.github.io/) - Cross-platform visual exoskeleton that combines arm tracking with camera-based hand tracking for dexterous teleoperation ([paper](https://arxiv.org/abs/2408.11805)).

### Handheld and wearable capture

- [UMI](https://umi-gripper.github.io/) - Universal Manipulation Interface: a handheld gripper with a wrist camera for collecting demonstrations without a robot ([code](https://github.com/real-stanford/universal_manipulation_interface)).
- [Pika](https://github.com/agilexrobotics/pika_ros) - AgileX's handheld data-collection kit (Pika Sense) with 6-DoF pose, depth, ultra-wide RGB and gripper state ([SDK](https://github.com/agilexrobotics/pika_sdk), [arm teleoperation](https://github.com/agilexrobotics/PikaAnyArm)).
- [DexCap](https://dex-cap.github.io/) - Portable motion-capture gloves and cameras for recording dexterous hand demonstrations ([code](https://github.com/j96w/DexCap)).

### VR, XR and phone teleoperation

- [Open-TeleVision](https://robot-tv.github.io/) - Immersive teleoperation with stereo active vision that follows the operator's head, over WebXR on Vision Pro or Quest ([code](https://github.com/OpenTeleVision/TeleVision)).
- [Bunny-VisionPro](https://dingry.github.io/projects/bunny_visionpro.html) - Real-time bimanual dexterous teleoperation with Apple Vision Pro and low-cost haptic feedback ([code](https://github.com/Dingry/BunnyVisionPro), [paper](https://arxiv.org/abs/2407.03162)).
- [VisionProTeleop](https://github.com/Improbable-AI/VisionProTeleop) - Streams Apple Vision Pro head, wrist and hand tracking to Python for robot control.
- [teleop](https://pypi.org/project/teleop/) - Python package that turns a phone or VR headset into a robot arm teleoperation device through WebXR ([code](https://github.com/SpesRobotics/teleop)).
- [LeRobot phone teleoperation](https://huggingface.co/docs/lerobot/phone_teleop) - Guide to driving a LeRobot-supported arm from a phone.
- [oculus_reader](https://github.com/rail-berkeley/oculus_reader) - Reads Meta Quest controller poses and buttons for robot teleoperation, used in the DROID setup.
- [xr_teleoperate](https://github.com/unitreerobotics/xr_teleoperate) - Unitree's XR teleoperation for its humanoids from Vision Pro, PICO or Quest headsets.

### Humanoid whole-body teleoperation

- [OmniH2O](https://omni.human2humanoid.com/) - Whole-body humanoid teleoperation from a VR headset, RGB camera or language, with a learned control policy ([paper](https://arxiv.org/abs/2406.08858)).
- [HumanPlus](https://humanoid-ai.github.io/) - Humanoid shadowing of a human operator from a single RGB camera, then imitation learning on the recorded data ([code](https://github.com/MarkFzp/humanplus), [paper](https://arxiv.org/abs/2406.10454)).
- [TWIST](https://yanjieze.com/TWIST/) - Teleoperated whole-body imitation system that retargets human motion capture to a humanoid ([paper](https://arxiv.org/abs/2505.02833)).

## Software and frameworks

- [LeRobot](https://github.com/huggingface/lerobot) - Hugging Face's PyTorch library for real-world robot learning: teleoperation, recording, datasets, training and policies ([docs](https://huggingface.co/docs/lerobot), [teleoperators](https://github.com/huggingface/lerobot/tree/main/src/lerobot/teleoperators)).
- [LeRobot imitation learning on real robots](https://huggingface.co/docs/lerobot/il_robots) - Step-by-step guide to teleoperating, recording episodes and training a policy.
- [phosphobot](https://github.com/phospho-app/phosphobot) - Community middleware with a web UI for controlling robots, Meta Quest teleoperation and LeRobot dataset recording.
- [Isaac Lab teleoperation and imitation learning](https://isaac-sim.github.io/IsaacLab/main/source/overview/imitation-learning/teleop_imitation.html) - Collect demonstrations in simulation with keyboard, SpaceMouse or XR devices, then augment them ([code](https://github.com/isaac-sim/IsaacLab)).
- [robosuite input devices](https://robosuite.ai/docs/modules/devices.html) - Keyboard and SpaceMouse teleoperation for MuJoCo-based manipulation tasks ([code](https://github.com/ARISE-Initiative/robosuite)).
- [MuJoCo](https://github.com/google-deepmind/mujoco) - Physics engine behind robosuite, the ALOHA 2 simulation and many teleoperation-in-simulation setups.
- [teleop_twist_keyboard](https://github.com/ros2/teleop_twist_keyboard) - ROS 2 node that turns key presses into velocity commands.
- [teleop_twist_joy](https://github.com/ros2/teleop_twist_joy) - ROS 2 node that turns gamepad input into velocity commands.
- [MoveIt Servo](https://moveit.picknik.ai/main/doc/examples/realtime_servo/realtime_servo_tutorial.html) - Real-time Cartesian and joint jogging for ROS 2 arms, a common base for SpaceMouse and VR teleoperation.
- [DROID software](https://github.com/droid-dataset/droid) - The DROID platform's Franka plus Quest teleoperation and data-collection code.
- [libfranka](https://github.com/frankarobotics/libfranka) - C++ client for Franka's real-time control interface, used by GELLO and DROID.
- [dora-rs](https://github.com/dora-rs/dora) - Low-latency dataflow middleware for robot applications, written in Rust with Python bindings.

## Data formats and tooling

- [LeRobotDataset v3](https://huggingface.co/docs/lerobot/lerobot-dataset-v3) - LeRobot's dataset format: Parquet for state and actions, MP4 for camera streams, hosted on the Hugging Face Hub.
- [LeRobot dataset visualizer](https://huggingface.co/spaces/lerobot/visualize_dataset) - Browse episodes of any LeRobot dataset on the Hub in the browser.
- [RLDS](https://github.com/google-research/rlds) - Reinforcement Learning Datasets: episode and step format on [TensorFlow Datasets](https://github.com/tensorflow/datasets), used by Open X-Embodiment.
- [rlds_dataset_builder](https://github.com/kpertsch/rlds_dataset_builder) - Template for converting your own demonstrations into RLDS.
- [HDF5](https://www.hdfgroup.org/solutions/hdf5/) - Hierarchical binary format used by ALOHA, robomimic and many lab pipelines ([h5py](https://www.h5py.org/)).
- [Zarr](https://zarr.dev/) - Chunked array storage, used by the Diffusion Policy and UMI codebases.
- [MCAP](https://mcap.dev/) - Open container format for timestamped multimodal logs, the default storage for ROS 2 bags ([code](https://github.com/foxglove/mcap)).
- [rosbag2](https://github.com/ros2/rosbag2) - ROS 2 recording and playback, with MCAP and SQLite storage plugins.
- [Foxglove](https://foxglove.dev/) - Visualization and debugging for robotics logs and live data, including MCAP and ROS.
- [Rerun](https://rerun.io/) - Open-source SDK and viewer for logging and replaying multimodal robot data ([code](https://github.com/rerun-io/rerun)).
- [any4lerobot](https://github.com/Tavish9/any4lerobot) - Utilities for LeRobot, including converters between LeRobot, RLDS and other dataset formats.

## Datasets

- [Open X-Embodiment](https://robotics-transformer-x.github.io/) - Pooled dataset of over a million trajectories from 22 robot embodiments, in RLDS ([code](https://github.com/google-deepmind/open_x_embodiment), [paper](https://arxiv.org/abs/2310.08864)).
- [DROID](https://droid-dataset.github.io/) - Large in-the-wild Franka manipulation dataset collected by teleoperation across many labs and scenes ([paper](https://arxiv.org/abs/2403.12945), [LeRobot format](https://huggingface.co/datasets/lerobot/droid_1.0.1)).
- [BridgeData V2](https://rail-berkeley.github.io/bridgedata/) - Teleoperated WidowX demonstrations across many kitchen-style environments ([code](https://github.com/rail-berkeley/bridge_data_v2), [paper](https://arxiv.org/abs/2308.12952)).
- [LeRobot datasets on the Hub](https://huggingface.co/lerobot) - Official LeRobot datasets, including ALOHA and PushT, plus [community datasets tagged LeRobot](https://huggingface.co/datasets?other=LeRobot).
- [AgiBot World](https://agibot-world.com/) - Large-scale humanoid and dual-arm manipulation dataset from AgiBot ([code](https://github.com/OpenDriveLab/AgiBot-World)).
- [RoboMIND](https://x-humanoid-robomind.github.io/) - Multi-embodiment teleoperation dataset spanning single-arm, dual-arm and humanoid robots.
- [RH20T](https://rh20t.github.io/) - Contact-rich manipulation dataset with force-torque, audio and multiple camera views.

## Papers

- [Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware](https://arxiv.org/abs/2304.13705) - Zhao et al., 2023. ALOHA and ACT ([code](https://github.com/tonyzhaozh/act)).
- [Diffusion Policy: Visuomotor Policy Learning via Action Diffusion](https://arxiv.org/abs/2303.04137) - Chi et al., 2023 ([code](https://github.com/real-stanford/diffusion_policy)).
- [AnyTeleop: A General Vision-Based Dexterous Robot Arm-Hand Teleoperation System](https://arxiv.org/abs/2307.04577) - Qin et al., 2023.
- [Mobile ALOHA: Learning Bimanual Mobile Manipulation with Low-Cost Whole-Body Teleoperation](https://arxiv.org/abs/2401.02117) - Fu, Zhao and Finn, 2024.
- [Universal Manipulation Interface](https://arxiv.org/abs/2402.10329) - Chi et al., 2024. UMI.
- [DexCap: Scalable and Portable Mocap Data Collection System for Dexterous Manipulation](https://arxiv.org/abs/2403.07788) - Wang et al., 2024.
- [Open-TeleVision: Teleoperation with Immersive Active Visual Feedback](https://arxiv.org/abs/2407.01512) - Cheng et al., 2024.
- [ALOHA Unleashed: A Simple Recipe for Robot Dexterity](https://arxiv.org/abs/2410.13126) - Zhao et al., 2024.
- [HOMIE: Humanoid Loco-Manipulation with Isomorphic Exoskeleton Cockpit](https://arxiv.org/abs/2502.13013) - Ben et al., 2025.
- [π0: A Vision-Language-Action Flow Model for General Robot Control](https://arxiv.org/abs/2410.24164) - Physical Intelligence, 2024. Trained largely on teleoperated data ([code](https://github.com/Physical-Intelligence/openpi)).
- [π0.5: a Vision-Language-Action Model with Open-World Generalization](https://arxiv.org/abs/2504.16054) - Physical Intelligence, 2025.
- [SmolVLA: A Vision-Language-Action Model for Affordable and Efficient Robotics](https://arxiv.org/abs/2506.01844) - Shukor et al., 2025. Trained on community LeRobot datasets.

## Fleet teleoperation platforms

Software for monitoring, intervening in and remotely driving fleets of deployed robots.

- [Formant](https://www.formant.ai/) - Robot operations platform for monitoring, intervention and teleoperation across fleets.
- [InOrbit](https://www.inorbit.ai/) - Robot orchestration and fleet operations platform with remote monitoring and incident handling.
- [Transitive Robotics](https://transitiverobotics.com/) - Embeddable, open-source robot capabilities for building your own fleet system, including WebRTC video and remote teleoperation.
- [Viam](https://www.viam.com/) - Robotics software platform with remote control, data capture and fleet management.
- [Ottopia](https://www.ottopia.tech/) - Teleoperation and remote-operations platform, originally for autonomous vehicles, now aimed at physical-AI fleets.
- [Teleo](https://teleo.ai/) - Retrofit kits that turn heavy construction equipment into supervised autonomous machines with remote operators.

## Managed teleoperation and data-collection services

Companies that supply the people, the data, or both. Listed alphabetically. Descriptions are based on each company's own site as of 2026-10-26; check current offerings directly.

- [AuraOne](https://auraone.ai/human-data/physical-ai) - Human data provider whose physical-AI offering includes trained operators teleoperating customer robots, human demonstration capture and episode review.
- [Claru](https://claru.ai/) - Training data provider for physical AI: egocentric and other real-world video, annotation and custom capture.
- [FS Studio](https://fsstudio.com/robotics-operations/) - Robot teleoperation, data collection and deployment support, alongside robotics simulation services.
- [Humaid](https://humaid.co/teleoperation-data-collection) - Human-in-the-loop data collection for robotics: teleoperation datasets, egocentric capture, annotation and QC.
- [OBI Services](https://obi.services/remote-robot-operators-monitoring-services/) - Philippines-based outsourcing company offering remote robot teleoperation and monitoring operators.
- [Robotics Center](https://www.roboticscenter.ai/teleop) - Robot hardware sales and leasing with a teleoperation platform, teleoperation datasets and RL environments.
- [RoboPilots](https://www.robopilots.ai/) - Managed remote operators trained on your robot; one-week trial with a clean-episodes-per-operator-hour baseline. Data delivered as LeRobot, RLDS, HDF5 or MCAP.
- [Scale AI Physical AI](https://scale.com/physical-ai) - Data engine for physical AI, with a collection network of robotics data factories and distributed collectors.

## Jobs and careers

Teleoperation roles go by several titles: robot teleoperator, data collection operator, robot operator, remote pilot and remote operator. Search for all of them.

- [LinkedIn Jobs: robot teleoperator](https://www.linkedin.com/jobs/search/?keywords=robot%20teleoperator) - Broadest listing of teleoperator and data-collection roles at robotics companies.
- [Wellfound](https://wellfound.com/jobs) - Startup job board; search it for robotics operator and teleoperator roles.
- [Y Combinator jobs](https://www.ycombinator.com/jobs) - Openings at YC-backed companies, including robotics and physical-AI startups.
- [Built In](https://builtin.com/jobs) - US tech job board; search it for robot operator roles.
- [Awesome Embodied AI Job](https://github.com/StarCycle/Awesome-Embodied-AI-Job) - Community list of embodied-AI and robotics employers and openings, with a focus on China.
- [RoboPilots careers](https://www.robopilots.ai/careers) - Remote robot operator roles at RoboPilots, including [humanoid teleoperator](https://www.robopilots.ai/careers/humanoid-robot-teleoperator) and [remote drone pilot](https://www.robopilots.ai/careers/remote-drone-pilot).

## Tools and guides

- [Teleop Latency Calculator](https://huggingface.co/spaces/robopilots-ai/teleop-latency-calculator) - Estimate round-trip latency from operator and robot locations, network and video pipeline, and see the control mode it supports per robot type.
- [Teleoperation latency guide](https://www.robopilots.ai/guides/teleoperation-latency) - How much round-trip delay each kind of task tolerates, how to measure glass-to-glass latency and how to work around delay.

## Related lists

- [awesome-humanoid-robot-learning](https://github.com/YanjieZe/awesome-humanoid-robot-learning) - Paper list for humanoid robot learning.
- [Awesome-Robot-Learning](https://github.com/RayYoh/Awesome-Robot-Learning) - Robot learning resources, mainly for manipulation.
- [awesome-embodied-vla-va-vln](https://github.com/jonyzhang2023/awesome-embodied-vla-va-vln) - Research on vision-language-action models and embodied navigation.
- [awesome-robotics-libraries](https://github.com/jslee02/awesome-robotics-libraries) - Robotics libraries and software.
- [awesome-robotics](https://github.com/kiloreux/awesome-robotics) - General robotics resources.
