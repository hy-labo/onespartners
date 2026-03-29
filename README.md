# hy_labo Website

## GitHub Pagesへのデプロイ手順

### 1. GitHubリポジトリを作成する
1. GitHubにログイン（アカウントがなければ作成）
2. 新しいリポジトリを作成
   - Repository name: `hy-labo` （任意）
   - Public に設定
   - 「Create repository」をクリック

### 2. ファイルをアップロードする
```bash
cd hy-labo-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/hy-labo.git
git push -u origin main
```

### 3. GitHub Pagesを有効化する
1. リポジトリの「Settings」タブを開く
2. 左メニューの「Pages」をクリック
3. Source を「Deploy from a branch」に設定
4. Branch を「main」「/ (root)」に設定
5. 「Save」をクリック
6. 数分後に `https://YOUR_USERNAME.github.io/hy-labo/` で公開される

---

## お問い合わせフォームの設定（Formspree）

1. https://formspree.io でアカウント作成（無料）
2. 「New Form」を作成
3. 表示されるエンドポイントURL（例：`https://formspree.io/f/abcdefgh`）をコピー
4. `contact.html` の以下の部分を書き換える：
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
   ↓
   ```html
   action="https://formspree.io/f/abcdefgh"
   ```

---

## ファイル構成

```
hy-labo-website/
├── index.html     トップページ
├── about.html     プロフィールページ
├── service.html   サービス詳細ページ
├── column.html    コラム・発信ページ
├── contact.html   お問い合わせページ
├── css/
│   └── style.css  スタイルシート
└── README.md      このファイル
```
