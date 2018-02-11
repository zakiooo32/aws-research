## 目的
指定のAWSアカウントが保有しているリソースをID付きで一覧化し
csvやその他形式でエクスポートする


## 対象リソース
| リソース | リソースID |
|--------|--------|
|VPC||
|EC2||
|RDS||
|ELB||

##参照コマンド
・EC2
aws ec2 describe-tags --filters "Name=resource-type,Values=instance"

・ルートテーブル
aws ec2 describe-tags --filters "Name=resource-type,Values=route-table"
