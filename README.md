# workbuddy-git-test

## 项目用途

这是一个用于验证 **WorkBuddy 与本地 Git / GitHub 仓库集成** 的测试仓库。

当前仓库仅包含一个 Python 测试脚本 `hello_git.py`。运行该脚本会向标准输出打印两行测试信息，用于确认文件创建、Git 提交与远程推送流程可用。

目前该项目没有构建步骤、第三方依赖、自动化测试框架或 Web 服务，仅完成上述最小验证功能。

## 目录结构

```text
workbuddy-git-test/
├── .git/           # Git 元数据目录（隐藏），保存版本历史与远程配置
├── README.md       # 本说明文件（当前新建，尚未提交）
└── hello_git.py    # Python 测试脚本
```

已跟踪文件：

- `hello_git.py`

## 运行方法

环境要求：Python 3（当前环境已验证为 Python 3.13.14）。

在仓库根目录执行：

```bash
python hello_git.py
```

预期输出：

```text
Hello GitHub!
WorkBuddy Git integration test successful.
```

## Git 管理流程

- 仓库根目录即 Git 工作树，`.git` 目录用于保存版本历史、分支与远程配置。
- 当前分支为 `main`，远程仓库为 `origin`，并已设置跟踪关系 `main...origin/main`。
- 远程地址：

  ```text
  https://github.com/walkeralex3288-cloud/workbuddy-git-test.git
  ```

常用只读检查命令：

```bash
git status --short
git branch --show-current
git log -1 --oneline
git remote -v
```

如需提交新变更，可按以下流程操作：

```bash
git status --short
git add -- <文件名>
git diff --cached
git commit -m "<提交说明>"
git push -u origin main
```

说明：本次仅创建 `README.md`，暂未执行 `git add`、`git commit` 或 `git push`。
