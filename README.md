# project-tidy

轻量的 Codex skill：整理项目中的过程文件和历史版本，建立可按需检索、可恢复的归档。

**简体中文** · [English](README.en.md)

## 功能

- 按交付物区分版本和并行方案；定稿后保留最终版，迭代中默认保留最近三个版本组。
- 尊重项目已有的权威文档、活动依赖和归档规则；无法确定的文件保留原位。
- 将用户查看的成果目录尽量控制在三级，工程依赖和归档内部保留必要结构。
- 先建立包含原路径、归档路径、关键词及简注的索引，再移动文件；默认不删除或覆盖。
- 需要历史时先查索引，再逐步搜索相关档案，并回到原文核对适用范围。

这是给 AI 的工作指令，不是后台服务或自动清理程序。实际整理和检索效果取决于所用模型、工具和项目材料；安装本 skill 不会自动扫描文件。

## 安装

将本仓库克隆到 Codex 的 skills 目录。macOS / Linux：

```bash
git clone https://github.com/redmaplewww/project-tidy.git ~/.codex/skills/project-tidy
```

Windows PowerShell：

```powershell
git clone https://github.com/redmaplewww/project-tidy.git "$env:USERPROFILE\.codex\skills\project-tidy"
```

如果使用了自定义 `CODEX_HOME`，请将仓库放在该目录下的 `skills/project-tidy`。若目标目录已有同名 skill，请先处理冲突，避免覆盖。

## 使用

在项目对话中请求：

```text
使用 $project-tidy 整理当前项目。请先检查引用关系，归档必须可恢复。
```

也可以请求先预览整理方案、查找历史材料，或恢复指定档案。skill 会按需读取 [检索参考](references/retrieval.md)；归档内容不会因为有索引就自动成为当前有效结论。

## 限制

- 无法保证任意自然语言问题都能召回全部相关文件；检索应核对原文并说明未覆盖的格式或范围。
- 归档不是独立备份；保存项目时应另行考虑备份。
- 用户要求严格可逆时，指令要求记录原路径并逐文件核对哈希；实际结果应在每次整理后验证。

## 许可证

[MIT](LICENSE)
