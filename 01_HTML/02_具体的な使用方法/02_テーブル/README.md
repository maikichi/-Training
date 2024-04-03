## テーブル

・テーブル

・< td>データ< /td>を増やすと：列（横）が増える

```rb
<body>
        <section>
            <table border="1">
                <caption>最初のテーブル</caption>
                <thead>
                    <tr>
                        <th>見出し</th>
                        <th>見出し</th>
                        <th>見出し</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
            </table>
            </tbody>
            <tfoot>
                2024 04
            </tfoot>
        </section>
    </body>
```

※caption（説明文）ここでいう見出しの上のタイトル

```
<caption>最初のテーブル</caption>
```

<caption>最初のテーブル</caption>

<br>
<body>
    <section>
            <table border="1">
                <caption>最初のテーブル</caption>
                <thead>
                    <tr>
                        <th>見出し</th>
                        <th>見出し</th>
                        <th>見出し</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
            </table>
            </tbody>
            <tfoot>
                2024 04
            </tfoot>
        </section>
    </body><br>
下記を増やすと行（縦）が増える

```rb
    <tr>
        <td>データ</td>
        <td>データ</td>
        <td>データ</td>
    </tr>
```

th･･･太字<br>
td･･･細字

・colspan でセルを結合（列：横方向）

```
    <body>
        <section>
            <table border="1">
                <caption>最初のテーブル</caption>
                <thead>
                    <tr>
                        <th>見出し</th>
                        <th>見出し</th>
                        <th>見出し</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>データ</td>
                        <td colspan="2">データ</td>列増える
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>列増える
                        <td>データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>列増える
                        <td>データ</td>
                    </tr>
            </table>
            </tbody>
            <tfoot>
                2024 04
            </tfoot>
        </section>
    </body>
```

<body>
        <section>
            <table border="1">
                <caption>最初のテーブル</caption>
                <thead>
                    <tr>
                        <th>見出し</th>
                        <th>見出し</th>
                        <th>見出し</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
            </table>
            </tbody>
            <tfoot>
                2024 04
            </tfoot>
        </section>
    </body><br>
・rowspan でセルを結合（行:縦方向）

```rb
    <body>
        <section>
            <table border="1">
                <caption>最初のテーブル</caption>
                <thead>
                    <tr>
                        <th>見出し</th>
                        <th>見出し</th>
                        <th>見出し</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td colspan="3">データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td rowspan="2">データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
            </table>
            </tbody>
            <tfoot>
                2024 04
            </tfoot>
        </section>
    </body>
```

<body>
        <section>
            <table border="1">
                <caption>最初のテーブル</caption>
                <thead>
                    <tr>
                        <th>見出し</th>
                        <th>見出し</th>
                        <th>見出し</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td colspan="3">データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                        <td rowspan="2">データ</td>
                    </tr>
                    <tr>
                        <td>データ</td>
                        <td>データ</td>
                    </tr>
            </table>
            </tbody>
            <tfoot>
                2024 04
            </tfoot>
        </section>
</body>
