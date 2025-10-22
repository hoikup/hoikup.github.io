# CLAUDE.md

### 🪄 プロジェクト概要
**HoikUp（ほいくあっぷ）** は、保育士さんが **保育アイデアを探して・シェアできるアプリ** です。  
このLPは、アプリのコンセプトを紹介しながら、リリース前の **事前登録（LINE公式アカウント登録）** を目的としています。

---

### 🎯 目的
- HoikUpアプリのコンセプトと世界観を紹介  
- 保育士が「使ってみたい」と感じる期待感を醸成  
- アプリリリースに向けて **LINE公式アカウントへの登録** を促す  

---

### 🧩 ページ構成

0. **ヘッダー（固定）**
   - ロゴ画像：`img/Logo.png`（左上）
   - ロゴサイズ：PC 40px高さ / スマホ 32px高さ
   - 事前登録ボタン：青色（#6DADE3）、右上配置
   - 固定ヘッダー（スクロール追従）、半透明白背景 + backdrop-blur

1. **ヒーローセクション**
   - キービジュアル：`img/women.jpg`
   - タイトル：「HoikUp」（Poppinsフォント、#FFC5D0）
   - キャッチコピー：「明日の保育が、もっと楽しくなる。」
   - サブコピー：「保育士が『明日』もっとワクワクするアプリ。毎日の保育に、すこしの『あっぷ』を届けます。」
   - 背景：パステルグラデーション（#FDF6F0 → #FFF9F9 → #FFC5D0）
   - グラデーション円×2（blur効果）
   - メインCTAボタン：「事前登録はこちらから（LINEアプリ）」 → `https://lin.ee/pg7pZQL`

2. **画面イメージセクション（カルーセル）**
   - モックアップ3画面：`img/mock1.png`, `img/mock2.png`, `img/mock3.png`
   - カルーセル幅：PC 320px / スマホ 280px（縦長スマホに最適化）
   - フェードアニメーション：0.8秒
   - 自動再生：5秒間隔
   - 前後ボタン + ドットインジケーター
   - キャプション：「※開発中のイメージです」
   - 説明文：「HoikUp（ほいくあっぷ）は、保育アイデアを探して・シェアできるアプリです。製作・遊び・行事…あなたの工夫が、誰かの助けになります。」

3. **特徴セクション01 - こんなお悩みありませんか？**
   - 番号：「01」（大きく表示、#FFC5D0）
   - 画像：`img/introduction01.png`（左配置、400px高さ/300px@mobile、object-fit: cover）
   - 悩みリスト×4項目

4. **特徴セクション02 - HoikUpでできること**
   - 番号：「02」
   - 画像：`img/introduction02.png`（右配置）
   - 機能説明：検索/投稿/保存/共有（絵文字付き）

5. **特徴セクション03 - 使うメリット**
   - 番号：「03」
   - 画像：`img/introduction03.png`（左配置）
   - メリットリスト×4項目

6. **4つの便利機能**
   - 見出し：「4つの便利機能」
   - 4カラムグリッド（スマホ2カラム）
   - 各カード：白背景、角丸、シャドウ
   - 画像：正方形（aspect-ratio 1:1、object-fit: cover）
     - SEARCH：`img/feature1.jpg`
     - SAVE：`img/feature2.jpg`
     - POST：`img/feature3.jpg`
     - SHARE：`img/feature4.jpg`

7. **問い合わせ / SNSリンクセクション**
   - 見出し：「お問い合わせ」
   - Instagramリンク：`https://www.instagram.com/hoikup_official/`
   - アイコン：`img/Instagram_Glyph_Gradient.svg`
   - アカウント名：@hoikup_official
   - サブテキスト：「DMにてお問い合わせください。」
   - 背景：#FFF9F9

8. **フッター**
   - コピーライト：Copyright 2025 HoikUp. All Rights Reserved.  

---

### 🎨 デザイン要件
- **カラーパレット**
  - ベースカラー：#FDF6F0（ベージュ系）
  - アクセントカラー：#FFC5D0（ピンク）
  - 補助カラー：#FFF9F9、#D6A7B4（淡ピンクブラウン）
  - CTAボタン：#6DADE3（青）
- **フォント**
  - 日本語：Noto Sans JP
  - 英字タイトル：Poppins
- **UI要素**
  - ボタン・カードは角丸（16px〜24px）
  - シャドウは柔らかく薄め（自然光を意識）
  - セクション間の余白を広くとり、清潔感を重視
- **アニメーション**
  - スクロール時フェードイン（Intersection Observer使用）
  - ボタンホバー時に軽いスケールアップ（1.02倍）
  - カルーセルフェード効果（0.8秒、ease-in-out）
- **画像処理**
  - イントロ画像：object-fit: cover で統一比率
  - 機能カード画像：aspect-ratio 1:1 で正方形化
  - モックアップ画像：縦長スマホ比率を維持  

---

### ⚙️ 実装要件
- 使用技術：HTML + Tailwind CSS (CDN) + JavaScript
- レスポンシブ対応（スマホ中心）
- メールフォームは設置しない
- **実際のURL**
  - LINE公式アカウント：`https://lin.ee/pg7pZQL`
  - Instagram：`https://www.instagram.com/hoikup_official/`
- GA4タグは `<head>` 内に挿入
- 軽量なフェードインアニメーションをJSまたはCSSで実装

### 📁 画像アセット
- `img/Logo.png` - ヘッダーロゴ
- `img/women.jpg` - ヒーローセクション背景
- `img/mock1.png`, `img/mock2.png`, `img/mock3.png` - アプリモックアップ
- `img/introduction01.png`, `img/introduction02.png`, `img/introduction03.png` - 特徴セクション画像
- `img/feature1.jpg`, `img/feature2.jpg`, `img/feature3.jpg`, `img/feature4.jpg` - 機能カード画像
- `img/Instagram_Glyph_Gradient.svg` - Instagramアイコン  

---

### 📊 Google Analytics（GA4）要件
- GA4のトラッキングコードを `<head>` 内に埋め込む  
- 計測IDは変数として扱う（例：`G-XXXXXXXXXX`）  
- 例：
```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
