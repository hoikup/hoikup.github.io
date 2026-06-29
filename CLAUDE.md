# CLAUDE.md

### 🪄 プロジェクト概要
**HoikUp（ほいくあっぷ）** は、保育士さんが **保育アイデアを探して・シェアできるアプリ** です。  
このLPは、アプリの魅力を紹介しながら **App Storeからのアプリダウンロード** を促すことを目的としています。

---

### 🎯 目的
- HoikUpアプリのコンセプトと世界観を紹介
- 保育士が「使ってみたい」と感じる期待感を醸成
- **App Store（iOS）へのダウンロード** を最優先で促す
- Instagram（@hoikup_official）へのフォロー導線も設ける

---

### 🧩 ページ構成（上から順）

0. **ヘッダー（固定）**
   - ロゴ画像：`img/Logo.png`（左上、PC 60px高さ / スマホ 44px高さ）
   - App Storeダウンロードボタン（黒・右上）、SM以上で表示
   - 固定ヘッダー（スクロール追従）、半透明白背景 + backdrop-blur

1. **ヒーローセクション**
   - 2カラム（左: テキスト＋CTA / 右: mock1.png）
   - キャッチコピー：「毎日の保育アイデアが、ここで見つかる。」
   - サブコピー：「製作・遊び・行事のアイデアを、全国の保育士とシェアできる無料アプリ。」
   - 背景：パステルグラデーション（#FFF9F5 → #FFE5CC → #FFDCE5 → #FFD5E0）
   - メインCTA：App Storeボタン（黒・バッジ風）

2. **アプリ画面紹介（カルーセル）**
   - モックアップ3画面：`img/mock1.png`（ホーム）/ `img/mock2.png`（詳細）/ `img/mock3.png`（投稿）
   - カルーセル幅：PC 320px / スマホ 280px
   - フェードアニメーション：0.8秒 / 自動再生：5秒間隔
   - 各スライドにラベルとキャプション付き
   - AIイメージ画像のさりげない訴求テキスト
   - セクション末尾にApp StoreCTA

3. **特徴セクション01 - こんなお悩みありませんか？**
   - 画像：`img/introduction01.png`（左配置）
   - 悩みリスト×4項目（絵文字付き）

4. **特徴セクション02 - その悩み、HoikUpで解決。**
   - 画像：`img/introduction02.png`（右配置）
   - できること×5項目（チェックマーク付き）
   - セクション末尾にApp Store CTA

5. **使い方紹介（実際の画面）**
   - mock2.png（詳細画面）＋説明テキスト
   - mock3.png（投稿画面）＋説明テキスト

6. **4つの便利機能**
   - 4カラムグリッド（スマホ2カラム）
   - SEARCH / SAVE / POST / SHARE
   - 各カード：白背景、角丸、シャドウ
   - 画像：正方形（aspect-ratio 1:1）
     - SEARCH：`img/feature1.jpg`
     - SAVE：`img/feature2.jpg`
     - POST：`img/feature3.jpg`
     - SHARE：`img/feature4.jpg`

7. **利用実績（定性カード）**
   - 毎週更新 / 全国の保育士 / 全カテゴリ網羅 / ずっと無料
   - 各カードに `<!-- 数字に変更可 -->` コメントあり（後から数値に差し替え可能）

8. **毎週更新・季節特集**
   - 春夏秋冬の特集タグを表示

9. **投稿者向けメリット**
   - 画像：`img/mock3.png`（投稿画面、左配置）
   - タイトル：「アイデアを探すだけじゃない。あなたの保育も発信できます。」
   - 投稿するメリット×5項目（投稿者名表示 / Instagram・Webリンク掲載 など）
   - 「アプリで投稿してみる」App Store CTA（location: post）
   - ※断定的表現は避け「活動を知ってもらえる」等の自然な表現に統一

10. **Instagram導線**
   - アイコン：`img/Instagram_Glyph_Gradient.svg`
   - 「毎日、保育アイデアを配信中！」訴求
   - @hoikup_official フォローボタン → `https://www.instagram.com/hoikup_official/`

11. **最後のCTA**
    - 「明日の保育、もっとワクワクしよう。」
    - App Store ボタン（黒・大）

12. **フッター**
    - 利用規約（`terms/`）・プライバシーポリシー（`privacy/`）リンク
    - コピーライト：Copyright 2026 HoikUp. All Rights Reserved.

+ **モバイル固定下部CTAバー**（768px未満のみ表示）
    - App Storeボタンを常時表示
    - body に padding-bottom: 84px を付与して被りを防止

---

### 🎨 デザイン要件
- **カラーパレット**
  - ベースカラー：#FFF9F5（ベージュ系）
  - アクセントカラー（オレンジ）：#FFB366
  - アクセントカラー（ピンク）：#FFB3C5
  - 補助カラー：#FFF9F9、#FFD9A3
  - CTAボタン（App Store）：#000（黒）
- **フォント**
  - 日本語：Noto Sans JP
  - 英字タイトル：Poppins
- **UI要素**
  - ボタン・カードは角丸（16px〜24px）
  - シャドウは柔らかく薄め（自然光を意識）
  - セクション間の余白を広くとり、清潔感を重視
- **アニメーション**
  - スクロール時フェードイン（Intersection Observer使用）
  - ボタンホバー時に軽いスケールアップ（1.02〜1.03倍）
  - カルーセルフェード効果（0.8秒、ease-in-out）
- **画像処理**
  - イントロ画像：object-fit: cover で統一比率（PC 400px / スマホ 300px）
  - 機能カード画像：aspect-ratio 1:1 で正方形化
  - モックアップ画像：縦長スマホ比率を維持（max-width 280px）

---

### ⚙️ 実装要件
- 使用技術：HTML + Tailwind CSS (CDN) + JavaScript
- レスポンシブ対応（スマホファースト）
- メールフォームは設置しない
- **実際のURL**
  - App Store：`https://apps.apple.com/jp/app/hoikup/id6760159380`
  - Instagram：`https://www.instagram.com/hoikup_official/`
- App StoreボタンはすべてGA4イベント付き（`gtag('event','click_appstore',{location:'...'})`）
- GA4計測ID：`G-QZ5B6WNKS0`（`<head>` 内に挿入）

### 📁 画像アセット
- `img/Logo.png` - ヘッダーロゴ
- `img/women.jpg` - （現在未使用）
- `img/mock1.png` - ホーム画面（iPhoneモック）
- `img/mock2.png` - アイデア詳細画面（iPhoneモック）
- `img/mock3.png` - 新規投稿画面（iPhoneモック）
- `img/introduction01.png`, `img/introduction02.png`, `img/introduction03.png` - 特徴セクション画像
- `img/feature1.jpg`, `img/feature2.jpg`, `img/feature3.jpg`, `img/feature4.jpg` - 機能カード画像
- `img/Instagram_Glyph_Gradient.svg` - Instagramアイコン

---

### 📊 Google Analytics（GA4）要件
- GA4のトラッキングコードを `<head>` 内に埋め込む
- 計測ID：`G-QZ5B6WNKS0`
- 各App StoreボタンにCTAクリック計測：
```html
onclick="gtag('event','click_appstore',{location:'ボタン名'})"
```
- locationの値：`header` / `hero` / `showcase` / `solution` / `footer_cta` / `sticky_bar`
