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
```python

#The largest subarray with even sum is the subarray 
#[2,2,1,1][2,2,1,1] having size 4

# cook your dish here
for _ in range(int(input())):
    n=int(input())
    # a=[0]*n
    a=list(map(int,input().split()))
    sums=0
    st=0
    res=[]
    for i in range(n):
        for j in range(i+1,n+1):
            if sum(a[i:j])%2==0:
                res.append(len(a[i:j]))
        
    if res:        
        print(max(res))
    else:
        print(0)
```