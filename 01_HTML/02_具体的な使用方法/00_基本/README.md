### VS コードの便利な使い方

・Script を埋め込む<br>
CSS → link:css で自動変換<br>
JavaScript → script:src で自動変換<br>
※command を押しスクリプトをクリックするとファイル開ける、なければ作成できる

・選択して F2 を押し変更すると開始タグと終了タグがセットで変更される<br>

・`ol>{ポテト} `で簡単に`<ol>ポテト</ol>`コード化できる<br>
・`strong{ポテト}`で`<strong>ポテト</strong>`になる

・indent-rainbow で色付拡張

### HTML メモ

**section と div の使い分け**<br>
section：意味の塊<br>
div：見た目を変えたい時、JS で使いたい時

`&copy;Copyright`→ ©

### 書き順

seciton の中で header,footer をそれぞれ作ってもいい<br>
・head の書く順番<br>
meta は meta で固める。タイトルを一番下にするのが良い（変更するときに見つけやすいため）

### テキスト

`<ul>順序なしリスト</ul>`<br>
`<ol>順序付きリスト</ol>`

・説明リスト（あまり使わない）

```rb
<dl>
    <dt>HTML</dt>
    <dd>Hypertext Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Styke Sheet</dd>
</dl>
```

強調　`<em>`<br>
重要 `<strong>`<br>
↑ あまり変わらない、違いがわからない、滅多に使わない
strong{ポテトフライ}で一発でコードに変換される →<strong>ポテトフライ</strong>

・リンク （img も同じ。URL 書くところでは使用可能）<br>
① 完全な URL：`<a href="http://" title="レシピページ">ここ</a> `<br><a href="http://" title="レシピページ">ここ</a>　 title をつけるとカーソルに合わせると吹き出しが出る<br>
② 相対パスで指定：`<a href="./cooking.html">ここ</a>`<br>
作成したファイルにも飛べる<br>

※相対パス<br>
. 今いるところ<br>
.. 1 つ上

・空白を保持<br>
空白文字：タブ、改行、スペース<br>
< pre>タグを使うと空白をそのまま表示できる

```rb
<code>
    <pre>
        public static void main{
            system.out.
        }
    </pre>
</code>
```
