# AGENTS.md - 核多体理论（Peter Ring）中文翻译项目工作区指南

欢迎来到 **Peter Ring & Peter Schuck《The Nuclear Many-Body Problem》（原子核多体问题 / 原子核理论）** 中文翻译与研注项目。

本文件旨在让每一位进入此工作区的 AI Agent 能够迅速理解项目背景、文件架构、编译设置、LyX 语法规范与学术翻译准则，**无需反复扫描与探测环境，即可立即进入高效工作状态**。

---

## 1. 项目基本概况

* **原著**：*The Nuclear Many-Body Problem* (Peter Ring, Peter Schuck 著，Springer-Verlag 出版)
* **中文书名**：原子核理论（读书笔记 / 译注本）
* **译注者**：陈佳炜、甄昕
* **项目目标**：将这本理论核物理领域的经典多体理论专著翻译为高质量、学术规范严谨、排版优良的中文专著。

---

## 2. 关键路径与资源位置

| 资源类型 | 绝对路径 / 说明 |
| :--- | :--- |
| **英文原著 PDF** | `/Users/javion/10-EBooks/1_physics&math&techniques/00_Nuclear_Physics/The Nuclear Many-Body Problem by Peter Ring.pdf` <br>*(734页单色清晰影印扫描件，JBIG2编码，各Agent查阅时可结合 `view_file` 或相关脚本定位指定章节页码)* |
| **项目工作区根目录** | `/Users/javion/01-Writtings/Lectures/PeterRing/` |
| **主控主文档** | `PeterRing.lyx`（主文档，包含各章节与附录的 include 声明） |
| **LaTeX 导言区配置** | `preamble.tex`（宏包、字体映射、页面几何、自定义数学算符） |
| **专有术语对照表** | `TERMINOLOGY.md`（涵盖全书13章与附录的核心理论物理中英术语） |
| **数学公式排版规范** | `MATH_GUIDE.md`（正斜体、Dirac 符号、算符、单位、超大括号等严格规范） |
| **格式检查工具** | `check_lyx.py`（自动化校验 Inset 闭合、公式平衡、行边界及学术规范） |
| **封面样式定义** | `Titlepage.sty`（绘制定制封面与元数据） |
| **插图资源目录** | `pictures/`（包含正文引用的高清图表 `.png`、`.pdf`、`.eps`） |
| **编译输出 PDF** | `PeterRing.pdf`（目前本地编译生成的中文排版成果） |

---

## 3. 全书章节架构与翻译进度现状

全书结构采用 `PeterRing.lyx` 作为主控文档，通过子文档形式引入各章节。

> **注意**：在 `PeterRing.lyx` 中，`literal "true"` 表示已激活包含在编译中；`literal "false"` 表示尚未完成或暂不参与编译的骨架章节。

| 章节编号 | 文件名 | 原书标题 (En) | 译本标题 (Zh) | 当前状态 |
| :--- | :--- | :--- | :--- | :--- |
| **第 1 章** | `Chapter1液滴模型.lyx` | The Liquid Drop Model | 液滴模型 | **已完成主体** (~3860行) |
| **第 2 章** | `Chapter2壳模型.lyx` | The Shell Model | 壳模型 | 部分翻译 (~503行) |
| **第 3 章** | `Chapter3转动与单粒子运动.lyx` | Rotation and Single-Particle Motion | 转动与单粒子运动 | **已完成主体** (~1422行) |
| **第 4 章** | `Chapter4核力.lyx` | Nuclear Forces | 核力 | **已完成主体** (~3537行) |
| **第 5 章** | `Chapter5Hartree-Fock方法.lyx` | The Hartree-Fock Method | Hartree-Fock方法 | **已完成主体** (~2786行) |
| **第 6 章** | `Chapter6对关联与超流核.lyx` | Pairing Correlations and Superfluid Nuclei | 对关联与超流核 | **已完成主体** (~3761行) |
| **第 7 章** | `Chapter7推广的单粒子模型（HFB理论）.lyx` | The Generalized Single-Particle Model (HFB Theory) | 推广的单粒子模型（HFB理论） | **已完成主体** (~2791行) |
| **第 8 章** | `Chapter8简谐振动.lyx` | Harmonic Vibrations | 简谐振动 | **骨架占位 / 待翻译** (~127行) |
| **第 9 章** | `Chapter9玻色展开方法.lyx` | Boson Expansion Methods | 玻色展开方法 | **骨架占位 / 待翻译** (~127行) |
| **第 10 章** | `Chapter10生成坐标法.lyx` | The Generator Coordinate Method | 生成坐标法 | **骨架占位 / 待翻译** (~131行) |
| **第 11 章** | `Chapter11对称性的恢复.lyx` | Restoration of Broken Symmetries | 对称性的恢复 | **详尽完成** (~9691行) |
| **第 12 章** | `Chapter12时间相关Hartree-Fock方法.lyx` | The Time-Dependent Hartree-Fock Method | 时间相关Hartree-Fock方法 | **骨架占位 / 待翻译** (~134行) |
| **第 13 章** | `Chapter13核物理中的半经典方法.lyx` | Semiclassical Methods in Nuclear Physics | 核物理中的半经典方法 | **骨架占位 / 待翻译** (~131行) |
| **附录 A** | `附录A.lyx` | Angular Momentum Algebra in the Laboratory and Body-Fixed System | 实验室坐标系和体固坐标系中的角动量代数 | 已翻译 (~431行) |
| **附录 B** | `附录B.lyx` | Electromagnetic Moments and Transitions | 电磁极矩与跃迁 | **详尽完成** (~3310行) |
| **附录 C** | `附录C.lyx` | Second Quantization | 二次量子化 | 骨架待充实 (~120行) |
| **附录 D** | `附录D.lyx` | Density Matrices | 密度矩阵 | 部分翻译 (~735行) |
| **附录 E** | `附录E.lyx` | Theorems for Many-Fermion Systems | 直积波函数相关的定理 | **详尽完成** (~3288行) |
| **附录 F** | `附录F.lyx` | Many-Body Green's Functions | 多体Green函数 | 部分翻译 (~489行) |

---

## 4. 排版与编译技术栈

* **文档引擎**：LyX 2.4+ (`\lyxformat 620`)
* **文档类**：`ctex-book`
* **编译器**：XeLaTeX / LuaLaTeX（配置了 `use_non_tex_fonts true`）
* **宏包体系**（在 `preamble.tex` 中配置）：
  * 数学核心：`amsmath`, `amssymb`, `amsthm`, `mathtools`, `unicode-math`, `physics`, `tensor`
  * 符号字体：`TeX Gyre Pagella`, `Pagella Math`, `xitsmath`, `Cambria Math`
  * 物理学常用：`physics` 宏包、`mhchem`（核素/同位素化学式，version=3）
  * 多体图符：`simpler-wick`（Wick 缩并与费曼图线）
  * 页面与排版：`geometry`（A4, scale=0.8）、`fancyhdr`、`perpage`（每页脚注重置编号）
* **自定义命令**：
  * 超大括号：`\biggg`, `\bigggl`, `\bigggr`, `\Biggg`, `\bigggg`, `\Bigggg`
  * 实虚部算符：`\Re`, `\Im`
  * 中文交叉引用（通过 `\autoref` 重定义）：式 (`\equationautorefname`)、图 (`\figureautorefname`)、表 (`\tableautorefname`)、节 (`\sectionautorefname`)、小节 (`\subsectionautorefname`)

### 4.1 命令行导出 PDF 标准方法

在无 GUI 界面或执行自动化构建时，可通过命令行直接从主文档 `PeterRing.lyx` 导出并生成全书 `PeterRing.pdf`。

由于本项目采用 XeLaTeX、系统字体与复杂宏包（如 `ctex-book`, `unicode-math`, `physics` 等），推荐采用 **LyX 批处理导出 XeTeX + 两遍 xelatex 编译** 的流水线：

```bash
# 1. 确保 TeX Live 环境在 PATH 中
export PATH="/Library/TeX/texbin:$PATH"

# 2. 清理旧生成的子章节 tex 文件（防止 LyX 批处理时因目标已存在而跳过重新生成）
rm -f Chapter*.tex 附录*.tex PeterRing.tex

# 3. 调用 LyX 批处理导出包含全部激活子章节的 XeTeX 源码
/Applications/LyX.app/Contents/MacOS/lyx -batch -E xetex PeterRing.tex PeterRing.lyx

# 4. 运行 xelatex 进行编译（进行两次以确保目录、图表标号与交叉引用全部稳定收敛）
xelatex -interaction=nonstopmode PeterRing.tex
xelatex -interaction=nonstopmode PeterRing.tex
```

> **注意与建议**：
> - 编译生成的文件为 `PeterRing.pdf`，日志位于 `PeterRing.log`。
> - 连续两遍 `xelatex` 能够消除 `LaTeX Warning: Label(s) may have changed`，确保目录页码与 `\autoref` 引用标签精确对应。

---

## 5. LyX 2.4 源码格式规范（Agent 必须严格遵守）

Agent **可以直接读写 `.lyx` 文本文件**，但必须保持其纯文本结构完整，禁止用裸 LaTeX 覆盖摧毁 LyX 结构树。

### 5.1 基础文件结构模版
```lyx
#LyX 2.4 created this file. For more info see https://www.lyx.org/
\lyxformat 620
\begin_document
\begin_header
\save_transient_properties true
\origin unavailable
\textclass ctex-book
\begin_preamble
\input{preamble.tex}
\setlength{\parskip}{\medskipamount}
\setlength{\parindent}{0pt}
\end_preamble
\use_default_options true
\begin_modules
beautiful-booknotes
theorems-ams-chap-bytype
\end_modules
\maintain_unincluded_children no
\language chinese-simplified
\language_package none
\inputencoding utf8
\fontencoding default
\font_roman "default" "default"
\font_sans "default" "default"
\font_typewriter "default" "default"
\font_math "auto" "auto"
\font_default_family default
\use_non_tex_fonts true
...
\end_header

\begin_body

\begin_layout Chapter
章节标题
\end_layout

\begin_layout Section
节标题
\end_layout

\begin_layout Standard
正文内容...
\end_layout

\end_body
\end_document
```

### 5.2 常用元素写法示例

1. **普通段落**：
   ```lyx
   \begin_layout Standard
   这里是中文正文内容。
   \end_layout
   ```

2. **行内公式**：
   ```lyx
   在结合能公式中，参数为
   \begin_inset Formula $a_{V}=15.68\,\text{MeV}$
   \end_inset
   的值。
   ```

3. **无编号独立展示公式**：
   ```lyx
   \begin_layout Standard
   \begin_inset Formula 
   \[
   H = \sum_{k} \epsilon_k a_k^\dagger a_k + \frac{1}{4}\sum_{klmn} \bar{v}_{klmn} a_k^\dagger a_l^\dagger a_n a_m
   \]
   \end_inset
   \end_layout
   ```

4. **带编号与标签的公式**：
   ```lyx
   \begin_layout Standard
   \begin_inset Formula 
   \begin{equation}
   i\hbar \frac{\partial}{\partial t}\rho = [h(\rho), \rho]\label{eq:tdhf_equation}
   \end{equation}
   \end_inset
   \end_layout
   ```

5. **交叉引用公式或图表**：
   ```lyx
   如
   \begin_inset CommandInset ref
   LatexCommand ref
   reference "eq:tdhf_equation"
   plural "false"
   caps "false"
   noprefix "false"
   nolink "false"

   \end_inset
   所示。
   ```

6. **插图（浮动体）**：
   ```lyx
   \begin_layout Standard
   \begin_inset Float figure
   placement htbp
   wide false
   sideways false
   status open

   \begin_layout Plain Layout
   \align center
   \begin_inset Graphics
   	filename pictures/xxx.png
   	lyxscale 50
   	width 80text%

   \end_inset
   \end_layout

   \begin_layout Plain Layout
   \begin_inset Caption Standard

   \begin_layout Plain Layout
   \begin_inset CommandInset label
   LatexCommand label
   name "fig:xxx"

   \end_inset
   这是图片标题说明
   \end_layout

   \end_inset
   \end_layout

   \end_inset
   \end_layout
   ```

---

## 6. 学术翻译与名词术语对照表

详细完整的理论核物理专有术语对照表请参见 **[`TERMINOLOGY.md`](TERMINOLOGY.md)**，数学公式的详细排版与书写铁律请参见 **[`MATH_GUIDE.md`](MATH_GUIDE.md)**。

> **人名规范（最高铁律）**：
> 所有人名，包括与人名有关的定理、定律、模型、方程、势阱、效应、算符、变换等（例如 Slater, Bogoliubov, Thouless, Bloch-Messiah, Onishi, BCS, Wigner-Eckart, Clebsch-Gordan, Nilsson, Strutinsky, Skyrme, Gogny, Yukawa, Coriolis, Dirac, Pauli, Green, Hamilton 等），**全部直接使用英文原文，严禁音译为中文！**

翻译应保持严谨的高等理论核物理学术风格，推导详实、文字简练。常用核心术语映射如下：

| 原著英文 (En) | 规范中文译名 (Zh) | 典型符号 / 说明 |
| :--- | :--- | :--- |
| Many-Body Problem | 多体问题 | |
| Liquid Drop Model (LDM) | 液滴模型 | |
| Shell Model | 壳模型 | 幻数、自旋-轨道耦合 |
| Mean Field Approximation | 平均场近似 | |
| Hartree-Fock (HF) Method | Hartree-Fock 方法 / HF 方法 | 单体密度矩阵 $\rho$ |
| Pairing Correlation | 对关联 | 单态、配对力 $G$ |
| Superfluid Nuclei | 超流核 | 能隙 $\Delta$ |
| Quasiparticle | 准粒子 | 产生算符 $\alpha_k^\dagger$ |
| Bogoliubov Transformation | Bogoliubov 变换 | $u, v$ 系数矩阵 |
| Hartree-Fock-Bogoliubov (HFB) | Hartree-Fock-Bogoliubov 理论 / HFB 理论 | 广义密度矩阵 $\mathcal{R}$ |
| Harmonic Vibrations / RPA | 简谐振动 / 随机相位近似 (RPA) | 正向 $X$、反向 $Y$ 振幅 |
| Spurious State / Spurious Mode | 赝态 / 赝模（虚假激发） | 质心运动或平移/转动对称性破缺产生 |
| Boson Expansion Method | 玻色展开方法 | Marumori / Belyaev-Zelevinsky 展开 |
| Generator Coordinate Method (GCM) | 生成坐标法 | Hill-Wheeler 方程 |
| Broken Symmetries | 破缺对称性 | 规范对称性、空间转动对称性 |
| Restoration of Symmetries | 对称性的恢复 | 投影算符 $P^N$, $P^J$ |
| Time-Dependent Hartree-Fock (TDHF) | 时间相关 Hartree-Fock 方法 | 非平衡核动力学、重离子碰撞 |
| Semiclassical Approximation | 半经典近似 | WKB 近似、Thomas-Fermi 近似、Wigner 变换 |
| Electromagnetic Transitions | 电磁跃迁 | $B(E\lambda)$, $B(M\lambda)$ |
| Second Quantization | 二次量子化 | 反对易关系 $\{a_i, a_j^\dagger\} = \delta_{ij}$ |

---

## 7. Agent 执行翻译任务的七步标准化流水线 (SOP)

当执行具体章节翻译、排版或审校任务时，必须严格按以下七个阶段推进：

1. **准备与规范对齐**：
   * 在原著 PDF 中精确定位章节页码、公式与图表；
   * 严守人名规范（所有人名一律保留英文原名，严禁音译）；核对 [`TERMINOLOGY.md`](TERMINOLOGY.md) 与 [`MATH_GUIDE.md`](MATH_GUIDE.md)；
   * 任何临时脚本或图像统一放在工作区 `./tmp/` 目录中。
2. **文本翻译与公式转录**：
   * 严格遵循 LyX 2.4 AST 结构（`\begin_inset`, `\end_inset`, `\begin_layout`, `\end_layout` 独立成行）；
   * 原文中的 `†` 等标记必须转为标准 LyX 脚注 Inset，严禁使用伪横线（`\HRule`）截断正文；
   * 微分 `\,\mathrm{d}`、虚数单位 `\mathrm{i}`、粗斜体矢量 `\boldsymbol{...}`、态矢原生 `|\Psi\rangle`（杜绝 `\ket` 宏包）。
3. **图表提取与规范排版**：
   * **插图 (Figure)**：使用 `gs -sDEVICE=pnggray -r300` 从原著高清提取并精准裁剪（剔除原页眉/页码/原英文题），保存于 `pictures/X_Y.png`；设置 `placement H` 紧邻正文首次引用下方；图题在图下方；
   * **表格 (Table)**：使用标准 LyX `Float table`，严禁 `LyX-Code` 缩进；表题在表格上方居中；闭合标签必须使用 XML 样式的 `</lyxtabular>`（严防写为 `\end{lyxtabular}` 导致批处理死锁）。
4. **自动化格式校验（必做）**：
   * 运行 `python3 check_lyx.py ChapterX.lyx --style`；
   * 校验 AST 标签栈深度、`<lyxtabular>` 闭合配对以及音译人名拦截。
5. **清理与双遍编译构建**：
   * 清理历史缓存：`rm -f Chapter*.tex 附录*.tex PeterRing.tex`；
   * 批处理导出 XeTeX：`/Applications/LyX.app/Contents/MacOS/lyx -batch -E xetex PeterRing.tex PeterRing.lyx`；
   * 连续运行两遍 `xelatex -interaction=nonstopmode PeterRing.tex`，保证目录与标签完全收敛。
6. **PDF 版面质检与视觉走查**：
   * 扫描 `PeterRing.log` 中的 `Overfull \hbox`、未定义引用（`??`）与字体缺失；
   * 使用 `gs` 抽检渲染关键页面到 `tmp/`，确认图表清晰、排版居中且无大块悬空留白；走查完毕清理临时图片。
7. **主控集成与交付**：
   * 在 `PeterRing.lyx` 中将该章节子文档声明激活为 `literal "true"`；
   * 交付成果并汇报修改点与公式标签。
