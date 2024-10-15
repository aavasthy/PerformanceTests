# Benchmark Results

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
