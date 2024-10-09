# SWE_2021_41_2024_2_week_6

## Week 4 Assignment

Link to my code! [[link]](https://github.com/vladimirgluten-1/SWE_2021_41_2024_2_week_4/blob/main/2024310693_%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%AF%E1%86%AB%E1%84%80%E1%85%B5.ipynb)

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


## Week 5 Assignment
