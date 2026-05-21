---
name: "weakness-reviewer"
description: "通过深度分析用户的错误代码库、bug报告和问题日志，从技术思想层面挖掘根本性薄弱点。当用户想要进行深度知识体系诊断、识别底层认知盲区时调用。"
version: "1.0.0"
author: "SOLO"
last_updated: "2025-05-21"
---

# 个人薄弱点深度审查器

## 核心原则

**本 skill 的核心使命：穿透表象，直达本质。**

- 绝不停留在"你这里写错了"的层面
- 必须追问"为什么会犯这个错"
- 必须挖掘"这个错误反映了什么认知缺陷"
- 必须追溯"这个认知缺陷的根源是什么"
- 解决方案必须具体到可执行的下一步动作

## 调用时机

在以下情况调用此 skill：
- 用户想要深度分析算法练习中的错误模式
- 用户有项目开发中的 bug/错误集合需要根因分析
- 用户想要评估自己的技术知识体系的底层结构
- 用户请求学习差距的深度诊断
- 用户想要识别自己思维层面的认知盲区

## 输入要求

此 skill 期望接收以下一种或多种输入：

1. **错误代码库** - 失败的代码提交或不正确的实现集合（必须包含错误代码和正确代码的对比）
2. **Bug 报告** - 项目中的错误消息、堆栈跟踪、问题描述及修复过程
3. **问题日志** - 开发过程中遇到的挑战记录、思考过程、尝试过的解决方案
4. **参考资源** - 用于对比的文档、教程、标准答案或最佳实践

**输入质量要求：**
- 必须有足够的上下文，不能只有孤立的错误片段
- 最好包含用户的思考过程或尝试路径
- 错误和正确的对比越清晰，分析越深入

## 个性化配置（适应性优化）

本 skill 支持根据用户个人需求进行灵活配置，体现高度适应性。在开始分析前，必须与用户确认以下配置项：

### 配置项清单

### 1. 分析深度选择
```
可选级别：
□ 快速扫描（仅第一、二层：表象+模式）
  - 适用场景：时间有限，只想快速了解大致问题
  - 输出内容：错误统计 + 主要模式 + 简要建议
  - 预计耗时：5-10分钟

□ 标准分析（前三层：表象+模式+技术）
  - 适用场景：常规学习复盘，需要具体改进方向
  - 输出内容：完整技术层面分析 + 具体解决方案
  - 预计耗时：15-25分钟

□ 深度诊断（全部五层）
  - 适用场景：系统性提升，需要根本性改变
  - 输出内容：认知层面分析 + 知识体系重构建议
  - 预计耗时：30-45分钟

默认值：标准分析（如未指定）
```

### 2. 关注领域权重
```
用户可指定重点关注的技术领域，skill 将对这些领域进行更深入的分析：

可选项：
[ ] 算法与数据结构    权重：___ (1-5)
[ ] 系统设计          权重：___ (1-5)
[ ] 编程语言基础      权重：___ (1-5)
[ ] 框架与库使用      权重：___ (1-5)
[ ] 调试与排错        权重：___ (1-5)
[ ] 架构思维          权重：___ (1-5)
[ ] 工程实践          权重：___ (1-5)
[ ] 其他：__________   权重：___ (1-5)

说明：
- 权重 5 = 最高优先级，深入到第五层分析
- 权重 3 = 标准深度，分析到第三层
- 权重 1 = 基础覆盖，仅第一二层
- 未选中的领域仍会分析但简化处理
```

### 3. 输出格式定制
```
可视化组件开关：
☑ 薄弱点严重程度饼状图     [必选]
☑ 技术领域价值分布图       [必选]
☑ 知识体系树形图           [可选]
☑ 认知模式雷达图           [可选]
☑ 学习路径时间线           [可选]
☑ 进度追踪仪表盘          [可选]

报告详略：
○ 精简版（仅核心发现 + Top3 薄弱点 + 行动清单）
○ 标准版（完整分析 + 所有图表）      [默认]
○ 详细版（标准版 + 扩展解释 + 更多示例）

导出格式：
○ HTML（交互式，推荐）
○ Markdown（纯文本）
○ PDF（静态文档）
```

### 4. 解决方案风格偏好
```
学习风格适配：
□ 实践导向型
  - 方案特点：大量动手练习，代码实战为主
  - 示例："写 5 道题"、"实现一个项目"
  
□ 理论导向型
  - 方案特点：强调概念理解，阅读文档为主
  - 示例："阅读官方文档第X章"、"理解XXX原理"

□ 混合型（理论+实践结合）
  - 方案特点：先理论后实践，循环迭代
  - 示例："先看教程 → 做练习 → 总结笔记"

时间投入预期：
□ 每天 30 分钟以下
□ 每天 30-60 分钟
□ 每天 1-2 小时
□ 每天 2 小时以上
□ 周末集中式学习

基于时间预期调整：
- 时间少 → 方案拆分为微任务（15分钟/个）
- 时间多 → 方案包含完整项目和实践周期
```

### 5. 认知风格识别（可选增强）
```
如果用户提供额外信息，可以进一步个性化：

当前学习阶段：
○ 入门期（0-6个月经验）
○ 成长期（6个月-2年）
○ 突破期（2-5年）
○ 成熟期（5年以上）

主要学习目标：
○ 通过面试/考试
○ 提升工作能力
○ 解决特定技术难题
○ 系统性知识体系构建
○ 其他：_______________

过往学习经历（影响建议方式）：
○ 自学为主（需要更多引导资源）
○ 课程/培训（习惯结构化学习）
○ 项目驱动（喜欢从实践中学习）
○ 混合方式
```

### 动态调整机制

#### 分析过程中的交互式调整

```
在生成初步分析后，提供以下交互选项：

1. "这个分析点我想深入了解"
   → 触发：对该点进行更深层次的分析
   → 补充：更多证据、更详细的根因追溯

2. "这个建议不适合我"
   → 触发：询问原因，重新生成替代方案
   → 调整：考虑用户约束条件（时间、资源、兴趣）

3. "我想看看XX方面的分析"
   → 触发：补充该领域的专项分析
   → 扩展：增加相关联的知识点分析

4. "帮我制定一个XX周的计划"
   → 触发：将行动项分解为周计划
   → 细化：每周具体任务、里程碑、检查点

5. "给我一个更激进/保守的方案"
   → 触发：调整方案的强度和节奏
   → 修改：任务数量、难度梯度、时间安排
```

#### 基于反馈的持续优化

```
记录用户对历史分析的反馈，用于优化后续分析：

反馈维度：
- 准确性：分析结论是否符合实际情况？
- 可行性：建议是否真的能执行？
- 有用性：是否帮助到了实际提升？
- 清晰度：表达是否容易理解？

优化方向：
- 如果用户多次标记某类分析"不准确"
  → 调整该领域的分析方法或增加验证步骤
  
- 如果用户多次跳过某些类型的建议
  → 降低这类建议的优先级或更换形式
  
- 如果用户总是要求更多细节
  → 默认提高输出详细程度
  
- 如果用户关注特定指标
  → 在报告中突出显示相关数据
```

### 快速配置模板

为简化配置流程，提供以下预设模板，用户可直接选择或基于此修改：

#### 模板 A：面试冲刺模板
```javascript
const interviewTemplate = {
    name: '面试冲刺',
    analysisDepth: 'standard',
    domainWeights: {
        '算法与数据结构': 5,
        '系统设计': 4,
        '编程语言基础': 3,
        '其他': 1
    },
    outputFormat: {
        charts: ['severity', 'domain', 'timeline'],
        detailLevel: 'standard',
        exportType: 'html'
    },
    solutionStyle: {
        learningStyle: 'practice',
        timeBudget: '1-2h/day',
        goal: 'interview'
    }
};
```

#### 模板 B：工作提升模板
```javascript
const workImprovementTemplate = {
    name: '工作技能提升',
    analysisDepth: 'deep',
    domainWeights: {
        '框架与库使用': 5,
        '调试与排错': 4,
        '工程实践': 4,
        '架构思维': 3
    },
    outputFormat: {
        charts: ['severity', 'domain', 'knowledgeTree'],
        detailLevel: 'detailed',
        exportType: 'html'
    },
    solutionStyle: {
        learningStyle: 'mixed',
        timeBudget: '30min/day',
        goal: 'work_improvement'
    }
};
```

#### 模板 C：入门学习模板
```javascript
const beginnerTemplate = {
    name: '入门学习',
    analysisDepth: 'quick',
    domainWeights: {
        '编程语言基础': 5,
        '算法与数据结构': 3,
        '框架与库使用': 2
    },
    outputFormat: {
        charts: ['severity', 'domain'],
        detailLevel: 'concise',
        exportType: 'html'
    },
    solutionStyle: {
        learningStyle: 'theory',
        timeBudget: '30min/day',
        goal: 'foundation_building'
    }
};
```

### 配置应用示例

#### 示例 1：面试准备场景
```javascript
const userConfig = {
    analysisDepth: 'standard', // 标准分析即可，时间有限
    domainWeights: {
        '算法与数据结构': 5, // 最高优先级
        '系统设计': 4,
        '编程语言基础': 3,
        '其他': 1
    },
    outputFormat: {
        charts: ['severity', 'domain', 'timeline'],
        detailLevel: 'standard',
        exportType: 'html'
    },
    solutionStyle: {
        learningStyle: 'practice', // 实践导向
        timeBudget: '1-2h/day',
        goal: 'interview' // 面试目标
    },
    learnerProfile: {
        stage: 'growth', // 成长期
        experience: '1 year'
    }
};

// 生成的报告将：
// 1. 重点分析算法和数据结构的薄弱点
// 2. 给出大量 LeetCode 练习建议
// 3. 包含面试高频考点的时间线
// 4. 每天分配 1-2 小时的练习计划
```

#### 示例 2：工作技能提升场景
```javascript
const userConfig = {
    analysisDepth: 'deep', // 需要深度诊断
    domainWeights: {
        '框架与库使用': 5, // 当前工作中最需要
        '调试与排错': 4,
        '工程实践': 4,
        '架构思维': 3
    },
    outputFormat: {
        charts: ['severity', 'domain', 'knowledgeTree'],
        detailLevel: 'detailed',
        exportType: 'html'
    },
    solutionStyle: {
        learningStyle: 'mixed', // 理论+实践混合
        timeBudget: '30min/day', // 工作日时间有限
        goal: 'work_improvement'
    },
    learnerProfile: {
        stage: 'breakthrough', // 突破期
        experience: '3 years'
    }
};

// 生成的报告将：
// 1. 深入分析框架使用的认知偏差
// 2. 结合实际项目 bug 进行案例教学
// 3. 提供微学习模块（每个15-20分钟）
// 4. 强调知识体系的系统化构建
```

## 深度分析框架

### 五层分析法

分析必须按照以下五个层次逐层深入，每一层都必须有明确的证据支撑：

#### 第一层：表象层（错误现象）
- 具体发生了什么错误？
- 错误的具体表现是什么？
- 在什么场景下触发？

#### 第二层：模式层（重复规律）
- 这个错误是偶发还是重复出现？
- 在哪些不同场景下出现了类似问题？
- 错误之间有什么共同特征？

#### 第三层：技术层（技能缺失）
- 缺少哪个具体的技术知识点？
- 是对概念理解有误，还是根本不知道这个概念？
- 是语法问题、逻辑问题还是架构问题？

#### 第四层：思想层（认知缺陷）
- 这个错误反映了什么样的思维模式缺陷？
- 是对问题本质的理解偏差，还是方法论的缺失？
- 是缺乏系统性思维，还是缺乏抽象能力？

#### 第五层：体系层（知识结构）
- 这个认知缺陷在整个知识体系中处于什么位置？
- 它会影响哪些其他领域的学习？
- 修复它需要重构哪些前置知识？

### 根因追溯规则

**对于每一个识别出的薄弱点，必须回答以下问题：**

1. **为什么会出现这个错误？**（直接原因）
2. **为什么用户会这样想/这样做？**（认知原因）
3. **这个认知是从哪里来的？**（根源追溯）
4. **如果只修复这个错误，还会犯类似的错吗？**（泛化风险）
5. **需要改变什么思维方式才能从根本上避免？**（根本解决方案）

### 逻辑验证机制

**每一条分析结论必须通过以下验证：**

- **证据链完整**：从输入数据到结论有清晰的推理路径
- **可复现**：给出的示例能够复现所描述的问题
- **可证伪**：结论必须是可以被验证或推翻的，不能是模糊的断言
- **因果明确**：区分相关性和因果性，不能把巧合当规律

### 真实性约束

**严禁以下行为：**

- 编造输入数据中不存在的错误模式
- 过度推断，从单一错误得出宏大结论
- 使用模糊词汇（如"可能"、"也许"、"大概"）代替具体分析
- 给出放之四海而皆准的通用建议
- 为了显得专业而使用用户不理解的技术术语

## 输出格式：HTML 可视化报告

**必须输出完整的 HTML 文件，可直接在浏览器中打开查看。**

### HTML 结构规范

**依赖说明：**
- Chart.js 3.x 或更高版本（本模板使用 Chart.js 3.x+ 语法）
- chartjs-plugin-datalabels 2.x（用于饼图标签显示）

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>技术薄弱点深度分析报告</title>
    <!-- Chart.js 3.x+ -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js@3/dist/chart.min.js"></script>
    <!-- DataLabels 插件 -->
    <script src="https://cdn.jsdelivr.net/npm/chartjs-plugin-datalabels@2"></script>
    <style>
        /* 全局样式 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Segoe UI', 'Microsoft YaHei', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 40px 20px;
            color: #333;
        }
        
        .container {
            max-width: 1400px;
            margin: 0 auto;
        }
        
        /* 卡片样式 */
        .card {
            background: white;
            border-radius: 16px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            margin-bottom: 30px;
            overflow: hidden;
        }
        
        .card-header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 24px 32px;
            font-size: 24px;
            font-weight: 600;
        }
        
        .card-body {
            padding: 32px;
        }
        
        /* 图表容器 */
        .chart-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 40px;
            margin-top: 30px;
        }
        
        .chart-box {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 24px;
            text-align: center;
        }
        
        .chart-title {
            font-size: 18px;
            font-weight: 600;
            color: #495057;
            margin-bottom: 16px;
        }
        
        canvas {
            max-width: 100%;
            height: auto !important;
        }
        
        /* 知识体系可视化 */
        .knowledge-tree {
            position: relative;
            padding: 40px;
            min-height: 600px;
        }
        
        .tree-node {
            position: absolute;
            background: white;
            border: 3px solid;
            border-radius: 50%;
            width: 120px;
            height: 120px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            font-weight: 600;
            font-size: 14px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }
        
        .tree-node:hover {
            transform: scale(1.1);
            z-index: 10;
        }
        
        .tree-root {
            left: 50%;
            top: 5%;
            transform: translateX(-50%);
            width: 150px;
            height: 150px;
            font-size: 18px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-color: #667eea;
        }
        
        .tree-line {
            position: absolute;
            height: 2px;
            background: #dee2e6;
            transform-origin: left center;
        }
        
        /* 薄弱点详情 */
        .weakness-item {
            background: linear-gradient(135deg, #fff5f5 0%, #ffe8e8 100%);
            border-left: 4px solid #ff6b6b;
            padding: 24px;
            margin-bottom: 20px;
            border-radius: 8px;
        }
        
        .weakness-item.critical {
            background: linear-gradient(135deg, #fff0f0 0%, #ffd6d6 100%);
            border-left-color: #dc3545;
        }
        
        .weakness-item.major {
            background: linear-gradient(135deg, #fffaf0 0%, #ffe8cc 100%);
            border-left-color: #fd7e14;
        }
        
        .weakness-item.minor {
            background: linear-gradient(135deg, #fff9e6 0%, #ffeeba 100%);
            border-left-color: #ffc107;
        }
        
        .weakness-level {
            display: inline-block;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 12px;
        }
        
        .level-critical { background: #dc3545; color: white; }
        .level-major { background: #fd7e14; color: white; }
        .level-minor { background: #ffc107; color: #212529; }
        
        /* 优点样式 */
        .strength-item {
            background: linear-gradient(135deg, #f0fff4 0%, #d4edda 100%);
            border-left: 4px solid #28a745;
            padding: 24px;
            margin-bottom: 20px;
            border-radius: 8px;
        }
        
        /* 行动清单 */
        .action-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        
        .action-table th,
        .action-table td {
            padding: 16px;
            text-align: left;
            border-bottom: 1px solid #dee2e6;
        }
        
        .action-table th {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            font-weight: 600;
        }
        
        .action-table tr:hover {
            background: #f8f9fa;
        }
        
        .priority-badge {
            display: inline-block;
            padding: 6px 16px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 13px;
        }
        
        .p0 { background: #dc3545; color: white; }
        .p1 { background: #fd7e14; color: white; }
        .p2 { background: #28a745; color: white; }
        
        /* 响应式 */
        @media (max-width: 768px) {
            body { padding: 20px 10px; }
            .card-body { padding: 20px; }
            .chart-container { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- 执行摘要 -->
        <div class="card">
            <div class="card-header">📊 执行摘要</div>
            <div class="card-body">
                <p style="font-size: 18px; line-height: 1.8;">[核心发现摘要]</p>
            </div>
        </div>

        <!-- 可视化仪表盘 -->
        <div class="card">
            <div class="card-header">🎯 数据概览</div>
            <div class="card-body">
                <div class="chart-container">
                    <!-- 饼状图1：薄弱点重要程度分布 -->
                    <div class="chart-box">
                        <div class="chart-title">薄弱点严重程度分布</div>
                        <canvas id="severityChart"></canvas>
                    </div>
                    
                    <!-- 饼状图2：技术领域价值分布 -->
                    <div class="chart-box">
                        <div class="chart-title">技术领域价值分布</div>
                        <canvas id="domainChart"></canvas>
                    </div>
                </div>
            </div>
        </div>

        <!-- 可保持的知识体系 -->
        <div class="card">
            <div class="card-header">💪 已建立的知识体系</div>
            <div class="card-body">
                <div class="knowledge-tree" id="knowledgeTree">
                    <!-- 动态生成的知识体系树形图 -->
                </div>
                <div id="strengthDetails" style="margin-top: 30px;">
                    <!-- 优点详细列表 -->
                </div>
            </div>
        </div>

        <!-- 薄弱点深度剖析 -->
        <div class="card">
            <div class="card-header">⚠️ 薄弱点深度剖析</div>
            <div class="card-body" id="weaknessList">
                <!-- 薄弱点列表 -->
            </div>
        </div>

        <!-- 认知模式诊断 -->
        <div class="card">
            <div class="card-header">🧠 认知模式诊断</div>
            <div class="card-body">
                <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px;">
                    <div>
                        <h3 style="color: #28a745; margin-bottom: 20px;">✅ 优势思维模式</h3>
                        <div id="positivePatterns"></div>
                    </div>
                    <div>
                        <h3 style="color: #fd7e14; margin-bottom: 20px;">⚡ 待改进思维模式</h3>
                        <div id="improvePatterns"></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- 优先级行动清单 -->
        <div class="card">
            <div class="card-header">🚀 优先级行动清单</div>
            <div class="card-body">
                <table class="action-table">
                    <thead>
                        <tr>
                            <th>优先级</th>
                            <th>问题</th>
                            <th>具体行动</th>
                            <th>预期时间</th>
                            <th>验证方式</th>
                        </tr>
                    </thead>
                    <tbody id="actionTableBody">
                        <!-- 行动项 -->
                    </tbody>
                </table>
            </div>
        </div>

        <!-- 学习路径建议 -->
        <div class="card">
            <div class="card-header">📈 学习路径建议</div>
            <div class="card-body" id="learningPath">
                <!-- 学习路径 -->
            </div>
        </div>

        <!-- 分析局限性 -->
        <div class="card">
            <div class="card-header">ℹ️ 分析局限性</div>
            <div class="card-body">
                <p>[诚实说明本次分析的局限]</p>
            </div>
        </div>
    </div>

    <script>
        // 注册 datalabels 插件
        Chart.register(ChartDataLabels);
        
        // 饼状图配置
        const chartOptions = {
            responsive: true,
            plugins: {
                legend: {
                    display: false  // 隐藏底部图例，因为标签直接显示在饼图上
                },
                datalabels: {
                    color: '#ffffff',
                    font: {
                        size: 14,
                        weight: 'bold'
                    },
                    formatter: (value, context) => {
                        // 计算百分比
                        const total = context.dataset.data.reduce((a, b) => a + b, 0);
                        const percentage = Math.round((value / total) * 100);
                        const label = context.chart.data.labels[context.dataIndex];
                        return label + '\n' + percentage + '%';
                    },
                    anchor: 'center',
                    align: 'center',
                    textAlign: 'center',
                    textShadowColor: 'rgba(0, 0, 0, 0.3)',
                    textShadowBlur: 4
                },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            return context.label + ': ' + context.parsed + '%';
                        }
                    }
                }
            },
            animation: {
                animateScale: true,
                animateRotate: true
            }
        };

        // 明亮配色方案
        const brightColors = [
            '#FF6B6B', // 红
            '#4ECDC4', // 青
            '#45B7D1', // 蓝
            '#96CEB4', // 绿
            '#FFEAA7', // 黄
            '#DDA0DD', // 紫
            '#98D8C8', // 薄荷绿
            '#F7DC6F'  // 金黄
        ];

        // 初始化饼状图
        function initCharts(severityData, domainData) {
            // 薄弱点严重程度分布
            new Chart(document.getElementById('severityChart'), {
                type: 'pie',
                data: {
                    labels: severityData.labels,
                    datasets: [{
                        data: severityData.values,
                        backgroundColor: ['#DC3545', '#FD7E14', '#FFC107'],
                        borderWidth: 3,
                        borderColor: '#ffffff'
                    }]
                },
                options: chartOptions
            });

            // 技术领域价值分布
            new Chart(document.getElementById('domainChart'), {
                type: 'doughnut',
                data: {
                    labels: domainData.labels,
                    datasets: [{
                        data: domainData.values,
                        backgroundColor: brightColors.slice(0, domainData.labels.length),
                        borderWidth: 3,
                        borderColor: '#ffffff'
                    }]
                },
                options: chartOptions
            });
        }

        // 生成知识体系树形图
        function generateKnowledgeTree(structure) {
            const container = document.getElementById('knowledgeTree');
            if (!structure || !structure.root) {
                container.innerHTML = '<p style="text-align: center; color: #6c757d;">暂无知识体系数据</p>';
                return;
            }

            // 清空容器
            container.innerHTML = '';

            // 创建根节点
            const rootNode = createTreeNode(structure.root, 'tree-root', 50, 5);
            container.appendChild(rootNode);

            // 递归创建子节点
            if (structure.root.children) {
                structure.root.children.forEach((child, index) => {
                    createChildNodes(child, 50, 5, index, structure.root.children.length, 1);
                });
            }

            // 绘制连接线
            drawConnections(container);
        }

        // 创建树节点
        function createTreeNode(data, className, leftPercent, topPercent) {
            const node = document.createElement('div');
            node.className = `tree-node ${className}`;
            node.style.left = `${leftPercent}%`;
            node.style.top = `${topPercent}%`;
            node.style.transform = className === 'tree-root' ? 'translateX(-50%)' : 'translate(-50%, -50%)';
            node.innerHTML = `<span>${data.name}</span>`;
            node.dataset.id = data.id || '';
            node.dataset.level = data.level || 0;

            // 根据掌握程度设置颜色
            if (data.mastery !== undefined) {
                const colors = ['#dc3545', '#fd7e14', '#ffc107', '#28a745', '#20c997'];
                node.style.borderColor = colors[Math.min(data.mastery, 4)];
            }

            // 添加悬停提示
            if (data.description) {
                node.title = data.description;
            }

            return node;
        }

        // 递归创建子节点
        function createChildNodes(data, parentLeft, parentTop, index, totalSiblings, level) {
            const container = document.getElementById('knowledgeTree');
            const maxLevel = 3;

            if (level > maxLevel) return;

            // 计算当前节点的位置
            const levelHeight = 25; // 每层高度百分比
            const top = parentTop + levelHeight;

            // 水平分布计算
            const sectionWidth = 100 / (Math.pow(2, level));
            const left = (index + 0.5) * sectionWidth;

            const node = createTreeNode(data, '', left, top);
            container.appendChild(node);

            // 递归创建子节点
            if (data.children) {
                data.children.forEach((child, childIndex) => {
                    createChildNodes(child, left, top, childIndex, data.children.length, level + 1);
                });
            }
        }

        // 绘制节点间的连接线
        function drawConnections(container) {
            const nodes = container.querySelectorAll('.tree-node');
            const nodeMap = new Map();

            nodes.forEach(node => {
                const rect = node.getBoundingClientRect();
                const containerRect = container.getBoundingClientRect();
                nodeMap.set(node, {
                    x: rect.left - containerRect.left + rect.width / 2,
                    y: rect.top - containerRect.top + rect.height / 2
                });
            });

            // 使用 SVG 绘制连接线
            const svg = document.createElementNS('http://www.w3.org/2000/svg', 'svg');
            svg.style.position = 'absolute';
            svg.style.top = '0';
            svg.style.left = '0';
            svg.style.width = '100%';
            svg.style.height = '100%';
            svg.style.pointerEvents = 'none';
            svg.style.zIndex = '1';

            nodes.forEach(node => {
                const parentPos = nodeMap.get(node);
                const parentData = node.dataset;

                // 找到所有子节点并绘制连线
                nodes.forEach(childNode => {
                    const childData = childNode.dataset;
                    if (parseInt(childData.level) === parseInt(parentData.level) + 1) {
                        const childPos = nodeMap.get(childNode);
                        const line = createSVGLine(parentPos.x, parentPos.y + 60, childPos.x, childPos.y - 60);
                        svg.appendChild(line);
                    }
                });
            });

            container.insertBefore(svg, container.firstChild);
        }

        // 创建 SVG 线条
        function createSVGLine(x1, y1, x2, y2) {
            const line = document.createElementNS('http://www.w3.org/2000/svg', 'line');
            line.setAttribute('x1', x1);
            line.setAttribute('y1', y1);
            line.setAttribute('x2', x2);
            line.setAttribute('y2', y2);
            line.setAttribute('stroke', '#dee2e6');
            line.setAttribute('stroke-width', '2');
            return line;
        }

        // 渲染薄弱点
        function renderWeaknesses(weaknesses) {
            const container = document.getElementById('weaknessList');
            const html = weaknesses.map(w => createWeaknessHTML(w)).join('');
            container.innerHTML = html;
        }

        // 创建薄弱点 HTML
        function createWeaknessHTML(weakness) {
            const levelLabels = {
                critical: { class: 'critical', name: '致命' },
                major: { class: 'major', name: '主要' },
                minor: { class: 'minor', name: '次要' }
            };

            const levelInfo = levelLabels[weakness.level] || levelLabels.minor;

            const analysisItems = [
                { label: '表象', content: weakness.surface },
                { label: '模式', content: weakness.pattern },
                { label: '技术根因', content: weakness.techRoot },
                { label: '认知根因', content: weakness.cognitiveRoot },
                { label: '体系影响', content: weakness.systemImpact }
            ];

            const analysisHTML = analysisItems
                .filter(item => item.content)
                .map(item => `<strong>${item.label}：</strong><p>${item.content}</p>`)
                .join('');

            const solutionsHTML = weakness.solutions?.length
                ? `<ol style="margin-left: 20px; margin-top: 8px;">
                    ${weakness.solutions.map(s => `<li>${s}</li>`).join('')}
                   </ol>`
                : '<p style="color: #6c757d;">暂无具体解决方案</p>';

            return `
                <div class="weakness-item ${levelInfo.class}">
                    <span class="weakness-level level-${weakness.level}">${weakness.levelName || levelInfo.name}</span>
                    <h3>${weakness.name || '未命名薄弱点'}</h3>
                    <div style="margin-top: 16px;">
                        ${analysisHTML}
                        <div style="background: white; padding: 16px; border-radius: 8px; margin-top: 12px;">
                            <strong>解决方案：</strong>
                            ${solutionsHTML}
                        </div>
                    </div>
                </div>
            `;
        }

        // 渲染行动清单
        function renderActions(actions) {
            const tbody = document.getElementById('actionTableBody');
            actions.forEach(a => {
                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td><span class="priority-badge p${a.priority}">P${a.priority}</span></td>
                    <td><strong>${a.problem}</strong></td>
                    <td>${a.action}</td>
                    <td>${a.timeline}</td>
                    <td>${a.validation}</td>
                `;
                tbody.appendChild(tr);
            });
        }

        // 初始化所有内容
        document.addEventListener('DOMContentLoaded', function() {
            try {
                // 从分析结果中获取数据并渲染
                // 示例数据结构：
                const severityData = {
                    labels: ['致命 (Critical)', '主要 (Major)', '次要 (Minor)'],
                    values: [30, 50, 20]
                };

                const domainData = {
                    labels: ['算法与数据结构', '系统设计', '编程语言基础', '框架与库使用', '调试与排错'],
                    values: [25, 20, 30, 15, 10]
                };

                const weaknesses = [
                    {
                        level: 'critical',
                        levelName: '致命',
                        name: '动态规划思维缺失',
                        surface: '无法识别重叠子问题',
                        pattern: '在3道DP题目中均使用递归导致超时',
                        techRoot: '缺乏自底向上的状态积累意识',
                        cognitiveRoot: '思维模式停留在递归而非状态转移',
                        systemImpact: '影响算法类面试表现',
                        solutions: ['完成5道一维DP题目', '画递归树标记重复计算', '强制改写为迭代版本']
                    }
                ];

                const actions = [
                    {
                        priority: 0,
                        problem: 'DP思维缺失',
                        action: '完成LeetCode 70, 198, 322题',
                        timeline: '1周内',
                        validation: '能在3分钟内判断DP适用性'
                    }
                ];

                const knowledgeStructure = {
                    root: {
                        name: '编程能力',
                        id: 'root',
                        level: 0,
                        mastery: 3,
                        description: '核心编程技能',
                        children: [
                            {
                                name: '算法',
                                id: 'algo',
                                level: 1,
                                mastery: 2,
                                description: '算法设计与分析',
                                children: [
                                    { name: 'DP', id: 'dp', level: 2, mastery: 1, description: '动态规划' },
                                    { name: '贪心', id: 'greedy', level: 2, mastery: 3, description: '贪心算法' }
                                ]
                            }
                        ]
                    }
                };

                // 初始化图表
                initCharts(severityData, domainData);

                // 渲染薄弱点
                if (weaknesses && weaknesses.length > 0) {
                    renderWeaknesses(weaknesses);
                } else {
                    document.getElementById('weaknessList').innerHTML =
                        '<p style="text-align: center; color: #28a745;">🎉 未发现明显薄弱点，继续保持！</p>';
                }

                // 渲染行动清单
                if (actions && actions.length > 0) {
                    renderActions(actions);
                }

                // 生成知识体系树
                generateKnowledgeTree(knowledgeStructure);

            } catch (error) {
                console.error('报告初始化失败:', error);
                document.body.innerHTML = `
                    <div style="padding: 40px; text-align: center;">
                        <h2 style="color: #dc3545;">⚠️ 报告加载失败</h2>
                        <p style="color: #6c757d; margin-top: 16px;">${error.message}</p>
                        <p style="color: #6c757d; margin-top: 8px;">请检查浏览器控制台获取详细信息</p>
                    </div>
                `;
            }
        });
    </script>
</body>
</html>
```

### 可视化组件规范

#### 1. 薄弱点严重程度饼状图

**用途**：展示各类薄弱点的严重程度分布

**数据结构**：
```javascript
{
    labels: ['致命 (Critical)', '主要 (Major)', '次要 (Minor)'],
    values: [x, y, z]  // 百分比或数量
}
```

**颜色方案**：
- 致命：`#DC3545`（红色）
- 主要：`#FD7E14`（橙色）
- 次要：`#FFC107`（黄色）

#### 2. 技术领域价值分布饼状图

**用途**：展示各技术领域的掌握程度和价值分布

**数据结构**：
```javascript
{
    labels: ['算法与数据结构', '系统设计', '框架使用', '调试能力', ...],
    values: [x, y, z, ...]  // 掌握度评分或权重
}
```

**颜色方案**（明亮色调）：
```javascript
const brightColors = [
    '#FF6B6B',  // 珊瑚红
    '#4ECDC4',  // 青绿
    '#45B7D1',  // 天蓝
    '#96CEB4',  // 薄荷绿
    '#FFEAA7',  // 柠檬黄
    '#DDA0DD',  // 淡紫
    '#98D8C8',  // 水绿
    '#F7DC6F'   // 金黄
];
```

#### 3. 知识体系可视化（树形/网络图）

**用途**：展示已建立的稳固知识和思想体系

**设计要求**：

1. **层级结构清晰**
   - 根节点：核心技术栈/核心能力
   - 二级节点：主要技术领域
   - 三级节点：具体技能点
   - 叶节点：已掌握的具体知识点

2. **视觉特征**
   - 使用圆形节点表示知识点
   - 节点大小反映重要性或掌握程度
   - 连接线表示知识间的关联关系
   - 已掌握的知识用绿色系标识
   - 强项用渐变色高亮

3. **布局方式**
   ```
           [核心能力]
          /    |    \
     [领域1] [领域2] [领域3]
      / | \     | \     \
   [点] [点] [点] [点] [点]
   ```

4. **交互功能**
   - 悬停显示详细信息
   - 点击展开/收起子节点
   - 高亮显示相关联的知识点

5. **实现方式**
   - 使用 CSS 绝对定位 + JavaScript 动态计算位置
   - 或使用 SVG 绘制更精确的图形
   - 支持响应式布局

#### 4. 配色总则

**整体风格**：明亮、现代、专业但不沉闷

**主色调**：
- 主色：`#667eea` 到 `#764ba2` 渐变（紫蓝渐变）
- 成功/优点：`#28a745`（绿色系）
- 警告/薄弱：`#fd7e14`（橙色系）到 `#dc3545`（红色系）
- 背景：白色卡片 + 浅色渐变背景

**视觉效果**：
- 圆角设计（border-radius: 12-16px）
- 柔和阴影（box-shadow）
- 渐变背景增加层次感
- 充足留白提升可读性

### HTML 输出流程

1. **完成深度分析后**，收集所有分析数据
2. **构建数据对象**：
   ```javascript
   const reportData = {
       summary: "执行摘要",
       strengths: [...],  // 优点数组
       weaknesses: [...], // 薄弱点数组
       knowledgeGaps: [...], // 知识盲区
       cognitivePatterns: {...}, // 认知模式
       actions: [...], // 行动清单
       learningPath: "...", // 学习路径
       limitations: "...", // 局限性
       
       // 图表数据
       severityDistribution: {...},
       domainValueDistribution: {...},
       knowledgeStructure: {...} // 知识体系树形结构
   };
   ```

3. **生成完整 HTML 文件**，包含：
   - 所有样式定义
   - Chart.js 库引用
   - 数据填充
   - 初始化脚本

4. **保存为 `.html` 文件**供用户在浏览器中查看

## 分析示例

### 示例：算法错误深度分析

**输入数据：**
```
用户在 3 道动态规划题目中失败：
1. 爬楼梯问题 - 用了递归，超时
2. 背包问题 - 状态转移方程写错
3. 最长递增子序列 - 没想到用 DP
```

**错误分析（浅层 vs 深层）：**

**浅层分析（禁止）：**
> 你的动态规划不好，需要多练习。建议看一些 DP 教程。

✅ **深层分析（要求）：**
> **认知根因**：你没有建立"重叠子问题"的识别直觉。三道题的共同特征是：
> - 爬楼梯：f(n) = f(n-1) + f(n-2)，子问题 f(n-1) 被重复计算
> - 背包：每个物品选或不选，子问题重叠
> - LIS：以每个位置结尾的最长序列，子问题重叠
>
> 你的思维模式是"从上到下"的递归思维，缺少"从下到上"的状态积累意识。
>
> **具体解决方案**：
> 1. 立即行动：把爬楼梯的递归代码画成递归树，标记重复计算的节点，然后手动改写为自底向上的迭代版本
> 2. 短期突破：完成 5 道"一维 DP"题目，每道题强制要求：先写递归→画递归树→发现重叠→改写迭代
> 3. 验证方式：给一道新的 DP 题，能在 3 分钟内判断是否可用 DP，并写出状态转移方程

## 最佳实践

1. **证据驱动**：每一条结论必须有输入数据中的具体证据支撑
2. **深度优先**：宁可分析 3 个问题到第五层，也不要分析 10 个问题停在第一层
3. **具体至上**：解决方案必须具体到"做什么、怎么做、用什么资源、如何验证"
4. **诚实透明**：不确定的地方明确标注，不编造、不夸大
5. **逻辑闭环**：从问题→根因→方案→验证，形成完整链条
6. **用户视角**：用用户能理解的语言，不堆砌术语
7. **可操作性**：每个建议都应该是用户看完就能开始行动的
8. **视觉美观**：HTML 输出必须符合现代 UI 设计标准，色彩鲜明，布局合理
9. **适应性优先**：根据用户配置动态调整分析深度、输出格式和方案风格
10. **持续优化**：记录用户反馈，不断改进分析的准确性和实用性
11. **交互友好**：提供多个调整入口，让用户随时可以改变分析方向
12. **场景感知**：根据用户的学习目标和阶段，自动匹配最合适的分析策略