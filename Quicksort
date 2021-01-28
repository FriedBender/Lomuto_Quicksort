



#Maksim Semchuk
#Homework 3 - Quicksort Algorithm
#CS 350 - 01/27/2021

#numpy to use for a randomized array.
import numpy as np

#swap function takes in the array and two indecies to swap
def swap(array, x, y):
    temp = array[x]
    array[x] = array[y]
    array[y] = temp
    return array

#partition function:
#left is the left side of index, right is the right side.
def Partition(array, left, right):
    pivot = array[right]
    i = left

    for j in range(left, right):
        if(array[j] <= pivot):
            swap(array, i, j)
            i = i + 1
    array = swap(array, i, right)
    return i

#recursive quicksort function
def Quicksort(array, left, right):
    if(left < right):
        partitionPoint = Partition(array, left, right)
        Quicksort(array, left, partitionPoint - 1)
        Quicksort(array, partitionPoint+1, right)


#shamelessly stolen from: https://www.geeksforgeeks.org/program-check-array-sorted-not-iterative-recursive/
#to verify if my algorithm works. Though it does NOT work with large arrays
def arraySortedOrNot(arr):
 
    # Calculating length
    n = len(arr)
 
    # Array has one or no element or the
    # rest are already checked and approved.
    if n == 1 or n == 0:
        return True
 
    # Recursion applied till last element
    return arr[0] <= arr[1] and arraySortedOrNot(arr[1:])
 


def main():
    #generate a randomized array of random numbers:
    print("\nGenerating array\n")
    someArray = np.random.randint(low=1 ,high=100000 , size=np.random.randint(low=1, high=1000000))

    left = 0
    right = (len(someArray) -1)

    #print(someArray)

    Quicksort(someArray, left, right)


    #print("\nArray is now sorted!\n")
    #print(someArray)

    if(arraySortedOrNot(someArray)):
        print("\nArray Confirmed Sorted\n")
    else:
        print("\nArray not Sorted\n")






if __name__ == "__main__":
    main()
