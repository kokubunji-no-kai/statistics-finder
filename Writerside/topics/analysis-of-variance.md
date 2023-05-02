# 分散分析（二要因以上）

## 手法の概要
[一要因分散分析](https://kokubunji-no-kai.com/post/2021/03/12/analysis-of-variance/)と同様，実験や調査などによって得られた平均値データに，有意な差が見られるかどうかを検定するための手法です。ただし，データに影響する要因が1つだけではなく，2つ（以上）あるときに使用します。  
　たとえば，実験参加者にクイズを解かせて，その得点を比較する実験を行ったとします。このとき，「クイズの難易度（難しい・易しい）と制限時間（長い・短い）によって，得点は異なるか」という問題を調べたい場合に，二要因分散分析を用いることができます（Figure 1）。  
　二要因以上の分散分析で重要なポイントは，一要因の分散分析とは異なり，交互作用を検討することができる，という点にあります。交互作用とは，2つ以上の要因の組み合わせによる影響のことです。  
　クイズ実験の例で交互作用について考えてみましょう。ここでは，クイズの難易度が易しい場合（グラフの右側を見てください），制限時間の長短によって得点に差が見られません。これに対して，クイズが難しい場合（グラフの左側を見てください），制限時間の長短によって得点に差が見られます。これらの状態が，交互作用にあたります。つまり，制限時間の影響はクイズの難易度との組み合わせを考慮する必要がある，ということです。[^1]このように，交互作用を検討することで，一方の要因を分析しただけではわからなかった事実を発見することができます。

![](analysis-of-variance_graph.png)

[^1]: 「クイズが難しいときの制限時間の影響」のように，一方の条件を固定したときの（ここではクイズの難易度を「難」に固定したときの），他方の要因（ここでは制限時間）による影響のことを「単純主効果」と呼びます。

## 分析するときの条件
- [分散分析（一要因）](https://kokubunji-no-kai.com/post/2021/03/12/analysis-of-variance/)の記事を参照してください

## 論文（レポート）における報告例
- クイズの難易度要因の主効果は有意であった (*F*(1, 35) = 9.21, *MSE* = 1212.50, *p* = .005)
- クイズの難易度要因と制限時間要因の交互作用が有意であった (*F*(1, 35) = 4.31, *MSE* = 1445.60, *p* = .045)
- 交互作用が有意であったため単純主効果の分析を行ったところ，制限時間要因の主効果は，クイズが難しい場合には有意であったが(*F*(1, 35) = 13.69, *MSE* = 1244.81, *p* < .001)，易しい場合には有意でなかった(*F* < 1)。

## 参考になる書籍・サイト
- [Rによる分析](http://mizumot.com/handbook/?page_id=295)
- [分散分析表の見方](https://bellcurve.jp/statistics/course/10059.html)

## より深く知りたい人は
- [分析するときの条件について，もっと詳しく知りたい場合](https://norimune.net/1761)
- [わかりやすい交互作用の説明](https://norimune.net/1733)（※タイトルに「重回帰分析」と入っていますが，基本的な考え方は分散分析と同じです）