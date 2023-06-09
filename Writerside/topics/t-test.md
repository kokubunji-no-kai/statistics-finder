# t検定

## 手法の概要
実験や調査の結果得られた平均値が，ある特定の値より大きい（小さい）かどうかを検定するときに用いる手法です。また，2つの条件における平均値が異なるかどうかを検定するときや，回帰分析の係数βが0か否かを検定するときにも用いられます。  
　たとえば，実験参加者5人にクイズを解かせて，その正解率や反応時間を測定する実験を行ったとします。このとき，実験参加者の平均正解率70％が，全国平均の50％よりも有意に高いかどうかを調べるためにt検定を用います。あるいは，実験参加者5人の平均反応時間15秒が，別の実験参加者5人の平均反応時間10秒よりも有意に長いかどうかを調べるときにも (下図)，t検定を用いることができます。ただし，3条件以上の比較はできないので注意しましょう。

クイズの平均反応時間（エラーバーは標準誤差）
: ![クイズの平均反応時間（エラーバーは標準誤差）](t-test_graph.png "クイズの平均反応時間（エラーバーは標準誤差）")



## 分析するときの条件
- 「データが正規分布に従う」という条件が満たされる場合に使える分析手法ですが，データ数が十分に大きい場合（基本的には）気にしなくても大丈夫です。
- 2条件の比較をする場合には，両条件で「同じ実験参加者か否か（データに対応があるか否か）」，また「分散が等しいと仮定できるか否か」によって，以下の方法からいずれを選ぶべきか異なるので注意しましょう。
    - 2条件に同じ実験参加者が参加した場合：対応のあるt検定をおこなう
    - 2条件に別々の実験参加者が参加した場合：対応のないt検定をおこなう
        - 分散が等しいと仮定できる場合：Studentのt検定をおこなう
        - 分散が等しいと仮定できない（あるいは不明な）場合：Welchのt検定をおこなう

## 論文（レポート）における報告例
> A条件における正解率は，チャンスレベル（50%）よりも有意に高かった (*t* (10) = 2.34, *p* = .023)

> 対応のあるt検定の結果，A条件の反応時間はB条件より有意に長かった (*t* (19) = 5.24, *p* < .001)。

## 参考になる書籍・サイト
- [Rによる分析](http://cse.naro.affrc.go.jp/takezawa/r-tips/r/65.html)
- [エクセルによる分析](https://udemy.benesse.co.jp/marketing/basic/excel_analyse.html)

## より深く知りたい人は
- [どのt検定を用いるべきか](https://bellcurve.jp/statistics/course/9936.html)
- [分析するときの条件について，もっと詳しく知りたい場合](https://norimune.net/1761)
