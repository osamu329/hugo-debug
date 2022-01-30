# hugo-debug
Hugo Theme providing template information for debugging

## 既知の問題

HugoのTemplate Lookupルール上、プロジェクト側の layouts に優先して解決される
テンプレートファイルがあるとそちらを適用して表示してしまう。

この場合は、対象のページまたはセクションの`_index.html` のfront matterで以下のように設定してください。

```
---
title: ....
type: hugo-debug
---

```




