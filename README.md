# hugo-debug

Hugo Theme providing template information for debugging

Hugo プロジェクトのルートディレクトリから、下記を実行します。

```bash
git clone https://github.com/osamu329/hugo-debug.git themes/hugo-debug
```

Hugo をサーバーモードで起動する際にコマンドラインオプションでテーマを指定します。

```bash
hugo server --theme=hugo-debug
```

## 既知の問題

HugoのTemplate Lookupルール上、プロジェクト側の layouts に優先して解決される
テンプレートファイルがあるとそちらを適用して表示してしまいます。

この場合は、対象のページまたはセクションの`_index.html` のfront matterを一時的に書き換えてください。
`type` に `hugo-debug` を設定してください。

```
---
title: ....
type: hugo-debug
---
```

もしくは、プロジェクトの `layouts` を 一時的に `layouts_` のように変更することで
テーマのテンプレートのみが適用されます。


