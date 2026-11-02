# 抖音卖房口播 Skill

从真实房源细节出发，创作有观点、自然顺口、能直接念的中文卖房口播。

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Skill: douyin-house-tour](https://img.shields.io/badge/Skill-douyin--house--tour-blue.svg)](douyin-house-tour/SKILL.md)

**`douyin-house-tour`** 重点服务 50 至 200 平方米家庭住宅，也适用于豪宅、四合院、毛坯、老房、地下或半地下空间，以及单独的家具、设备和室内物件。创意来自这套房的事实组合，不靠通用狠话替换面积和小区名。

## 能做什么

| 任务 | 常见交付 |
| --- | --- |
| 完整卖房口播、看房解说 | 一版连贯、可直接朗读的正文 |
| 已有文案改写 | 保留事实，调整开场、语气、结构和表达 |
| 同一房源多版本 | 改变主要出售理由、叙述视角或情绪推进 |
| 开场、收尾、营销金句 | 按指定部分交付，不强行扩成整稿 |
| 家具、柜体或局部空间介绍 | 围绕已知细节和可见动作写短片段 |
| 照片、视频或博主参考辅助创作 | 在宿主能够读取的范围内提炼事实和表达方法 |

默认约 60 秒、220 至 280 个汉字；也可指定 15 秒、30 秒或其他长度。朗读速度和镜头演示会影响实际时长。

## 快速安装

### 在 Codex 中安装

在 Codex 对话中发送：

```text
使用 $skill-installer，从下面的 GitHub 路径安装技能：
https://github.com/zhaopengbo-0702/douyin-house-tour/tree/main/douyin-house-tour
```

安装后在新一轮对话中调用 `$douyin-house-tour`。如果技能没有出现，重启 Codex 后再试。

### 手动安装

1. [下载仓库 ZIP](https://github.com/zhaopengbo-0702/douyin-house-tour/archive/refs/heads/main.zip)，或用 Git 克隆本仓库。
2. 找到里面**直接包含 `SKILL.md` 的 `douyin-house-tour` 文件夹**，完整复制该文件夹，保留 `agents/` 和 `references/`。
3. 按使用范围选择下面的位置。

| 使用范围 | 放置位置 |
| --- | --- |
| 当前用户的 Codex | `~/.agents/skills/douyin-house-tour/` |
| 当前项目的 Codex | `<项目根目录>/.agents/skills/douyin-house-tour/` |

Windows 中 `~` 表示用户目录，例如 `%USERPROFILE%`。复制后应能找到 `~/.agents/skills/douyin-house-tour/SKILL.md`，不要多套一层仓库目录。已有同名技能时先检查原内容，再决定如何更新。

安装位置与发现机制参考 [Codex 官方技能文档](https://developers.openai.com/codex/skills/)。其他支持文件式技能的 AI 工具，可按其自身规范安装；本仓库提供 Codex 的 `agents/openai.yaml` 元数据。

## 第一次使用

下面是**虚构练习房源**。复制到已安装技能的 Codex 对话中即可尝试：

```text
使用 $douyin-house-tour，写一版约 60 秒的抖音卖房口播。

房源：建筑面积 118 平方米，三室两厅。
玄关：换鞋凳、到顶鞋柜、挂衣位。
厨房：有门，U 形台面；水槽在左侧、切菜台在中间、灶具在右侧。
餐桌：在厨房门外。
主卧：有一排衣柜。
受众：家庭买家。
语气：活泼、有力度，别写成配置清单。
交付：只要可以直接念的正文。

价格、朝向、操作区尺寸和家具交付条件均未提供，不要补造。
```

默认直接给口播正文；标题、分镜、拍摄提示和多版本需要时再提出。完整成稿及其事实说明见 [现有案例](douyin-house-tour/references/examples.md#118平方米完整约60秒把每天的琐碎接住)。

更多可直接使用的提示词见 [使用指南](docs/usage.md)，包括改稿、多版本、短开场、家具特写、图片视频和参考链接。

## 提供哪些信息

不用填写完整表格。提供手头确定的信息，再说明想要的结果即可。

- **房源事实**：面积及口径、户型、楼层、电梯、装修、空间连接、已确认的配置和交易条件。
- **值得展示的细节**：照片、视频、一个动作、一个家具或一处布局关系。
- **创作要求**：受众、时长、主播语气、要整稿还是片段、是否要多个版本。
- **已有内容**：原稿、需要保留或避免的句子、希望借鉴的作品链接或文字。

资料缺一部分时，技能会围绕已知内容写作，省略未知信息。完全没有房源资料却要求一篇具体整稿时，会先询问基本情况。

## 表达与事实边界

可以有态度、幽默和生活想象，但不把想象写成房源事实。

- 不凭空补造价格优势、降价、抢购、成交、学位、升值回报、品牌材质或赠送条件。
- 不隐去已知缺点；共用院落不写成独占，毛坯不承诺任意拆改。
- 地下或半地下空间按已知用途介绍，不凭有窗就保证干燥、通风或适合居住。
- 照片与视频只支持明确可见的信息，不能证明未知产权、隔音、通勤或其他性能。
- 借鉴参考作品的信息组织和表达方法，不搬用别人的房源条件、人物经历或整段文案。

案例文件中的房源均为虚构练习。抖音观察记录是带访问日期的研究资料，不是实时榜单或当前在售房源信息。

## 依赖与能力

技能本体是 5 个 Markdown/YAML 文件，无需额外安装 Python、Node.js 包，不包含独立脚本，也不要求填写 API 密钥。实际写作由支持技能的 AI 宿主完成，宿主自身的账户、费用和可用能力由该服务决定。

图片、视频、网页链接能否读取取决于宿主环境。仓库不提供视频生成、剪辑、房源检索或自动发布功能；普通写稿不会自行搜索或要求登录抖音。

## 仓库结构

```text
.
|-- README.md
|-- LICENSE
|-- CHANGELOG.md
|-- CONTRIBUTING.md
|-- docs/
|   `-- usage.md
`-- douyin-house-tour/
    |-- SKILL.md
    |-- agents/
    |   `-- openai.yaml
    `-- references/
        |-- creative-engine.md
        |-- douyin-observations.md
        `-- examples.md
```

| 文件 | 内容 |
| --- | --- |
| [SKILL.md](douyin-house-tour/SKILL.md) | 技能入口、创作流程、交付方式与事实边界 |
| [creative-engine.md](douyin-house-tour/references/creative-engine.md) | 从房源事实形成创意、主张和叙事的方法 |
| [examples.md](douyin-house-tour/references/examples.md) | 不同房型与单物件的虚构输入、成稿和说明 |
| [douyin-observations.md](douyin-house-tour/references/douyin-observations.md) | 有日期的公开参考来源及可迁移方法 |
| [openai.yaml](douyin-house-tour/agents/openai.yaml) | Codex 中的展示名称、简介和默认提示词 |

## 反馈与贡献

遇到安装问题、事实补造或文案同质化，可 [提交 Issue](https://github.com/zhaopengbo-0702/douyin-house-tour/issues/new/choose)。请附上脱敏或虚构输入、实际输出和期望结果。修改建议与案例贡献方式见 [贡献指南](CONTRIBUTING.md)，更新记录见 [CHANGELOG.md](CHANGELOG.md)。

## 许可证

本仓库采用 [MIT License](LICENSE)。外部链接所指向的文章、视频及第三方内容，其权利归原权利人所有。
