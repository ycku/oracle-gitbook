# alter table shrink compact

```text
SQL> alter table mytable enable row movement;
Table altered

SQL> alter table mytable shrink compact;
Table altered
```

compact: 不需要完全鎖定資料表

1. [http://www.dba-oracle.com/t\_alter\_table\_shrink\_space\_command.htm](http://www.dba-oracle.com/t_alter_table_shrink_space_command.htm)

