# 里々サンプルゴースト ポストと狛犬

- original author : 櫛ヶ浜やぎ（Yagi Kushigahama。里々の作者。サンプルスクリプトとシェルの著作権は放棄されています）
- modernized by : ponapalt and contributors

「ポストと狛犬」は、SHIORI「里々（SATORI）」の作者・櫛ヶ浜やぎ氏が、里々の書き方を見せるために作ったサンプルゴーストです。この版は、いまの環境（UTF-8 の辞書、Unicode 版の `satori.dll`、SSP）で動くように直したものです。里々の辞書を書く練習台にも、自分のゴーストの土台にもなります。

原作の説明（元の readme）は [readme.txt](readme.txt) にあります。

# 改造のしかた

ポストと狛犬は、SHIORI「里々」で自分のゴーストを作るための土台（サンプル）です。辞書を編集して、自分のゴーストを作ってください。

## 手で編集する

- 辞書の本体は `ghost/master/` にある `dic*.txt`（`dic01_Base.txt` から `dic09_Timer.txt`）です。文字コードは UTF-8（BOM なし）です。里々は、`dic` で始まり `.txt` で終わるファイルをすべて読み込むので、`dic10_*.txt` のようにファイルを足すだけで増やせます。
- どのファイルに何が書いてあるか（ランダムトーク、起動・終了、マウスへの反応、メニューなど）、キャラクターと使えるサーフェス番号、トークの書き方の決まりは、[GHOST.md](GHOST.md) にまとめてあります。
- 詳しい仕様は、次を見てください。
  - 里々の文法、イベント、関数: 里々の仕様書 satori-docs（https://ukatech.shillest.net/satori-docs/ ）
  - さくらスクリプト、SHIORI イベント、設定ファイル: UKADOC（https://ssp.shillest.net/ukadoc/manual/ ）
  - 里々のリリースとソース: https://github.com/ukatech/satoriya-shiori
- 辞書の文法にエラーがあっても、里々は起動します（その文が動かなかったり、読み込まれなかったりします）。
- シェル（`shell/master/`）は、辞書と同じく櫛ヶ浜やぎ氏が著作権を放棄したものです。自由に改変・再配布できます。
- 自分のゴーストとして配布するときに変えるところ（名前、作者、インストール先、ネットワーク更新の URL など）は、[GHOST.md](GHOST.md) の「テンプレートから独立させるときの追加項目」にチェックリストがあります。

## AI エージェントで開発する

AI コーディングエージェント（Claude Code、Codex など）で開発するときは、スキル [ukagaka-developer](https://github.com/ukatech/ukagaka-developer) が使えます。このゴーストの SHIORI（里々）に合わせて、辞書の書き方、エラーのチェック、SSP での動作確認、シェル画像の編集、nar の作成、SHIORI の更新を手伝ってくれます。スキルは、このフォルダの外に入ります。

Claude Code の場合は、このフォルダで次を実行して、Claude Code を開き直します。

```
claude plugin marketplace add ukatech/ukagaka-developer
claude plugin install ukagaka-developer --scope project
```

Codex など、ほかのエージェントでの入れ方と、使い方は、[ukagaka-developer の README](https://github.com/ukatech/ukagaka-developer#readme) にあります。入れたら、「セットアップして」と頼んでください。ゴーストに固有の情報は、リポジトリの [GHOST.md](GHOST.md) にまとめてあります。

# ライセンス

- サンプルスクリプト（辞書 `dic*.txt`、`satori_conf.txt`、`replace*.txt`）とシェル: 櫛ヶ浜やぎ氏が著作権を放棄しています（[readme.txt](readme.txt)）。ご自由にお使いください。
- `ghost/master/satori.dll`、`satorite.exe`: 里々の配布物です。`ghost/master/satori_license.txt` の条件（再配布・改変は自由、ただしライセンス文書を同梱すること、ライセンスを変えないこと、無保証）に従います。辞書、設定ファイル、SAORI、画像などは、このライセンスの対象外です。

詳しいライセンスの整理は、[GHOST.md](GHOST.md) の「ライセンス」にあります。