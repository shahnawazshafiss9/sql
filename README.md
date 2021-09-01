# sql

SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''))

UPDATE `my_scoop_pdf_video_details` SET `pdf_file` = REPLACE(REPLACE(REPLACE(`pdf_file`, ' ', ''), '\t', ''), '\n', '')

## database null datetime
UPDATE users SET `columnName` = NULL WHERE CAST(`columnName` AS CHAR(20)) = '0000-00-00 00:00:00'

