# ZeroMover

# This function aims to move the elements that are zero in a list to 
# the end of the list, without changing the positions of the other elements.
# It is assumed that the input is provided separated by spaces.

def aranger(nums):
    index = 0

    for i in range(len(nums)):
        if nums[i] != 0:
            nums[index], nums[i] = nums[i], nums[index]
            index += 1
    return nums
    
user_input = input("Enter numbers separated by spaces: ")

nums = list(map(int, user_input.split()))
print(aranger(nums))
