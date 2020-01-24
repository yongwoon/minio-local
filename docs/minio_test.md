# TEST MINIO

* set minio via awscli

AWS Access Key ID, AWS Secret Access Key は docker-compose に記述されてる通りに入力する

```bash
# aws setting
aws configure --profile minio

# ----------
# AWS Access Key ID [None]: hogeaccess
# AWS Secret Access Key [None]: hogesecret
# Default region name [None]: ap-northeast-1
# Default output format [None]: [NO INPUT & ENTER]
```

* Create bucket

```bash
aws \
--endpoint-url http://127.0.0.1:9900 \
--profile minio s3 mb s3://bucket-01
```

* Upload file

```bash
aws \
--endpoint-url http://127.0.0.1:9900 \
--profile minio s3 cp ./docker-compose.yml \
s3://bucket-01
```

## reference

* bucket path

```bash
# export は docker-compose の services/minio/volume に書いている
/export/[BUCKET]
```
