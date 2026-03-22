# 中文起名 Skill

一个面向中文场景的 Codex skill，用于宝宝名、学名、笔名、小名、昵称与中英双语名建议。

这个 skill 保留了传统中文起名里最实用的一套判断框架，同时避免把输出写成空泛玄学。默认包含：

- 五宜：好听、好讲、好写、好运、好相
- 十忌：谐音、多音、生僻、难写、错位、浅显、不雅、不吉、贬义、同质化
- 两字名特殊要求：同源性、整体性、端庄大气
- 可选的五行/八字参考
- 适用于宝宝起名、成人改名、笔名、小名、兄弟姐妹成套命名

## 安装

安装完成后，请重启 Codex 以加载新 skill。

### 方式 1：Codex 内置安装器

如果你在 Codex 里，可以直接安装这个 skill 目录：

```text
$skill-installer install https://github.com/zhangjk1207/naming-skill/tree/main/naming
```

### 方式 2：Skills CLI

如果你使用 Skills CLI，可以尝试：

```bash
npx skills add zhangjk1207/naming-skill@naming
```

如果你的环境更偏向 GitHub 路径安装，也可以直接使用上面的 GitHub URL 方式。

## 使用示例

```text
使用 $naming 为宝宝提出五个中文名字方案，并附上出处、谐音避坑和简明理由。
```

或者直接告诉它：

```text
帮孩子取名，姓张，男孩，想要《诗经》风格，避开“康”字，名字稳重一点。
```

## 仓库结构

```text
naming-skill/
├─ README.md
└─ naming/
   ├─ SKILL.md
   ├─ agents/
   │  └─ openai.yaml
   └─ references/
      └─ name-modes.md
```

## Skill 特点

- 中文优先：提示词、结构和输出逻辑都围绕中文命名场景设计
- 保留原味：保留“五宜”“十忌”等传统筛选标准，而不是只剩抽象流程
- 通用可复用：移除了私人信息，但保留了“用户专属背景”这一可选层
- 易于扩展：后续可以继续补充 `references/`、`assets/` 或 `scripts/`

## 开发说明

这个仓库目前采用单-skill 结构，目标是让安装路径尽可能简单。

如果后续需要收录更多 skill，可以改为：

```text
skills/
  naming/
  another-skill/
```

