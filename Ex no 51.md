# EX 51 C program to reverse a string.
## DATE:
## AIM:
To write a C program to reverse a string.

## Algorithm
1. 1.Initialize two pointers:
2. One pointer start at the beginning of the string (index 0).
3. Another pointer end at the last character of the string (index length - 1).
4. Loop through the string:
5. While start is less than end, swap the characters at the start and end positions.
6. Increment start and decrement end to move towards the middle of the string.
7. Terminate when start is no longer less than end
8. Output the reversed string.

## Program:
```
#include<stdio.h>
#include<string.h>
void reverseString(char str[]){
    int n=strlen(str);
    for(int i=0;i<n/2;i++){
        char temp=str[i];
        str[i]=str[n-i-1];
        str[n-i-1]=temp;
    }
}
int main(){
    char str[100];
    fgets(str,sizeof(str),stdin);
    printf("Input String: %s",str);
    str[strcspn(str, "\n")] = '\0';
    reverseString(str);
    printf("Reverse String: %s\n",str);
    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/0ae1b183-e62e-47eb-9b8a-e9d8e6e2499e)

## Result:
Thus the program was executed and the output was verified successfully.
