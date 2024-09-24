# s3s-local

> s3s の実行を管理するリポジトリ

[issei-m/s3s-docker](https://github.com/issei-m/s3s-docker) の Image を使用します。

## トークンの取得

```sh
# s3s を実行する
s3s_config=$(cat config.txt); docker run --name s3s-local -it --rm -e S3S_CONFIG="$s3s_config" isseim/s3s -M

# 別ターミナルで s3s-local コンテナから config.txt をコピーする
docker cp s3s-local:/opt/s3s/config.txt .
```
