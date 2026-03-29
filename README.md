# OpenCode 修复版

## Overview

独立维护的 OpenCode 修复版本，针对使用中中发现的部分 bug 做修复，随缘维护。

由于官方仓库待处理 PR 过多（当前 1.8k 个），不考虑给官方仓库提交 PR。

## Contribute

### 提交修复

以 PR 的形式提交，合并到当前分支（`lilac-fix`)

### 同步官方 dev 分支

**step 1: 从官方拉最新代码**

```bash
git fetch upstream
git checkout dev
git merge upstream/dev --ff-only
```

其中 `upstream` 是 `git@github.com:anomalyco/opencode.git`。

**step 2: 把 lilac-fix rebase 到最新 dev**

```bash
git checkout lilac-fix
git rebase dev
```

**step 3: 推送更新**

```bash
git push origin lilac-fix --force-with-lease
```

## Change Logs & Todos

- [x] 修复 `opencode.json` 中的 `provider.<provider_id>.models.<model_id>.limit.input` 配置不被正确合并的问题
