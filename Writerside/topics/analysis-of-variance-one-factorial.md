# 分散分析（一要因）

## 概要


2条件（以上）の平均値に有意な差が見られるかどうかを検定するための手法です。t検定は3条件以上の差を調べるために用いることができないのに対して，分散分析は3条件以上でも用いることができます。  
　たとえば，実験参加者にクイズを解かせて，その得点を比較する実験を行ったとします。このとき，「クイズの難易度」という要因（難・中・易の3水準[(1)](#note_1 "分散分析では，要因に含まれる条件のことを「水準」と呼びます。")）によって，得点に有意な差が見られるかどうか調べるために，一要因分散分析を用いることができます（Figure 1）。  
　なお，3水準以上のデータを分析して有意差が見られた場合，「各水準間のどこかに有意差がある」ことは言えますが，「具体的にどの水準間で有意差があるか」までは言えないので注意しましょう。たとえば「難」と「易」の間に有意差が見られるか知りたい場合には，多重比較を行う必要があります。

Figure 1. 各条件におけるクイズの平均得点（エラーバーは標準誤差）
: ![Figure 1. 各条件におけるクイズの平均得点（エラーバーは標準誤差）](analysis-of-variance-one-factorial_image.png "Figure 1. 各条件におけるクイズの平均得点（エラーバーは標準誤差）")



> 分散分析では，要因に含まれる条件のことを「水準」と呼びます。この場合はクイズの難易度という要因内に3つの条件があるので，「3水準」となります。
> {id="note_1"}
> 
{style="note"}

[note_1]: #note_1

## 分析するときの条件
- 分散分析は，データが間隔尺度か比率尺度の連続量であり，正規分布に従っている（と仮定する）場合に用いることができます
- また，各要因のデータに対応があるか否かによって，検定方法が異なるので注意しましょう
    - 要因内の各水準に異なる実験参加者が割り当てられた（実験参加者間要因である）場合：対応のない分散分析をおこなう
    - 要因内の各水準に同じ実験参加者が割り当てられた（実験参加者内要因である）場合：対応のある分散分析をおこなう
- この他，各水準の分散が等しいことや，各データが独立に測定されていること等がわかっている（あるいは，そのように仮定できる）必要があります
- また，（少し高度な内容ですが）対応のある分散分析で3水準以上の場合は，球面性の仮定が満たされているか否かを考慮する必要もあります

## 論文（レポート）における報告例
> クイズの難易度要因の主効果は有意だった (*F* (1, 28) = 15.67, *p* < .001)

## 参考になる書籍・サイト
- [Rによる分析](http://mizumot.com/handbook/?page_id=219)
- [エクセルによる分析](https://udemy.benesse.co.jp/marketing/basic/excel_analyse.html)

## より深く知りたい人は
- [多重比較について](http://riseki.php.xdomain.jp/index.php?ANOVA君%2F多重比較の方法)
- [分析するときの条件について，もっと詳しく知りたい場合](https://norimune.net/1761)
