# List all table size

```text
SELECT segment_name, bytes/1024/1024 MB
FROM dba_segments
WHERE segment_type='TABLE'
ORDER BY bytes DESC
```

