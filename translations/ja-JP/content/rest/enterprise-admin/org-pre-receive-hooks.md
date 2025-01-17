---
title: Organization Pre-receive Hooks
intro: The Organization Pre-receive Hooks API allows you to view and modify enforcement of the pre-receive hooks that are available to an organization.
versions:
  ghes: '*'
topics:
  - API
miniTocMaxHeadingLevel: 3
allowTitleToDifferFromFilename: true
---

### オブジェクトの属性

| 名前                               | 種類        | 説明                       |
| -------------------------------- | --------- | ------------------------ |
| `name`                           | `string`  | フックの名前。                  |
| `enforcement`                    | `string`  | このリポジトリでのフックの適用状態。       |
| `allow_downstream_configuration` | `boolean` | リポジトリが適用をオーバーライドできるかどうか。 |
| `configuration_url`              | `string`  | 適用設定されているエンドポイントの URL。   |

*適用*可能な値は、`enabled`、`disabled`、`testing` です。 `disabled` は、pre-receive フックが実行されないことを示します。 `enabled` は、それが実行され、ゼロ以外の状態になるプッシュを拒否することを示します。 `testing` は、スクリプトは実行されるが、プッシュが拒否されないことを示します。

`configuration_url` may be a link to this endpoint or this hook's global configuration. サイトアドミンのみがグローバル設定にアクセスできます。
