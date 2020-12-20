# sql

SET GLOBAL sql_mode=(SELECT REPLACE(@@sql_mode,'ONLY_FULL_GROUP_BY',''))

UPDATE `my_scoop_pdf_video_details` SET `pdf_file` = REPLACE(REPLACE(REPLACE(`pdf_file`, ' ', ''), '\t', ''), '\n', '')
