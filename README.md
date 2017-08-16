# default html/css
velocity.jsについて
-----------------------------------------
ネットアンサー標準レスポンシブコード
	最終更新　17年08月01日

【全体構造】
------------------------------------------------------------------------------------
ディレクトリ構成はwp構築を想定した構造にする。

例
・会社概要ページ　/about/
・組織ページ　/about/organaization/


お問い合わせページに関しても

・お問い合わせ　/contact/
・送信完了画面　/contact/completed/
と送信完了画面ページもこの構成にする。



【meta領域】
------------------------------------------------------------------------------------
<script src="/js/viewport.js"></script>

Viewport設定はjsで管理する。タブレット用のwidth値はサイトに応じて変更する。

------------------------------------------------------------------------------------
<link rel="shortcut icon" href="/images/favicon.ico">
<link rel="apple-touch-icon" href="/images/apple-touch-icon.jpg">

Favicon画像・apple-touchアイコンを作成する。
------------------------------------------------------------------------------------
<title>タイトルタイトル</title>
各ページのタイトルを記述する。
基本「ページタイトル | 会社名」

------------------------------------------------------------------------------------
<body>
idに第一スラッグを代入、第二スラッグ、第三スラッグがある場合はclass名に記述する。
トップページの場合はbody id名をfrontpageとする

例
・トップページ
/
<body id="frontpage">


・会社概要ページ
/about/
<body id=" about ">

・組織ページ
/about/organaization/
<body id=" about " class=” organaization”>


・沿革ページ
/about/organaization/history/
<body id=" about " class=” organization history”>




【css構成】
------------------------------------------------------------------------------------
全ページ共通のcss
<link rel="stylesheet" href="/css/font-awesome.css">
<link rel="stylesheet" href="/css/common.css">


------------------------------------------------------------------------------------
第一ディレクトリ共通css 
例:<link rel="stylesheet" href="/css/about.css">

※css名はbody idと同じ
※第二ディレクトリ以下のcssコーディングもこのcssファイルに記述する。


【js構成】
------------------------------------------------------------------------------------



【各ページの個別領域】
------------------------------------------------------------------------------------
そのページ特有の領域。
基本的に<article class="main"></article>でくくられた領域。

●wide領域（画面サイズフルにコンテンツ領域を使用するとき）
<div class="wrap">
</div>


●wrap inner領域（規定サイズにコンテンツ領域を使用するとき）
<div class="wrap">
<div class="inner">

      </div>
</div>

