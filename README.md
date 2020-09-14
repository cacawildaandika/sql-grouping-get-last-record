# sql-grouping-get-lastrecord

```SELECT * FROM YOUR_TABLE a WHERE id = (SELECT MAX(id) FROM YOUR_TABLE WHERE a.FIELD_A = FIELD_A AND a.FIELD_B = FIELD_B )```
