修正内容をまとめたマークダウン形式のファイルを添付しますので、添付ファイルをダウンロードし、エディタで開いて修正内容を確認してください！
修正指示に対して、 *どのように修正したか* を確認したいので修正指示のすぐ下に直接 *修正内容を書き込み* 
再レビュー依頼の時に `review.md` ファイルを併せて添付してください！
マークダウンについて詳しく知りたい方は[こちら](https://giztech.gizumo-inc.work/lesson/40)にまとめてありますので読んでみてください
以上、よろしくお願いします！

# Bolt PC
## 修正内容
--- 例 ---
1. 修正指示を記載します(メンター)
  - 修正内容を記載してください(研修生)
    例) 〇〇クラスに××を指定して△△になるようにしました。
----------

## 前回の続き

### SNS

1.  aタグも削除しちゃってるかな？ここは仕様通りaタグで作成します。こうですね！
```html
<li class="nav_icon">
  <a>
    <i class="fab fa-facebook-f nav_icon_contents"></i>
  </a>
</li>
```
 →すみません、僕の書き方が悪かったです！aタグにhref属性は必須ですのでこうですね！
```html
<li class="nav_icon">
  <a href="">
    <i class="fab fa-facebook-f nav_icon_contents"></i>
  </a>
</li>
```

  --修正しました--

2. また、6枚画像、sns共にaタグの領域が小さいです。デベロッパーツールで確認してみましょう！

  --6枚画像のaタグに { display: block } を追記しました'
    snsのaタグに{ display: block; line-height:親要素のheightのpx }を追記しました--

## cssについて

### all 

1. innerについて追記
   1. heightは必要ありません！
   2. max-widthは使いません！widthで指定しましょう！

    --1.height削除しました
       2.max-width→widthに修正しました--