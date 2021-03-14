import time
import random
import string
from random import randint
def checkSort(arr,N,ind):
    if ind==1:
        for i in range(N-1):
            if arr[i]>arr[i+1]:
                return 0
    elif ind==-1:
        for i in range(N-1):
            if arr[i]<arr[i+1]:
                return 0
    return 1 
def quicksortC(arr,tim1):
    if len(arr) <= 1:
        return arr
    tim2=time.time()
    if tim2-tim1>20:
        return 0
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x< pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksortC(left,tim1) + middle + quicksortC(right,tim1)
def quicksortD(arr,tim1):
    if len(arr) <= 1:
        return arr
    tim2=time.time()
    if tim2-tim1>20:
        return 0
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x> pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x < pivot]
    return quicksortD(left,tim1) + middle + quicksortD(right,tim1)
def bubblesortC(a):
    temp=time.time()
    for i in range(0, len(a)):
        swapped = False
        temp2=time.time()
        if temp2-temp>10:
            return 0
        for j in range(0, len(a)-i-1):
            if (a[j] > a[j+1]):
                a[j], a[j+1] = a[j+1], a[j]
                swapped = True
        if(not (swapped)):
            break
    return 1
def bubblesortD(a):
    temp=time.time()
    for i in range(0, len(a)):
        swapped = False
        temp2=time.time()
        if temp2-temp>10:
            return 0
        for j in range(0, len(a)-i-1):
            if (a[j] < a[j+1]):
                a[j], a[j+1] = a[j+1], a[j]
                swapped = True
        if(not (swapped)):
            break
    return 1
def countSort(myList,ind):
    maxValue = 0
    for i in range(len(myList)):
        if myList[i] > maxValue:
            maxValue = myList[i]

    buckets = [0] * (maxValue + 1)

    for i in myList:
        buckets[i] += 1

    i = 0
    if ind==1:
        for j in range(maxValue + 1):
             for a in range(buckets[j]):
                 myList[i] = j
                 i += 1
    else:
        for j in range(maxValue,-1,-1):
             for a in range(buckets[j]):
                 myList[i] = j
                 i += 1
def mergesortC(x):
    def merge(array1, array2):
        merged_array = []
        a, b = 0, 0
        while a < len(array1) and b < len(array2):
            if array1[a] < array2[b]:
                merged_array.append(array1[a])
                a += 1
            else:
                merged_array.append(array2[b])
                b += 1
        while a < len(array1):
            merged_array.append(array1[a])
            a += 1

        while b < len(array2):
            merged_array.append(array2[b])
            b += 1

        return merged_array
    def mergeSort(array):
        if len(array) <= 1:
            return array
        else:
            left = array[:len(array)//2]
            right = array[len(array)//2:]
            return merge(mergeSort(left),mergeSort(right))
    return mergeSort(x)
def mergesortD(x):
    def merge(array1, array2):
        merged_array = []
        a, b = 0, 0
        while a < len(array1) and b < len(array2):
            if array1[a] > array2[b]:
                merged_array.append(array1[a])
                a += 1
            else:
                merged_array.append(array2[b])
                b += 1
        while a < len(array1):
            merged_array.append(array1[a])
            a += 1

        while b < len(array2):
            merged_array.append(array2[b])
            b += 1

        return merged_array
    def mergeSort(array):
        if len(array) <= 1:
            return array
        else:
            left = array[:len(array)//2]
            right = array[len(array)//2:]
            return merge(mergeSort(left),mergeSort(right))
    return mergeSort(x)
def radix_sort(source,f,b):
    if f<=b:
        ra=b
    else:
        ra = f//b;
    buckets = [[] for i in range(ra)]
    maxLength = False
    tmp = -1; placement = 0
    while not maxLength:
        maxLength = True
        for i in source:
            tmp = i >> placement
            buckets[tmp % ra].append(i)
            if maxLength and tmp > 0:
                maxLength = False
        a = 0
        for bucket in buckets:
            for i in bucket:
                source[a] = i
                a += 1
            bucket.clear()
        
        placement +=1# *ra
def RadixSortD(a, n):
    m=0
    exp=1
    b=[0]*n
    for i in range(0,n):
        if a[i]>m:
            m=a[i]
    while m//exp>0:
        bucket=[0]*10
        for i in range(0,n):
            bucket[9-a[i]//exp%10]+=1
        for i in range(1,10):
            bucket[i]+=bucket[i-1]
        for i in range(n-1,-1,-1):
            bucket[9-a[i]//exp%10]-=1
            b[bucket[9-a[i]//exp%10]]=a[i] 
        for i in range(0,n):
            a[i]=b[i]
        exp*=10
    return a

def randomword(length):
   letters = string.ascii_lowercase
   return ''.join(random.choice(letters) for i in range(length))
def aSA(N,maxim,caz,typ):
    l=[]
    if typ=='i':
        for i in range(0,N):
            l.append(random.randint(0, maxim))
    elif typ=='d':
        for i in range(0,N):
            l.append(random.uniform(0, maxim))
    elif typ=='c':
        for i in range(0,N):
            l.append(random.choice(string.ascii_letters))
    elif typ=='s':
        for i in range(0,N):
            l.append(randomword(maxim))
    l.sort()
    if N>10:
        for i in range(0,10):
            l[i],l[N-i-1]=l[N-i-1],l[i]
    else:
        l[i],l[N-1]=l[N-1],l[i]
    return l
def aSD(N,maxim,caz,typ):
    l=[]
    if typ=='i':
        for i in range(0,N):
            l.append(random.randint(0, maxim))
    elif typ=='d':
        for i in range(0,N):
            l.append(random.uniform(0, maxim))
    elif typ=='c':
        for i in range(0,N):
            l.append(random.choice(string.ascii_letters))
    elif typ=='s':
        for i in range(0,N):
            l.append(randomword(maxim))
    l.sort(reverse=True)
    if N>10:
        for i in range(0,10):
            l[i],l[N-i-1]=l[N-i-1],l[i]
    else:
        l[i],l[N-1]=l[N-1],l[i]
    return l
def ran(N,maxim,caz,typ):
    l=[]
    if typ=='i':
        for i in range(0,N):
            l.append(random.randint(0, maxim))
    elif typ=='d':
        for i in range(0,N):
            l.append(random.uniform(0, maxim))
    elif typ=='c':
        for i in range(0,N):
            l.append(random.choice(string.ascii_letters))
    elif typ=='s':
        for i in range(0,N):
            l.append(randomword(maxim))
    return l
def start(N,maxim,caz,typ):
    List=[]    
    print("numar de elemente:",N)
    ind=1
    if caz=='almostSortedAsc':
        List=aSA(N,maxim,caz,typ).copy()
        ind=1
    elif caz=='almostSortedDesc':
        List=aSD(N,maxim,caz,typ).copy()
        ind=-1
    elif caz=='random':
        List=ran(N,maxim,caz,typ).copy()
    temp=[]
    temp=List.copy()#
    start = time.time()
    if ind==1:
        List=quicksortC(List,start)
    else:
        List=quicksortD(List,start)
    #print(List)
    stop = time.time()

    if List==0:
        print('Time req for quicksort: Not possible')
    else:
        print('Time Required for quicksort:', (stop - start))
        if checkSort(List,N,ind)==1:
            print("A sortat corect")
        else:
            print("A sortat gresit")
    #print(temp)
    #print(List)
    List=temp.copy()#
    if typ!='c' and typ!='s' and typ!='d':
        start=time.time()
        if ind==1:
            radix_sort(List,N,10)
        elif ind==-1:
            RadixSortD(List,N)
        #print(List)
        stop=time.time()
        print("Time Required for radixsort :", stop-start)
        
        if checkSort(List,N,ind)==1:
            print("A sortat corect")
        else:
            print("A sortat gresit")
        List=temp.copy()#
    start = time.time()
    if ind==1 and bubblesortC(List)==0:
        print("Time Required for bubblesort: Cannot sort")
    elif ind==-1 and bubblesortD(List)==0:
        print("Time Required for bubblesort: Cannot sort")
    else:
        stop = time.time()
        print('Time Required for bubblesort:', (stop - start))
        if checkSort(List,N,ind)==1:
            print("A sortat corect")
        else:
            print("A sortat gresit")
    List=temp.copy()
    if typ!='c' and typ!='s' and typ!='d':
        start=time.time()
        countSort(List,ind)
        stop=time.time()
        print("Time Required for countsort:", stop-start)
        #print(List)
        if checkSort(List,N,ind)==1:
            print("A sortat corect")
        else:
            print("A sortat gresit")
        List=temp.copy()
    
    start=time.time()
    if ind==1:
        List=mergesortC(List)
    else:
        List=mergesortD(List)
    stop=time.time()
    #print(List)
    print("Time Required for mergesort:", stop-start)
    if checkSort(List,N,ind)==1:
        print("A sortat corect")
    else:
        print("A sortat gresit")
    List=temp.copy()
    start=time.time()
    if ind==1:
        List.sort()
    else:
        List.sort(reverse=True)
    stop=time.time()
    print("Time required for sort in python:",stop-start)
    if checkSort(List,N,ind)==1:
        print("A sortat corect")
    else:
        print("A sortat gresit")
if __name__ == '__main__':
    
    arr=[]
    fis=open("fis.txt","r")
    testsNum=fis.readline()
    for line in fis:
        temp=line.split()
        tup=[]
        tup.append(int(temp[0]))
        tup.append(int(temp[1]))
        tup.append(temp[2])
        tup.append(temp[3])
        arr.append(tup)
    for case in arr:
        N=case[0]
        maxim=case[1]
        caz=case[2]
        typ=case[3]
        print(N,maxim,caz,typ)
        start(N,maxim,caz,typ)
