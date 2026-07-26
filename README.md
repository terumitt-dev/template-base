# template-base

新規リポジトリ作成時のベーステンプレート。

## 使い方

1. このリポジトリをベースに新規リポジトリを作成
2. `.drone.yml` の `ECR_REPO` を対象リポジトリ用に設定
3. `steps:` に `build` / `deploy` ステップを追加

## CI/CD

Drone CI（drone-runner-kube）を使用。パイプラインの基本構成（変数チェック）のみ定義済み。

| Secret | 用途 |
|---|---|
| `AWS_REGION` | AWS リージョン |
| `AWS_ACCESS_KEY_ID` | AWS 認証 |
| `AWS_SECRET_ACCESS_KEY` | AWS 認証 |
| `ECR_REPO` | ECR リポジトリ名（各 repo で設定） |
