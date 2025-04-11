# Scoop 存储桶模板

[![Tests](https://github.com/PoeraWork/Scoop/actions/workflows/ci.yml/badge.svg)](https://github.com/PoeraWork/Scoop/actions/workflows/ci.yml) [![Excavator](https://github.com/PoeraWork/Scoop/actions/workflows/excavator.yml/badge.svg)](https://github.com/PoeraWork/Scoop/actions/workflows/excavator.yml)

用于 [Scoop](https://scoop.sh) 的 Windows 命令行安装程序的模板存储桶。

## 我如何使用这个模板？

1. 使用“使用此模板”按钮生成此存储库的副本。
2. 允许所有 GitHub Actions：
   - 导航到 `Settings` - `Actions` - `General` - `Actions permissions`。
   - 选择 `Allow all actions and reusable workflows`。
   - 然后点击 `Save`。
3. 允许从 GitHub Actions 写入存储库：
   - 导航到 `Settings` - `Actions` - `General` - `Workflow  permissions`。
   - 选择 `Read and write permissions`。
   - 然后点击 `Save`。
4. 在 `README.md` 中记录存储桶。
5. 替换 `bin/auto-pr.ps1` 中的占位符存储库字符串。
6. 通过将 `bucket/app-name.json.template` 复制到 `bucket/<app-name>.json` 创建新的清单。
7. 提交并推送更改。
8. 如果希望您的存储桶在 `https://scoop.sh` 上被索引，请将主题 `scoop-bucket` 添加到您的存储库。

## 我如何安装这些清单？

在提交并推送清单后，运行以下命令：

```pwsh
scoop bucket add PoeraScoop https://github.com/PoeraWork/Scoop
scoop install PoeraScoop/<manifestname>
```

## 我如何贡献新的清单？

要进行新的清单贡献，请阅读 [贡献指南](https://github.com/ScoopInstaller/.github/blob/main/.github/CONTRIBUTING.md) 和 [应用清单](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests) 维基页面。
