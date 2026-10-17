# 核多体理论（The Nuclear Many-Body Problem）专有术语对照表 (TERMINOLOGY.md)

本文档确立全书统一的理论核物理中文学术术语体系。

> **规范准则**：所有人名以及包含人名的定理、模型、方程、势阱、效应、算符、变换与单位等，均直接使用英文原名（例如 Slater 行列式、Bogoliubov 变换、Thouless 定理、Bloch-Messiah 定理、Onishi 公式、Wigner-Eckart 定理、Clebsch-Gordan 系数、Coriolis 力、BCS 理论、Skyrme 力、Gogny 力、Yukawa 势、Weisskopf 单位等），不作中文音译。

---

## 1. 核心模型、方法与理论框架 (Core Theories & Frameworks)

| 英文原名 (En) | 规范中文译名 (Zh) | 缩写/记号 | 重点说明 / 典型章节 |
| :--- | :--- | :--- | :--- |
| Many-Body Problem | 多体问题 | | 全书核心主题 |
| Liquid Drop Model | 液滴模型 | LDM | 第 1 章 |
| Shell Model | 壳模型 | SM | 第 2 章 |
| Deformed Shell Model | 形变壳模型 | | 第 2 章，Nilsson 势等 |
| Mean Field Approximation | 平均场近似 | | 贯穿全书 |
| Self-Consistent Field | 自洽场 | SCF | 第 5、7 章 |
| Hartree-Fock Method | Hartree-Fock 方法 / HF 方法 | HF | 第 5 章 |
| Density-Dependent Hartree-Fock | 密度依赖的 Hartree-Fock 方法 | DDHF | 第 5 章，Skyrme / Gogny 力 |
| Local Density Approximation | 局域密度近似 | LDA | 第 5、13 章 |
| Pairing Correlation | 对关联 | | 第 6 章 |
| Superfluid Nuclei | 超流核 | | 第 6 章 |
| Seniority Model | 辛弱数模型 | | 第 6 章，准自旋方法 |
| BCS Theory | BCS 理论 | BCS | Bardeen-Cooper-Schrieffer 理论，第 6 章 |
| Generalized Single-Particle Model | 推广的单粒子模型 | | 第 7 章 |
| Hartree-Fock-Bogoliubov Theory | Hartree-Fock-Bogoliubov 理论 | HFB | 第 7 章 |
| Constrained Hartree-Fock / HFB | 约束 Hartree-Fock / 约束 HFB 理论 | CHF / CHFB | 第 7 章 |
| Harmonic Vibrations | 简谐振动 | | 第 8 章 |
| Random Phase Approximation | 随机相位近似 | RPA | 第 8 章 |
| Quasiparticle RPA | 准粒子随机相位近似 | QRPA | 第 8 章 |
| Boson Expansion Method | 玻色展开方法 | BEM | 第 9 章 |
| Generator Coordinate Method | 生成坐标法 | GCM | 第 10 章 |
| Restoration of Broken Symmetries | 对称性的恢复 | | 第 11 章 |
| Spontaneous Symmetry Breaking | 自发对称性破缺 | SSB | 第 11 章 |
| Projection Method | 投影方法 | | 第 11 章，粒子数投影、角动量投影 |
| Time-Dependent Hartree-Fock | 时间相关 Hartree-Fock 方法 | TDHF | 第 12 章 |
| Semiclassical Methods | 半经典方法 | | 第 13 章 |

---

## 2. 微观多体物理与算符代数 (Many-Body Physics & Second Quantization)

| 英文原名 (En) | 规范中文译名 (Zh) | 常见符号 / 备注 |
| :--- | :--- | :--- |
| Second Quantization | 二次量子化 | 附录 C |
| Creation Operator | 产生算符 | 粒子 $c_k^\dagger, a_k^\dagger$；准粒子 $\alpha_k^\dagger, \beta_k^\dagger$ |
| Annihilation Operator | 湮灭算符 | 粒子 $c_k, a_k$；准粒子 $\alpha_k, \beta_k$ |
| Quasiparticle | 准粒子 | 产生算符 $\alpha^\dagger$ |
| Quasiparticle Vacuum | 准粒子真空态 | $|\Phi_0\rangle$，满足 $\alpha_k |\Phi_0\rangle = 0$ |
| Product Wave Function | 直积波函数 | 附录 E，独立粒子波函数 |
| Slater Determinant | Slater 行列式 | 费米子多体波函数 |
| Density Matrix | 密度矩阵 | $\rho_{kk'} = \langle c_{k'}^\dagger c_k \rangle$，附录 D |
| Pairing Tensor | 配对张量 | $\kappa_{kk'} = \langle c_{k'} c_k \rangle$ |
| Generalized Density Matrix | 广义密度矩阵 | $\mathcal{R} = \begin{bmatrix} \rho & \kappa \\ -\kappa^* & 1-\rho^* \end{bmatrix}$ |
| Bogoliubov Transformation | Bogoliubov 变换 | $u, v$ 振幅矩阵 |
| Bloch-Messiah Theorem | Bloch-Messiah 定理 | 附录 E，将广义 Bogoliubov 变换分解为典范基 |
| Canonical Basis | 典范基 / 标准基 | 对角化密度矩阵 $\rho$ 的单粒子表象 |
| Thouless Theorem | Thouless 定理 | 附录 E，联接两个非正交准粒子真空态 |
| Onishi Formula | Onishi 公式 | 附录 E，直积态重叠的行列式表达式 |
| Wick's Theorem | Wick 定理 | 算符乘积转正规序与缩并 |
| Normal Ordering | 正规序 | $: A B C :$ |
| Contraction | 缩并 | 费米子线缩并 |
| Particle-Hole (ph) Channel | 粒子-空穴通道 | $\text{ph}$ 相互作用，激发算符 $a_m^\dagger a_i$ |
| Particle-Particle (pp) Channel | 粒子-粒子通道 | $\text{pp}$ 相互作用，配对相互作用 |
| Hole-Hole (hh) Channel | 空穴-空穴通道 | $\text{hh}$ 相互作用 |
| Green's Function | Green 函数 | 附录 F，单体与两体传播子 |

---

## 3. 核结构、形变与转动运动 (Structure, Deformation & Rotation)

| 英文原名 (En) | 规范中文译名 (Zh) | 常见符号 / 备注 |
| :--- | :--- | :--- |
| Magic Numbers | 幻数 | 2, 8, 20, 28, 50, 82, 126 |
| Nuclear Deformation | 核形变 | 多极展开参数 $\alpha_{\lambda\mu}$ |
| Quadrupole / Octupole Deformation | 四极形变 / 八极形变 | $\lambda=2$ / $\lambda=3$ |
| Hexadecapole Deformation | 十六极形变 | $\lambda=4$ |
| Hill-Wheeler Coordinates | Hill-Wheeler 坐标 | $\beta, \gamma$ 形状参数 |
| Prolate Deformation | 长椭球形变 | $\gamma = 0^\circ$ |
| Oblate Deformation | 扁椭球形变 | $\gamma = 60^\circ$ |
| Triaxial Deformation | 三轴形变 | $0^\circ < \gamma < 60^\circ$ |
| Moment of Inertia | 转动惯量 | $\mathcal{J}$，刚体转动惯量 / 流体转动惯量 / Cranking 转动惯量 |
| Rigid-Body Moment of Inertia | 刚体转动惯量 | $\mathcal{J}_{\text{rig}}$ |
| Cranking Model | Cranking 模型 / 推引模型 | 描述转动核的 Inglis 理论，第 3、7 章 |
| Rotating Frame | 转动参考系 / 体固坐标系 | 坐标系与原子核形状共同转动 |
| Coriolis Force | Coriolis 力 | $-\boldsymbol{\omega} \cdot \boldsymbol{j}$ |
| Coriolis Anti-Pairing | CAP 效应 / Coriolis 反配对效应 | 强转动下配对能隙塌缩 |
| Backbending | 回弯现象 | 高自旋态下转动惯量剧增的现象 |
| Rotational Alignment | 转动顺排 | 高 $j$ 轨道核子角动量向转动轴顺排 |
| Particle-Rotor Model | 粒子加转子模型 | 第 3 章 |
| Band Crossing | 能带交叉 | 基态带 (g-band) 与顺排带 (s-band) 交叉 |
| Intrinsic State | 内秉态 | $|\Phi_{\text{intr}}\rangle$，体固坐标系波函数 |
| Laboratory System | 实验室坐标系 | 空间固定坐标系 |
| Body-Fixed System | 体固坐标系 / 内秉坐标系 | 附录 A |
| Euler Angles | Euler 角 | $\Omega = (\alpha, \beta, \gamma)$ |

---

## 4. 核力、核物质与相互作用 (Nuclear Forces & Interactions)

| 英文原名 (En) | 规范中文译名 (Zh) | 常见符号 / 备注 |
| :--- | :--- | :--- |
| Nucleon-Nucleon Interaction | 核子-核子相互作用 | NN 相互作用 |
| Bare Force / Realistic Force | 裸核力 / 现实核力 | Hamada-Johnston, Reid, Bonn 势 |
| Effective Interaction | 有效相互作用 | 平均场中使用的有效力，如 Skyrme, Gogny |
| Repulsive Core / Hard Core | 排斥核心 / 硬芯 | 短程强排斥势 ($r \lesssim 0.5\,\text{fm}$) |
| Soft Core | 软芯 | 连续平滑可微的短程排斥 |
| One-Boson-Exchange Potential | 单玻色子交换势 | OBEP，基于介子场论 |
| Yukawa Potential | Yukawa 势 | 介子交换势 |
| Tensor Force | 张量力 | $S_{12} = 3(\boldsymbol{\sigma}_1 \cdot \hat{\boldsymbol{r}})(\boldsymbol{\sigma}_2 \cdot \hat{\boldsymbol{r}}) - \boldsymbol{\sigma}_1 \cdot \boldsymbol{\sigma}_2$ |
| Spin-Orbit Force | 自旋-轨道力 | $\boldsymbol{l} \cdot \boldsymbol{s}$ |
| Isospin | 同位旋 | $\boldsymbol{\tau}$，质子与中子统一定义 |
| Charge Independence | 电荷无关性 | 同位旋标量性质 |
| Charge Symmetry | 电荷对称性 | $pp$ 与 $nn$ 相互作用的等价性 |
| Nuclear Matter | 核物质 | 无穷大均匀费米流体 |
| Saturation Density | 饱和密度 | $\rho_0 \simeq 0.16 \sim 0.17\,\text{fm}^{-3}$ |
| Incompressibility | 不可压缩模量 / 压缩系数 | $K \simeq 200 \sim 250\,\text{MeV}$ |
| Symmetry Energy | 对称能 | 结合能中与中子过剩 $(N-Z)^2/A$ 相关的项 |
| Surface Energy | 表面能 | $a_S A^{2/3}$ |
| Coulomb Energy | 库仑能 | 质子间静电排斥能 |
| Bethe-Weizsäcker Formula | Bethe-Weizsäcker 公式 / 半经验质量公式 | 第 1 章 |
| G-Matrix | G 矩阵 | Brueckner 理论处理硬芯的重整化相互作用 |

---

## 5. 对关联与超流核术语 (Pairing & Superfluidity)

| 英文原名 (En) | 规范中文译名 (Zh) | 常见符号 / 备注 |
| :--- | :--- | :--- |
| Cooper Pair | Cooper 对 | 时间反演态对 $(k, \bar{k})$ |
| Time-Reversal Conjugate | 时间反演共轭 | $|k\rangle \to |\bar{k}\rangle = \mathcal{T}|k\rangle$ |
| Pairing Force | 配对力 / 对力 | 常数单极对力 $-G \sum a_k^\dagger a_{\bar{k}}^\dagger a_{\bar{k}'} a_{k'}$ |
| Seniority Quantum Number | 辛弱数 | $v$（未配对核子数） |
| Quasi-spin Operators | 准自旋算符 | $S_+, S_-, S_0$ |
| Occupation Probability | 占据几率 | $v_k^2$ |
| Vacancy Probability | 空额几率 | $u_k^2 = 1 - v_k^2$ |
| Pairing Gap | 配对能隙 | $\Delta$ |
| Gap Equation | 能隙方程 | $\Delta = G \sum_k u_k v_k$ |
| Chemical Potential | 化学势 / Fermi 能 | $\lambda$（约束平均粒子数 $\langle \hat{N} \rangle = A$） |
| Quasiparticle Energy | 准粒子能量 | $E_k = \sqrt{(\epsilon_k - \lambda)^2 + \Delta^2}$ |
| Even-Odd Mass Staggering | 奇偶质量差 / 奇偶交错 | 配对效应导致的基态结合能系统性差异 |
| Pairing Vibration | 对振动 | 跨闭壳两核子转移激发的模式 |

---

## 6. 集体激发与动力学 (Excitation, RPA, TDHF, Semiclassical)

| 英文原名 (En) | 规范中文译名 (Zh) | 常见符号 / 备注 |
| :--- | :--- | :--- |
| Giant Resonance | 巨共振 | GR（核子集体相干运动激发） |
| Giant Dipole Resonance | 巨偶极共振 | GDR |
| Giant Quadrupole Resonance | 巨四极共振 | GQR |
| Giant Monopole Resonance | 巨单极共振（呼吸模） | GMR (Breathing Mode) |
| Isoscalar Mode | 同位旋标量模 | 质子与中子同相位运动 ($\Delta T = 0$) |
| Isovector Mode | 同位旋矢量模 | 质子与中子反相位运动 ($\Delta T = 1$) |
| Forward Amplitude | 正向振幅 | $X_{mi}$ (粒子-空穴激发振幅) |
| Backward Amplitude | 反向振幅 | $Y_{mi}$ (地面关联 / 粒子-空穴去激发振幅) |
| Spurious State / Spurious Mode | 赝态 / 赝模（虚假态） | 质心运动或平移/转动对称性自发破缺引入的无物理能量激发 |
| Goldstone Mode | Goldstone 模 / 零能模 | 恢复破缺对称性对应的零激发能本征模 |
| Energy-Weighted Sum Rule | 能量加权求和规则 | EWSR |
| Boson Expansion Method | 玻色展开方法 | 第 9 章 |
| Marumori Expansion | Marumori 展开 | 第 9 章 |
| Belyaev-Zelevinsky Expansion | Belyaev-Zelevinsky 展开 | 第 9 章 |
| Generator Coordinate | 生成坐标 | $q$ (形变参数、对能隙等动力学自由度) |
| Hill-Wheeler Equation | Hill-Wheeler 方程 | GCM 中的积分本征值方程 |
| Overlap Kernel | 重叠核 | $\mathcal{N}(q, q') = \langle \Phi(q) | \Phi(q') \rangle$ |
| Hamiltonian Kernel | Hamiltonian 核 / Hamilton 核 | $\mathcal{H}(q, q') = \langle \Phi(q) | H | \Phi(q') \rangle$ |
| Projection Before Variation | 变分前投影 | PBV / VAP (Variation After Projection) |
| Projection After Variation | 变分后投影 | PAV |
| Particle Number Projection | 粒子数投影 | PNP |
| Angular Momentum Projection | 角动量投影 | AMP |
| WKB Approximation | WKB 近似 | Wentzel-Kramers-Brillouin 半经典波函数 |
| Thomas-Fermi Model | Thomas-Fermi 模型 | 费米气体局域动量空间近似 |
| Extended Thomas-Fermi | 扩展 Thomas-Fermi 模型 | ETF，包含 $\hbar^2, \hbar^4$ 梯度修正 |
| Wigner Transform | Wigner 变换 | 相空间分布函数 $f(\boldsymbol{r}, \boldsymbol{p})$ |
| Wigner Function | Wigner 函数 | 经典相空间量子对应 |

---

## 7. 跃迁概率、角动量代数与电磁极矩 (Transitions & Electromagnetism)

| 英文原名 (En) | 规范中文译名 (Zh) | 常见符号 / 备注 |
| :--- | :--- | :--- |
| Reduced Matrix Element | 约化矩阵元 | $\langle I_f \| \mathcal{M} \| I_i \rangle$ |
| Reduced Transition Probability | 约化跃迁几率 / 约化跃迁概率 | $B(E\lambda), B(M\lambda)$ |
| Clebsch-Gordan Coefficient | Clebsch-Gordan 系数 / C-G 系数 | $\langle j_1 m_1 j_2 m_2 | J M \rangle$ |
| Wigner-Eckart Theorem | Wigner-Eckart 定理 | 附录 B，分解矩阵元为几何因子与动力学约化矩阵元 |
| Electric Multipole Operator | 电多极算符 | $\mathcal{M}(E\lambda, \mu)$ |
| Magnetic Multipole Operator | 磁多极算符 | $\mathcal{M}(M\lambda, \mu)$ |
| Electric Quadrupole Moment | 电四极矩 | $Q_0$ (内秉电四极矩), $Q_{\text{spec}}$ (谱学电四极矩) |
| Magnetic Dipole Moment | 磁偶极矩 | $\mu$ |
| Gyromagnetic Ratio | 旋磁比 / $g$ 因子 | $g_l, g_s, g_R$ |
| Weisskopf Single-Particle Unit | Weisskopf 单粒子单位 | W.u.，单粒子跃迁强度的基准单位 |
| Selection Rules | 选择定则 | 宇称、角动量三角定则 |

---

## 8. 经典文献与人名惯用列表 (Proper Names & Literature)

* **原著作者**：Peter Ring, Peter Schuck
* **文献著作**：
  * Bohr & Mottelson [BM 75]
  * Eisenberg & Greiner [EG 70]
  * de Shalit & Feshbach [SF 74]
  * Edmonds [Ed 57]
* **理论物理人名**：
  * Hartree, Fock
  * Bogoliubov
  * Slater
  * Bloch, Messiah
  * Thouless
  * Onishi
  * Wick
  * Bardeen, Cooper, Schrieffer
  * Strutinsky
  * Nilsson
  * Inglis
  * Skyrme, Gogny
  * Brueckner, Bethe, Goldstone
  * Yukawa
  * Coriolis
  * Clebsch, Gordan
  * Wigner, Eckart
  * Weisskopf
  * Hill, Wheeler
  * Marumori, Belyaev, Zelevinsky
  * Wentzel, Kramers, Brillouin (WKB)
  * Thomas, Fermi
  * Pauli
  * Dirac
  * Schrödinger
  * Hamilton
  * Feynman
