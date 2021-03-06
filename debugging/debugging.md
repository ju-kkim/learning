# Debugging🐞

## 디버깅
컴퓨텨 프로그램, 소프트웨어 또는 시스템 내에서 버그를 찾고 해결하는 과정

## 디버거
디버그를 돕는 도구.  
주로 원하는 코드에 breakpoint를 지정하여 프로그램 실행을 정지하고, 메모리에 저장된 값을 살펴보며, 실행을 재개하거나, 코드를 단계적으로 실행하는 등의 동작을 한다.


## breakpoint란?
디버깅 목적으로 배치된 프로그램의 의도적인 중지 또는 일시중지 위치.  
프로그램 실행이 중단되어야 하는 시기를 결정.
`edit breakpoint`를 사용하여 특정한 조건일 떄 멈춤수 있다.

## watch 사용법
`+`클릭하여 확인 하고 싶은 변수나 조건문 등을 입력해 작동과정을 좀 더 세밀하게 관찰할 수 있다.

## call stack의 의미
실행하는 함수를 추적하는 공간. (후입선출 Last In First Out, LIFO)
실행하는 함수를 스택에 쌓아 올리고 함수를 다 실행하면 제거한다.

## Step
- ### Step 
    다음 명령어 실행  
    다음 디버거를 만날 때까지 스크립트 실행을 계속한다.  
    디버거가 더이상 없으면, 나머지 스크립트를 실행하고 끝난다.

- ### step over
    다음 명령어를 실행하되, 함수 안으로 들어가진 않는다  
    Step은 함수 내부로 진입해 함수 본문 첫 번째 줄에서 실행을 멈추는 반면, Step Over는 함수를 실행하지만, 함수 내부로 진입하진 않는다.  
    실행은 함수 실행이 끝난 후 즉시 멈춘다. 함수 호출 시 내부에서 어떤 일이 일어나는지 궁금하지 않을 때 유용하다

- ### step into
    함수로 진입해 모든 작업을 한 줄씩 검사  
    Step은 비동기 동작은 무시하는 반면, Step Into는 비동기 동작을 담당하는 코드로 진입하고, 필요하다면 비동기 동작이 완료될 때까지 대기한다.

- ### step out
    함수를 검사하고 해당 함수를 호출하는 라인으로 돌아간다  
    현재 실행 중인 함수의 실행을 계속 이어가다가 함수 본문 마지막 줄에서 실행을 멈춘다. 빨리 함수 실행을 끝내고 싶은 경우에 사용한다.