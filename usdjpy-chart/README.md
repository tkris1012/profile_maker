# USD/JPY チャート（iPhone縦画面用ブラウザアプリ）

- 上半分：ローソク足（M1 / M5 / M15 / M30 / H1 / H4 / D1 を切り替え、足の確定までの残り時間を表示）
- 下半分：ティックチャート（直近3000ティック、Bid/Ask、1分あたりのティック数）
- 時刻はすべて日本時間

## データソース（⚙︎ から切り替え）
| モード | ティック | 過去足 | 必要なもの |
|---|---|---|---|
| デモ | 擬似データ | 擬似データ | なし |
| Twelve Data | WebSocket | REST（時間足ごとに1回） | Twelve Data APIキー |
| Finnhub | WebSocket（OANDA:USD_JPY） | Twelve Dataのキーがあれば REST、なければティックから作成 | Finnhub APIキー |

APIキーは端末のブラウザ内（localStorage）にだけ保存されます。

## 使い方
`index.html` と `lightweight-charts.standalone.production.js` を同じ場所に置いて、HTTPSで配信してください（GitHub Pages など）。
iPhoneのSafariで開き、「共有 → ホーム画面に追加」で全画面アプリとして使えます。

チャートは TradingView Lightweight Charts™ v5.3.0（Apache License 2.0）を使っています。
