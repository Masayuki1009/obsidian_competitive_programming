*概要*
一番よくあるやつ。
数字が入力される場合は以下のように表現する。
```java
int N = Integer.parseInt(sc.nextLine());
```

*sc.nextLine*の動作
・*現在位置から行末までの全文字列*を取得
・改行文字も*消費する*
・*行全体を一括で処理したい場合*に適している

**競技プログラミングでの利用例**: 
問題文の説明や、複数のスペースを含む文字列の入力がある場合、*1行全体を一度に受け取ってから*必要な部分を処理するのに向いています。

特徴
*改行文字までを1つの文字列として読み込む*ため、複数単語からなる入力を一度に取得できます。