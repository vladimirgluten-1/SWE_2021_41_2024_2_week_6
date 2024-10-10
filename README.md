# SWE_2021_41_2024_2_week_6

## Week 4 Assignment

- Link to my code! [[link]](https://github.com/vladimirgluten-1/SWE_2021_41_2024_2_week_4/blob/main/2024310693_%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%AF%E1%86%AB%E1%84%80%E1%85%B5.ipynb)

```python
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
> The function attempts to determine if repeatedly replacing the number n with the sum of the squares of its digits eventually leads to 1.
> 
> If a number is happy, the process will eventually reach 1, regardless of the starting number.
> 
> If a number is unhappy, the process will eventually fall into a repeating cycle of numbers and never reach 1.
> 
> So it is essential to check if the given number will fall into the never-ending cycle.
> 
> Example:
> 
> Determine if n=19 is a happy number using my code:
> 
> Start with tmp1 = 19.
> 
> $1^{2}$ + $9^{2}$ = 1 + 81 = 82
> 
> $8^{2}$ + $2^{2}$ = 64 + 4 = 68
>
> $6^{2}$ + $8^{2}$ = 36 + 64 = 100
>
> $1^{2}$ + $0^{2}$ + $0^{2}$ = 1
>
> Since tmp1 ended up being 1, 19 is a happy number.
>
> I had to implement the cycle itself to check whether a number would fall into an infinite cycle.
>
> So, within the main loop,
>
> ```
>   tmp2=0;
>   for i in str(tmp1):
>   tmp2+=(int(i))**2
>   tmp1=tmp2;
>   if(tmp1==20): return False
>   if(tmp1==1): return True;
> ```
> I have created the cycle by squaring every digit of the number(tmp1) and adding them up to another variable(tmp2)
>
> And what I have figured out by testing with some numbers, is that if a number is unhappy, it goes through a cycle that includes the number 20.
>
> While I have to admit that choosing this exact number isn't the most precise method of solving this problem, my intuition and mathematical proof reassured my solution to be correct no matter the input number.



## Week 5 Assignment

```command
docker exec ossp-container cat /etc/os-release
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION_CODENAME=noble
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=noble
LOG0=ubuntu-logo
```
> - exec: Commands that allow specific commands to be executed in the container.
> - cat /etc/os-release : Command to check the os version on Linux.
> This container's OS is Ubuntu 24.04.
```command
docker exec ossp-container git --version
git version 2.43.0
```
> - This command prints out the current version of git the user has on the computer.
```command
docker exec ossp-container python3 —-version
Python 3.12.3
```
> - This command prints out the current version of Python3 the user has on the computer.
```command
docker inspect --format="{{ «HostConfig-Binds }}" ossp-container
[/Users/alexlee/ossp_host_dir:/mnt/ossp_container_dir]
```
> - This command code will output a list of volume bindings for the ossp-container. These represent the directories/files on the computer that are mounted into the container.
