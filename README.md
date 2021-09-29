# Visual Studio Codeで作るLT資料

## はじめに

VSCodeで作成するプレゼンテーション資料のサンプルコードを載せています。

## 環境

- VS Code 1.38

## VS CodeでのLT資料作成

パワーポイントを使わずに、マークダウンでLT資料を作成します。
ここでは2つのプラグインを紹介します。

### Marp for VS Code

Markdown形式のファイルをプレゼンテーション用のスライドに変換してくれます。PDFに書き出す事もできます。

#### 使ってみる

##### plugin(Marp for VS Code)をインストールする

<img width="1202" alt="スクリーンショット 2019-11-03 17.24.57.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/bd501cd4-e6e2-64fb-7ad8-a57c8ad307a6.png">

##### スライド（.md）を作成する

先頭にYAMLヘッダを記述するだけです。
細かな設定を知りたい方は、[Marp公式ページ](https://marpit.marp.app/markdown)をご覧ください。

```md
---
marp: true
header: 'header text'
footer: 'footer text'
---
<!-- $theme: gaia -->
<!-- $size: 16:9 -->
<!-- page_number: true -->
<!-- paginate: true -->
```

今回は以下のファイルを作成しました。

``` md:slide.md
---
marp: true
header: 'header text'
footer: 'footer text'
---
<!-- $theme: gaia -->
<!-- $size: 16:9 -->
<!-- page_number: true -->
<!-- paginate: true -->

# Marp for VS Code スライドサンプル

***@gonkunkun***

---

## もくじ

1. Marp for VS Codeとは
2. 使い方
3. ユースケース

---

## 1. Marp for VS Codeとは

- VS Codeの拡張機能
  マークダウンでスライドが作れる

---

## 2. 使い方

1. リスト
2. 背景画像

---

## 2.1 リスト

- One
- Two
- Three

---

## 2.2 背景画像

![bg right](https://picsum.photos/720?image=29)

---

## 3. ユースケース

- ほげほげ

```

##### プレビューを表示する

VS Code上からmdファイルを右クリックして`Open Preview`を選択
<img width="796" alt="スクリーンショット 2019-11-03 17.37.14.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/51e3d598-e020-0edd-d341-46b2a8422f23.png">

こんな感じでスライドが作成できます。
<img width="1177" alt="スクリーンショット 2019-11-03 17.37.33.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/8e8c67bb-75b8-5a55-4b4a-9c9415aa6025.png">

##### 作ったスライドをPDFで出力

青い三角のアイコンをクリックして、`Export slide deck...`を選択
<img width="583" alt="スクリーンショット 2019-11-03 17.42.54.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/834fa20e-2176-a8d7-e8c0-a787e68c7e2b.png">

### vscode-reveal

Marp for VS Codeを使用してスライドを作成することはできました。しかし、Marpでは作成したスライドをVS Code上に投影することができません。そこで、vscode-reveal（プラグイン）を使用します。
（私が知らないだけですが・・・ VS Code上に投影する良い方法知っている方がいれば、コメントで教えていただければ幸いです）

#### 使ってみる

##### plugin(vscode-reveal)をインストールする

<img width="1073" alt="スクリーンショット 2019-11-03 17.55.39.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/4c6c3249-e118-5139-19fd-935214b5d733.png">

##### スライド（.md）を作成する

先頭にYAMLヘッダに以下を追記します。ファイル自体はYAMLヘッダを変更しただけです。気になる方はGithubリポジトリのslide-reveal.mdをご確認ください。
細かな設定を知りたい方は、[こちら](https://marketplace.visualstudio.com/items?itemName=evilz.vscode-reveal)をご覧ください。

```md
---
theme: "black"
transition: "none"
---
```

##### VS Code上でプレゼンテーションを実施する

コマンドパレットを表示して、`Revealjs: Show Presentation by side`を選択します。
コマンドパレットは`Ctrl + Shift + p`で表示できます。
<img width="1080" alt="スクリーンショット 2019-11-03 18.03.54.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/e31ba9ea-d34f-8d9c-b87b-0df2f18168a6.png">

こんな感じで、VS Code上でスライドを表示できるようになります。
<img width="1361" alt="スクリーンショット 2019-11-03 18.05.22.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/653bd02c-70f1-4f59-87eb-ddbde15399cd.png">

### Presentation Mode

VS Code上でスライドを表示できるようになると、このスライドを全画面表示できるようにならないのかな…と考えます。そこで使用するのがPresentation Mode（プラグイン）です。
VS Codeをプレゼンテーション用に全画面に表示することができます。

#### 使ってみる

##### plugin(Presentation Mode)をインストールする

<img width="935" alt="スクリーンショット 2019-11-03 18.12.16.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/57f61757-5751-731a-8e51-246e02ce68f5.png">

##### プレゼンテーション用に表示してみる

先程のスライドを全画面で表示してみます。
コマンドパレットを表示して、`Presentation Mode`を選択

全画面表示になりました
<img width="1435" alt="スクリーンショット 2019-11-03 18.16.38.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/0c6cd67b-a13f-7ab5-75ea-26bc31600dcf.png">

全画面表示から戻す場合には、再度コマンドパレットを表示して、`Presentation Mode`を選択します。

##### ソースコードの共有

同じ要領で、ソースコードを全画面表示にすることで、発表中にコードを見せながら解説する際にも活用できます。
<img width="1434" alt="スクリーンショット 2019-11-03 18.23.11.png" src="https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/186355/f18cbc65-9e11-9313-1771-075dba7bdbd8.png">
