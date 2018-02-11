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

test

##参照コマンド
・EC2
aws ec2 describe-tags --filters "Name=resource-type,Values=instance"

・ルートテーブル
aws ec2 describe-tags --filters "Name=resource-type,Values=route-table"

・インターネットゲートウェイ
[ec2-user@ip-10-0-62-116 ~]$ aws ec2 describe-tags --filters "Name=resource-type,Values=internet-gateway" "Name=key,Values=Name" --output table

・スナップショット
[ec2-user@ip-10-0-62-116 ~]$ aws ec2 describe-tags --filters "Name=resource-type,Values=snapshot" "Name=key,Values=Name" --output table

・ENI
aws ec2 describe-tags --filters "Name=resource-type,Values=network-interface" "Name=key,Values=Name" --output table

・VPN-GW
aws ec2 describe-tags --filters "Name=resource-type,Values=vpn-gateway" "Name=key,Values=Name" --output table


