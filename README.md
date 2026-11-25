# Codex 项目文档工作流

`docs` skill 帮助 Codex 从项目文档接手任务、查询接口和开发进展，并维护相关记录。Codex 可以依据任务自动选择 skill，也可以显式输入 `$docs`。自动调用取决于任务和 agent 的判断。

`$docs init` 根据现有项目补齐文档。`$docs sync` 按现状同步全部现行文档。两项操作仅在用户明确要求时执行，含义明确的自然语言请求也适用。添加“先给我看差异”可先审阅再写入。

## 安装

```bash
git clone https://github.com/LinKai2002/my-codex-skills.git ~/my-codex-skills
mkdir -p ~/.agents/skills
ln -s ~/my-codex-skills/skills/docs ~/.agents/skills/docs
```

创建链接前检查目标路径是否已存在。开启新 Codex session 后输入 `$docs` 并附上任务。

## 更新

```bash
git -C ~/my-codex-skills pull --ff-only
```

重新开启 Codex session，使用更新后的 skill。

本项目采用 MIT 许可证，详见 [LICENSE](LICENSE)。
