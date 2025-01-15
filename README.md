# Go Race Condition Example
This repository demonstrates a race condition in Go.  Multiple goroutines concurrently access and modify a shared variable (counter) without proper synchronization, resulting in an incorrect final count.  The solution demonstrates the correct use of mutex locks to prevent data races and ensure accurate results.  This example highlights the importance of concurrency safety in Go and provides a practical demonstration of how to resolve a common concurrency bug.

## How to Run
1. Clone the repository: `git clone <repository_url>`
2. Navigate to the project directory: `cd go-race-condition`
3. Run the buggy code: `go run bug.go` (Observe the incorrect counter value)
4. Run the corrected code: `go run bugSolution.go` (Observe the correct counter value)

## Note
The bug is the race condition between the goroutines trying to increment the shared counter variable without protection. The solution involves correctly using the mutex to synchronize access to the shared variable.