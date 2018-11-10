# AWS lambdaを使ってAWSの料金をslackに通知する

### lambda-uploaderのインストール

```
pip install lambda-uploader
```

### awscliのインストール

```
pip install awscli
```

### credential/regionの設定

- aws configureで設定する場合
```
aws configure
>> AWS Access Key ID [****************IT2Q]: hoge
>> AWS Secret Access Key [****************6uEx]:fuga
>> Default region name [ap-northeast-1]:piyo
```

- `~/.aws`以下の`config`と`credential`を直接書き換える
```
cd ~/.aws
vi config
vi credentials
```

### ディレクトリ/ ファイル構成


```
awscost_to_slack/
|--lambda_function.py
|--requirements.txt
|--lambda.json
```

### デプロイ

```
cd awscost_to_slack
lambda-uploader　　--profile profile_name
Î» Building Package
Î» Uploading Package
Î» Fin
```

