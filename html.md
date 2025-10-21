# サンプルコード
## 3.1
・index.html
```
<h1>Hello, World!</h1>
```

## 3.2
・signup.html
```
<h2>入会申込</h2>
<p>メールアドレス<input type="email" name="mymail"></p>
<p>パスワード<input type="password" name="mypass"></p>
<button type="submit">送信</button>
```

## 3.3
・userList.html
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <title>会員一覧ページ</title>
</head>

<body>

  <h2>会員一覧</h2>

  <table border="1">
    <tr>
      <th>会員ID</th>
      <th>名前</th>
      <th>メールアドレス</th>
    </tr>
    <tr>
      <td>001</td>
      <td>山田 太郎</td>
      <td>taro@example.com</td>
    </tr>
    <tr>
      <td>002</td>
      <td>鈴木 花子</td>
      <td>hanako@example.com</td>
    </tr>
    <tr>
      <td>003</td>
      <td>佐藤 次郎</td>
      <td>jiro@example.com</td>
    </tr>
  </table>

  <div>
    <span>※上記はサンプルデータです。</span><br>
    <span>データは随時更新されます。</span>
  </div>

</body>

</html>
```

## 3.4
・userDetail.html
```
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <title>会員詳細ページ</title>
</head>
<body>

  <h2>会員詳細</h2>

  <!-- メニュー -->
  <div>
    <ul>
      <li><a href="./userList.html">会員一覧へ戻る</a></li>
      <li><a href="./edit.html">会員情報を編集</a></li>
    </ul>
  </div>
  <br>

  <!-- 会員の詳細情報 -->
  <div>
    <div>
      <img src="https://placehold.jp/150x150.png" alt="会員の写真">
    </div>
    <div>
      <p><strong>名前：</strong>山田 太郎</p>
      <p><strong>会員ID：</strong>001</p>
      <p><strong>メール：</strong>taro@example.com</p>
    </div>
  </div>
  <br>

  <!-- コメントフォーム -->
  <h4>この会員へのコメント</h4>
  <form action="/submit_comment" method="post">
    <!-- 性別選択（ラジオボタン） -->
    <a>性別：</a>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">男性</label>

    <input type="radio" id="female" name="gender" value="female">
    <label for="female">女性</label>

    <input type="radio" id="other" name="gender" value="other">
    <label for="other">その他</label>
    <br>

    <!-- 年齢選択（プルダウン） -->
    <label for="age">年齢：</label>
    <select id="age" name="age">
        <option value="">-- 選択してください --</option>
        <option value="10">10代</option>
        <option value="20">20代</option>
        <option value="30">30代</option>
        <option value="40">40代</option>
        <option value="50">50代</option>
        <option value="60">60代以上</option>
    </select>
    <br>

    <!-- コメント入力 -->
    <label for="comment">コメント：</label><br>
    <textarea id="comment" name="comment" placeholder="コメントを入力してください..."></textarea>
    <br>

    <!-- 送信ボタン -->
    <button type="submit">送信</button>
  </form>

</body>
</html>
```


## 3.5
・myblog.html
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <title>セクショニングコンテンツのサンプル</title>
  <style>
    body {
      font-family: sans-serif;
      line-height: 1.6;
    }

    header,
    nav,
    main,
    section,
    article,
    aside,
    footer {
      border: 1px solid #ccc;
      padding: 10px;
      margin: 10px;
    }

    nav ul {
      list-style: none;
      padding: 0;
    }

    nav ul li {
      display: inline;
      margin-right: 10px;
    }
  </style>
</head>

<body>

  <header>
    <h1>Myブログ</h1>
    <p>セクショニング要素のデモページ</p>
  </header>

  <nav>
    <ul>
      <li><a href="#">ホーム</a></li>
      <li><a href="#">記事一覧</a></li>
      <li><a href="#">お問い合わせ</a></li>
    </ul>
  </nav>

  <main>
    <section>
      <h2>最新の記事</h2>
      <article>
        <h3>HTMLの基本</h3>
        <p>HTMLはWebページを作るためのマークアップ言語です。</p>
      </article>
      <article>
        <h3>CSSの基本</h3>
        <p>CSSはページのデザインやレイアウトを担当します。</p>
      </article>
    </section>

    <aside>
      <h2>おすすめリンク</h2>
      <ul>
        <li><a href="#">HTML入門</a></li>
        <li><a href="#">CSS入門</a></li>
      </ul>
    </aside>
  </main>

  <footer>
    <p>&copy; 2025 Myブログ</p>
  </footer>

</body>

</html>
```

## 4.1
・cssSample.html
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <title>CSSの基礎</title>
</head>

<body>

  <h1 style="color: blue; margin: 50px;">初めてのCSS</h1>
  <p>CSSの基礎を学習する</p>

</body>

</html>
```

## 4.1.2
・cssSample.html（修正）
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <title>CSSの基礎</title>
  <style>
    h1 {
      color: blue;
      margin: 50px;
    }
  </style>
</head>

<body>

  <h1>初めてのCSS</h1>
  <p>CSSの基礎を学習する</p>

</body>

</html>
```

## 4.1.3
・cssSample.html（修正）
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <title>CSSの基礎</title>
  <link rel="stylesheet" href="css/style.css">
</head>

<body>

  <h1>初めてのCSS</h1>

  <p class="classA">CSSの基礎を学習することで</p>
  <p class="classA">WEBページのデザインを</p>
  <p id="idA">作成することができます</p>
  <br>

  <div class="classB">
    <p>スタイルの適用方法は</p>
    <p>style属性、&lt;style&gt;タグ、外部参照があります</p>
  </div>

</body>

</html>
```

・style.css
```
h1 {
  color: blue;
  margin: 20px;
}

.classA {
  color: rgb(174, 100, 25);
}

#idA {
  color: rgba(30, 171, 30, 0.878);
}

.classB p {
  color: #fff;
  background-color: #ba2caf;
}
```

## 4.2.1
・siginup.html
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width">
  <title>入会申込</title>
  <link rel="stylesheet" href="css/signupStyle.css">
</head>

<body>

  <div class="container">
    <h2>入会申込</h2>

    <form action="#" method="get">
      <div class="form-group">
        <label for="email">メールアドレス</label>
        <input type="email" id="email" name="mymail" required>
      </div>
      <div class="form-group">
        <label for="password">パスワード</label>
        <input type="password" id="password" name="mypass" required>
      </div>
      <button type="submit">送信</button>
    </form>
  </div>

</body>

</html>
```
・signupStyle.css
```
.container {
  background-color: #fff;
}
```

## 4.2.2
・signupStyle.css（追記）
```
@import url(normalize.css);

.container {
  background-color: #fff;
}
```

## 4.2.3
・signupStyle.css（追記）
```
.container {
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 400px;
  border-radius: 8px;
  padding: 20px 30px;
}
```

## 4.2.3.5
・signupStyle.css（追記）
```
.container {
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 400px;
  border-radius: 8px;
  padding: 20px 30px;
  margin: 10px auto;
}
```

## 4.2.4
・signupStyle.css（追記）
```
h2 {
  color: #333;
  margin-bottom: 20px;
  text-align: center;
}
```

## 4.2.5
・signupStyle.css（追記）
```
.form-group label {
  color: #555;
  font-weight: bold;
}
```

## 4.2.5.2
・signupStyle.css（追記）
```
.form-group label {
  color: #555;
  font-weight: bold;
  display: block;
  margin-bottom: 5px;
}
```

## 4.2.6
・signupStyle.css（追記）
```
.form-group input {
  width: 100%;
  padding: 10px 0;
  margin: 0 0 15px 0;
  border-radius: 4px;
  border: 1px solid #ddd;
  font-size: 16px;
}
```

## 4.2.7
・signupStyle.css（追記）
```
button {
  padding: 12px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  width: 100%;
  cursor: pointer;
}
```

## 4.2.7.2
・signupStyle.css（追記）
```
button:hover {
  background-color: #0056b3;
}
```

## 4.2.7.4
・signupStyle.css（追記）
```
button {
  〜中略〜
  width: 100%;
  cursor: pointer;
  transition: background-color 0.3s ease 0s;
}

button:hover {
  background-color: #0056b3;
}
```

## 4.2.8
・signupStyle.css（追記）
```
body {
  background-color: #f0f2f5;
}
```

・signupStyle.css
```
@import url(normalize.css);

.container {
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  width: 400px;
  border-radius: 8px;
  padding: 20px 30px;
  margin: 10px auto;
}

h2 {
  color: #333;
  margin-bottom: 20px;
  text-align: center;
}

.form-group label {
  color: #555;
  font-weight: bold;
  display: block;
  margin-bottom: 5px;
}

.form-group input {
  width: 100%;
  padding: 10px 0;
  margin: 0 0 15px 0;
  border-radius: 4px;
  border: 1px solid #ddd;
  font-size: 16px;
}

button {
  padding: 12px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  width: 100%;
  cursor: pointer;
  transition: background-color 0.3s ease 0s;
}

button:hover {
  background-color: #0056b3;
}

body {
  background-color: #f0f2f5;
}
```

## 5.2
・movieSelection.html
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="css/movieSelectionStyle.css">
  <title>映画紹介ページ</title>
</head>

<body>
  <div class="container">
    <div class="header">
      映画紹介サイト
    </div>

    <div class="sidebar">
      <h3>ジャンル</h3>
      <ul>
        <li>アクション</li>
        <li>ドラマ</li>
        <li>コメディ</li>
        <li>ホラー</li>
      </ul>
    </div>

    <div class="main">

      <div class="movie-content">
        <img src="https://placehold.jp/100x150.png" alt="映画ポスター">
        <div class="movie-text">
          <h2>ニューヨークの空に</h2>
          <p>あらすじ：感動的なストーリーが展開されるヒューマンドラマ。</p>
        </div>
        <div class="movie-rank">
          <h3>オススメ度</h3>
          <p>★★★☆☆</p>
        </div>
      </div>

      <div class="movie-content">
        <img src="https://placehold.jp/100x150.png" alt="映画ポスター">
        <div class="movie-text">
          <h2>砂の恒星</h2>
          <p>あらすじ：未来の世界を舞台にした壮大なSFアドベンチャー。</p>
        </div>
        <div class="movie-rank">
          <h3>オススメ度</h3>
          <p>★★★★★</p>
        </div>
      </div>

    </div>

    <div class="footer">
      &copy; 20XX 映画紹介サイト All Rights Reserved.
    </div>
  </div>
</body>

</html>
```

・movieSelectionStyle.css
```
body {
  margin: 0;
}

/* グリッドレイアウトでコンテンツを配置 */
.container {
  height: 100vh;
}

.header {
  background-color: #2c3e50;
  color: white;
  padding: 20px;
  font-size: 24px;
}

.sidebar {
  background-color: #ecf0f1;
  padding: 20px;
}

.main {
  background-color: #fff;
  padding: 20px;
}

.footer {
  background-color: #2c3e50;
  color: white;
  text-align: center;
  padding: 10px;
}

/* フレックスボックスでコンテンツを配置 */
.movie-content {
  margin-bottom: 20px;
  padding: 10px;
  border: 1px solid #ccc;
}

.movie-content img {
  width: 100px;
  height: 150px;
}

.movie-text {
}

.movie-rank {
  text-align: center;
}
```
## 5.3
・movieSelectionStyle.css（追記）
```
/* グリッドレイアウトでコンテンツを配置 */
.container {
  display: grid;
  grid-template-columns: 200px 1fr;
  grid-template-rows: 80px 1fr 50px;
  height: 100vh;
}

.header {
  grid-column: 1 / 3;
  grid-row: 1 / 2;
  background-color: #2c3e50;
  color: white;
  padding: 20px;
  font-size: 24px;
}

.sidebar {
  grid-column: 1 / 2;
  grid-row: 2 / 3;
  background-color: #ecf0f1;
  padding: 20px;
}

.main {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
  background-color: #fff;
  padding: 20px;
}

.footer {
  grid-column: 1 / 3;
  grid-row: 3 / 4;
  background-color: #2c3e50;
  color: white;
  text-align: center;
  padding: 10px;
}
```

## 5.4
・movieSelectionStyle.css（追記）
```
/* フレックスボックスでコンテンツを配置 */
.movie-content {
  display: flex;
  gap: 20px;
  align-items: flex-start;
  margin-bottom: 20px;
  padding: 10px;
  border: 1px solid #ccc;
}
```

## 5.4.2
・movieSelectionStyle.css（追記）
```
.movie-text {
  flex: 3 1 0;
}

.movie-rank {
  flex: 1 1 0;
  text-align: center;
}
```

## 5.5
・movieSelectionStyle.css（追記）
```
〜前略〜

.movie-rank {
  flex: 1 1 0;
  text-align: center;
}

/* 画面幅が768px以下の場合：モバイル向けにレイアウト変更 */
@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
    grid-template-rows: auto auto auto auto;
  }

  .header {
    grid-column: 1 / 2;
    grid-row: 1 / 2;
  }

  .sidebar {
    grid-column: 1 / 2;
    grid-row: 2 / 3;
  }

  .main {
    grid-column: 1 / 2;
    grid-row: 3 / 4;
  }

  .footer {
    grid-column: 1 / 2;
    grid-row: 4 / 5;
  }

  .movie-content {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .movie-text {
    text-align: left;
  }
}
```

## 6.3
・albumSelection.html
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>アルバム紹介サイト</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>

<body>
  <!-- メインコンテンツ -->
  <div class="container my-5">
    <h2 class="mb-4 text-center">おすすめアルバム一覧</h2>
    <div class="row g-4">
      <!-- アルバム1 -->
      <div class="col-12 col-md-4 bg-light">
        album1
      </div>

      <!-- アルバム2 -->
      <div class="col-12 col-md-4 bg-info">
        album2
      </div>

      <!-- アルバム3 -->
      <div class="col-12 col-md-4 bg-warning">
        album3
      </div>
    </div>
  </div>

</body>

</html>
```

## 6.4
・albumSelection.html（修正）
```
<!-- メインコンテンツ -->
<div class="container my-5">
  <h2 class="mb-4 text-center">おすすめアルバム一覧</h2>
  <div class="row g-4">
    <!-- アルバム1 -->
    <div class="col-12 col-md-4">
      <div class="card h-100">
        <img src="https://placehold.jp/300x200.png" class="card-img-top" alt="アルバム1">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">Blue Sky Dreams</h5>
          <p class="card-text">爽やかなメロディが特徴のポップアルバム。夏にぴったりの1枚！</p>
          <div>
            <a href="#" class="btn btn-outline-primary me-2">詳細を見る</a>
            <a href="#" class="btn btn-primary">購入</a>
          </div>
        </div>
      </div>
    </div>

    <!-- アルバム2 -->
    <div class="col-12 col-md-4">
      <div class="card h-100">
        <img src="https://placehold.jp/300x200.png" class="card-img-top" alt="アルバム2">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">Night Jazz Vibes</h5>
          <p class="card-text">夜のドライブにぴったりなジャズナンバーを詰め込んだアルバム。</p>
          <div>
            <a href="#" class="btn btn-outline-primary me-2">詳細を見る</a>
            <a href="#" class="btn btn-primary">購入</a>
          </div>
        </div>
      </div>
    </div>

    <!-- アルバム3 -->
    <div class="col-12 col-md-4">
      <div class="card h-100">
        <img src="https://placehold.jp/300x200.png" class="card-img-top" alt="アルバム3">
        <div class="card-body d-flex flex-column">
          <h5 class="card-title">Rock Legend</h5>
          <p class="card-text">伝説のロックバンドによる名曲を集めた1枚。熱い魂を感じろ！</p>
          <div>
            <a href="#" class="btn btn-outline-primary me-2">詳細を見る</a>
            <a href="#" class="btn btn-primary">購入</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

## 6.5
・albumSelection.html（修正）
```
<!-- ナビゲーションバー -->
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">アルバム紹介</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link" href="#">ホーム</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">特徴</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">お問い合わせ</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<!-- メインコンテンツ -->
〜中略〜

<!-- フッター -->
<footer class="bg-dark text-white text-center py-3">
  &copy; 20XX アルバム紹介サイト All rights reserved.
</footer>

<!-- Bootstrap JSの読み込み -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

## 7.2.1
・jsSample.html
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <script>
    console.log("Hello World!");
  </script>
</head>

<body>

  <h1>JavaScriptサンプル</h1>

</body>

</html>
```

## 7.2.2
・sampleScript.js
```
console.log("これは sampleScript から実行しています");
```

・jsSample.html（修正）
```
<!DOCTYPE html>
<html lang="ja">

<head>
  <script src="sampleScript.js"></script>
</head>

<body>

  <h1>JavaScriptサンプル</h1>

</body>

</html>
```

## 7.3
```
・buttonAlert.html
<!DOCTYPE html>
<html lang="ja">
<head>
</head>
<body>
  <button id="btn">押してね</button>

  <script>
    // 変数
    let name = "tanaka";
    let age = 25;
    let message = "";

    // 条件分岐
    if(age > 18) {
      message = name + " は成人です";
    }
    else {
      message = name + " は未成年です";
    }

    // 繰り返し
    for(let i = 0; i < 5; i++) {
      console.log(message + ": " + i);
    }

    // DOM操作(HTMLをコードから操作)
    let button = document.getElementById("btn");
    button.addEventListener("click", () => {
      alert(message);
    });
  </script>
</body>
</html>
```
