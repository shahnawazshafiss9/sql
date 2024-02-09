## sql group by update  full
```sql
SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''))

UPDATE `my_scoop_pdf_video_details` SET `pdf_file` = REPLACE(REPLACE(REPLACE(`pdf_file`, ' ', ''), '\t', ''), '\n', '')
```

## database null datetime

```sql
UPDATE users SET `columnName` = NULL WHERE CAST(`columnName` AS CHAR(20)) = '0000-00-00 00:00:00'
````

## show all columns in comma seprated
```sql
SELECT CONCAT("'", GROUP_CONCAT(column_name ORDER BY ordinal_position SEPARATOR "', '"), "'") AS columns FROM information_schema.columns WHERE table_schema = 'coinlend_prod_lendingplate' AND table_name = 'aa_emi_details';
```
