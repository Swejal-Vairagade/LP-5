<img width="828" height="1792" alt="image" src="https://github.com/user-attachments/assets/70ef50bf-ebec-45d0-8ec4-f21d75b9f97a" /># LP-5

## use OnlineGDB C++ compiler 
## add flags setting>extra compiler flags> -fopenmp
### https://chatgpt.com/share/6a010ec0-39d8-83ec-98c6-fb17109279c9
### code theory
### https://chatgpt.com/share/6a0145a6-65d8-83a5-a2eb-badaa3fe5682
### https://chatgpt.com/share/6a0156e2-3760-8323-978d-ef6df5a9959f
### Practical No: 3

Title: Implementation of Min, Max, Sum and Average using Parallel Reduction

Aim

To implement Minimum, Maximum, Sum and Average operations using Parallel Reduction in OpenMP.

Theory

Parallel Reduction is a technique in parallel computing used to combine multiple values into a single result using multiple threads simultaneously.

In sequential programming, operations like:
	•	finding minimum
	•	finding maximum
	•	calculating sum
	•	calculating average

are performed using a single thread. This increases execution time for large datasets.

Using OpenMP, the array is divided among multiple threads. Each thread computes a partial result independently, and finally OpenMP combines all partial results into one final result using the reduction clause.

OpenMP provides the reduction directive:#pragma omp parallel for reduction(operator:variable)
where:
	•	operator specifies the reduction operation
	•	variable stores the final combined result

Reduction operations used:
	•	min → minimum value
	•	max → maximum value
	•	+ → sum

Average is calculated using:

\text{Average} = \frac{\text{Sum of Elements}}{\text{Number of Elements}}

Parallel reduction improves:
	•	execution speed
	•	CPU utilization
	•	performance for large datasets.

⸻

Algorithm

Algorithm for Minimum
	1.	Initialize minimum value with first array element.
	2.	Divide array among multiple threads using OpenMP.
	3.	Each thread finds local minimum.
	4.	Combine all local minimum values.
	5.	Display final minimum value.

⸻

Algorithm for Maximum
	1.	Initialize maximum value with first array element.
	2.	Divide array among multiple threads.
	3.	Each thread finds local maximum.
	4.	Combine local maximum values.
	5.	Display final maximum value.

⸻

Algorithm for Sum
	1.	Initialize total sum as 0.
	2.	Divide array among multiple threads.
	3.	Each thread calculates partial sum.
	4.	Combine all partial sums.
	5.	Display total sum.

⸻

Algorithm for Average
	1.	Calculate sum of array elements.
	2.	Divide total sum by number of elements.
	3.	Display average.
Advantages
	1.	Faster execution
	2.	Efficient CPU utilization
	3.	Suitable for large datasets
	4.	Reduced computation time
	5.	Improved performance using multithreading

⸻

Applications
	•	Scientific computing
	•	Data analysis
	•	Big data processing
	•	Statistical calculations
	•	Parallel computing systems

