# 大阪たこ焼き屋 — デモサイト

Claude Design で作成したデザイン（`大阪たこ焼き屋.dc.html`）を、そのまま公開できる静的Webサイト（HTML / CSS / Vanilla JS）として実装したものです。

## 構成

```
demo_012/
├── index.html        … サイト本体（1ファイル完結・依存ライブラリなし）
├── assets/           … 画像（たこ焼き写真）
│   ├── takoyaki-hero.jpg
│   ├── takoyaki-making.jpg
│   ├── takoyaki-wood.jpg / mayo / nori / aonori / wood2 / closeup .jpg
├── .nojekyll         … GitHub Pages 用
└── README.md
```

## 特長

- **1ファイル完結**：`index.html` を開くだけで動作します。ビルド不要・フレームワーク不要。
- **レスポンシブ対応**：PC / タブレット / スマホに対応。920px以下でハンバーガーメニューに切り替わります。
- **インタラクション**：
  - ヘッダー追従＋ページ内スムーズスクロール（固定ヘッダー分のオフセット込み）
  - モバイルメニューの開閉
  - お問い合わせフォームの送信完了表示（デモのため実送信はしません）
  - 提灯のゆらぎ／流れる帯／フェードインなどのアニメーション
- **フォント**：Google Fonts（Yuji Syuku / RocknRoll One / Zen Maru Gothic）

## ローカルで確認する

`index.html` をブラウザで直接開くだけでOKです。簡易サーバーで確認する場合：

```bash
cd demo_012
python -m http.server 8000
# → http://localhost:8000 を開く
```

## 公開（GitHub Pages）

リポジトリの **Settings → Pages → Build and deployment → Source: Deploy from a branch** で
`main` ブランチ・`/ (root)`（または `/demo_012`）を選択すると公開できます。

## 画像について

メニューやヒーローの写真は、本プロジェクトに同梱されていたたこ焼き写真を
Web表示用に最適化（リサイズ・JPEG圧縮）して `assets/` に配置しています。
別の写真に差し替える場合は、`assets/` 内の同名ファイルを上書きするだけでOKです。

> 文章・価格・住所・電話番号などは仮の内容です。実際の店舗情報に差し替えてご利用ください。

---
🤖 Generated with [Claude Code](https://claude.com/claude-code)
