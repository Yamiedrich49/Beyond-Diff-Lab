# BEYOND DIFF. — DISCOVERY LAB 02

**二つの新しい数学パズルの発掘実験。** まず合計12問を遊び、シンプルな規則の先に本当の推理があるか検証する。

- `index.html` だけで完結。外部ライブラリ・ネットワーク通信なし。
- iPhone Safariの縦画面向け。音ON/OFF・進捗・評価は端末内に保存。
- 一次問題は3問、上級の試験問題が3問。ゲーム本編として完成・審査通過したわけではない。

## 1. RADIUS ORDER — 波が星に触れる順序

円形の波の中心を格子点に置いて放つ。波はすべての方向へ同じ速度で進む。星に触れる順番を指定どおりにする。二つの星に同時に触れた場合は不正解。発射前には現在の順序を表示しない（発射後に結果を表示）。

**試行錯誤からの成長:** 点から点への距離 → 垂直二等分線で区切られる領域 → 複数の距離条件の交差。

数理検証: 9×9格子・各星の平方距離を厳密な整数で比較。6問すべてに到達可能な正解中心があり、問題1〜6の正解格子点数は 18, 12, 11, 6, 4, 6（81点中）。複数の中心が有効だが、正解判定は任意の有効中心を許容する。少なすぎる正解位置への依存は今後の大きなリスク。

## 2. ECHO MAP — 全ての2点間の距離から配置を復元

0と最大位置の2点だけ固定し、点を追加・ドラッグ。全ペアの距離の**重複も含めた多重集合**を目標と一致させる。点の左右反転は同じ距離集合を作るため、同様に正解として認める。

**試行錯誤からの成長:** 両端からの距離 → 一番長い残りの距離 → 候補間の整合性 → 反射対称性。

これはTurnpike Reconstruction Problemとして知られる古典的な問題。数学的に独創的な発見ではなく、操作・見せ方・上達体験を新しくできるかが研究対象。

数理検証: 各問題で固定端点0とWの間に必要な点数を置く全組合せを列挙し、入力距離集合と完全一致する配置を調査。6問すべて鏡像2配置だけが正解（左右対称を除くと1種類）。問題は実現可能で意図しない異なる別解なし。各問題の距離数は3, 6, 6, 10, 15, 15。

## 実験設計と評価指針

| 観点 | RADIUS ORDER | ECHO MAP |
|---|---|---|
| 何を動かす | 1つの波源を直接ドラッグ | 数直線上の可動点をドラッグ |
| 結果は | 星の接触順序 | 全ペアの距離集合 |
| 数学的な核 | 距離の大小、垂直二等分線 | 距離多重集合からの逆問題 |
| 懸念 | 正解領域が狭くなる、適当に位置探し | 多すぎる距離チップ、計算作業 |
| 継続判断 | 上級問題を見て面白いか | 発見があるか／手作業に感じるか |

両作品とも500問への拡張は**未承認**。実機iPhone Safariでの操作音・タッチ感は未確認。先に遊んで判定する。

## 探索ロングリスト（今回の検討メモ）

| 数学領域 | 検討した種 | 一次判断 |
|---|---|---|
| 整数 | 剰余ループ、最短Golomb定規 | 規則の発見後に作業化しやすい |
| 代数 | 逆関数の連結、合成変換 | INVERSE FACTORY等と重なる |
| 確率 | 分配確率の逆算、条件付き推理 | 結果が確率的で成功判定が難しい |
| 組合せ | 駐車関数、置換の反転、円卓削除 | 既出・操作が並べ替えに寄りやすい |
| 論理・情報 | 質問一回の情報分離 | ONE EXPERIMENT不採用の教訓 |
| ネットワーク | 最小カット、ロータールーター | CUT CIRCUIT、FLOW SPLITTERと重複 |
| 平面幾何 | 距離順序、最近点融合、凸包変形 | RADIUS ORDERだけ先行試作 |
| 空間幾何 | 複数投影からの立体復元 | 既存作品との類似と複雑なUIに注意 |
| 位相 | 輪の切断、紐の交差 | 説明不要の操作UIを作る難易度が高い |
| 周期・時間 | 整数比のビリヤード、位相同期 | LASER CUBE類似／成長幅の検証要 |
| 最適化 | 区域被覆、施設の距離配置 | 汎用的な最適化問題になりやすい |
| 逆問題・復元 | unlabeled距離から点列復元、影から形を復元 | ECHO MAP先行試作 |

新規性を断言するものではなく、過去の試作結果と既存の数学的仕組みの類似を調べた一次選別。

### 背景参考

- [Turnpike Problem — FIU](https://users.cs.fiu.edu/~weiss/cop3530_spr09/assignments/turnpike.pdf)
- [Reconstructing sets from interpoint distances — DIMACS](https://archive.dimacs.rutgers.edu/TechnicalReports/abstracts/2002/2002-37.html)
- [Golomb Ruler — MathWorld](https://mathworld.wolfram.com/GolombRuler.html)
- [Billiard trajectory and unfolding — Quanta](https://www.quantamagazine.org/the-mysterious-math-of-billiards-tables-20240215/)
- [NRICH dynamic geometry](https://nrich.maths.org/dynamic-geometry)

## GitHub Pages

- リポジトリ: https://github.com/Yamiedrich49/Beyond-Diff-Lab
- Pages設定: https://github.com/Yamiedrich49/Beyond-Diff-Lab/settings/pages
- 公開URL: https://yamiedrich49.github.io/Beyond-Diff-Lab/lab-02/

既存のrootの`index.html`およびFLOW SPLITTER v2は変更していません。