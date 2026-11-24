# garlic-work

项目协作主仓库。所有开发工作在独立分支上进行，通过 PR 合并到 `main`。

## 目录

```
├── docs/       # 文档、方案
├── src/        # 源码
└── README.md
```

## 协作流程

1. 从 `main` 切分支：`git switch -c feat/简短描述`
2. 本地改动后提交：`git commit -m "feat: 做了什么"`
3. 推送到远端：`git push -u origin feat/简短描述`
4. 在 GitHub 上提交 PR，等待至少一人 review 后合并
5. 合并后删除本地分支：`git switch main && git pull && git branch -d feat/简短描述`

## 分支命名

| 前缀 | 用途 |
| --- | --- |
| `feat/` | 新功能 |
| `fix/` | 修复问题 |
| `docs/` | 文档 |
| `chore/` | 配置、依赖等杂项 |

## 提交信息

采用 `类型: 内容` 格式，类型同分支前缀，例如 `fix: 修正登录超时判断`。

## 约定

- 不直接向 `main` 推送，所有改动走 PR
- 提交前确认 `git status` 没有多余文件
- 大文件（视频、数据集）不入库，放共享盘并在 `docs/` 里记录链接
