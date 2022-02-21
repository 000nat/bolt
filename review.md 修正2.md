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

### all

1. titleをdivで囲っている箇所がいくつかありますが、ブロック要素一つをブロック要素で囲うことは基本的にしませんので直接hタグにスタイルを当てればいいと思います！

   --余分なdivタグは削除しました--

   → inner用のタグも削除しちゃったかな？`ブロック要素「一つ」を`囲う場合の話ですので、複数入るinner用のdivは必要なタグとなります！

    --'<article class="article_contents_wrapper">'の下に'<div>'タグを追加しました
       '<section class="section_textcontents_our">'の下に'<div>'タグを追加しました--

### SNS

1. iconはiタグを使います

   --footer側のaタグをiタグにしました--

   → aタグも削除しちゃってるかな？ここは仕様通りaタグで作成します。こうですね！
```html
<li class="nav_icon">
  <a>
    <i class="fab fa-facebook-f nav_icon_contents"></i>
  </a>
</li>
```

    --修正しました--

## cssについて

### all 

1. `font-family: "Lato";`は指示通りinnerではなく、bodyにつけます。

  --'.body'につけました--

### title

1. `.title-inner`のpaddingは 250px 0;です。headerに隠れてる部分を足してくれたのかと思いますが、足すのはmainタグにしましょう！

  --'  .main_wrapper { padding-top: 70px; }'を追記しました--

### what

1. `.section_inner_img`をmarginを使って中央寄せしていますが、text-align: center;で真ん中に寄ります（inline要素なので！）

  --'text-align: center;'に修正しました--

### work

1. こちら「四つ目以下にmargin-topを付与」となっていますが、「三つ目までmargin-topを削除」の方が、もっと複雑な指定にも対応しやすいです。またnth-childは基本的に「例外」のように使います。以上2点の理由から変更した方がいいと思います！

```css
.article_contents_img_item:nth-child(n+4) {
  margin-top: 80px;
}
```

  --'  .article_contents_img_item:nth-child(-n+3) { margin-top: 0px; }'に変更しました--