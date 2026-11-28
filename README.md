# わたしの簿記ノート

ふくしままさゆきさんの動画を参考にした、簿記3級の講義図解・学習マップ・復習記録です。

## サイトの階層

全ページに共通のヘッダー（学ぶ／解く／復習する／論点から探す）・パンくず・フッター（サイトマップ）があります。

- ホーム：`index.html`
- 学ぶ：`course.html`（学習マップ）→ 第0〜25回の図解講義 `lesson00.html`〜`lesson25.html`
- 解く：`practice.html` → `review18-random.html`・`pass-drill.html`・`exam-final.html`・`review24.html`
- 復習する：`review.html` → 第1〜18回の復習 `review01.html`〜`review18.html`、第24回50問の振り返り `review24.html`、
  第2〜5回のつまずきまとめ `notes02-05.html`（以前のトップページ）
- 論点から探す：`topics.html`

講義と復習のページの上には「講義｜自分の復習」の切り替え・前後の回・その回の論点へのリンクがあります。

## 公開

GitHub Pages： https://tomita-koki.github.io/boki-review/

`main` ブランチのルートから公開します。HTML/CSS/JavaScriptのみで動作し、ビルドは不要です。
`.nojekyll` によりJekyllの変換を無効にしています。
`/course/`・`/lesson13/`・`/review18/`などは対応するHTMLへ移動し、クエリ文字列とハッシュを引き継ぎます。

## 更新

講義・復習の本文は各HTML内にあります。検索・問題の絞り込み・解説の開閉はブラウザ内で動作します。
本人の回答と自己採点、照合結果は区別し、過去の学習記録は上書きせず保持します。
HTMLの更新後は、内部リンク・スマホ表示・JavaScriptの動作を確認してから反映してください。

### 共通ナビと入口のページ

共通のヘッダー・パンくず・フッターと、入口のページ4つ（`index.html`・`practice.html`・`review.html`・`topics.html`）は、
このリポジトリの外にある `tools/build_site_nav.py`（`work/簿記/tools/`）で作ります。

```
python tools/build_site_nav.py
```

- サイトの階層（回の名前・章・論点・演習の一覧）は `build_site_nav.py` の上のほうにまとめてあります。ページを足したら、そこに登録してから実行します
- 各ページの共通部分は `<!-- site-nav:… -->` の印で囲んであり、実行すると印の中だけが入れ替わります。印の中は手で直さないでください
- `assets/site-nav.css`（共通部分）と `assets/hub.css`（入口のページ）も、このスクリプトが書き出します
- `review24.html`・`pass-drill.html`・`review18-random.html` を作るスクリプトは、最後に共通部分を差し込みます

## 出典と記録

各ページに元動画などの参照先を記載しています。学習用に整理した説明であり、公式の解答・採点基準ではありません。
学習記録・誤答履歴も公開内容に含みます。検索エンジン向けの`noindex`指定は維持していますが、アクセス制限ではありません。

旧ChatGPT Sites公開済み版（version 34）を元に、既存の第24回復習ページを統合しています。
認証情報・Sitesの設定ファイル・ローカル作業用ファイルは含めません。
