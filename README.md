# 目的

書籍「SQL実践入門」を用い最適なクエリの使いかたを学ぶ

# バージョン情報

- mysql 8.0

# セクション

1. DBMSのアーキテクチャ

2. SQLの基礎

3. SQLにおける条件分岐

4. 集約とカット

5. ループ

6. 結合

7. サブクエリ

8. SQLにおける順序

9. 更新とデータモデル

10. インデックスを使いこなす

# サンプルデータ作成手順

```bash
# コンテナ内で実行
cd /var/tmp/sample_data_init
mysql -u root -p < employees.sql
```

[参考サイト](https://qiita.com/ya-san-abs/items/fae99144d254e898a641)