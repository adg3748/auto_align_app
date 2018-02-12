# auto_align_app

## なぜ作ったのか
「本当に大切なことに時間が使えてないんではないか」そう危惧したことが始まりです。

「じゃあ、どうすれば最も効率のいい時間の使い方ができるのか？」その1つの方法論として、タスクを4象限に分ける、というものがあります。

![](https://blog-imgs-42.fc2.com/k/a/o/kaorilavender/Image_20140116111333df8.png)
出典:http://kaorilavender.blog.fc2.com/blog-entry-404.html

「人は得てして、第1領域、第3領域にばかり気を取られて、長期的なスパンで考えると、一番影響力の大きい第2領域を考慮できてないのではないか」そう思うようになりました。

しかし、既存のタスク管理アプリを試せども、どれもこの4象限を手動で並べ替えないといけなかったり、そもそもタスクごとの重要度が定量化できてないものばかりでした。

そこで、「タスクの重要度を定量的に評価し、優先順位順に自動で並べ替えてくれて、『上から順番にこなすだけで最も効率のいい順番でタスクの処理ができる』アプリを作ろう、ということで作成に至りました。

## なんのために作ったのか
最も効率のいい処理手順にタスクを自動並べ替えすることで、タスクをこなす順番を考える手間と順番を間違えることによる人生の機会損失を最小化するため

## 何を作ったのか
影響力の大きさ(重要度)と期日までの残り日数(緊急度)を入力することで、優先度の高い順にタスクを自動で並べ替えてくれるwebアプリケーション

## どのように作ったのか
フロントはjQuery、サーバーサイドはRailsをAPI化して非同期通信を実装。インフラはherokuに仮アップロード。

整序アルゴリズムは、重要度と緊急度を1対1の仮おき評価。(緊急度100かつ緊急度1のタスクと、重要度1かつ緊急度100のタスクを同等と考える)

## どのように使うのか
1. ユーザー登録を行う

2. フォームからタスクを投稿する

3. 投稿したタスクの編集したい箇所をクリックすると、その場で編集することが可能(編集フォーム以外のところをクリックすると更新できます)

4. 不要になったタスクは右端の削除ボタンで削除 

## オススメの使い方
一応、モバイルファーストで作っていて、スマホブラウザの読み上げ機能を使うと、タスクを上から順番に読み上げてくれます。(そのうち、アプリ自体に読み上げ機能を実装したい)

## 課題
- websocketの実装が間に合っていないこと

- アルゴリズムが不完全であること(重要度と緊急度を1対1で仮おき評価しているため)

- タスク編集の際にエンターで更新する実装が間に合ってないこと

## 展望
- 優先順位順に視覚的な図形の大きさでタスクを表示できるようにすること(箇条書きは直感的でないため）

- チーム単位、プロジェクト単位でのタスクの表示を可能にすること

- 読み上げ機能の実装（箇条書きを読むのは疲れるため)

## お願い
よりよい整序アルゴリズムなど知っている方がいらっしゃれば、教えていただけると、とても嬉しく思います。

## 試しに使ってみたい方へ

サンプルユーザーでのデモンストレーションが可能です。

ユーザーid:demo
メールアドレス:demo@demo.com
パスワード:demo0000

上記、入力してお試しくださいませ。
