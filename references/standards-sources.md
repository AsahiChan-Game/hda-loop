# 资产标准研究：官方来源与边界

核对日期 **2026-09-08**。以下为公开一手来源；“当前网页可查”不等于“为当前硬件新写”，网页显示的默认引擎版本也不是本机版本。未研究各主机厂商保密认证规范或商业工作室内部预算，不能宣称覆盖它们。

## 技术指南

| 来源 | 支持的判断 | 使用限制 |
|---|---|---|
| [Google/Arm：Geometry](https://developer.android.com/games/optimize/geometry) | 轮廓相关几何、LOD、避免低收益几何、设备上检查 | 旧索引/设备示例按当前硬件与引擎核对，不变成所有资产面数上限 |
| [Google/Arm：Textures](https://developer.android.com/games/optimize/textures) | 图集、mip、分辨率、颜色与数据通道、压缩 | 页面部分引擎示例仍为旧版，不照搬具体操作或过滤器性能结论 |
| [Unity：Graphics and assets optimization](https://unity.com/blog/games/optimize-your-mobile-game-performance-expert-tips-on-graphics-and-assets) | 批处理、几何/材质开销、移动透明 overdraw | 2021 年经验；不把 Unity 操作直接写成 UE API |
| [Epic：Mobile rendering and shading modes](https://dev.epicgames.com/documentation/en-us/unreal-engine/mobile-rendering-and-shading-modes-for-unreal-engine) | 移动渲染路径具有性能与特性取舍 | 项目版本和设备决定选择，不因文档存在就自动切换 |
| [Epic：Mobile performance guidelines](https://dev.epicgames.com/documentation/en-us/unreal-engine/performance-guidelines-for-mobile-devices-in-unreal-engine) | 移动光照/品质档应按目标设备安排 | 设备示例与默认值不是跨项目标准 |
| [Epic：Nanite overview](https://dev.epicgames.com/documentation/unreal-engine/nanite-virtualized-geometry-in-unreal-engine) 与 [technical details](https://dev.epicgames.com/documentation/en-us/unreal-engine/nanite-technical-details) | 高密度几何、精度、fallback、驻留与数据大小 | 不推出着色、透明、实例及整帧成本无限；按安装版本确认能力 |
| [Epic：Physically Based Materials](https://dev.epicgames.com/documentation/en-us/unreal-engine/physically-based-materials-in-unreal-engine) | 物理材质参数及非写实用途 | 物理测量示例不强迫所有风格照搬 |
| [Epic：Ray tracing and path tracing](https://dev.epicgames.com/documentation/unreal-engine/ray-tracing-and-path-tracing-features-in-unreal-engine) 与 [Path Tracer](https://dev.epicgames.com/documentation/en-us/unreal-engine/path-tracer-in-unreal-engine) | 实时与离线输出区别、MRQ 渲染 | 离线成片不能证明实时帧率；本次未实测渲染器 |
| [OpenUSD Introduction](https://openusd.org/release/intro.html) | 场景层级、几何/着色表示、资产引用 | 格式与工具能力不是视觉品质认证或材质无损互通保证 |
| [ACEScg Specification](https://docs.acescentral.com/encodings/acescg/) | 影视工作空间的明确色彩定义 | 不等于每个项目必须使用，不自动覆盖已有 OCIO/显示设置 |

## 美术方向与案例

- [Valve：Dota 2 Character Art Guide](https://help.steampowered.com/en/faqs/view/0688-7692-4D5A-1935)：轮廓、明暗、色彩、细节与留白，以及在实际观看环境下评估。提炼方法，不移植英雄专属要求。
- [Riot：Making VALORANT’s Fracture](https://playvalorant.com/en-gb/news/dev/controlled-ruptures-making-valorant-s-fracture/)：从整体美术意图明确形状、色板、情绪，再与关卡空间协作。它不是通用房屋生成规范。
- [Pixar：Stylization at Pixar](https://renderman.pixar.com/stories/stylization-at-pixar)：材质、渲染和合成支持多种风格；风格化并不是写实流程的低质量降级。

研究产物为 [asset-standards.md](asset-standards.md) 和 [art-direction.md](art-direction.md)。平台档位、任务规格、美术表格和两阶段应用方式为本工具的归纳建议；具体数值必须有项目依据或标为估算，不能给它们加上官方统一标准的名义。
