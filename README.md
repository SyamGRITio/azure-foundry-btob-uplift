# BtoB大企業のAI投資はAzureへ／単価を上げる業務AI構築の最新ガイド

しゃま作成 ／ 2026年5月公開

---

## このリポジトリは何か

公式LINE登録特典として配布する、無料配布資料 #3 のGitHub Pagesソースです。

- **メインページ**：`index.html`（単一ファイル、CSSはインライン）
- **画像素材**：`assets/`（pixel retro テイストの夕日バナー、表紙、街並みフッター、キャラクターアイコン）
- **構成図**：`assets/diagram_*.drawio`（Azure公式アイコン使用）

---

## デプロイ手順

### 1. GitHub Pagesでホスティング

```bash
# このフォルダの中身を、新規GitHubリポジトリにpush
git init
git add .
git commit -m "initial commit"
git branch -M main
git remote add origin git@github.com:<ユーザー名>/<リポジトリ名>.git
git push -u origin main
```

リポジトリの **Settings → Pages → Source** で `main / root` を指定すると、`https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます。

### 2. 独自サブドメインを使う場合（任意）

`syam-gritio.com` 配下で配信したい場合は、ルートに `CNAME` ファイルを置き、ドメインのDNSにCNAMEレコードを追加してください。

---

## 構成図について

### 埋め込み方法

`index.html` 内では `viewer.diagrams.net` のJSビューワーを使って、`.drawio` のXMLをそのままインラインで描画しています。GitHub Pages公開時、追加の操作は不要です。

### 図を編集したい場合

1. `assets/diagram_foundry.drawio` または `assets/diagram_family_ai.drawio` を [draw.io](https://app.diagrams.net) で開く
2. 編集して保存（同じファイルパスで上書き）
3. push すると自動で更新されます

### 静的SVG/PNGとして埋め込みたい場合（任意）

埋め込み速度を上げたい場合は、draw.ioで `ファイル → エクスポート → SVG（または PNG）` で書き出し、`assets/` に配置。`index.html` の `<div class="mxgraph">` 部分を `<img src="assets/diagram_foundry.svg">` に差し替えてください。

---

## 画像素材について

| ファイル | 用途 | 元データ |
|---|---|---|
| `cover_main.png` | 表紙ヒーロー画像 | Nano Banana 生成・Geminiアイコン除去済み |
| `banner_sunset.png` | イントロ後の区切りバナー | 同上 |
| `banner_skyline.png` | フッター上の街シルエット | 同上 |
| `character_syama.png` | しゃまアイコン（透明背景） | vanceai版を黒背景透過処理 |

すべて pixel art テイストで統一しています。Geminiの透かしアイコン（✦）は除去済みです。

---

## ページ構成

1. ヒーロー（表紙画像）
2. FREE GUIDE イントロ＋著者プロフィール
3. **No.01** なぜBtoB大企業のAI投資はAzureなのか／本資料で得られるもの
4. **No.02** Azure AIの全体像 ─ Microsoft Foundryで何ができるか（**★図1**）
5. **No.03** Azureならではの装備（閉域・認証・監視）
6. **No.04** BtoB業務AIで使われている機能・ユースケース（単価メッセージ）
7. **No.05** アプリ構成パターン（ホスティング選択肢）
8. **No.06** 自分で試す最小構成（ハマりポイント付き）
9. **No.07** 実例：家族用AIエージェント（**★図2＋Loom動画＋月額表**）
10. **No.08** キャッチアップ術＋次の一歩（既存PDF #1への動線・一言）
11. フッター（街シルエット → HANDS-ON TIPS → CONTACT → 著者プロフィール → 奥付）

---

## 連絡先

- **公式LINE**：登録特典付き
- **X (DM)**：[@syam_nihick](https://x.com/syam_nihick)
- **Web**：[syam-gritio.com](https://syam-gritio.com)
