# TCG Collection note

## 置くファイル（リポジトリの直下）
- `index.html` … アプリ本体
- `data/poke.json` … ポケモンのカード一覧（最初は空。Actionsが自動で埋めます）
- `scripts/fetch-poke.mjs` … データ取得スクリプト（TCGdexの日本語データ）
- `.github/workflows/update-data.yml` … 毎週日曜に自動更新

## 手順
1. 上のファイルをリポジトリに追加（GitHubの Add file → Create new file で、パスを入力して中身を貼り付け）
2. Settings → Pages → Branch を `main` / `/ (root)` にして Save
3. Actions タブ → `update-card-data` → Run workflow（初回のデータ取得）
4. 数分後、`data/poke.json` にデータが入ります。Pages のURLでアプリを開く
5. 旧URLのデータは引き継がれないので、旧アプリで「その他→バックアップ」→新URLで「復元」

## 使い方
カード登録でジャンルを「ポケモン」にして、カード名か番号を入力すると候補が出ます。
タップすると、名前・番号・パック名・画像が入ります。
