# win12-locales

[![Crowdin Sync](https://github.com/win12-online/win12-locales/workflows/Crowdin%20Sync/badge.svg)](https://github.com/win12-online/win12-locales/actions/workflows/crowdin-sync.yml)
[![Crowdin](https://badges.crowdin.net/win12/localized.svg)](https://crowdin.com/project/win12)

这是 [win12](https://github.com/win12-online/win12) 项目的本地化翻译文件仓库。

所有翻译在 [Crowdin](https://crowdin.com/project/win12) 上进行协作。

## 翻译进度

| 语言 | 同步状态 | 翻译进度 |
|------|----------|----------|
| 英文（`en`） | [![Crowdin Sync](https://github.com/win12-online/win12-locales/workflows/Crowdin%20Sync/badge.svg)](https://github.com/win12-online/win12-locales/actions/workflows/crowdin-sync.yml) | [![Crowdin](https://badges.crowdin.net/win12/language/en.svg)](https://crowdin.com/project/win12) |
| 繁体中文（`zh-TW`） | [![Crowdin Sync](https://github.com/win12-online/win12-locales/workflows/Crowdin%20Sync/badge.svg)](https://github.com/win12-online/win12-locales/actions/workflows/crowdin-sync.yml) | [![Crowdin](https://badges.crowdin.net/win12/language/zh-TW.svg)](https://crowdin.com/project/win12) |

## 文件说明

- 格式：Java `.properties`（`key=value`）
- 源语言：简体中文（`zh-CN`）
- 目标语言：
  - 英文（`en`）→ `lang/lang_en.properties`
  - 繁体中文（`zh-TW`）→ `lang/lang_zh_TW.properties`
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
git submodule add https://github.com/win12-online/win12-locales.git lang
```

## 参与翻译

1. 访问 [Crowdin 项目页面](https://crowdin.com/project/win12) 加入翻译。
2. 开始翻译前，请先阅读 [`lang/readme.md`](lang/readme.md) 中的翻译贡献指南。

## 许可

本仓库的翻译文件遵循原 win12 项目的许可协议。具体内容请参阅 [`LICENSE`](LICENSE)。
