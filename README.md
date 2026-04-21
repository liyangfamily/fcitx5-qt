# fcitx5 Qt6 输入法插件构建

使用 GitHub Actions 自动编译 `libfcitx5platforminputcontextplugin.so`，基于 Qt 6.8.2 源码构建。

## 使用方法

1. Fork 或 clone 本仓库到 GitHub
2. Push 到 `main` 分支，自动触发构建
3. 在 Actions → 对应的 workflow run → Artifacts 中下载 `libfcitx5platforminputcontextplugin-qt682`

也可以在 Actions 页面手动点击 **Run workflow** 触发。

## 构建环境

| 项目 | 版本 |
|------|------|
| 系统 | Ubuntu 24.04 |
| Qt | 6.8.2（源码编译） |
| fcitx5-qt | 5.1.7 |

## 安装插件

将下载的 `.so` 放到 Qt 插件目录：

```bash
# 查找当前 Qt6 的插件路径
qtpaths6 --plugin-dir

# 复制到 platforminputcontexts 目录（示例路径）
sudo cp libfcitx5platforminputcontextplugin.so \
    /usr/lib/x86_64-linux-gnu/qt6/plugins/platforminputcontexts/
```
