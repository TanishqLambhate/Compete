```python
# cook your dish here
x,y=map(int,input().split())

if x>=2*y :
    print("Yes")
else:
    print("No")
```

```python
t=int(input())
for k in range(t):
    n=int(input())
    a=[0]*n
    v=[0]*n
    for i in range(0,n):
        v[i],a[i]=map(int,input().split())
        
    ma=0
    for i in range(n):
        for j in range(i+1,n):
            sums=a[i]*v[j]+a[j]*v[i]
            ma=max(sums,ma)
            
    print(ma)
```