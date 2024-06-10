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
```python
# cook your dish here
def help(a,i,k):
    a[i]=k
    sums=0
    for i in range(1,n):
        difference=abs(a[i-1]-a[i])
        sums=sums+difference
    return sums
for _ in range(int(input())):
    n,k=map(int,input().split())
    a=list(map(int,input().split()))
    maxi=-1
    b=a[:]
    for i in range(n):
        maxi=max(maxi,help(b,i,1))
        maxi=max(maxi,help(b,i,k))
        b=a[:]
    print(maxi)
```