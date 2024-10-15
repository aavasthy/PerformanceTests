# Benchmark Results Comparison

#### Processor: AMD EPYC 7763, 1 CPU, 16 logical and 8 physical cores  

---

## Comparison Table: Master vs. users/dkunda/4644_binary_encoding_for_point_ops

|           Method        |   Branch                               | IterationCount | LaunchCount | RunStrategy | WarmupCount |   Mean    |   Error  |  StdDev  |  Median  |    P95   |   Op/s  |   Gen0   | Allocated   |
|-------------------------|----------------------------------------|----------------|-------------|-------------|-------------|-----------:|---------:|---------:|----------:|----------:|---------:|----------:|-------------:|
| **ReadItemsAsync**      | Master                                 |              5 |           1 | Throughput  |           3 | 2,019.4 ms |  9.82 ms |  2.55 ms | 2,018.6 ms | 2,022.1 ms | 0.4952  | 1000.0000 | 22,901,176 B |
|                         | users/dkunda/4644_binary_encoding_for_point_ops |        5 |           1 | Throughput  |           3 | 2,032.0 ms | 42.52 ms | 11.04 ms | 2,035.8 ms | 2,043.0 ms | 0.4921  | 1000.0000 | 22,963,432 B |
| **QueryItemsAsync**     | Master                                 |              5 |           1 | Throughput  |           3 |   341.0 ms | 43.67 ms | 11.34 ms |   347.7 ms |   351.1 ms | 2.9325  |     -     |   539,136 B |
|                         | users/dkunda/4644_binary_encoding_for_point_ops |        5 |           1 | Throughput  |           3 |   321.8 ms | 20.31 ms |  3.14 ms |   323.1 ms |   323.7 ms | 3.1080  |     -     |   540,016 B |
| **UpsertItemsAsync**    | Master                                 |              5 |           1 | Throughput  |           3 | 2,307.6 ms | 21.35 ms |  3.30 ms | 2,309.1 ms | 2,309.4 ms | 0.4334  | 1000.0000 | 23,553,768 B |
|                         | users/dkunda/4644_binary_encoding_for_point_ops |        5 |           1 | Throughput  |           3 | 2,435.5 ms | 22.70 ms |  5.89 ms | 2,436.8 ms | 2,441.8 ms | 0.4106  | 1000.0000 | 23,856,208 B |
| **DeleteItemsAsync**    | Master                                 |              5 |           1 | Throughput  |           3 | 2,160.1 ms | 42.22 ms | 10.96 ms | 2,153.4 ms | 2,172.2 ms | 0.4629  | 1000.0000 | 22,111,528 B |
|                         | users/dkunda/4644_binary_encoding_for_point_ops |        5 |           1 | Throughput  |           3 | 2,300.2 ms | 77.18 ms | 20.04 ms | 2,290.1 ms | 2,326.7 ms | 0.4347  | 1000.0000 | 22,109,248 B |
| **QueryItemsAsync**     | Master (MediumRun)                     |             15 |           2 | Default     |          10 |   137.4 ms | 47.03 ms | 68.94 ms |   197.3 ms |   210.4 ms | 7.2775  |     -     |   344,008 B |
|                         | users/dkunda/4644_binary_encoding_for_point_ops (MediumRun) | 15 | 2 | Default  |          10 |   143.2 ms | 46.75 ms | 67.05 ms |   196.9 ms |   210.7 ms | 6.9816  |     -     |   354,936 B |
| **UpsertItemsAsync**    | Master (MediumRun)                     |             15 |           2 | Default     |          10 | 2,370.0 ms | 25.70 ms | 37.68 ms | 2,388.6 ms | 2,415.7 ms | 0.4219  | 1000.0000 | 23,579,448 B |
|                         | users/dkunda/4644_binary_encoding_for_point_ops (MediumRun) | 15 | 2 | Default  |          10 | 2,308.2 ms |  7.65 ms | 11.22 ms | 2,306.0 ms | 2,330.6 ms | 0.4332  | 1000.0000 | 23,844,400 B |
| **DeleteItemsAsync**    | Master (MediumRun)                     |             15 |           2 | Default     |          10 | 2,128.8 ms | 48.44 ms | 64.66 ms | 2,078.5 ms | 2,199.1 ms | 0.4698  | 1000.0000 | 22,119,016 B |
|                         | users/dkunda/4644_binary_encoding_for_point_ops (MediumRun) | 15 | 2 | Default  |          10 | 2,254.6 ms | 57.15 ms | 83.77 ms | 2,264.3 ms | 2,401.9 ms | 0.4435  | 1000.0000 | 22,026,672 B |

---



# Individual Benchmark Results


#### Processor: AMD EPYC 7763, 1 CPU, 16 logical and 8 physical cores  
#### Branch: Master
---

## Summary Table

|           Method        |        Job | IterationCount | LaunchCount | RunStrategy | WarmupCount |    Mean   |   Error |  StdDev |  Median  |   P95   |   Op/s  |   Gen0   | Allocated |
|-------------------------|------------|----------------|-------------|-------------|-------------|-----------:|--------:|--------:|----------:|---------:|---------:|----------:|----------:|
| **ReadItemsAsync**      | Job-NXGPKS |              5 |           1 | Throughput  |           3 | 2,019.4 ms |  9.82 ms |  2.55 ms | 2,018.6 ms | 2,022.1 ms | 0.4952 | 1000.0000 | 22,901,176 B |
| **QueryItemsAsync**     | Job-NXGPKS |              5 |           1 | Throughput  |           3 |   341.0 ms | 43.67 ms | 11.34 ms |   347.7 ms |   351.1 ms | 2.9325 |     -     |   539,136 B |
| **UpsertItemsAsync**    | Job-NXGPKS |              5 |           1 | Throughput  |           3 | 2,307.6 ms | 21.35 ms |  3.30 ms | 2,309.1 ms | 2,309.4 ms | 0.4334 | 1000.0000 | 23,553,768 B |
| **DeleteItemsAsync**    | Job-NXGPKS |              5 |           1 | Throughput  |           3 | 2,160.1 ms | 42.22 ms | 10.96 ms | 2,153.4 ms | 2,172.2 ms | 0.4629 | 1000.0000 | 22,111,528 B |
| **ReadItemsAsync**      | MediumRun  |             15 |           2 | Default     |          10 |      N/A   |     N/A  |     N/A  |      N/A   |     N/A   |     N/A  |     -     |        -   |
| **QueryItemsAsync**     | MediumRun  |             15 |           2 | Default     |          10 |   137.4 ms | 47.03 ms | 68.94 ms |   197.3 ms |   210.4 ms | 7.2775 |     -     |   344,008 B |
| **UpsertItemsAsync**    | MediumRun  |             15 |           2 | Default     |          10 | 2,370.0 ms | 25.70 ms | 37.68 ms | 2,388.6 ms | 2,415.7 ms | 0.4219 | 1000.0000 | 23,579,448 B |
| **DeleteItemsAsync**    | MediumRun  |             15 |           2 | Default     |          10 | 2,128.8 ms | 48.44 ms | 64.66 ms | 2,078.5 ms | 2,199.1 ms | 0.4698 | 1000.0000 | 22,119,016 B |

---

## Detailed Results

### **BinaryEncodingBenchmark.ReadItemsAsync**  
- **Job**: Job-NXGPKS  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 2.019 s  
- **StdDev**: 0.003 s  
- **Confidence Interval (99.9%)**: [2.010 s; 2.029 s]  


---

### **BinaryEncodingBenchmark.QueryItemsAsync**  
- **Job**: Job-NXGPKS  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 341.009 ms  
- **StdDev**: 11.340 ms  
- **Confidence Interval (99.9%)**: [297.343 ms; 384.675 ms]  


---

### **BinaryEncodingBenchmark.UpsertItemsAsync**  
- **Job**: Job-NXGPKS  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 2.308 s  
- **StdDev**: 0.003 s  
- **Confidence Interval (99.9%)**: [2.286 s; 2.329 s]  


---

### **BinaryEncodingBenchmark.DeleteItemsAsync**  
- **Job**: Job-NXGPKS  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 2.160 s  
- **StdDev**: 0.011 s  
- **Confidence Interval (99.9%)**: [2.118 s; 2.202 s]

---

## Branch:  users/dkunda/4644_binary_encoding_for_point_ops  

#### Processor: AMD EPYC 7763, 1 CPU, 16 logical and 8 physical cores  


---

## Summary Table

|           Method        |        Job | IterationCount | LaunchCount | RunStrategy | WarmupCount |    Mean   |   Error |  StdDev |  Median  |   P95   |   Op/s  |   Gen0   | Allocated |
|-------------------------|------------|----------------|-------------|-------------|-------------|-----------:|--------:|--------:|----------:|---------:|---------:|----------:|----------:|
| **ReadItemsAsync**      | Job-GBWISA |              5 |           1 | Throughput  |           3 | 2,032.0 ms | 42.52 ms | 11.04 ms | 2,035.8 ms | 2,043.0 ms | 0.4921 | 1000.0000 | 22,963,432 B |
| **QueryItemsAsync**     | Job-GBWISA |              5 |           1 | Throughput  |           3 |   321.8 ms | 20.31 ms |  3.14 ms |   323.1 ms |   323.7 ms | 3.1080 |     -     |   540,016 B |
| **UpsertItemsAsync**    | Job-GBWISA |              5 |           1 | Throughput  |           3 | 2,435.5 ms | 22.70 ms |  5.89 ms | 2,436.8 ms | 2,441.8 ms | 0.4106 | 1000.0000 | 23,856,208 B |
| **DeleteItemsAsync**    | Job-GBWISA |              5 |           1 | Throughput  |           3 | 2,300.2 ms | 77.18 ms | 20.04 ms | 2,290.1 ms | 2,326.7 ms | 0.4347 | 1000.0000 | 22,109,248 B |
| **ReadItemsAsync**      | MediumRun  |             15 |           2 | Default     |          10 |      N/A   |     N/A  |     N/A  |      N/A   |     N/A   |     N/A  |     -     |        -   |
| **QueryItemsAsync**     | MediumRun  |             15 |           2 | Default     |          10 |   143.2 ms | 46.75 ms | 67.05 ms |   196.9 ms |   210.7 ms | 6.9816 |     -     |   354,936 B |
| **UpsertItemsAsync**    | MediumRun  |             15 |           2 | Default     |          10 | 2,308.2 ms |  7.65 ms | 11.22 ms | 2,306.0 ms | 2,330.6 ms | 0.4332 | 1000.0000 | 23,844,400 B |
| **DeleteItemsAsync**    | MediumRun  |             15 |           2 | Default     |          10 | 2,254.6 ms | 57.15 ms | 83.77 ms | 2,264.3 ms | 2,401.9 ms | 0.4435 | 1000.0000 | 22,026,672 B |

---

## Detailed Results

### **BinaryEncodingBenchmark.ReadItemsAsync**
- **Job**: Job-GBWISA  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 2.032 s  
- **StdDev**: 0.011 s  
- **Confidence Interval (99.9%)**: [1.989 s; 2.075 s]  


---

### **BinaryEncodingBenchmark.QueryItemsAsync**
- **Job**: Job-GBWISA  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 321.753 ms  
- **StdDev**: 3.144 ms  
- **Confidence Interval (99.9%)**: [301.439 ms; 342.067 ms]  

---

### **BinaryEncodingBenchmark.UpsertItemsAsync**
- **Job**: Job-GBWISA  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 2.435 s  
- **StdDev**: 0.006 s  
- **Confidence Interval (99.9%)**: [2.413 s; 2.458 s]  


---

### **BinaryEncodingBenchmark.DeleteItemsAsync**
- **Job**: Job-GBWISA  
- **Iteration Count**: 5  
- **Warmup Count**: 3  
- **Mean**: 2.300 s  
- **StdDev**: 0.020 s  
- **Confidence Interval (99.9%)**: [2.223 s; 2.377 s]  





