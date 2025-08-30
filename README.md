# Twitter Auto Post via Dify + GitHub Actions

## セットアップ
1. このリポジトリを fork / clone
2. GitHub Secrets を設定:
   - `DIFY_API_KEY` : Dify の API Key
   - `DIFY_WORKFLOW_URL` : Dify Workflow の公開エンドポイント
   - `X_API_KEY` / `X_API_SECRET` / `X_ACCESS_TOKEN` / `X_ACCESS_TOKEN_SECRET` : X (Twitter) API 認証情報
3. `.github/workflows/post.yml` の cron を調整して投稿時間を決定（デフォルトは毎朝9時 JST）
4. Actions タブで `Run workflow` を押すと手動実行も可能

## 注意
- ツイート文字数は自動で 280 字以内にカット
- 投稿ログは GitHub Actions の実行結果で確認
- 画像付きツイートは別途メディアAPIを組み込む必要あり
