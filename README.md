a=[0,1,1,0,1,1]
b=[0,1,1,1,1,0]

TP=0
FN=0
TN=0
FP=0
for i in range(len(a)):
    if a[i]==1 and b[i]==1:
        TP=TP+1
        print(i,a[i],b[i])
    elif a[i]==1 and b[i]==0:
        FN=FN+1
        print(i,a[i],b[i])
    elif a[i]==0 and b[i]==1:
        FP=FP+1
        print(i,a[i],b[i])
    elif a[i]==0 and b[i]==0:
        TN=TN+1
        print(i,a[i],b[i])
    else:
        pass  
accuracy=(TP+TN)/len(a)
TPR = TP/(TP+TN)
TNR = TN/(TN+FN)

print("accuracy",accuracy)
print("Sensitivity:",TPR)
print("Specificity:",TPR)
