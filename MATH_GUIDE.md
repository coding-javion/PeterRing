# 核多体理论翻译项目：数学公式书写与排版规范 (MATH_GUIDE.md)

为了确保全书（各章节与附录）数学公式排版的高标准、严谨性与视觉一致性，结合当前项目 `preamble.tex` 配置及已有数万行已完成章节的实际代码统计，特制定本**数学公式规范**。

后续编写与翻译所有 `.lyx` 文件时，所有 Agent 与参与人员必须严格遵循本规范。

---

## 1. LyX 公式结构与环境语法

在 LyX 纯文本源码中，所有数学公式必须完整封装在 `\begin_inset Formula ... \end_inset` 块内。

### 1.1 行内公式 (Inline Math)
使用单美元符号包裹：
```lyx
核子的平均动能约为
\begin_inset Formula $E_{\text{kin}}\simeq 25\,\text{MeV}$
\end_inset
左右。
```

### 1.2 独立无编号公式 (Display Math Unnumbered)
使用 `\[ ... \]` 包裹：
```lyx
\begin_layout Standard
\begin_inset Formula 
\[
H = \sum_{k} \epsilon_k a_k^\dagger a_k + \frac{1}{4}\sum_{klmn} \bar{v}_{klmn} a_k^\dagger a_l^\dagger a_n a_m
\]
\end_inset
\end_layout
```

### 1.3 独立编号公式 (Numbered Equation)
必须使用 `\begin{equation} ... \label{eq:...} \end{equation}` 环境：
```lyx
\begin_layout Standard
\begin_inset Formula 
\begin{equation}
\Delta_{k} = -\frac{1}{2}\sum_{k'} G_{kk'} \frac{\Delta_{k'}}{\sqrt{(\epsilon_{k'}-\lambda)^2 + \Delta_{k'}^2}}\label{eq:bcs_gap_equation}
\end{equation}
\end_inset
\end_layout
```

### 1.4 多行对齐公式 (Aligned Multi-line Equations)
推导较长或由多个等式组成时，使用 `align` 环境：
```lyx
\begin_layout Standard
\begin_inset Formula 
\begin{align}
\alpha_{k} & = u_k a_k - v_k a_{\bar{k}}^\dagger,\label{eq:bcs_quasiparticle_annihilate}\\
\alpha_{\bar{k}}^\dagger & = u_k a_{\bar{k}}^\dagger + v_k a_k\label{eq:bcs_quasiparticle_create}
\end{align}
\end_inset
\end_layout
```

### 1.5 分段函数 / 分类讨论 (Cases)
使用 `cases` 环境：
```lyx
\begin_inset Formula 
\[
\rho_{kk'} = \begin{cases}
v_k^2 & (k = k'),\\
0 & (k \neq k').
\end{cases}
\]
\end_inset
```

---

## 2. 字体与正斜体规范（核心铁律）

| 元素分类 | 正确写法规范 | 严禁/错误写法 | 说明与示例 |
| :--- | :--- | :--- | :--- |
| **虚数单位** | `\mathrm{i}` | `i` (斜体) | **严禁斜体**！避免与单粒子态指标 $i, j, k$ 混淆。<br>正确：$\mathrm{i}\hbar \frac{\partial}{\partial t}\Psi$，$\mathrm{e}^{\mathrm{i}\phi}$ |
| **微分符号** | `\mathrm{d}` (前面加 `\,`) | `d` (斜体), `\dd` | **严格正体**，前置薄空格。<br>正确：$\int f(r)\,\mathrm{d}r$；$\,\mathrm{d}^3 r$；$\frac{\mathrm{d}E}{\mathrm{d}t}$ |
| **转置符号** | `^{\mathrm{T}}` | `^T`, `^\top`, `^{\mathrm{t}}` | **严格正体大写 T**。<br>正确：$U^{\mathrm{T}}$, $\mathcal{W}^{\mathrm{T}}$, $V^{\mathrm{T}}$ |
| **厄米共轭** | `^{\dagger}` | `^+`, `\dag` | **严格使用 dagger**。<br>正确：$c_k^\dagger$, $\alpha_k^\dagger$, $H^\dagger$ |
| **复共轭** | `^{*}` | `\bar{...}` | **星号上标**。<br>正确：$U^*_{kl}$, $\Delta^*$（时间反演态用上横线 $\bar{k}$） |
| **空间/自旋矢量** | `\boldsymbol{...}` | `\vec{...}`, `\mathbf{...}` | 导言区已映射为 `\symbfit` 斜粗体。<br>正确：$\boldsymbol{r}, \boldsymbol{p}, \boldsymbol{j}, \boldsymbol{S}, \boldsymbol{\sigma}, \boldsymbol{\tau}$ |
| **物理常数 $\pi$** | `\mathrm{\pi}` 或 `\pi` | | 项目中多处使用 ISO 标准正体 `\mathrm{\pi}`，如 $\frac{1}{4\mathrm{\pi} r_0^2}$ |
| **普朗克常数** | `\hbar` | `h` | 正确：$\hbar\omega$, $\hbar^2 / 2m$ |
| **物理单位** | `\,\text{...}` | 斜体，或缺少空格 | 必须正体并加薄空格。<br>正确：$1.2\,\text{fm}$, $15.68\,\text{MeV}$, $-8.5\,\text{MeV}/\text{nucleon}$ |
| **同位素/核素** | `\ce{_{Z}^{A}X}` | $X_Z^A$ (手写上下标) | 调用 `mhchem`。<br>正确：`\ce{_{50}Sn}`, `\ce{^{208}Pb}` |

---

## 3. 下标与描述性文本规范

公式中所有**具有特定物理意义的单词缩写、模型名称或状态名称**，必须使用正体（`\text{...}` 或 `\mathrm{...}`），绝不能直接写为斜体变量相乘！

### 3.1 常用理论模型与方法下标
* **Hartree-Fock**：`_{\text{HF}}`（如 $E_{\text{HF}}$, $h_{\text{HF}}$）
* **Hartree-Fock-Bogoliubov**：`_{\text{HFB}}`（如 $E_{\text{HFB}}$, $\mathcal{H}_{\text{HFB}}$）
* **BCS 理论**：`_{\text{BCS}}`（如 $|\text{BCS}\rangle$, $E_{\text{BCS}}$）
* **随机相位近似**：`_{\text{RPA}}`（如 $\Omega_{\text{RPA}}$）
* **液滴模型**：`_{\text{LDM}}`（如 $E_{\text{LDM}}$）

### 3.2 物理通道与运动模式下标
* **粒子-空穴通道**：`_{\text{ph}}`（如 $v^{\text{ph}}$，绝不能写成 $v^{ph}$）
* **粒子-粒子通道**：`_{\text{pp}}`（如 $v^{\text{pp}}$）
* **空穴-空穴通道**：`_{\text{hh}}`（如 $v^{\text{hh}}$）
* **集体运动**：`_{\text{coll}}`（如 $H_{\text{coll}}$, $B_{\text{coll}}$）
* **内秉坐标系**：`_{\text{intr}}`（如 $|\Phi_{\text{intr}}\rangle$）
* **实验室坐标系**：`_{\text{lab}}`（如 $J_{\text{lab}}$）
* **基态**：`_{\text{gs}}`（如 $E_{\text{gs}}$）
* **有效值**：`_{\text{eff}}`（如 $e_{\text{eff}}$, $m^*_{\text{eff}}$）
* **动能 / 势能**：`_{\text{kin}}`, `_{\text{pot}}`

---

## 4. 量子力学与多体微观记号规范

### 4.1 Dirac 符号 (Bra-Ket)
* **编写原则**：本项目**统一使用基础 LaTeX 符号** `|\Psi\rangle` 与 `\langle\Psi|`，**禁止使用 `physics` 宏包的 `\bra{}`, `\ket{}`, `\braket{}`**（已统计现有几万行源码，全书统一为原生 `\langle`, `\rangle`，使用宏包会导致代码风格割裂）。
* **常用形式**：
  * 右矢：`|\Psi\rangle`, `|\Phi_0\rangle`, `|0\rangle`
  * 左矢：`\langle\Psi|`, `\langle\Phi_0|`, `\langle 0|`
  * 内积 / 重叠：`\langle\Psi|\Phi\rangle`
  * 期望值 / 矩阵元：`\langle\Psi|H|\Psi\rangle`
  * 大尺寸 / 复杂算符矩阵元：使用自适应定界符 `\left\langle k_1 \left| r^2 Y_{2\mu} \right| k_2 \right\rangle`

### 4.2 费米子与准粒子算符
* **真实粒子表象**：
  * 单粒子指标通常用 $k, l, m, n$ 或 $i, j$
  * 产生/湮灭算符：$c_k^\dagger, c_k$ 或 $a_k^\dagger, a_k$
* **时间反演态**：
  * 时间反演共轭态统一用顶线表示：$a_{\bar{k}}^\dagger$ 或 $| \bar{k} \rangle$
* **准粒子表象**：
  * 产生/湮灭算符统一用希腊字母：$\alpha_k^\dagger, \alpha_k$ 或 $\beta_k^\dagger, \beta_k$
* **声子 / 玻色子算符**：
  * 统一用 $b^\dagger, b$ 或 $B^\dagger, B$ 或 $Q^\dagger, Q$

### 4.3 对易子与反对易子 (Commutators)
* 对易子统一写为中括号：`[A, B]` 或 `\left[ A, B \right]`
* 反对易子统一写为大括号或加号下标：`\{A, B\}` 或 `[A, B]_+` 或 `\left\{ A, B \right\}`
* **禁止**使用 `\comm{A}{B}` 或 `\acomm{A}{B}`。

### 4.4 矩阵与张量环境
* 矩阵**统一优先使用方括号环境 `bmatrix`**：
  ```latex
  \mathcal{W} = \begin{bmatrix}
  U & V^* \\
  V & U^*
  \end{bmatrix}, \quad
  \mathcal{R} = \begin{bmatrix}
  \rho & \kappa \\
  -\kappa^* & 1 - \rho^*
  \end{bmatrix}
  ```
* 列向量：
  ```latex
  \begin{bmatrix}
  c \\
  c^\dagger
  \end{bmatrix}, \quad
  \begin{bmatrix}
  \alpha \\
  \alpha^\dagger
  \end{bmatrix}
  ```

---

## 5. 自定义宏包命令与高级符号 (preamble.tex 配置)

`preamble.tex` 中提供了几个针对性解决复杂多体推导的定制宏，遇到相应场景时应直接调用：

### 5.1 超大括号 (Extra-Large Brackets)
标准 LaTeX 的 `\Bigg` 只有约 2.5 倍行高。当多体波函数或多重对易子展开极其庞大时，使用导言区定制的阶梯式超大括号：
* `\bigggl( ... \bigggr)`：3 倍高度
* `\Bigggl( ... \Bigggr)`：3.5 倍高度
* `\biggggl( ... \biggggr)`：4 倍高度
* `\Biggggl( ... \Biggggr)`：4.5 倍高度

### 5.2 实部与虚部
导言区已重载 `\Re` 与 `\Im`，直接输出为正体算符：
* 正确：`\Re(z)`, `\Im(z)`（自动生成 $\text{Re}(z)$, $\text{Im}(z)$）

### 5.3 张量下标与上标
如需处理复杂角动量张量上下标对齐，可使用 `\tensor` 宏包：
* `\tensor{T}{^a_b^c_d}`

---

## 6. 公式编号、标签与正文引用规范

### 6.1 标签命名法 (Label Naming)
* **前缀**：所有数学公式标签一律严格以 `eq:` 开头。
* **语义化**：标签内容必须是**纯英文、全小写、用下划线或连字符连接的物理意义描述**。
* **严禁**：严禁出现纯数字标签（如 `eq:1`）、无物理意义的标签（如 `eq:a`）或中文标签（如 `eq:能隙方程`）。
* **优秀示例**：
  * `\label{eq:bcs_gap_equation}`
  * `\label{eq:hfb_generalized_density}`
  * `\label{eq:rpa_secular_equation}`
  * `\label{eq:cranking_hamiltonian}`
  * `\label{eq:thouless_theorem}`

### 6.2 交叉引用 (Cross-referencing)
在导言区 `preamble.tex` 中，已配置：
```latex
\let\ref\autoref
\renewcommand\equationautorefname{式}
```
因此在 LyX 中引用公式标签时，输出的 PDF 会自动带有“式”字前缀。
在 LyX 源码中的标准插入语法为：
```lyx
根据
\begin_inset CommandInset ref
LatexCommand ref
reference "eq:bcs_gap_equation"
plural "false"
caps "false"
noprefix "false"
nolink "false"

\end_inset
可以求解得到配对能隙。
```

---

## 7. 规范速查与常见反模式对照表 (Dos & Don'ts)

| 场景 | 规范标准写法 (DO) | 违规写法 (DON'T) | 违规原因 |
| :--- | :--- | :--- | :--- |
| **虚数单位** | `\mathrm{i}` | `i` | 严禁斜体，避免与求和指标混淆 |
| **空间微分** | `\,\mathrm{d}^3 r` | `d^3r`, `\dd{r}` | 严格正体加薄空格，不依赖外部特殊宏 |
| **转置** | `U^{\mathrm{T}}` | `U^T`, `U^\top`, `U^t` | 保持全书转置记号统一为大写正体 $\mathrm{T}$ |
| **厄米共轭** | `c_k^\dagger` | `c_k^+`, `c_k^\dag` | 必须统一为 `\dagger` |
| **波函数态矢**| `|\Psi\rangle` | `\ket{\Psi}` | 全书统一基础符号，避免 `physics` 兼容问题 |
| **平均场能量**| $E_{\text{HF}}$ | $E_{HF}$ | 下标两个字母为单词缩写，斜体视为 $H$ 乘 $F$ |
| **相互作用** | $v^{\text{ph}}$ | $v^{ph}$ | $\text{ph}$ 代表粒子-空穴通道，必须正体 |
| **配对能隙** | $\Delta$ | $\delta$ | 能隙符号严格为大写 Delta |
| **矢量** | `\boldsymbol{r}` | `\vec{r}`, `\mathbf{r}` | 保持斜粗体渲染规范 |
| **能量单位** | `15.68\,\text{MeV}` | `15.68MeV`, `15.68\text{ MeV}` | 必须正体并使用精确薄空格 `\,` |
| **同位素** | `\ce{_{50}Sn}` | `Sn_{50}` | 统一化学式排版宏包 |
| **对易子** | `[A, B]` | `\comm{A}{B}` | 原生括号，代码清晰无依赖 |
| **矩阵** | `\begin{bmatrix}` | `\begin{pmatrix}` (混用) | 矩阵统一使用方括号 `bmatrix` |
