# 2.5.1 インテグレーションを作成する

1. **【インテグレーション】**&#x30E1;ニューをクリックします。

<figure><img src="../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

2. **【インテグレーション作成】**&#x30DC;タンをクリックします。

<figure><img src="../../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>



3. インテグレーションカードをクリックしてインテグレーションを作成します。例えば、使用するモニタリングツールが**AWS CloudWatch**の場合、**AWS CloudWatch**カードをクリックします。

<figure><img src="../../.gitbook/assets/image (276).png" alt=""><figcaption></figcaption></figure>



4. インテグレーション作成画面が次の通り表示されます。

<figure><img src="../../.gitbook/assets/image (278).png" alt=""><figcaption></figcaption></figure>

* **インテグレーション入力項目**

| 項目               | 説明                     |
| ---------------- | ---------------------- |
| **インテグレーション名**   | ユーザーがインテグレーション名を設定します。 |
| **インテグレーションタイプ** | 選択した対象のロゴが表示されます。      |



## **新規サービス作成の場合**

インテグレーション作成時、サービスも同時に作成されます。新規サービス作成画面でインテグレーションを作成できます。

設定方法は通知を受けるサービスを新規登録するとき：サービスを追加するのサービス作成方法と同じです。



## **サービス選択の場合**

インテグレーション作成時、既存サービスがマッピングされます。

<figure><img src="../../.gitbook/assets/image (279).png" alt=""><figcaption></figcaption></figure>



1. 基本サービスルールを選択します。



2. 【ユーザー設定条件追加】のチェックボックスを有効化して、条件項目(アラートのまとめ、アラートメトリック名)を設定します。設定時に基本ルールより優先的に適用されます。



3. 名前を入力してサービス作成または選択後、**【確認】**&#x30DC;タンをクリックすると次の通り表示されます。

<figure><img src="../../.gitbook/assets/image (280).png" alt=""><figcaption></figcaption></figure>

4. URLの場合、SNS(Simple Notification Service)とAlertNowを接続するためのSNS Webhook URL情報をコピーしてください。
