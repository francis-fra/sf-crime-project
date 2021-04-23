### Questions
1. How did changing values on the SparkSession property parameters affect the throughput and latency of the data?

    By adjusting the following three parameters, the throughput and latency are affected:
    * numInputRows
    * inputRowsPerSecond
    * processedRowsPerSecond

2. What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?

    - spark.sql.shuffle.partitions: 20
    - spark.default.parallelism: 100

    The first paramter configures the number of paritions that are used when shuffling data for joins or aggregations. The second parameter sets the number of patitions in RDD returned by transformations.

