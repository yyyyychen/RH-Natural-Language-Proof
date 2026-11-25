# 黎曼猜想的自然语言证明

[English](README.md) · 简体中文

本项目以[Levent Alpöge 的 Lean 证明](https://github.com/leanprover-community/riemann-hypothesis/blob/a172c464fd4bcfc4f53e394dcba45d742b1409a6/src/Main.lean#L4)为基础，在 GPT 的辅助下写成了这份[自包含的黎曼猜想自然语言证明（PDF）](RH-Natural-Language-Proof.pdf)。这是独立维护的个人项目，不代表 Levent Alpöge 本人或任何组织。 [直接下载 PDF](https://github.com/yyyyychen/RH-Natural-Language-Proof/raw/refs/heads/main/RH-Natural-Language-Proof.pdf)

---

[第一章 *Introduction*（第 19–44 页）](RH-Natural-Language-Proof.pdf#page=19)介绍了证明的整体思路。

- 假设临界带内、临界线右侧有一个零点 $\rho$。从一个关于素数幂的平滑加权和中扣除 $s=1$ 处的已知贡献后，其梅林变换在 $\rho$ 处仍有极点。[§§1.1–1.2](RH-Natural-Language-Proof.pdf#page=20)
- 把一族狄利克雷特征对应的和合成一个实值和 $G(x)$。由于权重都为正，各特征的零点重数不会相互抵消，因此极点得以保留。接下来的算术目标是给 $G(x)$ 建立单侧上界。[§1.3](RH-Natural-Language-Proof.pdf#page=23)
- 用一条 theta 提升链恢复 $G(x)$。对有限群取傅里叶平均，从局部算术数据中选出目标特征的贡献，剩下的是需要估计的误差。[§1.4](RH-Natural-Language-Proof.pdf#page=25)
- 在同一条链上估计误差。周期配对把复积分与整格联系起来。几何估计控制格指数，插值和 Gram 矩阵估计则控制能保留多少个线性无关的方向。[§§1.5–1.8](RH-Natural-Language-Proof.pdf#page=31)
- 取接近 $\sqrt{x}$ 的链长 $m$，平衡量级分别为 $x/m$ 和 $m$ 的两项误差。对充分小的 $\varepsilon \gt 0$，可以找到任意大的 $Y$，使整个区间 $[Y,Y^{3/2}]$ 上都有 $G(x)\le x^{1/2+9\varepsilon}$。[§1.9](RH-Natural-Language-Proof.pdf#page=40)
- 回到假设的零点，取 $1/2+9\varepsilon \lt \Re(\rho)$。区间上界约束了拉普拉斯变换的一对高阶导数，而邻近的极点会迫使导数增长得更快，产生矛盾。这样排除了临界带内临界线右侧的零点，再由函数方程排除左侧的零点。[§§1.10–1.11](RH-Natural-Language-Proof.pdf#page=41)

---

黎曼猜想已经得到证明，对这一定理的理解才刚刚开始。欢迎在本仓库的 Issues 中提出关于这份自然语言证明或原始 Lean 文件的疑问，也欢迎指出疏漏、错误，或提出修改建议。维护者会在 GPT 的辅助下定期回复，希望大家都能有所收获。
