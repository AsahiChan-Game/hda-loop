# 案例证据与适用边界

平台、游戏与影视技术指南，以及跨风格美术研究另见 [standards-sources.md](standards-sources.md)；它们用于形成任务规格，不把案例或平台建议当作统一行业认证。

核对日期：2026-09-08。以下页面支持工作流背景；具体节点、插件属性、许可证和引擎版本在实施时按项目再核对。下文的多层 HDA、完整室内与验证约定是本技能设计，不宣称全部来自示例项目。

## Project Titan：小工具组成大环境

[SideFX Project Titan](https://www.sidefx.com/titan/) 是面向 UE5 的程序化环境制作技术演示，展示建筑、植物、线缆、围栏等可供艺术家在 UE 编辑器中使用的工具。项目也使用了 KitBash3D 几何；因此它不证明所有输入几何都由 HDA 从零生成，也不自动授予第三方素材使用权。

- [Shrub Tool](https://www.sidefx.com/tutorials/project-titan-shrub-tool/)：枝叶程序化生成、输入形状控制灌木外形、封装 HDA。适合参考小型植物工具的控制方式。
- [Ivy Tool](https://www.sidefx.com/tutorials/project-titan-ivy-tool/)：依附输入形状生成藤蔓、放置叶片并处理下垂枝条。适合参考附着与增长的职责划分。
- [Building Tool](https://www.sidefx.com/tutorials/project-titan-building-tool/)：从 UE 中的体量输入生成建筑，使用模块实例并处理屋顶。不能据此宣称已具备完整可进入室内和所有家具生成。

这些教程发布于 2022 年；它们是设计参考，不是本机新版本直接可运行的保证。不要照搬旧版本安装步骤或未经检查的节点 API。

## Anastasia Opara：Procedural Lake Houses

[SideFX 的课程介绍](https://www.sidefx.com/tutorials/procedural-lake-houses-volume-1/) 标明作者 Anastasia Opara，内容覆盖建筑轮廓、模块、材质及布景。作者公开的 [Volume 2](https://anopara.gumroad.com/l/XWhv)、[Volume 4](https://anopara.gumroad.com/l/sVtLq) 和 [Volume 5](https://anopara.gumroad.com/l/qXIjl) 介绍了模块关系、表面图案和受约束的变化。仅核对公开说明，不声称审核了完整课程。

公开案例说明用于归纳设计问题，不证明任何私人课程工程的节点结构、模型质量或运行兼容性。使用自有工程时应另行检查实际输出及授权。

可归纳的设计问题是：基础构件是否合格、部件如何匹配、比例如何统一、表面与变化如何受控。它帮助充实 [质量框架](quality-framework.md)，不作为固定木屋生产配方。未来使用用户工程时重新确认文件现状及授权；本技能不复制工程或素材，也不依赖它们存在于固定磁盘路径。

## The Matrix Awakens / City Sample：分层生成城市

- [Epic 官方介绍](https://www.unrealengine.com/blog/introducing-the-matrix-awakens-an-unreal-engine-5-experience?lang=en)：介绍 Houdini 程序规则与 UE 世界系统共同构建城市。
- [Generating a World 官方技术演讲](https://www.sidefx.com/learn/talks/the-matrix-awakens-generating-a-world/)：了解 Houdini 与 UE 工具分工；本次核对了官方页面介绍，未逐帧审核演讲视频。
- [City Sample 官方文档](https://dev.epicgames.com/documentation/unreal-engine/city-sample-project-unreal-engine-demonstration)：城市生成、渲染和运行系统的背景。
- [生成城市与高速路的 UE 导入指南](https://dev.epicgames.com/documentation/en-us/unreal-engine/city-sample-quick-start-for-generating-a-city-and-freeway-in-unreal-engine-5)：展示 Houdini 数据、几何及点云导入后构建城市的流程。不要把这条工作流简化成“拖一个通用 HDA 就有完整 Matrix 城市”，也不要将样例专用点云路径与现代 PCG 自动等同。

参考分层布局、模块复用和大范围数据组织。完整室内、每种家具的生成器、交互、交通和人群需分别确认范围与实现证据。

## Houdini Engine for Unreal

- [Introduction](https://www.sidefx.com/docs/houdini/unreal/intro.html)：HDA 输入、参数、输出和 recook/rebuild/bake 的区别；烘焙产物脱离原 HDA 参数连接。
- [Instancers](https://www.sidefx.com/docs/houdini/unreal/instancing.html)：packed primitives、实例组件与现有资源引用的输出方式。具体属性与限制按项目版本查询，不固定沿用教程设置。

当前网页可能展示比项目更新的 Houdini/UE 版本。记录本机事实后再选择对应文档，不能通过查到新版页面就宣布本机兼容或自动升级。
