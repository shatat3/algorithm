# algorithm
############################################################
############# Quick find algorithm in python ###############
############################################################
# worst case is n2
ii=[]
def implementgraph(n):
    for i in range(0,n):
       ii.append(i)

def connected(p,q):
    return  ii[p]==ii[q]       

def QuickFind(p,q):
    pid=ii[p]
    qid=ii[q]
    i=0
    while i<len(ii):
        if ii[i] ==pid:
            ii[i]=ii[q]
        i+=1    

n=int(input('Enter how many union do you want?'))

implementgraph(n)
while(n>0):
   n-=1
   p=int(input())
   q=int(input())
   
   if connected(p,q) != True :
      QuickFind(p,q) 

print(ii)   
print(connected(2,1))
