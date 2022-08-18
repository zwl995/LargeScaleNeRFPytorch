
Weekly Classified Neural Radiance Fields - dynamic ![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)
===================================================================================================================================================================
## Filter by classes: 
 [all](../weekly_nerf.md) | [dynamic](./dynamic.md) | [editing](./editing.md) | [fast](./fast.md) | [generalization](./generalization.md) | [human](./human.md) | [video](./video.md) | [lighting](./lighting.md) | [reconstruction](./reconstruction.md) | [texture](./texture.md) | [semantic](./semantic.md) | [pose-slam](./pose-slam.md) | [others](./others.md) 
## Jul31 - Aug6, 2022
  - [NFOMP: Neural Field for Optimal Motion Planner of Differential Drive Robots With Nonholonomic Constraints, IEEE Robotics and Automation Letters, IEEE Robotics and Automation Letters](https://ieeexplore.ieee.org/abstract/document/9851532/) | [code]
    > Optimal motion planning is one of the most critical problems in mobile robotics. On the one hand, classical sampling-based methods propose asymptotically optimal solutions to this problem. However, these planners cannot achieve smooth and short trajectories in reasonable calculation time. On the other hand, optimization-based methods are able to generate smooth and plain trajectories in a variety of scenarios, including a dense human crowd. However, modern optimization-based methods use the precomputed signed distance function for collision loss estimation, and it limits the application of these methods for general configuration spaces, including a differential drive non-circular robot with non-holonomic constraints. Moreover, optimization-based methods lack the ability to handle U-shaped or thin obstacles accurately. We propose to improve the optimization methods in two aspects. Firstly, we developed an obstacle neural field model to estimate collision loss; training this model together with trajectory optimization allows improving collision loss continuously, while achieving more feasible and smoother trajectories. Secondly, we forced the trajectory to consider non-holonomic constraints by adding Lagrange multipliers to the trajectory loss function. We applied our method for solving the optimal motion planning problem for differential drive robots with non-holonomic constraints, benchmarked our solution, and proved that the novel planner generates smooth, short, and plain trajectories perfectly suitable for a robot to follow, and outperforms the state-of-the-art approaches by 25% on normalized curvature and by 75% on the number of cusps in the MovingAI environment.
  - [Controllable Free Viewpoint Video Reconstruction Based on Neural Radiance Fields and Motion Graphs, IEEE Transactions on Visualization and Computer Graphics](https://ieeexplore.ieee.org/abstract/document/9845414) | [code]
    > In this paper, we propose a controllable high-quality free viewpoint video generation method based on the motion graph and neural radiance fields (NeRF). Different from existing pose-driven NeRF or time/structure conditioned NeRF works, we propose to first construct a directed motion graph of the captured sequence. Such a sequence-motion-parameterization strategy not only enables flexible pose control for free viewpoint video rendering but also avoids redundant calculation of similar poses and thus improves the overall reconstruction efficiency. Moreover, to support body shape control without losing the realistic free viewpoint rendering performance, we improve the vanilla NeRF by combining explicit surface deformation and implicit neural scene representations. Specifically, we train a local surface-guided NeRF for each valid frame on the motion graph, and the volumetric rendering was only performed in the local space around the real surface, thus enabling plausible shape control ability. As far as we know, our method is the first method that supports both realistic free viewpoint video reconstruction and motion graph-based user-guided motion traversal. The results and comparisons further demonstrate the effectiveness of the proposed method.
  - [Robust Change Detection Based on Neural Descriptor Fields, IROS2022](https://ieeexplore.ieee.org/abstract/document/9845414) | [code]
    > The ability to reason about changes in the environment is crucial for robots operating over extended periods of time. Agents are expected to capture changes during operation so that actions can be followed to ensure a smooth progression of the working session. However, varying viewing angles and accumulated localization errors make it easy for robots to falsely detect changes in the surrounding world due to low observation overlap and drifted object associations. In this paper, based on the recently proposed category-level Neural Descriptor Fields (NDFs), we develop an object-level online change detection approach that is robust to partially overlapping observations and noisy localization results. Utilizing the shape completion capability and SE(3)-equivariance of NDFs, we represent objects with compact shape codes encoding full object shapes from partial observations. The objects are then organized in a spatial tree structure based on object centers recovered from NDFs for fast queries of object neighborhoods. By associating objects via shape code similarity and comparing local object-neighbor spatial layout, our proposed approach demonstrates robustness to low observation overlap and localization noises. We conduct experiments on both synthetic and real-world sequences and achieve improved change detection results compared to multiple baseline methods. Project webpage: this https URL
## Jul24 - Jul30, 2022
  - [Deforming Radiance Fields with Cages, ECCV2022](https://arxiv.org/abs/2207.12298) | [code]
    > Recent advances in radiance fields enable photorealistic rendering of static or dynamic 3D scenes, but still do not support explicit deformation that is used for scene manipulation or animation. In this paper, we propose a method that enables a new type of deformation of the radiance field: free-form radiance field deformation. We use a triangular mesh that encloses the foreground object called cage as an interface, and by manipulating the cage vertices, our approach enables the free-form deformation of the radiance field. The core of our approach is cage-based deformation which is commonly used in mesh deformation. We propose a novel formulation to extend it to the radiance field, which maps the position and the view direction of the sampling points from the deformed space to the canonical space, thus enabling the rendering of the deformed scene. The deformation results of the synthetic datasets and the real-world datasets demonstrate the effectiveness of our approach.
## Previous weeks
  - [D-NeRF: Neural Radiance Fields for Dynamic Scenes, CVPR2021](https://arxiv.org/abs/2011.13961) | [***``[code]``***](https://github.com/albertpumarola/D-NeRF)
    > Neural rendering techniques combining machine learning with geometric reasoning have arisen as one of the most promising approaches for synthesizing novel views of a scene from a sparse set of images. Among these, stands out the Neural radiance fields (NeRF), which trains a deep network to map 5D input coordinates (representing spatial location and viewing direction) into a volume density and view-dependent emitted radiance. However, despite achieving an unprecedented level of photorealism on the generated images, NeRF is only applicable to static scenes, where the same spatial location can be queried from different images. In this paper we introduce D-NeRF, a method that extends neural radiance fields to a dynamic domain, allowing to reconstruct and render novel images of objects under rigid and non-rigid motions from a \emph{single} camera moving around the scene. For this purpose we consider time as an additional input to the system, and split the learning process in two main stages: one that encodes the scene into a canonical space and another that maps this canonical representation into the deformed scene at a particular time. Both mappings are simultaneously learned using fully-connected networks. Once the networks are trained, D-NeRF can render novel images, controlling both the camera view and the time variable, and thus, the object movement. We demonstrate the effectiveness of our approach on scenes with objects under rigid, articulated and non-rigid motions. Code, model weights and the dynamic scenes dataset will be released.
  - [Dynamic Neural Radiance Fields for Monocular 4D Facial Avatar Reconstruction, CVPR2021](https://gafniguy.github.io/4D-Facial-Avatars/) | [***``[code]``***](https://github.com/gafniguy/4D-Facial-Avatars)
    > We present dynamic neural radiance fields for modeling the appearance and dynamics of a human face. Digitally modeling and reconstructing a talking human is a key building-block for a variety of applications. Especially, for telepresence applications in AR or VR, a faithful reproduction of the appearance including novel viewpoint or head-poses is required. In contrast to state-of-the-art approaches that model the geometry and material properties explicitly, or are purely image-based, we introduce an implicit representation of the head based on scene representation networks. To handle the dynamics of the face, we combine our scene representation network with a low-dimensional morphable model which provides explicit control over pose and expressions. We use volumetric rendering to generate images from this hybrid representation and demonstrate that such a dynamic neural scene representation can be learned from monocular input data only, without the need of a specialized capture setup. In our experiments, we show that this learned volumetric representation allows for photo-realistic image generation that surpasses the quality of state-of-the-art video-based reenactment methods.
  - [Non-Rigid Neural Radiance Fields: Reconstruction and Novel View Synthesis of a Deforming Scene from Monocular Video,, ICCV2021](https://vcai.mpi-inf.mpg.de/projects/nonrigid_nerf/) | [***``[code]``***](https://github.com/facebookresearch/nonrigid_nerf)
    > We present Non-Rigid Neural Radiance Fields (NR-NeRF), a reconstruction and novel view synthesis approach for general non-rigid dynamic scenes. Our approach takes RGB images of a dynamic scene as input (e.g., from a monocular video recording), and creates a high-quality space-time geometry and appearance representation. We show that a single handheld consumer-grade camera is sufficient to synthesize sophisticated renderings of a dynamic scene from novel virtual camera views, e.g. a `bullet-time' video effect. NR-NeRF disentangles the dynamic scene into a canonical volume and its deformation. Scene deformation is implemented as ray bending, where straight rays are deformed non-rigidly. We also propose a novel rigidity network to better constrain rigid regions of the scene, leading to more stable results. The ray bending and rigidity network are trained without explicit supervision. Our formulation enables dense correspondence estimation across views and time, and compelling video editing applications such as motion exaggeration. Our code will be open sourced.
  - [Neural Body: Implicit Neural Representations with Structured Latent Codes for Novel View Synthesis of Dynamic Humans, CVPR2021](https://zju3dv.github.io/neuralbody/) | [***``[code]``***](https://github.com/zju3dv/neuralbody)
    > This paper addresses the challenge of novel view synthesis for a human performer from a very sparse set of camera views. Some recent works have shown that learning implicit neural representations of 3D scenes achieves remarkable view synthesis quality given dense input views. However, the representation learning will be ill-posed if the views are highly sparse. To solve this ill-posed problem, our key idea is to integrate observations over video frames. To this end, we propose Neural Body, a new human body representation which assumes that the learned neural representations at different frames share the same set of latent codes anchored to a deformable mesh, so that the observations across frames can be naturally integrated. The deformable mesh also provides geometric guidance for the network to learn 3D representations more efficiently. To evaluate our approach, we create a multi-view dataset named ZJU-MoCap that captures performers with complex motions. Experiments on ZJU-MoCap show that our approach outperforms prior works by a large margin in terms of novel view synthesis quality. We also demonstrate the capability of our approach to reconstruct a moving person from a monocular video on the People-Snapshot dataset.
  - [Dynamic View Synthesis from Dynamic Monocular Video, ICCV2021](https://free-view-video.github.io/) | [***``[code]``***](https://github.com/gaochen315/DynamicNeRF)
    > We present an algorithm for generating novel views at arbitrary viewpoints and any input time step given a monocular video of a dynamic scene. Our work builds upon recent advances in neural implicit representation and uses continuous and differentiable functions for modeling the time-varying structure and the appearance of the scene. We jointly train a time-invariant static NeRF and a time-varying dynamic NeRF, and learn how to blend the results in an unsupervised manner. However, learning this implicit function from a single video is highly ill-posed (with infinitely many solutions that match the input video). To resolve the ambiguity, we introduce regularization losses to encourage a more physically plausible solution. We show extensive quantitative and qualitative results of dynamic view synthesis from casually captured videos.
  - [TöRF: Time-of-Flight Radiance Fields for Dynamic Scene View Synthesis, NeurIPS2021](https://imaging.cs.cmu.edu/torf/) | [***``[code]``***](https://github.com/breuckelen/torf)
    > Neural networks can represent and accurately reconstruct radiance fields for static 3D scenes (e.g., NeRF). Several works extend these to dynamic scenes captured with monocular video, with promising performance. However, the monocular setting is known to be an under-constrained problem, and so methods rely on data-driven priors for reconstructing dynamic content. We replace these priors with measurements from a time-of-flight (ToF) camera, and introduce a neural representation based on an image formation model for continuous-wave ToF cameras. Instead of working with processed depth maps, we model the raw ToF sensor measurements to improve reconstruction quality and avoid issues with low reflectance regions, multi-path interference, and a sensor's limited unambiguous depth range. We show that this approach improves robustness of dynamic scene reconstruction to erroneous calibration and large motions, and discuss the benefits and limitations of integrating RGB+ToF sensors that are now available on modern smartphones.
  - [Object-Centric Neural Scene Rendering](https://shellguo.com/osf/) | [***``[code]``***](https://shellguo.com/osf/)
    > We present a method for composing photorealistic scenes from captured images of objects. Our work builds upon neural radiance fields (NeRFs), which implicitly model the volumetric density and directionally-emitted radiance of a scene. While NeRFs synthesize realistic pictures, they only model static scenes and are closely tied to specific imaging conditions. This property makes NeRFs hard to generalize to new scenarios, including new lighting or new arrangements of objects. Instead of learning a scene radiance field as a NeRF does, we propose to learn object-centric neural scattering functions (OSFs), a representation that models per-object light transport implicitly using a lighting- and view-dependent neural network. This enables rendering scenes even when objects or lights move, without retraining. Combined with a volumetric path tracing procedure, our framework is capable of rendering both intra- and inter-object light transport effects including occlusions, specularities, shadows, and indirect illumination. We evaluate our approach on scene composition and show that it generalizes to novel illumination conditions, producing photorealistic, physically accurate renderings of multi-object scenes.
  - [Learning Compositional Radiance Fields of Dynamic Human Heads, CVPR2021(oral)](https://ziyanw1.github.io/hybrid_nerf/) | [code]
    > Photorealistic rendering of dynamic humans is an important ability for telepresence systems, virtual shopping, synthetic data generation, and more. Recently, neural rendering methods, which combine techniques from computer graphics and machine learning, have created high-fidelity models of humans and objects. Some of these methods do not produce results with high-enough fidelity for driveable human models (Neural Volumes) whereas others have extremely long rendering times (NeRF). We propose a novel compositional 3D representation that combines the best of previous methods to produce both higher-resolution and faster results. Our representation bridges the gap between discrete and continuous volumetric representations by combining a coarse 3D-structure-aware grid of animation codes with a continuous learned scene function that maps every position and its corresponding local animation code to its view-dependent emitted radiance and local volume density. Differentiable volume rendering is employed to compute photo-realistic novel views of the human head and upper body as well as to train our novel representation end-to-end using only 2D supervision. In addition, we show that the learned dynamic radiance field can be used to synthesize novel unseen expressions based on a global animation code. Our approach achieves state-of-the-art results for synthesizing novel views of dynamic human heads and the upper body.
  - [Neural Scene Graphs for Dynamic Scenes, CVPR2021(oral)](https://arxiv.org/abs/2011.10379) | [***``[code]``***](https://github.com/princeton-computational-imaging/neural-scene-graphs)
    > Recent implicit neural rendering methods have demonstrated that it is possible to learn accurate view synthesis for complex scenes by predicting their volumetric density and color supervised solely by a set of RGB images. However, existing methods are restricted to learning efficient representations of static scenes that encode all scene objects into a single neural network, and lack the ability to represent dynamic scenes and decompositions into individual scene objects. In this work, we present the first neural rendering method that decomposes dynamic scenes into scene graphs. We propose a learned scene graph representation, which encodes object transformation and radiance, to efficiently render novel arrangements and views of the scene. To this end, we learn implicitly encoded scenes, combined with a jointly learned latent representation to describe objects with a single implicit function. We assess the proposed method on synthetic and real automotive data, validating that our approach learns dynamic scenes -- only by observing a video of this scene -- and allows for rendering novel photo-realistic views of novel scene compositions with unseen sets of objects at unseen poses.
  - [3D Neural Scene Representations for Visuomotor Control, CoRL2021(oral)](https://3d-representation-learning.github.io/nerf-dy/) | [code]
    > Humans have a strong intuitive understanding of the 3D environment around us. The mental model of the physics in our brain applies to objects of different materials and enables us to perform a wide range of manipulation tasks that are far beyond the reach of current robots. In this work, we desire to learn models for dynamic 3D scenes purely from 2D visual observations. Our model combines Neural Radiance Fields (NeRF) and time contrastive learning with an autoencoding framework, which learns viewpoint-invariant 3D-aware scene representations. We show that a dynamics model, constructed over the learned representation space, enables visuomotor control for challenging manipulation tasks involving both rigid bodies and fluids, where the target is specified in a viewpoint different from what the robot operates on. When coupled with an auto-decoding framework, it can even support goal specification from camera viewpoints that are outside the training distribution. We further demonstrate the richness of the learned 3D dynamics model by performing future prediction and novel view synthesis. Finally, we provide detailed ablation studies regarding different system designs and qualitative analysis of the learned representations.
  - [Vision-Only Robot Navigation in a Neural Radiance World](https://arxiv.org/abs/2110.00168) | [code]
    > Neural Radiance Fields (NeRFs) have recently emerged as a powerful paradigm for the representation of natural, complex 3D scenes. NeRFs represent continuous volumetric density and RGB values in a neural network, and generate photo-realistic images from unseen camera viewpoints through ray tracing. We propose an algorithm for navigating a robot through a 3D environment represented as a NeRF using only an on-board RGB camera for localization. We assume the NeRF for the scene has been pre-trained offline, and the robot's objective is to navigate through unoccupied space in the NeRF to reach a goal pose. We introduce a trajectory optimization algorithm that avoids collisions with high-density regions in the NeRF based on a discrete time version of differential flatness that is amenable to constraining the robot's full pose and control inputs. We also introduce an optimization based filtering method to estimate 6DoF pose and velocities for the robot in the NeRF given only an onboard RGB camera. We combine the trajectory planner with the pose filter in an online replanning loop to give a vision-based robot navigation pipeline. We present simulation results with a quadrotor robot navigating through a jungle gym environment, the inside of a church, and Stonehenge using only an RGB camera. We also demonstrate an omnidirectional ground robot navigating through the church, requiring it to reorient to fit through the narrow gap. Videos of this work can be found at this https URL .