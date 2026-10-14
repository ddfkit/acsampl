# acsampl

競技プログラミング（AtCoder）用のスニペット集です。  
※ [AtCoder生成AI対策ルール（20251003版）](https://atcoder.jp/posts/1567) に準拠し、コンテスト開始前にあらかじめ作成・公開しています。

---

## 一覧

### グラフ
- [`dijkstra.py`](./dijkstra.py) : ダイクストラ法 / 経路復元 / 01-BFS
- [`bellman.py`](./bellman.py) : ベルマンフォード法 / 負閉路検出
- [`w_f.py`](./w_f.py) : ワーシャルフロイド法 (全点対最短路)
- [`cycle.py`](./cycle.py) : トポロジカルソート / 閉路検出・復元
- [`tree.py`](./tree.py) : 木の直径 / LCA (ダブリング) / 頂点間距離
- [`znhoui.py`](./znhoui.py) : 全方位木DP (Rerooting DP)
- [`graphth.py`](./graphth.py) : 最大クリーク / 最大独立集合 / 最小点被覆

### データ構造
- [`dsu_.py`](./dsu_.py) : Union-Find / 重み付き (ポテンシャル付き) DSU
- [`sortedset.py`](./sortedset.py) : `sortedcontainers.SortedSet` 使い方・使用例
- [`sortedlist.py`](./sortedlist.py) : `SortedMultiset` (平衡二分木・multiset代替)
- [`sorted.py`](./sorted.py) : Fenwick Tree (BIT) / $k$-th element 探索 / 座標圧縮
- [`tentou.py`](./tentou.py) : 転倒数計算 (座標圧縮内蔵 BIT)
- [`que.py`](./que.py) : 最大ヒープ / 削除可能ヒープ / スライド最小値
- [`tri.py`](./tri.py) : Trie木 / BinaryTrie (XOR最大化)
- [`rope.py`](./rope.py) : Rope木 (動的配列・列操作)

### 数学・代数
- [`prime.py`](./prime.py) : Miller-Rabin 素数判定 / Pollard's rho 素因数分解 / 篩 / 約数
- [`ntt.py`](./ntt.py) : 数論変換 NTT (mod 998244353 畳み込み)
- [`fft.py`](./fft.py) : 高速フーリエ変換 FFT (複素数多項式乗算)

### 探索・配列・ユーティリティ
- [`bisect_.py`](./bisect_.py) : 二分探索早見表 / めぐる式二分探索
- [`shakutori.py`](./shakutori.py) : 尺取り法パターン集
- [`d2.py`](./d2.py) : 2次元グリッド探索 (4/8近傍・渦巻き・回転)
- [`high_array.py`](./high_array.py) : フラット多次元配列 / Bitset 高速化
- [`tuple.py`](./tuple.py) : タプル・ベクトル加減算 / 距離 / 回転
- [`iter.py`](./iter.py) : itertools 早見表 / ランレングス圧縮 (RLE)
- [`recursion_mod.py`](./recursion_mod.py) : 再帰深度制限回避 / bootstrap
- [`game.py`](./game.py) : Alpha-Beta 枝刈り / Grundy数 (Nim)

### ツール・テンプレート
- [`inputt.py`](./inputt.py) : 高速入出力テンプレ (`sys.stdin.buffer.read`) / 転置
- [`interactive.py`](./interactive.py) : インタラクティブ問題用ローカルモックテスター
- [`atcoder_test.py`](./atcoder_test.py) : AtCoder Library (ACL) チートシート
- [`testset.py`](./testset.py) : ランダムテストケース生成 / ストレステスター
