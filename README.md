**Q1. How did changing values on the SparkSession property parameters affect the throughput and latency of the data?**

By changing the configurations, I was able to notice a difference in the `processedRowsPerSecond`.

**Q2. What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?**

```
"spark.streaming.kafka.maxOffsetsPerTrigger", 1000
"spark.streaming.kafka.maxRatePerPartition", 300
```

These were the values that generated the greater processedRowsPerSecond rate.