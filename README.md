# Pi
function printNthDigitOfPi(n) {
    /**
     * This function prints the nth digit of Pi.
     * 
     * Parameters:
     * n (number): The position of the digit to be printed.
     * 
     * Returns:
     * None
     */
    
    try {
        // Check if the input is a positive integer
        if (!Number.isInteger(n) || n <= 0) {
            throw new Error("n must be a positive integer");
        }
        
        // Calculate Pi using the Math.PI property
        const pi = Math.PI.toString();
        
        // Check if the requested digit is within the range of Pi
        if (n > pi.length - 2) {
            throw new Error("n is out of range");
        }
        
        // Print the nth digit of Pi
        console.log(pi[n]);
    } catch (error) {
        // Log the error
        console.error("Error:", error.message);
    }
}
