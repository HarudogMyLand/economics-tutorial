# 微观经济学-市场理论III

寡头垄断 (Oligopoly) 相比之前的两种市场结构更为现实，少数几个寡头厂商占据整个市场。这些寡头可以合作（组成一个卡特尔组织，例如 OPEC），也可以不合作（通常情况下）。

寡头竞争的市场也被称为垄断竞争市场：在一个自由进出的市场中，厂商销售既有差异性又有高度替代性；相反，寡头各自进行垄断的市场就是寡头垄断市场，再者，寡头合谋的市场就是一个卡特尔市场。

我们将研究寡头垄断到底偏向哪里，并用到简单博弈论知识 (Game Theory)，例如纳什均衡 (Nash Equilibrium) 来研究寡头垄断中的经济行为。

我们主要研究双寡头（Duopoly），即市场上只有两个厂商：厂商1和厂商2。

## 寡头垄断

我们还是要首先从博弈论说起，博弈论有两个要点：策略与均衡规则。

### 策略

策略是博弈论中的行为规则或计划，最优策略就是能最大化优势与期望的策略，占优策略（Dominant Strategy) 是不管对手做什么对参与人而言都是最优的策略。

双方同时达到占优策略的均衡是很好的结果，然而这种结果未必一定成立。

譬如，纳什均衡。

**纳什均衡**：在给定了其他参与者的策略的情况下，参与者不会改变自己的策略；即，参与者不可能通过单方面改变自己的策略来获得更高的收益。

囚徒困境是典型的纳什均衡，研究纳什均衡的一个方法是绘制收益矩阵：

<svg id="prisoners-dilemma" width="800" height="500" viewBox="0 0 800 500" xmlns="http://www.w3.org/2000/svg">
                <rect width="800" height="500" fill="#f8f9fa" rx="8" />
                <text x="570" y="90" text-anchor="middle" font-size="20" font-weight="bold" fill="#3498db">囚徒 B</text>
                <g transform="translate(80, 250) rotate(-90)">
                </g>
                <rect x="150" y="110" width="500" height="280" fill="white" stroke="#2c3e50" stroke-width="2" />
                <line x1="350" y1="110" x2="350" y2="390" stroke="#2c3e50" stroke-width="2" />
                <line x1="550" y1="110" x2="550" y2="390" stroke="#2c3e50" stroke-width="2" />
                <line x1="150" y1="190" x2="650" y2="190" stroke="#2c3e50" stroke-width="2" />
                <line x1="150" y1="270" x2="650" y2="270" stroke="#2c3e50" stroke-width="2" />
                <rect x="150" y="110" width="200" height="80" fill="#e8f4fc" />
                <rect x="350" y="110" width="200" height="80" fill="#e8f4fc" />
                <rect x="150" y="190" width="200" height="80" fill="#fdeaea" />
                <rect x="150" y="270" width="200" height="80" fill="#fdeaea" />
                <text x="250" y="155" text-anchor="middle" font-size="18" font-weight="bold" fill="#2c3e50">沉默</text>
                <text x="450" y="155" text-anchor="middle" font-size="18" font-weight="bold" fill="#2c3e50">坦白</text>
                <text x="250" y="235" text-anchor="middle" font-size="18" font-weight="bold" fill="#2c3e50">沉默</text>
                <text x="250" y="315" text-anchor="middle" font-size="18" font-weight="bold" fill="#2c3e50">坦白</text>
                <g id="cell1">
                    <rect x="350" y="190" width="200" height="80" fill="#d5f4e6" />
                    <text x="450" y="235" text-anchor="middle" font-size="22" font-weight="bold" fill="#27ae60">(1, 1)</text>
                    <text x="420" y="260" text-anchor="middle" font-size="16" fill="#555">各判1年</text>
                </g>
                <g id="cell2">
                    <rect x="550" y="190" width="100" height="80" fill="#fef9e7" />
                    <text x="600" y="235" text-anchor="middle" font-size="22" font-weight="bold" fill="#f39c12">(5, 0)</text>
                    <text x="600" y="260" text-anchor="middle" font-size="16" fill="#555">A:5年, B:0年</text>
                </g>
                <g id="cell3">
                    <rect x="350" y="270" width="200" height="80" fill="#fef9e7" />
                    <text x="450" y="315" text-anchor="middle" font-size="22" font-weight="bold" fill="#f39c12">(0, 5)</text>
                    <text x="450" y="340" text-anchor="middle" font-size="16" fill="#555">A:0年, B:5年</text>
                </g>
                <g id="cell4">
                    <rect x="550" y="270" width="100" height="80" fill="#fadbd8" />
                    <text x="600" y="315" text-anchor="middle" font-size="22" font-weight="bold" fill="#e74c3c">(3, 3)</text>
                    <text x="600" y="340" text-anchor="middle" font-size="16" fill="#555">各判3年</text>
                </g>
                <path id="arrow1" d="M 480 180 Q 500 160 520 140" fill="none" stroke="#3498db" stroke-width="2" marker-end="url(#arrowhead)" />
                <text x="520" y="130" font-size="14" fill="#3498db">B的决策</text> 
                <path id="arrow2" d="M 140 240 Q 120 240 100 240 Q 80 240 60 220" fill="none" stroke="#e74c3c" stroke-width="2" marker-end="url(#arrowhead)" />
                <text x="30" y="210" font-size="14" fill="#e74c3c">A的决策</text>
                <defs>
                    <marker id="arrowhead" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto">
                        <polygon points="0 0, 10 3.5, 0 7" fill="#3498db" />
                    </marker>
                </defs>
                <circle id="nash-equilibrium" cx="600" cy="315" r="8" fill="none" stroke="#e74c3c" stroke-width="3" opacity="0" />
                <rect id="dominant-strategy" x="545" y="105" width="110" height="170" fill="none" stroke="#9b59b6" stroke-width="3" stroke-dasharray="5,5" opacity="0" />
</svg>


可见对于每个囚徒，他们的**占优策略**就是招供，然而这必然导致双方都达到一个折中的刑期（纳什均衡结果：A=3，B=3），且该结果比 “双方都沉默”（A=1，B=1）的总收益更低。

关于博弈论的知识将在本章后半部分介绍。

### 古诺模型

基于此，我们将引入一个更具体的模型：非合作-寡头垄断模型。假定我们的市场中仅有两个厂商，这样的市场称为**双寡头垄断**（Duopoly）。

古诺模型的提出者奥古斯丁·古诺假设两个厂商生产同质商品，了解市场需求，决定生产产量。厂商将竞争者的产出视为不变，决定自己生产多少。

古诺模型的核心假设

1. 仅有两家厂商，生产完全同质的产品；
2. 同时决定产量，不存在先后顺序；
3. 厂商知道市场需求曲线（假设为线性需求：$P=a−bQ$，其中 $Q=Q1+Q2$）；
4. 厂商的边际成本恒定（设为$MC1=MC2=c$），无固定成本；
5. 每个厂商都认为对手的产量固定，通过调整自身产量实现利润最大化（“古诺猜想”）

厂商1会试图最大化利润
$$
\max_{q_1} \pi_1 = [a-b(q_1+q_2)]q_1-cq_1
$$
求导极值点得到
$$
q_1=R_1(q_2)=\frac{a-c-bq_2}{2b}
$$
同理，有
$$
q_2=R_2(q_1)=\frac{a-c-bq_1}{2b}
$$
联立解得
$$
q_1^*=q_2^*=\frac{a-c}{3b}
$$
这就是均衡时的价格

### 斯塔克伯格模型

该模型下，先发优势是一个重要概念，一个厂商比另一个决定产出。在这里，你可以视为厂商A先制定了价格与产量，厂商B因此相应制定自己的价格与产量，在这里厂商A就是价格*领导者*，厂商B就是价格*追随者*。在这些情况下，策略的相互影响将构成序贯博弈。[^2]

标准斯塔克伯格模型通常讨论**产量**。如果是先定**价格**，那是价格领导模型（Price Leadership），结论会完全不同。考试默认指产量博弈。

在这里，厂商2的行为与古诺模型一致
$$
q_2=R_2(q_1)=\frac{a-c-bq_1}{2b}
$$
但是厂商1作为先发者，预判了厂商2的反应函数，将 $q_2$ 代入自己的利润函数
$$
\pi_1=[a-b(q_1+\frac{a-c-bq_1}{2b})]q_1-cq_1
$$
得到
$$
\pi_1=\frac{a-c}{2}q_1-\frac{b}{2}q_1^2
$$
求导得到
$$
q^*_1=\frac{a-c}{2b},\qquad q^*_2=\frac{a-c}{4b}
$$


### 伯特兰模型

**伯特兰模型 (Bertrand Model)** 是寡头垄断章节中唯一的**价格竞争**模型。伯特兰模型（1883）认为，厂商实际上设定的是**价格**，并让市场决定销量。

假设条件

1. 决策变量：价格 $P$
2. 产品性质：可以是同质的，也可以是有差异的
3. 消费者行为：消费者完全知情，对于同质商品，总是选择价格最低的购买
4. 产能：厂商有足够的产能满足所有需求

1. 同质产品

消费者只卖便宜的同质产品，其中 $\max\{P_1, P_2\}$ 的销量为0。
$$
P_1=P_2=\text{MC}=c
$$

2. 差异化产品

消费者有品牌偏好，不会因为对手降价就全部跑光。

需求函数示例：
$$
q_1=a-p_1+dp_2
$$
写出利润：
$$
\pi_1=(p_1-c)(a-p_1+dp_2)
$$
对 $p_1$ 求导为0，得到 $p_1=R_1(p_2)$ 。

联立方程求解。

## 简单博弈论

博弈论 (Game Theory) 是寡头模型的**方法论基础**。我们之前的寡头模型其实就是博弈论的具体应用。现在我们将这套分析框架抽象出来，研究理性决策者之间存在**策略互动**时的决策问题。

### 静态博弈 (Simultaneous Games)

参与者同时行动，或者在行动时不知道对手的选择。我们通常用**收益矩阵 (Payoff Matrix)** 来表示策略与结果。

#### 单方占优策略

智猪博弈 (Boxed Pigs) —— 大猪去按按钮，小猪吃现成的；大猪如果不按，大家都饿死。

- **结果**：小猪的占优策略是“等待”，大猪无奈只能“按按钮”。
- *启示：市场中的小企业往往搭大企业的便车。*

### 混合策略 (Mixed Strategy NE)

我们引入概率，随机选择策略。

计算逻辑：让对手无差异 (Indifference Principle)

假设 A 和 B 玩“猫抓老鼠”游戏，没有纯策略均衡。

- A 以概率 $p$ 选上，$(1−p)$ 选下。
- B 以概率 $q$ 选左，$(1−q)$ 选右。

求解 A 的最优概率 $p$ 的步骤：

并不是让 A 自己的收益最大化，而是让对手 B 选左和选右的期望收益相等。
(因为如果 B 选左的收益更高，B 就会 100% 选左，混合策略就不存在了)

通用公式：
$$
E(\pi_{B}^{\text{Left}})=E(\pi_B^{\text{Right}})
$$

### 动态博弈(Sequential Games)

参与者先后行动，后行动者可以看到先行动者的选择。我们使用**博弈树 (Game Tree)** 或**决策树**来表示。

核心解法：逆向归纳法。

1. 找到博弈树最末端的节点。
2. 在这个节点上，决策者会选哪个？（把不选的枝剪掉）。
3. 倒退回上一级节点，继续比较。

关键概念：可置信威胁 (Credible Threat)

- **不可置信威胁**：在逆向归纳中，不可置信威胁会被排除。
- **子博弈完美纳什均衡 (SPNE)**：排除了所有不可置信威胁后的纳什均衡。它要求在博弈树的每一个“子博弈”中，策略都是最优的。

### 重复博弈 (Repeated Games)

如果囚徒困境玩很多次，结果会变吗？

- **有限次重复 (Finite)**：

  - 只要次数是确定的（比如玩10次），根据逆向归纳法，最后一次大家肯定背叛。
  - 既然第10次肯定背叛，第9次为了避免吃亏也得背叛……
  - **结论**：合作无法达成，每一轮都背叛。

- **无限次重复 (Infinite)**：

  - 因为不知道哪一次是最后一次，**合作可能达成**。

  - **冷酷策略 (Grim Trigger Strategy)**：我们先合作。如果你敢背叛我一次，我从下轮开始永远背叛你（永远惩罚）。只要贴现因子 $\delta$ 足够大（看重未来），合作就能维持。

    

[^2]: 将在下文介绍
