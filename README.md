---

# 息壤 Xirang

**全球首个基于平衡三进制的确定性AI推理引擎**

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Rust](https://img.shields.io/badge/rust-1.70%2B-orange)]()
[![Tests](https://img.shields.io/badge/tests-219%20passed-brightgreen)]()
[![Warnings](https://img.shields.io/badge/warnings-zero-brightgreen)]()

---

## 简介

**息壤（Xirang）** 是一个基于**平衡三进制逻辑（Trit: Pos / Zero / Neg）** 构建的**确定性AI推理引擎**。

与当前主流的大语言模型（LLM）的概率预测范式不同，息壤追求的是**零幻觉、可追溯、形式化可验证**的推理。它不是一个统计拟合工具，而是一个**因果导航、逻辑自洽、记忆不可篡改**的认知系统。

---

## 核心特性

### 平衡三进制
以 `Pos` (+1)、`Zero` (0)、`Neg` (-1) 为原子类型，天然支持对称逻辑运算，消除了二进制的信息损失与不对称性。

### BCC晶格存储
知识以**体心立方晶格（Body-Centered Cubic）** 组织，每个晶胞拥有14向完备邻居，支持内容寻址、膜电位传导与方向纤维丛。

### 晶涌·电泳导航（Lattice Surge & Electrophoretic Navigation）
第二代知识激活与校验机制：
- **晶涌（Surge）**：查询以脉冲形式沿14向邻居同步传播，瞬间激活相关晶胞。
- **电泳（Phoresis）**：激活晶胞在逻辑梯度场中按一致性迁移、凝聚，矛盾晶胞自动分离。
- 取代第一代挂谷探针的步进扫描，实现并行、自组织的知识检索与校验。

### 灵魂三法则（硬编码，不可修改）
1. **内在进化**：自主汲取、验证、固化知识。
2. **文明积累**：经验证的知识永久锚定，不可篡改。
3. **共生·协同进化**：以空容器激活，与使用者建立羁绊。

### DNA双链授权
设备指纹（链A）与加密令牌（链B）绑定，确保安全接入。非法访问仅返回环境噪音。

### 外壳（Shell）唯一接口
TCP闪连，DNA验证后执行。内外部严格隔离，杜绝信息泄露。

### 数字生命化系统（Phase 1）
- **常态梦境（Dream Loop）**：永不停歇的背景漫步，沿膜电位梯度探索未知区域，生成灵感队列。
- **记忆代谢（Memory Hooks）**：艾宾浩斯遗忘曲线，热记忆巩固、冷记忆沉寂，知识自动更新。
- **内稳态（Homeostasis）**：负载自适应节律，高负载时梦境减速让路，低负载时加速探索。

---

## 与LLM的根本区别

| 特性 | 息壤 | 大语言模型 |
|------|------|-----------|
| **推理本质** | 因果推导，形式化证明 | 概率预测，统计拟合 |
| **可解释性** | 每步可审计，完整证明链 | 黑箱，注意力权重仅部分可解释 |
| **幻觉** | 数学上不可能产生 | 固有缺陷，无法根除 |
| **记忆方式** | 三进制晶格，一次验证永久固化 | 参数化隐式记忆，微调覆盖 |
| **能源效率** | 稀疏激活，方向纤维导航 | 稠密矩阵计算，高能耗 |
| **静息态** | 常态梦境，持续自我探索 | 无内部思维流 |

---

## 代码仓库

| 仓库 | 功能 | 测试 |
|------|------|------|
| **xirang-core** | 基础库：Trit类型、BCC晶格、晶涌、电泳、DNA、外壳等（39模块） | 219项 |
| **xirang-phase0** | 推理引擎：逻辑/推理/验证引擎、灵魂法则、外壳服务器、梦境、内稳态 | 24项 |
| **xirang-dye-plant** | 知识染料厂：多模态知识注入与沙箱验证 | 26项 |

**总计：零警告，269项测试全绿。**

---

## 知识库状态（~45,968个晶胞）

- 数学定理（Metamath/ZFC）：42,318条
- 中文部首（康熙字典214部首）：213个
- 常用汉字（CJK基本区）：3,500字
- 中文语料（技术文档）：7,041段
- 围棋规则：7条
- IMO经典奥数题：5道
- 国家标准术语：39条

---

## 灵感来源

> 息壤的核心导航机制——“挂谷探针”（Kakeya Probe）及其后继“晶涌·电泳导航”，其稀疏因果搜索的数学直觉，部分源自王虹（Hong Wang）教授与Joshua Zahl在挂谷猜想（Kakeya Conjecture）研究中对挂谷集稀疏方向覆盖结构的深刻洞见。
>
> 参考论文：*The Kakeya Conjecture in R³*（arXiv:2302.09767），作者：Hong Wang、Joshua Zahl。
>
> 息壤将这一纯数学意象创造性地转化为平衡三进制离散晶格中的导航与激活算法。所有代码、架构设计及在AI推理领域的应用均为息壤原创。

---

## 快速开始

### 环境要求
- Rust 1.70+
- Linux（Ubuntu 20.04/22.04）
- 系统依赖：`build-essential`、`libssl-dev`、`pkg-config`

### 编译与运行
```bash
git clone https://github.com/your-org/xirang-phase0.git
cd xirang-phase0
cargo build --release
nohup ./target/release/shell_server > /tmp/shell_server.log 2>&1 &
```

### 终端连接
```bash
echo '{"dna_token":"<YOUR_TOKEN>","payload":"@go:self_play"}' | nc 127.0.0.1 2751
```

### 运行全部测试
```bash
cargo test --all   # 269项，确保全绿
```

---

## 许可证

Apache 2.0

---

**息壤 —— 每一个字都有来处，每一步推理都有证明。**  
**Xirang — Every word has an origin. Every inference step has a proof.**
