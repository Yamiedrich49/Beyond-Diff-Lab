# BEYOND DIFF. LAB

**Small rules. Big surprises.**

4つの数学パズルをスマートフォンで遊び比べる研究ラボです。外部ライブラリやビルドは不要。単一の `index.html` で動作します。

| ゲーム | プレイヤーが考えること | 問題数 |
|---|---|---:|
| PEEL CORE | ネットワークに橋を1本足して、最後に残る点を設計する | 18 |
| TRIPLE TURN | 隣接する3個を回して、目標の順序にそろえる | 18 |
| ONE EXPERIMENT | 1回の入力で隠れた計算機を見分ける | 18 |
| FLOW SPLITTER | 分岐の向きを調整して、色玉の出口をそろえる | 18 |

計72ステージ。各ゲームの問題は固定シードで生成されます。

## 遊び方と機能

- 上部のタブでゲームを切り替え、画面内で次のステージに進めます。
- iPhone縦画面のタッチ操作を想定し、音のON/OFFを切り替えられます。
- ゲーム進捗と評価を `localStorage` に保存します。
- TRIPLE TURNには取り消し機能があります。
- 「研究記録をコピー」から各作品のプレイ記録を共有できます。

## GitHub Pages設定

このリポジトリの [Settings → Pages](https://github.com/Yamiedrich49/Beyond-Diff-Lab/settings/pages) で、**Build and deployment → Deploy from a branch → main → /(root) → Save** を選択してください。

公開予定URL: https://yamiedrich49.github.io/Beyond-Diff-Lab/

## 初期検証

- 4ゲームすべてでステージ開始・正解・成功演出をブラウザで確認。
- PEEL COREの18問すべてに一意の正解候補。
- TRIPLE TURNの18問すべてでBFSによる到達可能性・最短手数の検証。
- ONE EXPERIMENTの18問すべてで全候補を区別できる入力。
- FLOW SPLITTERの18問すべてに正解となるスイッチ設定。
- 320px幅でページ全体の横はみ出しなし。

## ラボ版について

v1は知的なゲーム性を公平に評価するための試作です。世界最高水準の完成を保証するものではありません。特にFLOW SPLITTERの合流順序は左の経路が先という固定ルールです。実際のiPhone Safariの操作感・音質は実機での確認が必要です。

既存のDIFF. MASTER 500リポジトリは変更しません。
