
每周分类神经辐射场 - fast ![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)
=================================================================================================================================
## 按类别筛选: 
 [全部](../weekly_nerf_cn.md) | [动态](./dynamic.md) | [编辑](./editing.md) | [快速](./fast.md) | [泛化](./generalization.md) | [人体](./human.md) | [视频](./video.md) | [光照](./lighting.md) | [重建](./reconstruction.md) | [纹理](./texture.md) | [语义](./semantic.md) | [姿态-SLAM](./pose-slam.md) | [其他](./others.md) 
## 大部分为机器翻译，少数论文手动翻译，有翻译错误可以PR修复。
## Jul31 - Aug6, 2022
  - [全息显示3D相位全息图的端到端学习](https://www.nature.com/articles/s41377-022-00894-6) | [code]
    > 计算机生成的全息术 (CGH) 提供相干波前的体积控制，是体积 3D 显示器、光刻、神经光刺激和光/声捕获等应用的基础。最近，基于深度学习的方法作为 CGH 合成的有前途的计算范式出现，克服了传统基于模拟/优化的方法中的质量-运行时权衡。然而，预测全息图的质量本质上受数据集质量的限制。在这里，我们介绍了一个新的全息图数据集 MIT-CGH-4K-V2，它使用分层深度图像作为数据高效的体积 3D 输入和用于直接合成高质量 3D 相位的两阶段监督+无监督训练协议-只有全息图。所提出的系统还可以校正视觉像差，从而允许为最终用户定制。我们通过实验展示了逼真的 3D 全息投影并讨论了相关的空间光调制器校准程序。我们的方法在消费级 GPU 上实时运行，在 iPhone 13 Pro 上以 5 FPS 运行，有望显着提高上述应用程序的性能。
## Jul24 - Jul30, 2022
  - [MobileNeRF：利用多边形光栅化管道在移动架构上进行高效的神经场渲染](https://arxiv.org/abs/2208.00277) | [***``[code]``***](https://github.com/google-research/jax3d/tree/main/jax3d/projects/mobilenerf)
    > 神经辐射场 (NeRFs) 展示了从新颖视图合成 3D 场景图像的惊人能力。但是，它们依赖于基于光线行进的专用体积渲染算法，这些算法与广泛部署的 g 的功能不匹配图形硬件。本文介绍了一种基于纹理多边形的新 NeRF 表示，它可以使用标准渲染管道有效地合成新图像。 NeRF 表示为一组多边形，其纹理表示二进制不透明度和特征向量。使用 z 缓冲区对多边形进行传统渲染会生成每个像素都有特征的图像，这些图像由在片段着色器中运行的小型、依赖于视图的 MLP 进行解释，以产生最终的像素颜色。这种方法使 NeRF 能够使用传统的多边形光栅化管道进行渲染，该管道提供大规模的像素级并行性，在包括手机在内的各种计算平台上实现交互式帧速率。
  - [通过 NeRF Attention 进行端到端视图合成](https://arxiv.org/abs/2207.14741) | [code]
    > 在本文中，我们提出了一个用于视图合成的简单 seq2seq 公式，其中我们将一组光线点作为输入和输出与光线相对应的颜色。在这个 seq2seq 公式上直接应用标准转换器有两个限制。首先，标准注意力不能成功地适应体积渲染过程，因此合成视图中缺少高频分量。其次，将全局注意力应用于所有光线和像素是非常低效的。受神经辐射场 (NeRF) 的启发，我们提出了 NeRF 注意力 (NeRFA) 来解决上述问题。一方面，NeRFA 将体积渲染方程视为软特征调制过程。通过这种方式，特征调制增强了具有类似 NeRF 电感偏置的变压器。另一方面，NeRFA 执行多阶段注意力以减少计算开销。此外，NeRFA 模型采用光线和像素转换器来学习光线和像素之间的相互作用。 NeRFA 在四个数据集上展示了优于 NeRF 和 NerFormer 的性能：DeepVoxels、Blender、LLFF 和 CO3D。此外，NeRFA 在两种设置下建立了新的 state-of-the-art：单场景视图合成和以类别为中心的新颖视图合成。该代码将公开发布。
  - [脱离网格：用于 3D 血管建模的连续隐式神经表示, MICCAI STACOM 2022](https://arxiv.org/abs/2207.14663) | [code]
    > 个性化 3D 血管模型对于心血管疾病患者的诊断、预后和治疗计划非常有价值。传统上，此类模型是用网格和体素掩码等显式表示或径向基函数或原子（管状）形状等隐式表示构建的。在这里，我们建议在可微的隐式神经表示 (INR) 中通过其有符号距离函数 (SDF) 的零水平集来表示表面。这使我们能够用隐式、连续、轻量级且易于与深度学习算法集成的表示来对复杂的血管结构进行建模。我们在这里通过三个实际示例展示了这种方法的潜力。首先，我们从 CT 图像中获得了腹主动脉瘤 (AAA) 的准确且防水的表面，并从表面上的 200 个点显示出稳健的拟合。其次，我们同时将嵌套的血管壁安装在单个 INR 中，没有交叉点。第三，我们展示了如何将单个动脉的 3D 模型平滑地融合到单个防水表面中。我们的结果表明，INR 是一种灵活的表示形式，具有最小交互注释的潜力复杂血管结构的研究和操作。
## Previous weeks
  - [神经稀疏体素场, NeurIPS2020](https://lingjie0206.github.io/papers/NSVF/) | [***``[code]``***](https://github.com/facebookresearch/NSVF)
    > 我们介绍了神经稀疏体素场 (NSVF)，这是一种用于快速和高质量自由视点渲染的新神经场景表示。 NSVF 定义了一组以稀疏体素八叉树组织的体素有界隐式字段，以对每个单元中的局部属性进行建模。 我们仅从一组姿势的 RGB 图像中通过可区分的光线行进操作逐步学习底层体素结构。 使用稀疏体素八叉树结构，可以通过跳过不包含相关场景内容的体素来加速渲染新颖的视图。 我们的方法在推理时比最先进的方法（即 NeRF (Mildenhall et al., 2020)）快 10 倍以上，同时获得更高质量的结果。 此外，通过利用显式稀疏体素表示，我们的方法可以很容易地应用于场景编辑和场景合成。 我们还展示了几个具有挑战性的任务，包括多场景学习、移动人体的自由视点渲染和大规模场景渲染。
  - [AutoInt：快速神经体积渲染的自动集成, CVPR2021](http://www.computationalimaging.org/publications/automatic-integration/) | [***``[code]``***](https://github.com/computational-imaging/automatic-integration)
    > 数值积分是科学计算的基础技术，是许多计算机视觉应用的核心。在这些应用中，隐式神经体绘制最近被提出作为视图合成的新范式，实现逼真的图像质量。然而，使这些方法实用的一个基本障碍是在训练和推理期间沿渲染光线所需的体积积分导致的极端计算和内存要求。需要数百万条光线，每条光线都需要数百次通过神经网络的前向传播，才能通过蒙特卡罗采样来近似这些集成。在这里，我们提出了自动积分，这是一种使用隐式神经表示网络来学习有效的、封闭形式的积分解决方案的新框架。对于训练，我们实例化对应于隐式神经表示的导数的计算图。该图适合要积分的信号。优化后，我们重新组装图以获得代表反导数的网络。根据微积分的基本定理，这可以在网络的两次评估中计算任何定积分。使用这种方法，我们展示了超过 10 倍的计算要求改进，从而实现了快速的神经体绘制。
  - [DeRF：分解的辐射场](https://arxiv.org/abs/2011.12490) | [code]
    > 随着神经辐射场 (NeRF) 的出现，神经网络现在可以渲染 3D 场景的新颖视图，其质量足以愚弄人眼。然而，生成这些图像的计算量非常大，限制了它们在实际场景中的适用性。在本文中，我们提出了一种基于空间分解的技术，能够缓解这个问题。我们的主要观察结果是，使用更大（更深和/或更宽）的网络会带来收益递减。因此，我们建议对场景进行空间分解，并为每个分解部分分配更小的网络。当一起工作时，这些网络可以渲染整个场景。这使我们无论分解部分的数量如何，都能获得近乎恒定的推理时间。此外，我们表明，Voronoi 空间分解更适合此目的，因为它可证明与 Painter 算法兼容，可实现高效且 GPU 友好的渲染。我们的实验表明，对于现实世界的场景，我们的方法提供的推理效率比 NeRF 高出 3 倍（具有相同的渲染质量），或者 PSNR 提高了 1.0~dB（对于相同的推理成本）。
  - [DONeRF：使用 Depth Oracle Networks 实现紧凑神经辐射场的实时渲染, CGF2021](https://depthoraclenerf.github.io/) | [***``[code]``***](https://github.com/facebookresearch/DONERF)
    > 最近围绕神经辐射场 (NeRFs) 的研究爆炸表明，在神经网络中隐式存储场景和照明信息具有巨大的潜力，例如，用于生成新的视图。然而，阻止 NeRF 广泛使用的一个主要限制是沿每个视图射线进行过多网络评估的计算成本过高，当针对当前设备上的实时渲染时需要数十 petaFLOPS。我们表明，当将局部样本放置在场景中的表面周围时，可以显着减少每个视图光线所需的样本数量。为此，我们提出了一个深度预言网络，它通过单个网络评估来预测每个视图光线的光线样本位置。我们表明，使用围绕对数离散和球面扭曲深度值的分类网络对于编码表面位置而不是直接估计深度至关重要。这些技术的结合产生了 DONeRF，这是一种双网络设计，第一步是深度预言网络，以及用于光线累积的局部采样着色网络。通过我们的设计，与 NeRF 相比，我们将推理成本降低了 48 倍。使用现成的推理 API 与简单的计算内核相结合，我们率先在单个 GPU 上以交互式帧速率（每秒 15 帧，800x800）渲染基于光线追踪的神经表示。同时，由于我们专注于表面周围场景的重要部分，与 NeRF 相比，我们获得了相同或更好的质量。
  - [FastNeRF：200FPS 的高保真神经渲染, ICCV2021](https://arxiv.org/abs/2103.10380) | [code]
    > 最近关于神经辐射场 (NeRF) 的工作展示了如何使用神经网络对复杂的 3D 环境进行编码，这些环境可以从新颖的视角进行逼真的渲染。渲染这些图像对计算的要求非常高，最近的改进距离实现交互速率还有很长的路要走，即使在高端硬件上也是如此。受移动和混合现实设备场景的启发，我们提出了 FastNeRF，这是第一个基于 NeRF 的系统，能够在高端消费 GPU 上以 200Hz 渲染高保真逼真图像。我们方法的核心是受图形启发的分解，它允许 (i) 在空间中的每个位置紧凑地缓存深度辐射图，(ii) 使用光线方向有效地查询该图以估计渲染图像中的像素值。大量实验表明，所提出的方法比原始的 NeRF 算法快 3000 倍，并且比现有的加速 NeRF 的工作至少快一个数量级，同时保持视觉质量和可扩展性。
  - [KiloNeRF：使用数千个微型 MLP 加速神经辐射场, ICCV2021](https://arxiv.org/abs/2103.13744) | [***``[code]``***](https://github.com/creiser/kilonerf/)
    > NeRF 通过将神经辐射场拟合到 RGB 图像，以前所未有的质量合成场景的新视图。然而，NeRF 需要数百万次查询深度多层感知器 (MLP)，导致渲染时间变慢，即使在现代 GPU 上也是如此。在本文中，我们证明了通过使用数千个微型 MLP 而不是一个大型 MLP，实时渲染是可能的。在我们的设置中，每个单独的 MLP 只需要表示场景的一部分，因此可以使用更小、更快评估的 MLP。通过将这种分而治之的策略与进一步的优化相结合，与原始 NeRF 模型相比，渲染速度提高了三个数量级，而不会产生高昂的存储成本。此外，使用师生蒸馏进行培训，我们表明可以在不牺牲视觉质量的情况下实现这种加速。
  - [用于实时渲染神经辐射场的 PlenOctrees, ICCV2021(oral)](https://alexyu.net/plenoctrees/) | [***``[code]``***](https://github.com/sxyu/volrend)
    > 实时性能是通过将 NeRF 预先制成基于八叉树的辐射场（我们称为 PlenOctrees）来实现的。为了保留与视图相关的效果，例如镜面反射，我们建议通过封闭形式的球面基函数对外观进行编码。具体来说，我们表明可以训练 NeRFs 来预测辐射的球谐表示，将观察方向作为神经网络的输入。此外，我们表明我们的 PlenOctrees 可以直接优化以进一步最小化重建损失，这导致与竞争方法相同或更好的质量。我们进一步表明，这个八叉树优化步骤可用于加快训练时间，因为我们不再需要等待 NeRF 训练完全收敛。我们的实时神经渲染方法可能会支持新的应用，例如 6 自由度工业和产品可视化，以及下一代 AR/VR 系统。
  - [用于高效神经渲染的体积基元混合, SIGGRAPH2021](https://arxiv.org/abs/2103.01954) | [code]
    > 人类的实时渲染和动画是游戏、电影和远程呈现应用中的核心功能。现有方法有许多我们的工作旨在解决的缺点。三角形网格难以建模像头发这样的细结构，像神经体积这样的体积表示在合理的内存预算下分辨率太低，而像神经辐射场这样的高分辨率隐式表示在实时应用中使用太慢。我们提出了体积基元混合（MVP），一种用于渲染动态 3D 内容的表示，它结合了体积表示的完整性和基于基元的渲染的效率，例如，基于点或基于网格的方法。我们的方法通过利用具有反卷积架构的空间共享计算以及通过使用可以移动以仅覆盖被占用区域的体积基元来最小化空间空白区域中的计算来实现这一点。我们的参数化支持对应和跟踪约束的集成，同时对经典跟踪失败的区域具有鲁棒性，例如薄或半透明结构周围以及具有大拓扑可变性的区域。 MVP 是一种混合体，它概括了基于体积和基元的表示。通过一系列广泛的实验，我们证明它继承了每种方法的优点，同时避免了它们的许多局限性。我们还将我们的方法与几种最先进的方法进行比较，并证明 MVP 在质量和运行时性能方面产生了卓越的结果。
  - [光场网络：具有单次评估渲染的神经场景表示, NeurIPS2021(spotlight)](https://www.vincentsitzmann.com/lfns/) | [***``[code]``***](https://github.com/vsitzmann/light-field-networks)
    > 从 2D 观察推断 3D 场景的表示是计算机图形学、计算机视觉和人工智能的基本问题。新兴的 3D 结构神经场景表示是一种有前途的 3D 场景理解方法。在这项工作中，我们提出了一种新的神经场景表示，光场网络或 LFN，它通过神经隐式表示在 360 度、四维光场中表示底层 3D 场景的几何形状和外观。渲染来自 LFN 的光线只需要*单个*网络评估，而 3D 结构化神经场景表示中的光线行进或基于体积的渲染器每条光线需要数百次评估。在简单场景的设置中，我们利用元学习来学习 LFN 的先验，从而能够从单个图像观察中进行多视图一致的光场重建。这导致时间和内存复杂性的显着降低，并实现了实时渲染。通过 LFN 存储 360 度光场的成本比 Lumigraph 等传统方法低两个数量级。利用神经隐式表示的分析可微性和光空间的新参数化，我们进一步证明了从 LFN 中提取稀疏深度图。
  - [深度监督的 NeRF：更少的视图和更快的免费训练, CVPR2022](https://arxiv.org/abs/2107.02791) | [***``[code]``***](https://github.com/dunbar12138/DSNeRF)
    > 当输入视图数量不足时，通常观察到的神经辐射场 (NeRF) 故障模式会拟合不正确的几何形状。一个潜在的原因是标准体积渲染不会强制执行大多数场景几何体由空白空间和不透明表面组成的约束。我们通过 DS-NeRF（深度监督神经辐射场）将上述假设形式化，这是一种利用现成的深度监督学习辐射场的损失。我们利用当前的 NeRF 管道需要具有已知相机姿势的图像这一事实，这些图像通常通过运行从运动结构 (SFM) 来估计。至关重要的是，SFM 还产生稀疏 3D 点，可在训练期间用作“免费”深度监督：我们添加损失以鼓励光线的终止深度分布匹配给定的 3D 关键点，并结合深度不确定性。 DS-NeRF 可以在训练视图更少的情况下渲染更好的图像，同时训练速度提高 2-3 倍。此外，我们表明我们的损失与最近提出的其他 NeRF 方法兼容，证明深度是一种廉价且易于消化的监督信号。最后，我们发现 DS-NeRF 可以支持其他类型的深度监督，例如扫描深度传感器和 RGB-D 重建输出。
  - [直接体素网格优化：辐射场重建的超快速收敛, CVPR2022(oral)](https://arxiv.org/abs/2111.11215) | [***``[code]``***](https://github.com/sunset1995/DirectVoxGO)
    > 我们提出了一种超快速收敛方法，用于从一组捕获具有已知姿势的场景的图像中重建每个场景的辐射场。这项任务通常应用于新颖的视图合成，最近因其最先进的质量和灵活性而被神经辐射场 (NeRF) 彻底改变。然而，对于单个场景，NeRF 及其变体需要很长的训练时间，从数小时到数天不等。相比之下，我们的方法实现了与 NeRF 相当的质量，并在不到 15 分钟的时间内使用单个 GPU 从头开始​​快速收敛。我们采用由用于场景几何的密度体素网格和具有浅层网络的特征体素网格组成的表示，用于复杂的依赖于视图的外观。使用显式和离散化的体积表示进行建模并不新鲜，但我们提出了两种简单但非平凡的技术，有助于快速收敛和高质量输出。首先，我们介绍了体素密度的激活后插值，它能够以较低的网格分辨率产生锐利的表面。其次，直接体素密度优化容易出现次优几何解决方案，因此我们通过强加几个先验来加强优化过程。最后，对五个内向基准的评估表明，我们的方法与 NeRF 的质量相匹配，甚至超过，但从头开始训练新场景只需要大约 15 分钟。
  - [实时隐式映射和定位, ICCV2021](https://arxiv.org/abs/2103.12352) | [code]
    > 我们首次展示了多层感知器 (MLP) 可以作为手持 RGB-D 相机的实时 SLAM 系统中唯一的场景表示。我们的网络在没有先验数据的情况下进行实时操作训练，构建了一个密集的、特定于场景的隐式 3D 占用率和颜色模型，该模型也可立即用于跟踪。
  - [Mip-NeRF：抗锯齿神经辐射场的多尺度表示, ICCV2021(oral)](https://jonbarron.info/mipnerf/) | [***``[code]``***](https://github.com/google/mipnerf)
    > 神经辐射场 (NeRF) 使用的渲染过程对每个像素单条射线进行采样，因此在训练或测试图像以不同分辨率观察场景内容时，可能会产生过度模糊或混叠的渲染。对于 NeRF 来说，通过每个像素渲染多条光线来进行超级采样的直接解决方案是不切实际的，因为渲染每条光线需要查询多层感知器数百次。我们的解决方案，我们称之为“mip-NeRF”（à la“mipmap”），扩展了 NeRF 以在连续值的尺度上表示场景。通过有效地渲染抗锯齿圆锥截头体而不是射线，mip-NeRF 减少了令人反感的锯齿伪影并显着提高了 NeRF 表示精细细节的能力，同时也比 NeRF 快 7% 和一半的大小。与 NeRF 相比，mip-NeRF 在使用 NeRF 呈现的数据集上将平均错误率降低了 17%，在我们呈现的该数据集的具有挑战性的多尺度变体上降低了 60%。 mip-NeRF 还能够在我们的多尺度数据集上匹配蛮力超采样 NeRF 的准确性，同时速度提高 22 倍。