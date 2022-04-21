### 1. basic

1. 프로그램 작성 언어   
    - 기계어: 0,1로 구성된 이진수 언어, CPU가 이해하고 처리하는 유일한 언어   
    - 어셈블리어: 기계어 명령을 ADD, SUB, MOVE등 상징적 단어인 니모닉 기호로 일대일 대응시킨 언어   
    - 고급언어: 인간이 이해하기 쉽고 복잡한 작업과 자료구조, 알고리즘 등을 표현하기 위한 언어 (절차지향 언어와 객체지향 언어)   
2. 컴파일   
    - 소스: PL언어로 작성된 텍스트 파일   
    - 컴파일: 소스코드를 기계어로 만드는 과정   
    - 소스 파일 확장자 -> 컴파일 된 파일의 확장자   
      자바: .java -> .class   
      C: .c->.obj->.exe / C++: .cpp->.obj->.exe   
3. 자바의 태동   
    - 1991 선마이크로시스템즈의 그린프로젝트(초기이름: 오크) -> 2009 선마이크로시스템즈를 오라클에서 인수   
      초기 목적: 내장형 시스템 충족을 위함(실시간 인터프리터로 속도가 느려 임베디드시스템 설계 실패)   
      이후 발전: 웹과 인터넷의 발전에 힘입고 퍼짐    
              <b>이유: 서로 다른 플랫폼에서 동일하게 동작 가능하며 독립적인 언어임   
                       당시 applet이라고 불리는 자바로 만든 웹브라우저 안에서 동작하는 프로그램 존재</b>   
4. 자바와 WORA   
    - WORA: Write Once Run Anywhere   
            한번 작성된 코드는 모든 플랫폼에서 바로 실행됨 (네트워크, 웹브라우저 등)     
            c++, c등의 프로그램 종속성 극복 (os, hw에 구애받지 않고 java프로그램 동일하게 실행됨)   
    - WORA가 가능한 이유: 2) Byte Code 2) JVM   
    
5. 플랫폼 종속성 (↔플랫폼 독립적)
    - 플랫폼 독립적: 생산성이 높음
      예시: 카카오톡이 OS, IOS버전이 있다고할 때,   
      사용자가 똑같은 프로그램에 대한 설치파일이 다르면 프로그램 종속적 아니면 독립적이라고 함   
    - 만일 플랫폼이 다를 경우 아래와 같이 비교할 수 있음   
    
|비교|타프로그램|자바|
|-----|---|---|
|기계어가 CPU마다 다름(컴파일)|n번|1번|
|운영체제마다 API다름(소스코드)|n번|1번|
|운영체제마다 실행파일 형식 다름(link)|n번|1번|

    - API와 Library   
    
|비교|정의|
|-----|---|
|API|논리적으로 .obj으로 되어있는 코드를 APP만들 때 호출함|   
|Library|특정 함수들이 이미 만들어져있고 사용자는 호출만 하면됨|   

*라이브러리 참고: 특정분야 APP만들 때 라이브러리가 없으면 모든 함수를 다 입력해야함.      
*플랫폼별 구성: 별로 동일 기능을 하지만 플랫폼이 다르므로 플랫폼별로 구성한 것임   
               jdk구성물(tools+jvm)이 플랫폼 종속적SW이다.   

#

### 2. 자바와 C/C++의 실행환경

|비교|자바|c/c++|
|-----|---|---|
|과정|컴파일러가 바로 바이트 코드한 후 링크과정 없음|컴파일러가 중간단계인 목적코드 생성|
|특징|jvm에서만 바이트코드 실행 가능|정적 라이브러리는 실행 파일에 포함됨(실행 파일 크기 커짐)|