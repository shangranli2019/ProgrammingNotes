## Upsert in MySQL

replace





```sql
INSERT INTO t1 
SET a=1,b=2,c=3 AS new 
ON DUPLICATE KEY 
UPDATE c = new.a+new.b;
```

