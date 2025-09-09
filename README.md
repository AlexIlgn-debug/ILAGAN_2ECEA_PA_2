# ILAGAN_2ECEA_PA_2

## The Normalization Problem requires getting the z-score or the normal by getting the mean and the standard deviation with a random 5x5 array

    import numpy as np

//import numpy

    X = np.random.random((5,5))
    print(X)
  
// create the 5x5 random array

    mean = X.mean()
    std = X.std()
    print("Mean: ")
    print(mean)
    print("Standard deviation: ")
    print(std)

// gets the mean and the standard deviation of the random array X 

    normalized = (X - mean)/std
    print("Normalized Array: ")
    normalized

  np.save('X_normalized', normalized)

// gets the normal using the formula and prints it, then save the result in the file "X_normalized"

    np.load('X_normalized.ppy.npy')

// this is to load in the saved file and to be able to see the result


## The Divisible by 3 Problem requires creating a 10x10 array of the first 100 positive integers and getting their perfect squares, then seeing which numbers are divisble by 3

    import numpy as np

// import numpy

  A = np.arange(1,101).reshape(10,10) ** 2
  
// put into an array numbers 1 to 100, then reshapes it into a 10x10 array, after all that it all gets squared

    div3 = A % 3 == 0
    div3_A = A[div3]
    div3_A

// gets the numbers in the array that are all divisible by 3, the second line is so it wont show a boolean result and instead the actual value

    np.save('div_by_3', div3_A)
  
// saves the result in the file 'div_by_3' 

    np.load('div_by_3.npy')

// to load in the results of what was saved
