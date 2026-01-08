# RDS 構築

## 構成概要

- VPC：study-vpc

- Subnet：Private Subnet

- DB：Amazon RDS (MySQL)

---

## RDSを選択した理由

- DBのパッチ・バックアップをAWSに任せるため。

- EC2でのDB運用は管理コスト・事故リスクが高いため。

---

## なぜ Private Subnet に配置したか（ネットワーク設計の考え方）

- DBは人が直接アクセスするものではない。

- Publicに配置すると攻撃対象になる。

- EC2経由のみで利用するためPrivate Subnetに配置。

---

## セキュリティ設定

- Public Access：無効

- Security Group：

- Inbound：MySQL(3306) from EC2 Security Group only

ポイント：SG → SG 許可。

---

## 確認内容

- RDSにPublic IPが付与されていないこと。

- Private Subnetに配置されていること。

- EC2以外から接続できないこと。

---

## 想定されるリスク

- セキュリティグループを0.0.0.0/0で開けると不正接続の恐れ

- Public Subnetに配置すると即セキュリティ指摘対象

