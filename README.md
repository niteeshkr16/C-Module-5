# Module-5

---

# 5a : C program to find  Largest of Three Numbers Using Pointer.

## AIM:
To write a C program to find  Largest of Three Numbers Using Pointer:

## ALGORITHM:
1. Start
2. Read three integers: a, b, c
3. Assign pointers to each variable
4. If value at pointer to a is greater than both b and c:
- Print value at pointer to a
5. Else if value at pointer to b is greater than both a and c:
- Print value at pointer to b
6. Else:
- Print value at pointer to c
7. End

## PROGRAM:
```
#include <stdio.h>
int main()
{
    int num1, num2, num3;
    scanf("%d %d %d", &num1, &num2, &num3);
    int *num1_ptr, *num2_ptr, *num3_ptr;
    num1_ptr = &num1;
    num2_ptr = &num2; 
    num3_ptr = &num3;
    if ((*num1_ptr > *num2_ptr) && (*num1_ptr > *num3_ptr))
        printf("Largest = %d", *num1_ptr);
    else if ((*num2_ptr > *num1_ptr) && (*num2_ptr > *num3_ptr))
        printf("Largest = %d", *num2_ptr);
    else 
        printf("Largest = %d", *num3_ptr);
}

```

## OUTPUT:
<img width="803" height="297" alt="Image" src="https://github.com/user-attachments/assets/c85ffb00-1bd4-4ced-b327-35187eb26772" />

## RESULT:
Thus, the program has been executed successfully.

---

# 5b : C program to swap any two values function pointers (using temporary variable).

## AIM:
To write a C program to swap any two values function pointers (using temporary variable). 

## ALGORITHM:
1. Start
2. Read integers m and n
3. Assign pointers to m and n
4. Print original values
5. Store value at m_ptr in temp
6. Assign value at n_ptr to m_ptr
7. Assign temp to n_ptr
8. Print swapped values
9. End

## PROGRAM:
```
#include <stdio.h>
int main()
{
    int m, n, temp;
    scanf("%d %d", &m, &n);
    int *m_ptr, *n_ptr;
    m_ptr = &m;
    n_ptr = &n;
    printf("m is %d, n is %d", *m_ptr, *n_ptr);
    temp = *m_ptr;
    *m_ptr = *n_ptr;
    *n_ptr = temp;
    printf("\nm is %d, n is %d", *m_ptr, *n_ptr); 
}
```

## OUTPUT:
<img width="800" height="311" alt="Image" src="https://github.com/user-attachments/assets/736e7850-195d-4268-8cc6-954d51fc9b46" />

## RESULT:
Thus, the program has been executed successfully.

---

# 5c : C Program to find the maximum element in each row of a matrix.

## AIM:
To write a C Program to find the maximum element in each row of a matrix.

## ALGORITHM:
1. Start
2. Read rows and cols
3. Read elements into a 2D array
4. For each row:
- Initialize max to first element
- For each column in that row:
- If current element > max, update max
- Print max for that row
5. End

## PROGRAM:
```
#include <stdio.h>
int main()
{
    int index1, index2, max = 0;
    scanf("%d %d", &index1, &index2);
    int arr1[index1][index1];
    for (int i = 0; i < index1; i++)
    {
        for (int j = 0; j < index2; j++)
        {
            scanf("%d", &arr1[i][j]);
            if ((arr1[i][0] > arr1[i][1]) && (arr1[i][0] > arr1[i][2]))
                max = arr1[i][0];
            else if ((arr1[i][1] > arr1[i][0]) && (arr1[i][1] > arr1[i][2]))
                max = arr1[i][1];
            else 
                max = arr1[i][2];
        }        
        printf("Maximum element of the row %d is: %d\n", i+1, max);    
    }
}
```

## OUTPUT:
<img width="1133" height="351" alt="Image" src="https://github.com/user-attachments/assets/936a13dd-70a3-4e11-aea8-5642dfca76f9" />

## RESULT:
Thus, the program has been executed successfully.

---

# 5d : C program to concatenate the two strings using pointers.

## AIM:
To write a C program to concatenate the two strings using pointers.

## ALGORITHM:
1. Start
2. Read string str1 and str2
3. Assign pointers to str1 and str2
4. Concatenate str2 to str1 using strcat()
5. Print the concatenated string
6. End

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int main()
{
    char ch1[100], ch2[100];
    scanf("%s %s", ch1, ch2);
    char *ch1_ptr, *ch2_ptr;
    ch1_ptr = ch1;
    ch2_ptr = ch2;
    strcat(ch1_ptr,ch2_ptr);
    printf("After concatenation the strings are\n");
    printf("%s", ch1_ptr);
}
```

## OUTPUT:
<img width="1136" height="246" alt="Image" src="https://github.com/user-attachments/assets/cce20a66-3058-4945-934f-62dd653694a7" />

## RESULT:
Thus, the program has been executed successfully.

---

# 5e : C program to find 222122 number is palindrome or not using recursion.

## AIM:
To write a C program to find 222122 number is palindrome or not using recursion.

## ALGORITHM:
1. Start
2. Read num
3. Set temp = num, rev = 0
4. While temp ≠ 0:
- digit = temp % 10
- rev = rev * 10 + digit
- temp = temp / 10
5. If rev == num:
- Print "Palindrome"
6. Else:
- Print "Not a palindrome"
7. End


## PROGRAM:
```
#include <stdio.h>
#include <math.h>
int pali(int a)
{
    int rem = a % 10;
    static int i = 6;
    if (rem != 0)
        {
            return (rem*pow(10,--i) + pali(a/10));
        }    
    else 
        return 0;
}
int main()
{
    int num1 = 222122;
    int check = pali(num1);
    if (check != num1)
        printf("%d is NOT palindrome number.", num1);
    else
        printf("%d is palindrome number.", num1); 
}
```

## OUTPUT:
<img width="806" height="164" alt="Image" src="https://github.com/user-attachments/assets/ab1e1d4c-20d3-4eed-a975-4ca750c55dfc" />

## RESULT:
Thus, the program has been executed successfully.

---
