# sql-hack
## grouping-get-lastrecord
```
SELECT * FROM YOUR_TABLE a WHERE id = (SELECT MAX(id) FROM YOUR_TABLE WHERE a.FIELD_A = FIELD_A AND a.FIELD_B = FIELD_B );
```
## find-in-jsonb-array-of-object
```
SELECT *
FROM class_scheduling.class_schedule_details
WHERE EXISTS (
    SELECT 1
    FROM jsonb_array_elements(schedule_day_time) AS j(element)
    WHERE j.element ->> 'day' = 'monday'
);
```
