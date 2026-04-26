Poker Hand Logger static v2

使い方:
1. ZIPを解凍
2. index.html をブラウザで開く
3. セッションを選び、2枚のカードを選択して保存

主な変更:
- npm不要。HTML/CSS/JSのみ。
- セッション名は「日付 + 任意追記」。例: 2026-04-26 Sunday Million
- 履歴 → 集計 → 操作 の順に配置。
- 操作系（CSV出力、CSV読取、削除）は履歴から分離。
- アクション順: 未選択, Fold, Limp, Open, Call, 3bet, Call3, 4bet, Call4, All-in
- コンパクト表示。

保存先:
- データはブラウザのIndexedDBに保存されます。
- フォルダを削除してもブラウザ内データは消えません。
- アプリ内の「全データ削除」またはブラウザのサイトデータ削除で消せます。

PWA:
- file:// で開いた場合、Service Worker/PWAインストールは制限されます。
- HTTPSで配信するとホーム画面追加が使いやすくなります。


v8変更:
- 集計の 3bet% を 3bet+% に変更。
- 3bet+% = (3bet + 4bet+ + All-in) / (Call + 3bet + Call3 + 4bet+ + Call4+ + All-in)。
- 未選択時の1枚目/2枚目ボタンをUnknownに近い明るい色へ変更。
