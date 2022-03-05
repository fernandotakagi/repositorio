            /** # QUESTÃO 2 **/

            public class Test {
    // method to find pair such that (a % b = k)
    static boolean printPairs(int arr[], int n, int k)
    {
        boolean isPairFound = true;
 
        // Consider each and every pair
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                // Print if their modulo equals to k
                if (i != j && arr[i] - arr[j] == k) {
                    System.out.print("(" + arr[i] + ", " + arr[j] + ")"
                                     + " ");
                    isPairFound = true;
                }
            }
        }
 
        return isPairFound;
    }
 
    // Driver method
    public static void main(String args[])
    {
        int arr[] = { 1, 5, 3, 4, 2 };
        int k = 2;
 
        if (printPairs(arr, arr.length, k) == false)
            System.out.println("No such pair exists");
    }
}
