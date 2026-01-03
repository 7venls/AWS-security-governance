# AWSサービスの全体像

・AWSのサービスは大きくカテゴリ分けされている。

## Compute(処理・計算)

・プログラムを動かす。

#### 代表サービス

・EC2：仮想サーバ

・Lambda：サーバレス処理

#### 実務イメージ

・Webサーバ

・バッチ処理

・APIの実行

## Storage（保存）

・データを保存する。

S3, EBS - データを保存

### Database（データ管理）

・データを構造的に管理する。

RDS, DynamoDB - データベース管理

### Networking（繋ぐ）

・通信の道を作る。

VPC, Route53 - ネットワーク構築


### Security（守る）

・誰が何をできるかを制御する。

IAM, KMS, CloudTrail - 認証・アクセス管理、監査

### Management（運用）

CloudWatch, CloudFormation - 監視や自動化
