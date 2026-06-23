# RoguelikeGame-Content

[RoguelikeGame](https://github.com/While941/RoguelikeGame) 的**资产内容仓库**。

本仓库以 **Git 子模块**挂载于主项目的 `godot/assets/` 路径下——这样 Godot 的 `res://assets/...` 引用零改动，游戏照常运行。仓库根目录即对应主项目的 `res://assets/`。

## 内容
- `sprites/`、`Tilesets/`、`Effects/`、`frames/`、`palette/` 等游戏运行时资产
- PNG / `.res` 等二进制由 **Git LFS** 管理（见 `.gitattributes`）；`.import` 等文本随资产一起版本化

## 使用
本仓库不单独使用，请通过主项目拉取：

```bash
# 首次克隆主项目（连同本子模块）
git clone --recurse-submodules https://github.com/While941/RoguelikeGame.git

# 已克隆主项目，补拉子模块
git submodule update --init godot/assets
```

> 需预先安装 **git-lfs**，否则拉到的是 LFS 指针文件而非真实资产。

## 说明
- **私有仓库**：当前含部分外部测试素材（DNF），不对外公开。
- 改资产流程：在本仓库提交并推送 → 回主项目 `godot/assets/` 更新 gitlink 提交。
