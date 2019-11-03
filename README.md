# VS CodeにPresentation Modeプラグインを入れてみた

## はじめに

雑誌の紹介ページを参考にやってみた。

## 環境

- VS Code 1.38

## 本記事で使用するVS Codeプラグイン

- Presentation Mode
- Marp for VS Code
- Auto-Open Markdwon Preview
- vscode-reveal

## セットアップ

- vscodeをインストールしていない人はここから

## 使い方

## デモ

## 終わりに

## 作業メモ

### プレゼンテーションでソースコードを表示する

- pluginインストール
  - Presentation Mode
    - VS Codeを全画面表示して、プレゼンテーション用の画面表示にできる
- ソースコードを開く
- コマンドパレット(Ctrl + Shift + p)を実行して「Presentation Mode」を選択する
  - Presentation Modeを終了する場合には、「Esc」, [もう一度Presentation Modeを選択]

### Markdownでスライドを作成する

- pluginインストール
  - Marp for VS Codeをインストール
- YAMLヘッダを先頭に記述
- Open  Previewからプレビューを表示（mdファイルを開いたときに自動でプレビュー表示するのもいいかも）
- こんな感じで記述
  - 詳しい使い方は公式ドキュメント参考（https://marpit.marp.app/markdown）
- Export slide deckでPDFファイルの出力も可能

### プレゼンテーションに動きをつける

- pluginインストール
  - vscode-revealをインストール
- コマンドパレットでreveal.jsを選択
  - https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal