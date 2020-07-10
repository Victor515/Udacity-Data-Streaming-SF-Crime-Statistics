# Spark Streaming on SF Crime Statistics

## Questions and Answers
1. How did changing values on the SparkSession property parameters affect the throughput and latency of the data?
They will affect parameters in progress report like `numInputRows`, `inputRowsPerSecond` or `processedRowsPerSecond`.

2. What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?
We can check the optimal variations when the throughput parameters above are optimized.
Through tuning, here is the most efficient properties:
- spark.streaming.kafka.maxRatePerPartition
- spark.sql.shuffle.partitions
- spark.default.parallelism
