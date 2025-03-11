# Module 5

## `/all-student-name`
| Before Optimization                                                  | After Optimization                    | 
 |----------------------------------------------------------------------|---------------------------------------|
| ![all-student-name before.png](assets/all-student-name%20before.png) |![all-student-name after.png](assets/all-student-name%20after.png) [](assets/all-student-name after.png) |

### Command line
![all-student-name command line.png](assets/all-student-name%20command%20line.png)


## `/highest-gpa`
| Before Optimization | After Optimization               | 
 |--|----------------------------------|
| ![highest-gpa before.png](assets/highest-gpa%20before.png) | ![highest-gpa after.png](assets/highest-gpa%20after.png)|

### Command line
![highest-gpa command line.png](assets/highest-gpa%20command%20line.png)


After profiling `/all-student-name` and `/highest-gpa`, by optimizing some of the methods like using the database to handle data processing.
As a result, the JMeter test after profiling shows a significant decrease in the execution time (from thousands milliseconds to only double-digit milliseconds).
This streamlined approach enhances the application’s efficiency, scalability, and overall responsiveness.

## Reflection
### Difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler
In JMeter, it mainly focuses on external load testing in different scenarios. While in IntelliJ Profiler, it provides internal code-level analysis of CPU and memory.
This means that both have different approach in testing, JMeter measures overall performance from user perspective, and IntelliJ Profiler indicates inefficient in the code.

### How does the profiling process help identify the weak points?
Profiling shows which methods consume the most resources by analyzing call stacks and CPU usage. 
Without profiling, it would be difficult to identify the bottlenecks.

### Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
Yes, IntelliJ Profiler is effective because it shows method-level CPU usage, flame graphs, and real-time insights that pinpoint bottlenecks.

### Challenges when conducting performance testing and profiling
- Setting up test conditions
- Understanding profiling data
- Interpreting complex frame graph

I overcome these by running multiple tests, using representative data, and carefully analyzing profiler reports.

### Benefits from using IntelliJ Profiler for profiling application code
- Detailed method-level insights
- Highlights performance hotspots through flame graph
- Seamless integration with IDE. 

### Handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with performance testing using JMeter
If the result from profiling and performance testing is inconsistent, I verify that both tests have the same conditions (such as workloads or data sets) and repeat the test to confirm that the discrepancies are not due to transient fluctuations.
By comparing both of the test results, I can identify potential gaps in the testing scenarios and this can be solved by adjusting the test environment or profiler settings.

### Strategies in optimizing application code after analyzing results from performance testing and profiling
- Reducing redundant queries
- Use more efficient data structures
- Minimizing unnecessary computations

I ensure changes don’t break functionality by creating tests to ensure the functionality stays the same even after optimization.

