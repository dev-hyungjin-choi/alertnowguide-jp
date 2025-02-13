# 3.3.1 ユースケース 1. サービスメニューで作成

1. **【サービス】**&#x30E1;ニューをクリックします。

<figure><img src="../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>



2. **【サービス作成】**&#x30DC;タンをクリックします。

<figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>



3. サービス作成ページで必要な項目を入力します。

<figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

| 項目          | 説明                                                                                                                                                                                    | 備考        |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| サービス名       | 顧客が作成しようとするサービス名を任意に入力します。                                                                                                                                                            | 必須入力事項    |
| エスカレーションルール | <p>•エスカレーション基本ルール</p><p><br></p><p>作成されたエスカレーションルールがない場合、「エスカレーション基本ルール」が作成されます。</p>                                                                                                  | 必須入力事項    |
| インシデント作成ルール | <p>• 作成制限ルール</p><p></p><p>条件項目(Alert Summary, Alert Metric Name)が </p><p>連続して発生する場合、秒/分/時/日を設定してインシデントの重複作成を防止できます。</p><p></p><ul><li>緊急度設定</li></ul><p>インシデントの緊急度を設定できます。</p><p></p> | オプション入力事項 |



## **作成されたサービス選択**

1. 作成されたサービスをクリックすると、次のような画面に移動します。

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

| 項目              | 説明                          | 備考   |
| --------------- | --------------------------- | ---- |
| **インシデント**      | 期間及び検索条件によるインシデント状態を確認できます。 |      |
| **インテグレーション**   | 該当サービスのインテグレーション情報を確認できます。  |      |
| **エスカレーションルール** | 該当サービスのエスカレーション情報を確認できます。   | 修正可能 |
| **インシデント作成ルール** | 該当サービスのインシデント作成ルールを確認できます。  | 修正可能 |
| **エクステンション**    | 該当サービスのエクステンション情報を確認できます。   | 修正可能 |
| **メンテナンス履歴**    | メンテナンス日程の追加、削除などの履歴を確認できます。 |      |



2. **ルーティングルール**タブで【+新規ルールの追加】ボタンをクリックして**ルーティングルール**のポップアップウィンドウを開きます。**ルーティングルール**がない場合は、自動でルーティング基本ルールが作成されます。サービスの作成者がデフォルトの受信者に設定されます。

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>



3.  **ルーティング条件**を選択して、受信するアラーム条件を設定します。例えば、**Metric Name**と**Contains**を条件として選択し、比較する値としてCPUを設定した場合、上記の条件に当てはまる場合のみアラームとして受信することができます。

    \
    ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdyL7pBpWzGS_afb1jW4XCIdeXqVF5xPRPbbSdaZGX4VBADWumWKrox7xg8HtxEF8fG-IS2dzb_l-sfidZlmfuUAnzN89kDlbyKR4Xomv7cSqgnCP9YErJs0juwKEQBFzKHcyvuZAWT27AQA82m8B_XDsg?key=0Xa7fMJhbTOfjN6ztS0Ywg)



●   インテグレーション別のマトリックス名

| **インテグレーション名**                | **マトリックス名**                                                                                | **備考**                                                                                                                                                               |
| ----------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Amazon Cloudwatch             | trigger.metricName                                                                         | <p><br></p>                                                                                                                                                          |
| Azure Alerts                  | context.condition.metricName                                                               | <p><br></p>                                                                                                                                                          |
| Azure Alerts(Classic)         | context.condition.metricName                                                               | <p><br></p>                                                                                                                                                          |
| CA UIM(OpsNow MD)             | metricName                                                                                 | <p><br></p>                                                                                                                                                          |
| Datadog                       | alertMetric                                                                                | <p><br></p>                                                                                                                                                          |
| Stackdriver                   | incident.condition\_name                                                                   | <p><br></p>                                                                                                                                                          |
| Prometheus                    | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| NewRelic                      | condition\_name                                                                            | <p><br></p>                                                                                                                                                          |
| Jennifer5                     | metricsName                                                                                | <p><br></p>                                                                                                                                                          |
| Grafana                       | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Sumo Logic                    | alertMetric                                                                                | <ul><li>Type Payloadの場合、searchQueryフィールドにメトリック値を抽出してalertMetric値として使用(ユーザーがクエリにメトリック値を入力して使用可能)</li></ul><p> </p><ul><li>Log Type Payloadの場合は使用しない</li></ul>         |
| SAMS                          | ALM\_CD\_ID                                                                                | <p><br></p>                                                                                                                                                          |
| Nagios                        | alertMetric                                                                                | <ul><li>Service Type Payloadの場合、serviceDescフィールドの値をalertMetricの値として使用</li></ul><p> </p><ul><li>Service Type Payloadの場合、hostStateフィールドの値をalertMetricの値として使用</li></ul> |
| Standard                      | metric\_name                                                                               | <p><br></p>                                                                                                                                                          |
| Kapacitor                     | id                                                                                         | <p><br></p>                                                                                                                                                          |
| SAMBA                         | metric\_name                                                                               | <p><br></p>                                                                                                                                                          |
| Dynatrace                     | metricNm                                                                                   | <ul><li>problemDetailsJson.rankedEventsの初のIndexデータのうち、entityName-ImpactLevel-EventTypeの形で結合してmetricNmで使用</li></ul>                                                   |
| Elasticsearch Watcher         | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Scouter                       | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Email                         | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Amazon Guard Duty             | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Consul                        | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Jennifer4                     | Fields excluding some key types: groupType, errorType, agentname, ipaddr, msg, value, type | 重複するKey形式のメトリックを除くフィールド                                                                                                                                              |
| WhaTap                        | metricName                                                                                 | 必須値ではない                                                                                                                                                              |
| Zenius                        | metric\_name                                                                               | <p><br></p>                                                                                                                                                          |
| Niffler                       | metric\_name                                                                               | <p><br></p>                                                                                                                                                          |
| ZMON                          | metric\_name                                                                               | <p><br></p>                                                                                                                                                          |
| Zabbix                        | subject                                                                                    | <p><br></p>                                                                                                                                                          |
| Tencent                       | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| AWS Personal Health Dashboard | detail.eventTypeCode                                                                       | <p><br></p>                                                                                                                                                          |
| CheckMK                       | SERVICEDESC                                                                                | <ul><li> Service Type Payloadの場合、SERVICEDESCフィールドの値をalertMetricの値として使用</li></ul><p> </p><ul><li>Host Type Payloadの場合、HOSTSTATEフィールドの値をalertMetricの値として使用</li></ul>   |
| Jira Service Management       | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Freshdesk                     | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| EventBridge                   | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| OpsNow                        | metric\_name                                                                               | <p><br></p>                                                                                                                                                          |
| Jira Software                 | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
| Azure Monitor Common Alerts   | <p><br></p>                                                                                | <p><br></p>                                                                                                                                                          |
