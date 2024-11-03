# 포인터의 포인터 


### 1. what is double pointer?

1. 포인터 변수를 가리키는 포인터.. 즉 포인터 변수의 주소를 가리키는 변수이다
2. 이때 가리키는 포인터가 가리키는 값을 불러오려면 **dptr을 해주면 된다
3. call by reference 시에 유용하게 활용된다 (PointerSwap)

  #include <stdio.h>

  void SwapIntPtr(int **dp1, int **dp2)
  {
    int *temp = *dp1;
    *dp1 = *dp2;
    *dp2 = temp;
  }

  int mian(void){
    int num1 = 10, num2 = 20;
    int *ptr1, *ptr2;
    ptr1 = &num1, ptr2 = &num2;
    printf("*ptr1, *ptr2: %d %d \n", *ptr1, *ptr2);
    
    SwapIntPtr(&ptr1, &ptr2);
    printf("*ptr1, *ptr2: %d %d \n", *ptr1, *ptr2);
    return 0;
  }
