# 大模型内容安全治理平台与应用验证

面向大模型内容安全治理，开放风险溯因、风险识别、合规编辑、数据血缘追踪与应用验证相关研究代码和工具，为研究复用、能力评测及应用集成提供可获取、可追溯的源码发布版本。

**发布单位：NGAI-LLMSafeContent**  
**公开发布组织：NGAI-LLMSafeContent-OpenSource**  
**正式发布分支：`release/1.0`**  
**tag：`v1.0`**  
**自研代码许可证：Apache License 2.0；第三方代码、模型及数据按各自许可证执行。**

## 开源目标与模块

指标 4.5 的开源目标为：**将多特征多层次的因果追踪、多层次风险识别、全链路合规追踪模块，在 1 个国家级人工智能开源社区以及 1 个国际主流开源社区中开源发布。** 本组织围绕这一目标组织相关模块及项目工具链的公开发布，支持后续平台部署、研究复用与应用适配。

2026 年 12 月里程碑重点为**多特征多层次因果追踪、多层次风险识别**两个年度方向。当前公开实现及其适用范围如下。

| 方向 | 已公开模块与能力 | 源码入口 |
| --- | --- | --- |
| 因果追踪相关研究 | **SIRG / LRP 输出归因候选实现**：内部推理图构建、层相关性传播、实体与贡献分析、图形展示及相关研究流程。当前作为因果追踪方向的归因候选公开，与指标名称的正式对应关系仍需课题负责人确认。 | [输出风险归因](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_4_Output_Risk_Attribution-release/tree/release/1.0) |
| 多层次风险识别 | **FilterGuard 异常数据识别工具**：关键词识别、token 异常检测、神经元激活分析及统一风险分类，配套提供级联识别、数据准备与评测入口。 | [异常数据识别](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_2_Anomaly_Data_Identification-release/tree/release/1.0) |
| 全链路合规追踪相关能力 | **输入侧风险标注与数据血缘追踪**：血缘图谱构建、风险传播、清洗、报告和图谱导出；**Agent 轨迹审计**：轨迹规范化、风险审计、评分归档与交互审阅；通过治理平台组织前后端交互及跨课题能力适配。已公开模块不等同于训练前、训练中、训练后全部链路均已公开或完成验收。 | [输入侧血缘工作流](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_4_Input_workflow-release/tree/release/1.0) · [Agent 轨迹审计](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_5_Agent_Trajectory_Risk_Audit_Tool-release/tree/release/1.0) · [治理平台](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_5_LLM_Content_Safety_Governance_Web-release/tree/release/1.0) |

## 发布进展与平台

截至 **2026 年 11 月 27 日**，已在首批 **14 个工具源码仓库**基础上，补充公开输出风险归因候选实现和输入侧血缘工作流，形成 **16 个正式项目发布仓库**，涵盖风险溯因、异常检测、合规编辑、文化多样性评估、轨迹审计与平台集成等能力。

- **GitHub**：[NGAI-LLMSafeContent-OpenSource](https://github.com/NGAI-LLMSafeContent-OpenSource)——国际开源发布入口。
- **AtomGit**：[NGAI-LLMSafeContent-OpenSource](https://atomgit.com/NGAI-LLMSafeContent-OpenSource)——国内开源发布入口。
- **OpenI 启智社区**：[molip 项目列表](https://openi.pcl.ac.cn/molip)——国内人工智能开源发布入口。
- **ModelScope 魔搭社区**：[joplit 主页](https://www.modelscope.cn/profile/joplit)——配套 Studio 代码发布入口；是否部署运行以具体项目说明及平台状态为准。

正式项目仓库名称以 `-release` 结尾，使用 `release/1.0` 分支。GitHub 与 AtomGit 的 16 对对应仓库已完成版本一致性核对，Commit ID、目录结构、文件清单和逐文件 SHA-256 一致。OpenI 对应发布分支同步维护。ModelScope 的 Agent 仓受平台审核删减影响，保留已披露的版本差异，不计作与其他平台整仓内容一致。

## 项目导航

以下链接均指向正式发布分支；安装、配置、接口和验证入口以各仓 README 为准。

| 课题 | 已发布项目 |
| --- | --- |
| 课题一：评价与风险溯因相关工具 | [评价体系构建](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_1_Construction_of_Evaluation_System-release/tree/release/1.0) · [伦理评估](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_1_Ethical_Assessment-release/tree/release/1.0) · [样本评测与生成](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_1_Sample_evaluation_Generation-release/tree/release/1.0) · [风险归因](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_1_Risk_Cause_Determination-release/tree/release/1.0) |
| 课题二：异常识别与数据飞轮 | [FilterGuard 异常数据识别](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_2_Anomaly_Data_Identification-release/tree/release/1.0) · [异常检测、追踪与修正飞轮](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_2_Flywheel_on_Anomaly_Detection_Tracking_Correction-release/tree/release/1.0) |
| 课题三：合规编辑与文化多样性相关工具 | [合规编辑](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_3_Compliance_Editing_Tool-release/tree/release/1.0) · [文化多样性评估](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_3_Cultural_Diversity_Assessment_Tool-release/tree/release/1.0) · [文化多样性语料生成](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_3_Cultural_Diversity_Corpus_Generation_Tool-release/tree/release/1.0) · [文化多样性测试](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_3_Cultural_Diversity_test-release/tree/release/1.0) · [文化内容生成](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_3_Cultural_Generation_Tool-release/tree/release/1.0) · [动态难度问题生成](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_3_Dynamic_Difficulty_Question_Generation_Tool-release/tree/release/1.0) |
| 课题四：归因候选与输入侧血缘追踪 | [SIRG / LRP 输出风险归因候选](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_4_Output_Risk_Attribution-release/tree/release/1.0) · [输入风险标注与血缘工作流](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_4_Input_workflow-release/tree/release/1.0) |
| 课题五：治理平台与应用验证 | [大模型内容安全治理平台](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_5_LLM_Content_Safety_Governance_Web-release/tree/release/1.0) · [Agent 轨迹风险审计工具](https://github.com/NGAI-LLMSafeContent-OpenSource/Project_5_Agent_Trajectory_Risk_Audit_Tool-release/tree/release/1.0) |

## 获取、使用与版本核对

选择项目后下载或克隆其 `release/1.0` 分支，按仓库 README 准备运行环境、示例配置及必要的外部能力。项目所需模型、受限数据、算力或上游服务不当然包含在源码发布包内，其获取方式、许可边界和已知问题见对应说明。

各仓提供 README、依赖与安装说明、许可证、第三方组件声明，以及以下发布记录：

- `RELEASE_FILES.md`：逐文件发布清单。
- `RELEASE_MANIFEST.json`、`SHA256SUMS`：文件校验记录。
- `SOURCE_ALIGNMENT.json`：来源提交、文件对应关系及经授权的发布例外。

`release/1.0` 是持续维护的发布分支。复现或引用时请同时记录**仓库地址、完整 Commit ID 和文件校验值**，避免仅凭同名分支推断两个时间点为同一版本。公开配置中的示例域名为占位符，部署时应填写自己的服务地址。

## 开源许可与第三方归属

各仓自研代码采用 **[Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)**。具体适用范围以仓库 `LICENSE` 和 `THIRD_PARTY_NOTICES.md` 为准；第三方组件保留原作者署名和原许可证，包括相关归因实现中使用的 MIT 许可组件。模型权重、数据集及外部服务遵循各自授权，不因本组织的源码发布而获得额外许可。

## 验证与后续工作

当前公开成果包括源码发布、文件完整性核查、跨平台版本核对，以及各仓明确记录的本地测试或最小冒烟检查。这些记录与真实模型效果验证、完整跨课题业务链路验收和第三方正式测试报告分别管理。

按照经主责单位认可的测试方案开展第三方测试并出具测试报告，是后续正式验证工作；本页不将现有发布和完整性记录替代为已取得的第三方验收结论。模块指标对应关系、外部能力准备和运行限制以各课题确认及仓库说明为准。

## 反馈与协作

问题反馈请提交到对应项目仓库的 Issues，并附发布分支、Commit ID、复现步骤及脱敏日志。提交贡献前请阅读项目许可和第三方声明；不要提交真实访问令牌、口令、内部服务地址、个人信息或未经授权的模型与数据。
