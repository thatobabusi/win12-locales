# win12-locales
Win 12 的本地化翻译文件

# win12-locales

这是 [win12](https://github.com/tjy-gitnub/win12) 项目的本地化翻译文件仓库。

本项目使用 [Crowdin](https://crowdin.com/project/win12) 进行翻译托管与协作。

## 文件说明

- 格式：Java `.properties`（`key=value`）
- 源语言：简体中文（`zh-CN`）
- 目标语言：
  - 英文（`en`）→ `lang_en.properties`
  - 繁体中文（`zh-TW`）→ `lang_zh_TW.properties`
- 源文件：`lang/lang_zh_CN.properties`

> 注意：`.properties` 文件中的 `value` 可能包含 HTML 标签（如 `<p class="tit">`），翻译时请务必保留这些标签，以确保界面正常渲染。

## 同步机制

本仓库通过 GitHub Actions 每天（UTC 0:00）自动与 Crowdin 同步：

- 上传源文件（`lang_zh_CN.properties`）到 Crowdin
- 下载最新翻译并直接提交回本仓库

详见 [`.github/workflows/crowdin-sync.yml`](.github/workflows/crowdin-sync.yml)。

## 在主项目中使用

win12 主项目通过 Git submodule 引用本仓库：

```bash
git submodule add https://github.com/tangyuan0821/win12-locales.git lang
```

## 初始翻译导入

仓库中已有的 `lang_en.properties` 和 `lang_zh_TW.properties` 仅作为初始参考，后续需要手动导入 Crowdin 项目作为初始翻译（不在本仓库自动化流程范围内）。
