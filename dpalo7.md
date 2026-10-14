# Profile: Daniel Palomino Gomez

- **NetID:** Dpalo7
- **Major:** Computer Science
- **Question that I chose from the memoization exercise:** Count ways to reach the nth stair using step 1, 2 or 3
- **Link to the question article:** https://www.geeksforgeeks.org/dsa/count-ways-reach-nth-stair-using-step-1-2-3/#usingtopdown-dp-memoization-on-time-and-on-space
- **My solution:**

\
struct whatever{
	
	int countWaysRecurs(int n) {
		// your code here
		
		if (n == 0) {
			return 1;
		} else if (n < 0) {
			return 0;
		}
		
		if (totalWays.at(n) != -1) {
			return totalWays.at(n);
		}
		
		int numWays = countWays(n - 1) + countWays(n - 2) + countWays(n - 3);
		totalWays[n] = numWays;
		
		return numWays;
	}
	
	int countWays(int n) {
		int totalWays[n + 1, -1];
		return countWaysRecurs(n);
	}
};
\