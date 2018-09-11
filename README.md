# Anagram1

list1=list(input().lower())
list2=list(input().lower())
list3=[]
#convert inputs to lowercase

for k in list1:
        if k ==" ":
            list1.remove(k)
for l in list2:
        if l == " ":
            list2.remove(l)
#remove spaces

          

if len(list1) != len(list2):
    print("No anagram!")
#Immediately not anagrams if words are different lengths.

else:            
    for i in list1:
        for j in list2:
            if i == j:
                list3.append(i)
                list2.remove(j)
              #Any letter from list1 that is found in list2 is added to list3. For an anagram this will be all letters.  

    if len(list1)==len(list3)and len(list2)==0:
        print("Anagram!")
    else:
        print("No anagram")
#list3 will be the same length as list1 in the case of anagram.
