# Swift-Binary-Search-on-Integer-Array

//main function user will use
func rank( a : [Int], n : Int ) -> Int
{
    //pass onto helper function
    return rankHelper(a, n, 0, array.count - 1)
    
}

//Helper function for recursion
func rankHelper( a : [Int], n : Int, lo : Int, hi : Int ) -> Int
{
    
    //calculate middle of array section
    var mid : Int = (Int)(((hi - lo) / 2) + lo)
    
    //if middle of array section is the answer
    if ( a[mid] == n )
    {
        return mid
    }
    else
    {
        //if we cannot recur anymore
        if hi <= lo
        {
            return -1
        }
        
        //recur
        return a[mid] > n ? rankHelper(a, n, lo, mid) : rankHelper(a, n, mid + 1, hi)
    }
    
}
