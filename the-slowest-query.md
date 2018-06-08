---
description: 'Tested: 11g'
---

# The Slowest query

```text
SELECT *
    FROM (
          SELECT sql_id,
                 command_type,
                 round(elapsed_time / 1000000, 2) "total_time",
                 round(elapsed_time / executeions, 2) "avg_time",
                 sql_text
          FROM v$sqlarea
          WHERE executions > 0
          ORDER BY (elapsed_time / executions) DESC
         )
WHERE rownum <= 50;
```

找出平均執行時間最長的查詢。

1. [v$sqlarea](https://docs.oracle.com/cd/B19306_01/server.102/b14237/dynviews_2129.htm#REFRN30259)

