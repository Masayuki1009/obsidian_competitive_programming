参照：paiza C162
index++ とは
*後置インクリメント*と呼ばれるもの。
`index` 変数は、新しい配列 `shuffled` にカードを順番に配置する際の「現在の挿入位置」を管理するための変数。

`index++` の意味
`index++` は「後置インクリメント」と呼ばれるもので、まず現在の `index` の値を使用し、その後 `index` の値を 1 増やします。
例えば、もし `index` の値が 0 であれば、`shuffled[index++] = value;` は以下のように動作します：
1. `shuffled[0]` に `value` を代入する。
2. その後、`index` の値を 0 から 1 に更新する。

**なぜ使うのか**
このように `index` を使うことで、配列 `shuffled` に対して連続的に値を入れていくとき、手動でインデックスを管理できるので、ループ内で位置をずらすために便利です。
```java
for (int t = 0; t < N; t++) {
int[] shuffled = new int[M];
int mid = M / 2;
int index = 0;

// 前半と後半を交互に入れる

for (int i = 0; i < mid; i++) {
// 現在の index (例：0) にカードを配置し、index を 1 にする
shuffled[index++] = cards[mid + i];
// 次の位置 (例：1) にカードを配置し、index を 2 にする
shuffled[index++] = cards[i]; 
}
// シャッフル結果を更新
cards = shuffled;
}
```
