## 59 viewテーブル

select文の結果をセットしておくテーブル
データを保存するわけではなく、あくまでselectするSQLが保存されている

従業員の性別毎の人数を調べるSQL
```
SELECT
	gender,
	COUNT(*)
FROM
	employees
GROUP BY
	gender;
```
上記をviewテーブルに保存
```
CREATE VIEW CountGenderEmployee (v_gender,
cnt) AS
SELECT
	gender,
	COUNT(*)
FROM
	employees
GROUP BY
	gender;
```
呼び出し
```
SELECT
	v_gender,
	cnt
FROM
	CountGenderEmployee;
```

*メリットは可読性と手間が省けるだけで、
データを格納するわけではないから速度は改善されない

## whereとhavingの違い

実行タイミングが異なる
where⇒groupby⇒havingの順
つまりhavingはグループ化した後の情報での、抽出条件を指定できる
[【SQL】一目でわかる!HAVINGとWHEREの違いと活用方法](https://www.sejuku.net/blog/73003)