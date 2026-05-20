# 作者其他应用

微光字典等应用的“作者其他应用”页面数据源仓库，同时托管 App Store 所需的公开隐私页面。

## API 地址

```text
https://raw.githubusercontent.com/tanxxjun321/author-apps/main/apps.json
```

## GitHub Pages

配置 GitHub Pages 后，可使用以下页面：

### 微光字典

- 隐私政策：`https://tanxxjun321.github.io/author-apps/privacy`
- 用户隐私选择：`https://tanxxjun321.github.io/author-apps/privacy-choices`

### 成语词典

- 隐私政策：`https://tanxxjun321.github.io/author-apps/chengyu/privacy`

### auralign

- 隐私政策：`https://tanxxjun321.github.io/author-apps/aura/privacy`
- 用户隐私选择：`https://tanxxjun321.github.io/author-apps/aura/privacy-choices`

建议在仓库 `Settings -> Pages` 中设置：

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/docs`

## 数据格式

`apps.json` 是一个 JSON 数组，每个元素代表一个推荐应用：

| 字段 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `id` | Integer | ✅ | 唯一标识 |
| `name` | String | ✅ | 应用名称 |
| `description` | String | ✅ | 应用简介 |
| `icon_url` | String | ✅ | 应用图标 URL |
| `appstore_url` | String | ✅ | App Store 页面链接 |
| `bundle_id` | String | 可选 | Bundle Identifier，用于检测是否已安装 |
| `category` | String | 可选 | 分类：`教育`、`工具`、`参考`、`娱乐` |
| `is_free` | Boolean | 可选 | 是否免费，默认 `true` |

## 示例

```json
[
  {
    "id": 1,
    "name": "微光字典",
    "description": "简洁优雅的中英词典，支持离线查词、发音、例句",
    "icon_url": "https://example.com/icon.png",
    "appstore_url": "https://apps.apple.com/app/id6443900310",
    "bundle_id": "com.tanjun.zidian",
    "category": "参考",
    "is_free": true
  }
]
```

## 图标资源

图标文件放在 `icons/` 目录下，通过 GitHub Raw 访问：

```text
https://raw.githubusercontent.com/tanxxjun321/author-apps/main/icons/{app-name}.png
```

建议图标尺寸：120x120px，PNG 格式。
