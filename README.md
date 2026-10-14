# acsampl - AtCoder Python Snippet & Template Library

[![AtCoder Rule 20251003 Compliant](https://img.shields.io/badge/AtCoder%20Rule%2020251003-Compliant-brightgreen.svg)](https://atcoder.jp/posts/1567)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/)

競技プログラミング（AtCoder / ABC, ARC, AGC）用の Python3 / PyPy3 スニペット・テンプレート集です。

---

## 📌 AtCoder生成AI対策ルール（20251003版）への準拠について

本リポジトリ内のコードはすべて、[AtCoder生成AI対策ルール（20251003版）](https://atcoder.jp/posts/1567) に則り、**コンテスト開始前にあらかじめ生成AI（Gemini / Antigravity）を用いて作成・公開されたコード**です。

> **ルール抜粋:**
> 「コンテスト開始前にあらかじめ生成AIを用いて作成しておいたコード等の使用は許容されます。」

競技参加中、本リポジトリ内のコードをコピー＆ペーストして利用することは公式ルール上明示的に許可されています。

---

## 🚀 特徴

1. **極限まで短いコード**: 競技中のコピペ・提出に最適化し、行数・文字数を極力短縮。
2. **充実した使い方・ドキュメント**: 各ファイルの先頭に計算量・引数・使用例を詳細記載。コピペ時に邪魔にならない分離設計。
3. **参照元リンク付き**: 各関数・クラス直前に本リポジトリへの参照URLがコメント記載されており、提出コード上でも参照元を明示可能。
4. **外部依存最小**: 基本的に Python 標準ライブラリのみで動作（一部 ACL ラッパー除く）。

---

## 📚 収録ライブラリ一覧

### グラフアルゴリズム (Graph)
| ファイル | 内容 | 計算量 / 備考 |
|---|---|---|
| [`dijkstra.py`](./dijkstra.py) | ダイクストラ法 / 経路復元 / 01-BFS | $O((V+E)\log V)$, $O(V+E)$ |
| [`bellman.py`](./bellman.py) | ベルマンフォード法 / 負閉路検出 | $O(VE)$ |
| [`w_f.py`](./w_f.py) | ワーシャルフロイド法 (全点対最短路) | $O(V^3)$ |
| [`cycle.py`](./cycle.py) | トポロジカルソート / 閉路検出・復元 | $O(V+E)$ |
| [`tree.py`](./tree.py) | 木の直径 / LCA (ダブリング) / 距離クエリ | 前計算 $O(V\log V)$, クエリ $O(\log V)$ |
| [`znhoui.py`](./znhoui.py) | 全方位木DP (Rerooting DP) 汎用フレームワーク | $O(V)$ |
| [`graphth.py`](./graphth.py) | 最大クリーク / 最大独立集合 / 最小点被覆 | Bron-Kerbosch ($N \le 40$) |

### データ構造 (Data Structures)
| ファイル | 内容 | 計算量 / 備考 |
|---|---|---|
| [`dsu_.py`](./dsu_.py) | 素集合データ構造 (Union-Find / 重み付きDSU) | ならし $O(\alpha(N))$ |
| [`sortedlist.py`](./sortedlist.py) | SortedMultiset (C++ `std::multiset` 相当) | 全操作 $O(\sqrt{N})$ |
| [`sortedset.py`](./sortedset.py) | SortedSet (C++ `std::set` 相当, 重複除外) | 全操作 $O(\sqrt{N})$ |
| [`sorted.py`](./sorted.py) | Fenwick Tree (BIT) / $k$-th element 二分探索 / 座標圧縮 | $O(\log N)$ |
| [`tentou.py`](./tentou.py) | 転倒数 (Inversion Number) | $O(N\log N)$ |
| [`que.py`](./que.py) | 最大ヒープ / 削除可能ヒープ / スライド最小値 | $O(\log N)$ / $O(N)$ |
| [`tri.py`](./tri.py) | FlatTrie (文字列木) / BinaryTrie (XOR最大化) | $O(\|S\|)$ / $O(\text{bits})$ |
| [`rope.py`](./rope.py) | Rope木 (動的配列・列操作・高速スライス) | $O(\log N)$ |

### 数学・代数 (Math)
| ファイル | 内容 | 計算量 / 備考 |
|---|---|---|
| [`prime.py`](./prime.py) | 高速素数判定 (Miller-Rabin) / 素因数分解 (Pollard's rho) / 篩 / 約数 | $O(N^{1/4})$, 64bit確定 |
| [`ntt.py`](./ntt.py) | 数論変換 NTT (mod 998244353 畳み込み) | $O(N\log N)$ |
| [`fft.py`](./fft.py) | 高速フーリエ変換 FFT (複素数・任意多項式積) | $O(N\log N)$ |

### 探索・配列・テクニック (Techniques & Utilities)
| ファイル | 内容 | 計算量 / 備考 |
|---|---|---|
| [`bisect_.py`](./bisect_.py) | 二分探索早見表 / めぐる式二分探索 (整数・小数) | $O(\log(\text{range}))$ |
| [`shakutori.py`](./shakutori.py) | 尺取り法 (Two Pointers) パターン集 | $O(N)$ |
| [`d2.py`](./d2.py) | 2次元グリッド探索 (4/8近傍・渦巻き・回転) | 便利ツール |
| [`high_array.py`](./high_array.py) | フラット多次元配列 (Flat2D, FlatND) / Bitset高速化 | 省メモリ・高速化 |
| [`tuple.py`](./tuple.py) | タプル・ベクトル演算 (加減算・マンハッタン距離) | 幾何・座標操作 |
| [`iter.py`](./iter.py) | itertools 早見表 / ランレングス圧縮 (RLE) | $O(N)$ |
| [`recursion_mod.py`](./recursion_mod.py) | 再帰深度制限回避 (sys.setrecursionlimit & bootstrap) | スタックオーバーフロー回避 |
| [`game.py`](./game.py) | ゲーム探索 (Alpha-Beta剪定 / Grundy数・Nim) | メモ化再帰 |

### ツール・テンプレート (Tools & Templates)
| ファイル | 内容 | 備考 |
|---|---|---|
| [`inputt.py`](./inputt.py) | 高速入出力テンプレ (`sys.stdin.buffer.read`) | 大規模入力対策 |
| [`interactive.py`](./interactive.py) | インタラクティブ問題用ローカルモックテスター | 対話型自動デバッグ |
| [`atcoder_test.py`](./atcoder_test.py) | AtCoder Library (ac-library-python) チートシート | ACL全機能の利用例 |
| [`testset.py`](./testset.py) | ランダムテストケース生成器 & ストレステスター | 愚直解突合デバッグ |

---

## 📜 ライセンス
CC0 / Public Domain
