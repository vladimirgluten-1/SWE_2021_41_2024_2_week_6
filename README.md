# SWE_2021_41_2024_2_week_6

## Week 4 Assignment

- Link to my code! [[link]](https://github.com/vladimirgluten-1/SWE_2021_41_2024_2_week_4/blob/main/2024310693_%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%AF%E1%86%AB%E1%84%80%E1%85%B5.ipynb)

```
def isHappy(n):
  tmp1=n
  tmp2=0
  #print(n)
  if(n==1): return True;
  while(1):
    tmp2=0;
    for i in str(tmp1):
      tmp2+=(int(i))**2
    tmp1=tmp2;
    if(tmp1==20): return False
    if(tmp1==1): return True;
```
- Description of my code
> My code is one of the many solutions to determine if a number is "happy" or not.
>
> A happy number is a number defined by the following process:
> - Starting with any positive integer, replace the number by the sum of the squares of its digits.
> - Repeat the process until the number equals 1 (where it will stay), or it loops endlessly in a cycle that does not include 1.
> - Those numbers for which this process ends in 1 are happy.
> - Return true if n is a happy number, and false if not.
> 
> I had to write an algorithm that determines a given number(n) where 1 <= n <= $2^{31}$ -1 in Python.
> 

## Week 5 Assignment
