# exercise-book
* CodeUp Link:[https://codeup.kr/problem.php?id=1098] [설탕과자 뽑기]


```python
a = input().split()
b = int(input())
c = []
for n in range(b):
    c += input().split()

a = [[0]*int(a[1]) for i in range(int(a[0]))]
c = list(map(int,c))

for i in range(0,len(c),4):
    f = c[i:i+4]
    if not f[1]:
        for i in range(f[0]):
            a[f[2]-1][f[3]-1+i]=1
    else:
        for j in range(f[0]):
            a[f[2]+j-1][f[3]-1]=1
            
for q in a:
    for w in q:
        print(w,end=' ')
    print()
```
