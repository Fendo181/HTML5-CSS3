# モダンコーディングへの道のり

- エンジニアが「デザインとは何か？」から考えて、HTML5/CSS3を極めていく道のりの記録です。
-基本的なHTML5/CSS3の習得を目的とし、ページデザインを1から構築します。

## やる時に意識する事

- 書いて覚えろ!!(重要)
- デザイン(使う人を)を意識する。
- コードは綺麗に整える。
- アウトプットを積極的に行う。
- わからなかい事があったら、とにかくメモを行う。

## HTML5/CSS3の基本知識

- HTML:`<要素名 属性="値">テキスト</要素名>`
- CSS:`セレクタ {プロパティ:値; }`
  - CSSのセレクタは以下の通りである。

|セレクタ | |
|:-|:-|
|p,h1,h2|要素型|
|.sample|クラス `class = "test"`|
|#sample|id `id = "test"`|

### コーディングの注意

#### 要素名にスタイルを指定しない

#ダメパターン

```.html
<div class="container">
<h1>HTML5</h1>
</div>

```

```.css
変更が多すぎるので推奨されない。
.container h1{
    coler:red;
}
```

#良いパターン

```.html
<div class="container">
<h1 class="heading">HTML5</h1>
</div>

```

```.css
変更が少ない。
.heading{
    coler:red;
}
```

#### CSSのセレクタにはIDではなく、クラスを使用する。

- 同じページの中で1つのidを使う事しかできないのでスタイルの使い回しができない。
- スタイルの上書きができない。
  - CSSにはスタイルの詳細度という概念がある。

```.html

<div id="sample" class="text-right">Hello wold</div>

```

```.css


#sample{
    text-arign:center;
}

<!-- IDの方が詳細度が高いので上書きが出来ない -->
.text-right{
    text-arign: right;
}

```

#### HTML5とJavaScriptは影響範囲を分離して使う。

はい

#### その他

- リセットCSSがあるよ
- Chromeのデベロッパーツールを正直に沢山使う。


## スタンダード レイアウト

- ヘッダー,サイドメニュー,メイン領域,フッターの4つの画面構成になっている。
- Simple is Best
- 2000年~2007年ぐらいに多くあったのかな...?
- オレオレCSS/HTML5のページを作ろう。

### 雛形

```.HTML5

<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Standad HTML5</title>
    <link rel="stylesheet" href="standard/css/rest.css">
    <link rel="stylesheet" href="standard/css/style.css">
  </head>
  <body>
      <header class="header">

      </header>
      <div class="wrapper">
          <main class="main">

          </main>
          <div calss = "sidmenu">

          </div>
      </div>
      <footer class = "footer">

      </footer>
  </body>
</html>

```

はい

### CSSの雛形


```.css
.header{
    width: 100%;
}

.wrapper{
    width: 970px;
    margin: 30px auto 40px;
}

.main{
    display: block;
    float: left;
    width: 660px;
}
.sidemenu{
    float: right;
    width:275px;
}

.footer{
    width: 100%;
}

```


## 更新履歴

- 2016_1013
  - HTML5/CSS3やっていく気持ち
- 2016_1023
  - ひさびさにHTML5/CSS3やる
- 2017_0102
  -Githubで公開

## メモ

## 本の資料

- [スタンダードレイアウ](http://www.shoeisha.com/book/hp/mcoding/1/)
- [グリッドレイアウト](http://www.shoeisha.com/book/hp/mcoding/2/#)
- [シングルページレイアウト](http://www.shoeisha.com/book/hp/mcoding/3/#)

## 参考文献
- [HTML5/CSS3モダンコーディング フロントエンドエンジニアが教える3つの本格レイアウト スタンダード・グリッド・シングルページレイアウトの作り方](http://www.shoeisha.co.jp/book/detail/9784798141572)
- [スタイルシート（CSS）の基本的な書き方【初心者向け】](http://techacademy.jp/magazine/4872)
