# 1.EC2インスタンス編
https://ap-northeast-1.console.aws.amazon.com/ec2/home?region=ap-northeast-1#Instances:

## 名前とタグ
- 『名前』:【Minecraft_Server】

![](https://storage.googleapis.com/zenn-user-upload/43bd8af615ef-20230922.png)  

## アプリケーションおよび OS イメージ (Amazon マシンイメージ)
- 『クイックスタート』:【Amazon Linux】
- 『Amazon マシンイメージ(AMI)』:【Amazon Linux 2 AMI (HVM) - Kernel 数字 SSD Volume Type】
- 『アーキテクチャ』:【64 ビット (x86)】

![](https://storage.googleapis.com/zenn-user-upload/ced00d8d835c-20230922.png)  

## インスタンスタイプ
- 『インスタンスタイプ』:【t3.large】

![](https://storage.googleapis.com/zenn-user-upload/77b267da7f3d-20230922.png)  

## キーペア(ログイン)
- 初回はキーペアを作成する
- 【新しいキーペアの作成】をクリック

![](https://storage.googleapis.com/zenn-user-upload/09bd553f8d38-20230922.png)  

- 『キーペア名』: [Minecraft-key]
- 『キーペアのタイプ』:【RSA】
- 『プライベートキーファイル形式』: 【.pem】

![](https://storage.googleapis.com/zenn-user-upload/ddf9a8b5f793-20230922.png)  

- 上記で作成したキーペアが記載されているかを確認

![](https://storage.googleapis.com/zenn-user-upload/958c96b8fda5-20230922.png)  

# ネットワーク設定
![](https://storage.googleapis.com/zenn-user-upload/d0c1eb1579b0-20230922.png)

- 『VPC - 必須』:【Minecraft-vpc】
- 『サブネット』:【Minecraft-subnet-public1-ap-northeast-1a】
- 『パブリック IP の自動割り当て』:【有効化】

ファイアウォール(セキュリティグループ)
- 【セキュリティグループを作成する】を選択
- 『セキュリティグループ名 - 必須』: [Minecraft-SG]
  - 『説明 - 必須』: [Minecraft-SG]

![](https://storage.googleapis.com/zenn-user-upload/8c1eadb4e60d-20230922.png)  

ファイアウォール(セキュリティグループ)

- 【セキュリティグループを作成する】を選択
- 『セキュリティグループ名 - 必須』: [Minecraft-SG]
- 『説明 - 必須』: [Minecraft-SG]

![Alt text](image-2.png)

セキュリティグループルール1
- ①『ソースタイプ』: 【自分の IP】
- ②【セキュリティグループルールを追加】をクリック

セキュリティグループルール 2
- ③『ポート範囲』: [25565]
- ④『ソースタイプ』:【任意の場所】

![Alt text](image-3.png)

# ストレージを設定
[10] と入力し､【gp3】を選択します｡
![Alt text](image-4.png)

# 概要
『インスタンス数』が [1] となっている事を確認し､【インスタンスを起動】をクリックします｡

![Alt text](image-5.png)

- 画面上部にて､『成功』と表示されていることを確認し､その後に【すべてのインスタンスを表示】をクリックします｡

![Alt text](image-6.png)


- ※t3.midiumで起動すると動きません

![Alt text](image-8.png)