```mermaid
flowchart TD
    A[问题界定与文献综述<br/>政策与平台材料整理] --> B[治理字段与Schema设计<br/>JSON定义与标注指南]
    B --> C[语料构建与数据治理<br/>公开政策/合同/CUAD/平台文档<br/>脱敏与质检]
    C --> D[LLM-Policy Extractor<br/>RAG检索 + 结构化提示 + 函数调用<br/>少量参数微调/LoRA]
    D --> E[抽取评测与不确定性校准<br/>micro/macro-F1, EM, 置信区间]
    E --> F[GII构建与权重学习<br/>法律/语义/技术/组织 四层<br/>AHP/贝叶斯/回归稳健性]
    F --> G[CID映射函数族<br/>线性 / 分段 / 指数]
    G --> H[价格核耦合<br/>P(q)=CID·a·ln(b+q)]
    H --> I[市场仿真与灵敏度分析<br/>福利/交易量/拒单率/弹性/费率崩塌阈值]
    I --> J[智能合约与账本设计<br/>策略哈希、GII/CID、用途/撤回/DP预算上链<br/>押金惩罚与审计回放]
    J --> K[系统集成与Dashboard<br/>指标可视化与策略沙盒]
    K --> L[结果评估与对照基线<br/>与固定价/线性价、无CID对照]
    L --> M[策略建议与扩展实验<br/>费率安全区间识别/套餐化定价/鲁棒性]
    style A fill:#f7f7ff,stroke:#6b6bff,stroke-width:1px
    style D fill:#eef9ff,stroke:#00a3d7,stroke-width:1px
    style F fill:#fff7ee,stroke:#ff9800,stroke-width:1px
    style H fill:#f0fff5,stroke:#27ae60,stroke-width:1px
    style J fill:#fff0f5,stroke:#d81b60,stroke-width:1px

```