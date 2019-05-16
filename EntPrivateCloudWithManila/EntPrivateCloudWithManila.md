# 企業プライベートIaaS ファイル共有サービス(CephFS NFS-ganesha) 構成

## 概要

このクラウドデザインターンでは、Red Hat OpenStack Platformのプライベートクラウドユースケースを想定た標準的な構成方法をしめします。加えて、CephFS NFS-Ganesha をバックエンドとしたファイ共有サービスを有効化する方法をまとめます。

* プライベートクラウドの具体的なユースケース
  * クラウド利用者は、OpenStack 上に、クローズドのプライベートネットワークが作成できる。
  * 各クラウド利用者が作成したネットワークのIPアドレス空間は、個々のプライベートネットワーク間で干渉しない。
  * クラウド利用者は、OpenStack 上に、ゲストVMを起動できる。
  * ゲストVMは、Floating IP を介して、外部のネットワークと相互通信でき、その通信は、ポートレベルで制御できる。
  * クラウド利用者は、ゲストVMを、予め用意されたゲストOSイメージから起動できる。ゲストOSのイメージは利用者でも登録できる。
  * クラウド利用者は、ゲストVMのキャパシティを自由には設定できないが、予め用意されているカタログ（flavor) から、要件に近いものを選択して利用することができる。
  * クラウド利用者は、ゲストVMに対して、拡張のストレージ領域を接続できる。
  * クラウド利用者は、オブジェクトストアサービスを利用して、クラウド環境上にファイルのアップロードし、その他のユーザに対して公開できる。
  * *** ゲストインスタンス間で、ファイル共有サービスを利用できる。 ***

![ユースケースイメージ](./images/Img0000.png "ユースケースのイメージ")
### * [計画／設計編](./design/design.md)

### * [構築／実装編](./build/build.md)