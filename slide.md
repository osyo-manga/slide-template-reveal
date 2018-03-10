### reveal.js のサンプルスライド

---

## これはなに
- - -

* reveal.js + markdown でスライドを書くためのテンプレート
* CDN から reveal.js などを読み込むことで最小限のファイル構成になっている
* `slide.md` を書き換えるだけでスライドがつくれる

---

## 使い方
- - -

1. [テンプレートをダウンロード]()
1. `slide.md` に markdown でスライドを書き込む
1. browser-sync 等でローカル環境で動作確認する
1. （必要であれば）gh-pages で公開する

---

## ファイル構成
- - -

```
.
├── index.html     # 本体
├── slide.md       # スライド
└── style.css      # スタイルシート
```

`slide.md` に markdown でスライドの内容を書いていく

---

## タイトルの変更
- - -

`index.html` の 6行目のタグを書き換える

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<!-- 個々を書き換える -->
<title>タイトル</title>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/reveal.js/3.5.0/css/reveal.min.css">
```

---

## markdown の書き方
- - -

* 通常の markdown と同じように記述できる  
* 詳しくはこのファイルを参考にしてください。  

---

### ページの区切り
- - -

`---` でページを区切る

```markdown
タイトル
---
1ページ目
---
2ページ目
---
...
```

---

1ページ目

---

2ページ目

---


### 下にページの区切り
- - -

`>>>` で下にスライドを追加する

```
※実際に >>> の先頭にスペースはつけない

 >>>

下ページ1

 >>>

下ページ2

 >>>
...

```

↓↓↓ サンプル ↓↓↓

>>>

下ページ1

>>>

下ページ2

---

### 見出し
- - -

# # 見出し1
## ## 見出し2
### ### 見出し3
#### #### 見出し4

---

### fragment
- - -

文章に対してエフェクトを追加できる

```markdown
フェードイン                      <!-- .element: class="fragment" -->
grow 大きくする                   <!-- .element: class="fragment grow" -->
shrink 小さくする                 <!-- .element: class="fragment shrink" -->
fade-out フェードアウト           <!-- .element: class="fragment fade-out" -->
visible only once 一度だけ表示    <!-- .element: class="fragment current-visible" -->
blue only once 一度だけ青くする   <!-- .element: class="fragment highlight-current-blue" -->
highlight-red 赤くハイライト      <!-- .element: class="fragment highlight-red" -->
highlight-green 緑にハイライト    <!-- .element: class="fragment highlight-green" -->
highlight-blue 青にハイライト     <!-- .element: class="fragment highlight-blue" -->
```

↓↓↓ サンプル ↓↓↓

>>>

### ほげほげ
- - -

* ほげほげ1                     <!-- .element: class="fragment" -->
* ほげほげ2                     <!-- .element: class="fragment" -->
* ほげほげ3                     <!-- .element: class="fragment" -->
* ほげほげ4                     <!-- .element: class="fragment" -->

>>>

* フェードイン                      <!-- .element: class="fragment" -->
* grow 大きくする                   <!-- .element: class="fragment grow" -->
* shrink 小さくする                 <!-- .element: class="fragment shrink" -->
* fade-out フェードアウト           <!-- .element: class="fragment fade-out" -->
* visible only once 一度だけ表示    <!-- .element: class="fragment current-visible" -->
* blue only once 一度だけ青くする   <!-- .element: class="fragment highlight-current-blue" -->
* highlight-red 赤くハイライト      <!-- .element: class="fragment highlight-red" -->
* highlight-green 緑にハイライト    <!-- .element: class="fragment highlight-green" -->
* highlight-blue 青にハイライト     <!-- .element: class="fragment highlight-blue" -->

---

### コード行のハイライト
- - -

```html
1行をハイライト

複数の箇所をハイライト

複数行をハイライト
複数行をハイライト
複数行をハイライト

複数の箇所をハイライト
```

```html
<span class="code-presenting-annotation fragment current-only" data-code-focus="1"></span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="3,9"></span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="5-7"></span>
```

↓↓↓ サンプル ↓↓↓

>>>

```html
1行をハイライト

複数の箇所をハイライト

複数行をハイライト
複数行をハイライト
複数行をハイライト

複数の箇所をハイライト
```

ハイライト色などは `style.css` で調整してください


<span class="code-presenting-annotation fragment current-only" data-code-focus="1"></span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="3,9"></span>
<span class="code-presenting-annotation fragment current-only" data-code-focus="5-7"></span>

---

## ローカル環境での動作確認
- - -

browser-sync を使用することで簡単にローカル環境で動作角にする事ができ、ライブリロード出来る

```
# グローバル環境にインストール
$ npm install browser-sync -g

# このファイルがあるディレクトリで実行することで
# ローカルサーバが立ち上がる
# --files を付けることでそのファイルが書き換えられたときに
# 自動的にブラウザが更新される
$ browser-sync start --server --files "**/*"
```

---

## github で公開
- - -

```
$ git init
# gh-pages ブランチで開発する
$ git checkout -b gh-pages
$ git add .
$ git commit -m "first commit"
```

---

---

## pdf で出力
- - -

* `/?print-pdf/#` にアクセスして、PDF で印刷を行う。
* `http://localhost:3000/#`
* ↓
* `http://localhost:3000/?print-pdf/#/`

---

## 参考リンク

* [reveal.jsのREADME.mdを翻訳してみた - Qiita](https://qiita.com/hilohiro/items/eab479f6dcf4a100e31b)


