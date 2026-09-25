# 🗾 日本地図クイズ — Japan Map Quiz

**47都道府県を楽しく覚えられる、ブラウザで遊べる地図クイズアプリです。**
日本語・English・Русский の3言語に対応しています。

▶ **プレイする：https://urmatkursan.github.io/JapanQuizgame/**

![スクリーンショット](screenshot.png)

---

## ✨ 主な機能

### 🎮 2つのゲームモード
- **4択クイズ**：地図で赤くなっている県の名前を4つの選択肢から選ぶ
- **地図で探す**：表示された県名を見て、地図上の正しい県をクリックする

### 📍 地域クイズ
全国のほか、北海道・東北／関東／中部／近畿／中国・四国／九州・沖縄から出題範囲を選べます。
地域を選ぶと地図がその地域に自動でズームし、選択肢も同じ地域から出題されます。

### 🎯 苦手モード（アダプティブ学習）
プレイヤーごとに県別の正解・不正解を記録し、間違えた県ほど多く出題します。

### 🗺️ 地図で学ぶ（学習モード）
- 県をクリックすると、県庁所在地・地方・豆知識・自分の成績を表示
- **進捗マップ**：自分の正答率で県を色分け（🟩 得意／🟨 まあまあ／🟥 苦手／⬜ 未出題）

### 🏆 ゲーム要素
- **実績（11種類）**：パーフェクト、10問連続正解、47都道府県コンプリートなど
- **連続正解（ストリーク）**：🔥 → ⚡ バッジ表示
- **制限時間**：4択は15秒、地図モードは20秒
- **ヒント**：かんたん1回／ふつう2回／むずかしい3回（1ゲームあたり）
- 正解時の効果音と紙吹雪

### 📊 結果と記録
- 地域別の正答率グラフ
- プレイ履歴（同じ名前のプレイヤーは1人としてまとめて集計）

### 🎨 そのほか
- 🌙 ダークモード（設定を保存）
- 📱 スマートフォン対応のレスポンシブデザイン

---

## 🛠 使用技術

| 分類 | 技術 |
|---|---|
| 言語 | HTML / CSS / JavaScript（フレームワークなし） |
| 地図の描画 | [D3.js](https://d3js.org/) v7、[TopoJSON](https://github.com/topojson/topojson) |
| 地図データ | [jpn-atlas](https://www.npmjs.com/package/jpn-atlas)（都道府県の境界データ） |
| 効果音 | Web Audio API（音声ファイルを使わずに生成） |
| データ保存 | localStorage（履歴・実績・県別成績・テーマ設定） |
| デザイン | CSS変数によるテーマ切り替え、Google Fonts（Noto Sans JP / Space Grotesk） |
| 公開 | GitHub Pages |

## 💡 工夫した点

- **アダプティブ出題**：県ごとの成績から重みを計算し、苦手な県が出やすくなるようにしました（重み付きランダム抽出）。
- **地域ズーム**：D3で選んだ地域の範囲を計算してSVGのviewBoxを変更し、小さな県もクリックしやすくしました。
- **多言語対応**：UIの文字列を1つのオブジェクトにまとめ、ページを再読み込みせずに言語を切り替えられます。
- **1ファイル構成**：index.html だけで動くので、インストール不要で誰でもすぐに遊べます。

## 🚀 ローカルで動かす方法

```bash
git clone https://github.com/urmatkursan/JapanQuizgame.git
```

`index.html` をブラウザで開くだけで動きます（地図データの読み込みにインターネット接続が必要です）。
VS Code の Live Server で開くのがおすすめです。

## 👤 作者

**Mamataliev Urmatbek**
早稲田文理専門学校 アプリ・Web制作学科 2年
卒業制作（2026年）

---

## 🌐 English

**Japan Map Quiz** is a browser game for learning all 47 prefectures of Japan. It's available in Japanese, English and Russian.

**Features:** two game modes (multiple choice and find-on-map), region quizzes with automatic map zoom, an adaptive "weak spots" mode that asks more of the prefectures you get wrong, a study map with a personal progress heatmap, 11 achievements, answer streaks, a timer, hints, region statistics, per-player history, dark mode and a responsive layout.

**Built with** vanilla HTML/CSS/JavaScript, D3.js, TopoJSON, the Web Audio API and localStorage. No framework, and everything is in a single `index.html`.

Graduation project by Urmat, Waseda Bunri College (App & Web Development), 2026.
