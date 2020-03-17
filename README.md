## How did changing values on the SparkSession property parameters affect the throughput and latency of the data?

Throughput increased if we incresed `processedRowsPerSecond`, and decreased accordingly as well.

## What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?

spark.sql.shuffle.partitions=10, spark.streaming.kafka.maxRatePerPartition=10 and spark.default.parallelism=10000 where the property key/value
pairs that were found to be best. These options produced the best value for `processedRowsPerSecond`.





