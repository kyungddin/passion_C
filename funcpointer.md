# 함수 포인터와 void 포인터에 대해 공부


### 1. 함수 포인터

1. 함수는 프로그램 실행 시 code 영역에 할당된다
2. 그러므로 함수도 주소가 있으며, 함수이름이 그 주소값을 의미한다
3. 함수 포인터의 type은 반환형과 매개변수 선언형태를 기준으로 구분한다
4. ex: int SoSimple(int num1, int num2) -> int (*fptr) (int, int) & fptr = SoSimple;


### 2. void 포인터

1. void형 포인터 변수는 어떠한 type의 주소도 담을 수 있으며, 함수의 주소도 담을 수 있다
2. but void형 포인터로는 포인터 연산이 불가능하다 (가리키는 대상의 조작, 또는 주소 연산)