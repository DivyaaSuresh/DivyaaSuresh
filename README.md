#include <stdbool.h>
#include <stdio.h>
 
// This function is to check
// if a given number is prime
bool isPrime(int n)
{
    // since 0 and 1 is not prime
    // number return false.
    if (n == 1 || n == 0)
        return false;
 
    // Run a loop from 2 to n/2
    for (int i = 2; i <= n / 2; i++) {
 
        // if the number is divisible by i, then n is not a
        // prime number, otherwise n is prime number.
        if (n % i == 0)
            return false;
    }
    return true;
}
 
// Driver code
int main()
{
    int N = 50;
 
    // check for the every number from 1 to N
    for (int i = 1; i <= N; i++) {
 
        // check if i (current number) is prime
        if (isPrime(i)) {
            printf("%d ", i);
        }
    }
    return 0;
}
