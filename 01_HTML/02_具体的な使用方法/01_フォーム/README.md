## フォーム

#### get と post の違い

- get：検索時などの記録に残るように使用

```rb
<main>
    <form action="index.html" method="get">←post
        <input type="hidden" name="username" value="ひみつのアッコちゃん">
        <button type="submit">送信</button>
    </form>
</main>
```

get：HT メソッド。見えてもいい取得(log ファイルで記録されてしまう)
何かを検索するとき記録に残るように使用

ドメインの?以降が見える

- post：見えない方が良い情報の時使用

```rb
<main>
    <form action="index.html" method="post">
        <input type="hidden" name="username" value="ひみつのアッコちゃん">
        <button type="submit">送信</button>
    </form>
</main>
```

自分の情報を登録するとき、HTTPS 安全なもの<br>
ドメインの?以降が見えない

### < input>要素（id や name は都度決めるもの）

・テキストボックス

```rb
<input type="text" name="user_name" id="userName">
```

<input type="text" name="user_name" id="userName"> <br>

・パスワード

```rb
<input type="password" name="password" required>
```

※required を入れると必須項目
<input type="password" name="password"><br>

・メールアドレス

```rb
<input type="email" name="mail_address">
```

<input type="email" name="mail_address"><br>

・数値入力

```rb
<input type="number" name="age" min="0" max="10">
```

<input type="number" name="age" min="0" max="10"><br>

・日付入力

```rb
<input type="date" name="publish_date">
```

<input type="date" name="publish_date"><br>

・カラー

```rb
<input type="color" name="" id="">
```

<input type="color" name="" id=""><br>

・ファイルを添付

```rb
<form action="index.html" method="get" enctype="multipart/form-data">
    <input type="file" name="file">
</form>
```

<form action="index.html" method="get" enctype="multipart/form-data">
    <input type="file" name="file">
</form><br>

その他の< input>要素は[こちら](https://developer.mozilla.org/ja/docs/Web/HTML/Element/input)を確認！

### 複数行入力部品

```rb
<textarea name="description" cols="30" rows="3"></textarea>
```

<textarea name="description" cols="30" rows="3"></textarea>

row：行数<br>
角を持って移動できる<br>
！pre タグを使用しないと改行されない

⚠️ textarea には複数行いれてテストする

・ボタン<br>

```rb
① <input type="button" value="送信">
```

<input type="button" value="送信">

```rb
② <button type="submit">送信</button>
```

<button type="submit">送信</button>
② の使用を推奨

```rb
<button type="button">ただのボタン</button>
```

<button type="button">ただのボタン</button>
JS で何かする時に使用<br>

```rb
<button type="reset">リセット</button>
```

<button type="reset">リセット</button>
全部消すではなく一番最初の状態に戻す<br>

・チェックボックス（文字にカーソル合わさればクリックできるようにする設定にする）

```rb
<div>
    <legend>好きな色</legend>
    <input type="checkbox" name="signal" id="green" value="green">
    <label for="green">青</label>
    <input type="checkbox" name="signal" id="yellow" value="yellow">
    <label for="yellow">黄</label>
    <input type="checkbox" name="signal" id="red" value="red">
    <label for="red">赤</label>
</div>
```

<div>
    <legend>好きな色</legend>
    <input type="checkbox" name="signal" id="green" value="green">
    <label for="green">青</label>
    <input type="checkbox" name="signal" id="yellow" value="yellow">
    <label for="yellow">黄</label>
    <input type="checkbox" name="signal" id="red" value="red">
    <label for="red">赤</label>
</div>

<br>
・ラジオボタン（1 つだけ選ぶ）

```rb
<ul>
    <li><input type="radio" name="meal" value="soup" checked>スープ</li>
    <li><input type="radio" name="meal" value="curry">カレー</li>
    <li><input type="radio" name="meal" value="pizza">ピザ</li>
</ul>
```

※checked を入れるとその項目にチェックが入った状態で出る

<ul>
    <li><input type="radio" name="meal" value="soup" checked>スープ</li>
    <li><input type="radio" name="meal" value="curry">カレー</li>
    <li><input type="radio" name="meal" value="pizza">ピザ</li>
</ul>

<br>
・選択ボックス（プルダウン）

```rb
<select name="fruit">
    <option value="apple">りんご</option>
    <option value="orange">みかん</option>
    <option value="banana" selected>バナナ</option>
</select>
```

※selected を入れるとその項目が入った状態で出る

<select name="fruit">
    <option value="apple">りんご</option>
    <option value="orange">みかん</option>
    <option value="banana" selected>バナナ</option>
</select>

<br>
・自動補完（文字を入れると補完される）

```rb
<input type="text" name="fruit" list="fruits">
    <datalist id="fruits">
        <option>りんご</option>
        <option>みかん</option>
        <option>バナナ</option>
    </datalist>
```

<input type="text" name="fruit" list="fruits">
    <datalist id="fruits">
        <option>りんご</option>
        <option>みかん</option>
        <option>バナナ</option>
    </datalist>

<br>
・ファイル

```rb
<form action="/upload" action="post" enctype="multipart/form-data">
    <input type="file" name="portrait">
</form>
```

<form action="/upload" action="post" enctype="multipart/form-data">
    <input type="file" name="portrait">
</form>

<br>
・隠し入力

```rb
<input type="hidden" name="uid" value="15D96933-4EF4-42B8-BD59-486CC827830D">
```

・ラベル

```rb
<label for="userName">名前</label>
```

<label for="userName">名前</label>

・フィールドセット、レジェンド（CSS でできるのであまり使用しない）

```rb
<fieldset>
    <legend>投稿フォーム</legend>
    <!-- ラベル、入力部品など -->
</fieldset>
```

<fieldset>
    <legend>投稿フォーム</legend>
    <!-- ラベル、入力部品など -->
</fieldset>
