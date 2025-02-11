---
uid: 2023080322244030
title: Obsidian 插件：【Readme】Periodic Notes
tags: ['日志类', 'obsidian插件', 'readme']
description: 创建/管理您的日常、每周和每月笔记
author: AI
type: readme
draft: false
editable: false
modified: 20230101000000
---

# Obsidian 插件：Periodic Notes

> [!Note] 插件名片
> - 插件名称：Periodic Notes
> - 插件作者：Liam Cain
> - 插件说明：创建/管理您的日常、每周和每月笔记
> - 插件分类：[' 日志类 ', 'obsidian 插件 ', 'readme']
> - 项目地址：[点我访问](https://github.com/liamcain/obsidian-periodic-notes)
> - 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?periodic-notes)

## 概述

创建/管理您的日常、每周和每月笔记

![Periodic Notes](https://cdn.pkmer.cn/covers/periodic-notes.gif!pkmer)

> [!tip] 原文出处
>
>下面自述文件的来源于 [Readme](https://ghproxy.net/https://raw.githubusercontent.com/liamcain/obsidian-periodic-notes/main/README.md)
>

---

## Readme(翻译）

下面是 [[periodic-notes]] 插件的自述翻译

# 周期性笔记

在 Obsidian 中创建和管理所有基于时间的笔记。

---

**注意：**此自述文件已经预先更新，以应对 v1.0 的发布。当前稳定版本 0.0.17 中并非所有描述的功能都可用。

---

此插件允许您：

- 为任何时间周期（每天、每周、每月等）创建笔记
- 使用日期切换器（需要 [NL Dates插件](https://github.com/argenos/nldates-obsidian)）以自然语言跳转到任何基于时间的笔记
- 使用时间线复杂化功能轻松定位在“202204101611 Zettelkasten 前缀笔记”的海洋中。

## 特点

### 📆 日历集合

**日历集合**描述了一组周期性的笔记。现在，您不再需要只有一个每日笔记；相反，您可以为生活的每个支柱都有一个笔记。在个人和工作之间有一个清晰的界限。跟踪一个项目。跟踪客户工作。组织学校作业。日历集合为您提供了更严格的生活方式的 _ 灵活性 _。

[设置您的第一个日历集合 →](#setting-up-your-first-calendar-set)

### ⚡️ 日期切换器

涉及周期性笔记和 Zettelkasten 风格笔记的工作流程中，最大的痛点之一是**笔记回忆**和**导航**。日期切换器试图解决这两个问题。使用自然语言快速查找周期性笔记和其他与日期相关的笔记。

想要找上周的会议笔记？只需搜索：`上周 ⇥ 会议`。

[使用方法 →](#使用日期切换器)

### ⌚️ 时间线复杂化

日期切换器会让你在笔记之间快速切换，可能会让你有点迷失。但不要担心！现在，在你的周期性笔记的右上方有一个时间线“复杂化”，以自然语言的方式准确地显示你所在的位置。

[使用方法 →](#using-the-timeline-complication)

使用方法

### 设置您的第一个日历集

在“周期性笔记”设置中，您将从一个“默认”日历集开始。单击它以打开日历集详细信息视图。

从这里，您可以选择要启用的**笔记类型**。为了开始，您可能想启用：**每日**，**每周**，**每月**和**每年**。

每种笔记类型都具有相同的配置选项：

- **格式：**用作新周期性笔记文件名的日期格式。这个值不仅用于生成文件名，插件在索引您的存储库时也使用这个格式来查找周期性笔记。
- **基本文件夹：**用于保存此日历集中所有周期性笔记的文件夹。例如，对于个人日记笔记，您可以选择选择一个 `Journal/` 文件夹。
- **模板位置：**您的笔记模板的路径。有关更多信息，请查看 [模板标签](#template-tags) 部分。

理解日历集

每个日历集都有完全独立的配置。最常见的用例是创建两个集合：“个人”和“工作”。这样，您可以将工作的日志保留在自己独立的文件夹中，而不会被个人信息污染。

当您拥有多个日历集时，一个集合被设置为**活动日历集**。所有涉及创建或查看特定周期性笔记的命令只会查看当前活动日历集中的笔记。您可以在设置中切换活动集，或使用命令“切换活动日历集...”。

使用命令“Periodic Notes: Show date switcher...”来访问日期切换器。打开后，日期切换器将显示一系列快速日期条目。

在每个条目上，它会显示活动日历集是否有相应的笔记，该笔记的路径，以及该时间段相关笔记的数量。选择一个条目将打开现有的笔记，如果不存在，则创建一个新的笔记。您可以通过点击或使用<kbd>Enter</kbd>来选择一个笔记。在选择一个条目时按住<kbd>ctrl</kbd>键将在新窗格中打开该笔记。

##### 相关笔记

按下 <kbd>Tab</kbd> 键将打开与所选条目相关的笔记视图。这将显示与该时间段对应的所有非精确匹配。在“今天”条目中，它将显示所有文件名中包含今天日期的笔记。对于“本月”条目，它将显示所有以 `YYYY-MM` 为前缀的笔记。

##### 扩展搜索

从相关笔记视图中，您可以按下 `*` 键来扩展搜索。扩展搜索意味着列表将包括该时期内的所有条目。因此，“本月”条目将包括该月份的所有周记和日记。

当您寻找特定的 Zettlekasten 笔记，并且记得它是上周的，但可能不记得具体的日期时，这一功能尤为强大。

使用时间线复杂化

复杂化将显示打开笔记的相对日期。

| 笔记                            | 外观                                                                                                                              |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `2022-04-14.md`                 | <img width="104" alt="image" src="https://user-images.githubusercontent.com/693981/163503952-a8619a42-a91a-43ea-af49-eb77744c5048.png"> |
| `202204141213 Meeting Notes.md` | <img width="100" alt="image" src="https://user-images.githubusercontent.com/693981/163503975-7a8f9798-5644-4d3d-8eeb-49c2e07d0884.png"> |

#### 每周日历

点击时间线复杂化将切换到每周内联日历。

配置

### 分类日期

Periodic Notes 在指定的文件夹中搜索并索引所有类型的与时间相关的文件。

- 符合设置中指定的日期格式的文件名完全匹配的笔记。因此，如果格式是 `YYYY-MM-DD`，它将找到并索引 `2022-04-10.md`。
- 文件名中包含日期的笔记。这包括以 Zettelkasten 前缀命名的笔记（例如 `202204101611 Meeting Notes.md`），但也包括像 `Budget cuts made in 2021.md` 这样的文件。
- 笔记 [根据 frontmatter 标识为周期性笔记](#parsing-frontmatter)

使用 frontmatter 来标识笔记可以让您以任何您想要的方式命名笔记，这意味着您不再受 Moment.js 可解析的固定格式的限制。

当打开特定日期的笔记时，算法始终寻找精确匹配，并且它优先选择 frontmatter 匹配而不是文件名匹配。

#### 解析文件名

Periodic Notes 将查看您配置的**文件夹**中嵌套的所有文件。

所以您可以有：

```
- daily_notes/
  # 所有笔记都在一个文件夹中
  - 2022-04-01.md

  # 或者嵌套在不同的文件夹中
  - 2020/
    - 03/
      - 2022-03-01.md
    - 04/
      - 2022-04-02.md
```

Periodic Notes 还会索引包含类似日期模式的任何文件名。这意味着它将捕获：

- 202204101611 会议记录
- 2021.02.04 锻炼日志
- 2001 太空漫游
- 1995 年最佳视频游戏

#### 解析前置元数据

您还可以使用前置元数据将笔记分类为周期性笔记。它将检查所有文件的前置元数据，查找具有以下键及其相应值的文件：

| 前置元数据键 | 格式         |
| --------------- | ------------ |
| day             | `YYYY-MM-DD` |
| week            | `GGGG-[W]WW` |
| month           | `YYYY-MM`    |
| quarter          | `YYYY-[Q]Q`  |
| year            | `YYYY`       |

例如：

```
---
day: 2022-01-12
---
```

具有这些前置元数据键的笔记将被分类为**完全匹配**。这意味着打开周期性笔记的命令将打开具有相应前置元数据的笔记。

#### 调和多个**精确匹配**

对于那些期望单个**精确匹配**的命令，比如“打开今天的日记”，插件会优先选择与“frontmatter”匹配的笔记，而不是与文件名匹配的笔记。

### 模板标签

| 标签                                                                                    | 支持的笔记类型 | 描述                                                                                                  | 接受日期计算 |
| -------------------------------------------------------------------------------------- | -------------- | ----------------------------------------------------------------------------------------------------- | ------------ |
| `title`                                                                                | 所有类型       | 插入笔记的标题                                                                                        | ❌           |
| `date`, `time`                                                                         | 所有类型       | 插入当前日期/时间。可选择接受格式。例如 `{{date:YYYY-MM-DD}}`                                       | ✅           |
| `yesterday`, `tomorrow`                                                                | 每日           | 插入对应的日期。可选择接受格式。例如 `{{tomorrow:YYYY-MM-DD}}`                                      | ✅           |
| `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`, `sunday` | 每周           | 引用一周中的特定日期 `{{sunday:gggg-MM-DD}}`。注意，**必须**指定日期格式！                           | ✅           |
| `month`                                                                                | 每月           | 引用月份的第一天。可选择接受格式。例如 `{{month:YYYY-MM}}`                                           | ✅           |
| `quarter`                                                                              | 每季度         | 引用季度的第一天。可选择接受格式。例如 `{{quarter:YYYY-[Q]Q}}`                                      | ✅           |
| `year`                                                                                 | 每年           | 引用年份的第一天。可选择接受格式。例如 `{{year:YYYY}}`                                               | ✅           |

#### 日期计算

周期性笔记在模板中提供了非常基本的日期计算功能。如果您想要在周期性模板中链接到不同的日期，这将非常有用。

日期计算的语法最好通过示例来理解。以下是如何在模板中插入**5 天后**的示例：

```
{{date+5d:YYYY-MM-DD}}
```

您可以添加或减去任意数量的天数（`d`）、周数（`w`）、月数（`m`）或年数（`y`）。

此功能适用于简单的用例，例如链接连续的每日笔记。如果您在模板中需要更复杂的内容，我强烈建议与周期性笔记一起使用 [Templater](https://github.com/SilentVoid13/Templater) 插件。

## 命令

<img width="723" alt="image" src="https://user-images.githubusercontent.com/693981/163568986-a30bfb3e-3a64-49fe-bdf1-d46ace8c2649.png">

| 命令名称                      | 描述                                                                                                 |
| ----------------------------- | ------------------------------------------------------------------------------------------------------ |
| 打开日期切换器                | 打开 [日期切换器](#️-date-switcher)。需要安装“自然语言日期”插件。                                          |
| 切换活动日历集...             | 从日历集列表中选择一个作为“活动”日历集。                                                               |
| 打开今天的日记                | 打开或创建当前活动日历集的日记。                                                                       |
| 打开本周的笔记                | 打开或创建当前活动日历集的周记。                                                                       |
| 打开本月的笔记                | 打开或创建当前活动日历集的月记。                                                                       |
| 打开本季度的笔记              | 打开或创建当前活动日历集的季度记。                                                                     |
| 打开今年的笔记                | 打开或创建当前活动日历集的年记。                                                                       |

## 相关插件

- [自然语言日期插件](https://github.com/argenos/nldates-obsidian) 由 [Argentina Ortega Sáinz](https://github.com/argenos) 开发
- [日历插件](https://github.com/liamcain/obsidian-calendar-plugin)

常见问题解答

这个和每日笔记插件有什么区别？

每日笔记插件是内置在 Obsidian _core_ 中的。这意味着您可以在不禁用 [安全模式](https://help.obsidian.md/Advanced+topics/Community+plugins) 的情况下使用它。它也非常简单：它可以打开或创建今天的每日笔记。另一方面，周期性笔记力求增加与其他插件的互操作性。即使您只对每日笔记感兴趣，周期性笔记也有很多可提供的功能。它可以创建未来或历史的每日笔记，提供更优秀的导航，并允许每天创建多个每日笔记。

如何使周数与 Google 日历、Outlook 和 Fantastical 中的周数匹配？

这些程序符合**ISO-8601**周编号规范。要遵循此标准，请确保在指定的格式中使用 `GGGG` 和 `WW` 标记。

<img width="864" alt="image" src="https://user-images.githubusercontent.com/693981/163471298-5c63da1b-7cba-4c94-b0e9-c54818703889.png">

如何在 Templater 中使用这个功能？

要在您的 Periodic Notes 模板中使用 Templater，请确保在 Templater 中启用以下设置：

我希望在我的周期笔记文件夹的子文件夹中创建新的笔记。我该怎么做？

如果你想要新的每日笔记显示在文件夹 `Journal/2022/` 中，你可以在 "Format" 字段中包含子文件夹。例如：

<img width="868" alt="image" src="https://user-images.githubusercontent.com/693981/163474542-f20c469d-95a1-4e7f-afbb-6f858a9aff32.png">

**重要提示：**请注意，插件将查看您提供的**文件夹**中的所有文件。因此，即使您希望将您的日志分段到子文件夹中，**文件夹**应该仅指基本文件夹。

```
journal
  ├── 2021
  │   ├── 2021-12-30.md
  │   └── 2021-12-31.md
  └── 2022
      ├── 2022-04-01.md
      └── 2022-04-02.md
```

对于这个配置，**文件夹**应该是 `journal/`，**格式**应该是 `YYYY/YYYY-MM-DD`。

## 🎞 鸣谢

感谢所有帮助测试新功能并报告错误的人。特别感谢 Argentina Ortega Sáinz 为日期切换器提供动力的 [自然语言日期插件](https://github.com/argenos/nldates-obsidian)。

## 表达感谢 🙏

如果你喜欢这个插件并想请我喝杯咖啡，你可以！

[<img src="https://cdn.buymeacoffee.com/buttons/v2/default-violet.png" alt="BuyMeACoffee" width="100">](https://www.buymeacoffee.com/liamcain)

喜欢我的工作并想看到更多类似的内容？你可以赞助我。

[![GitHub Sponsors](https://img.shields.io/github/sponsors/liamcain?style=social)](https://github.com/sponsors/liamcain)
