# Shell-Programming

	
Shell Script 기초_(변수, #!/bin/sh, 주석, 출력(echo), 값 비교)   낙서장  
2015.09.08. 16:49
복사http://blog.naver.com/birhday/220475439145
전용뷰어 보기
1. 번역기 지정
- Shell Script 가장 첫줄에 명시하며 리눅스에게 스크립트를 실행하기 위한 번역기를 알려주는 역할
ex) #!/bin/sh
     #!/bin/bash
 
 
2. 출력 명령(echo)
- echo는 prinf 같은 역할
 
- echo -n 은 자동개행을 막아줌
 
ex) echo "Hello World"
ex) echo -n "."
     echo -n "."
 
 
3. 주석
- 첫 줄을 제외한 #으로 시작하는 모든 라인은 주석
ex)
#!/bin/sh
#주석은 프로그램에 영향을 주지 않음
echo "Hello World"
 
 
4. 지역변수
​ex)
#!/bin/sh
a=20;                                         -> 변수=값 사이에 space 없어야 함
echo "The value of a is $a"          -> 변수 값 출력은 $를 붙여서 사용
 
 
5. 환경변수
- etc/profile과 ~/.bash_profile 에 정의되어 있음
​
​ex>
#!bin/sh
path=$PATH
y=$SHELL
 
echo "test path is $path"
echo "Shell is $y"
 
결과 : 환경 설정에 따라 다를 수 있음
test path is /sbin:/usr/sbin:/bin:/usr/bin
Shell is /bin/bash
 
 
6. 변수 값 대입
- 변수=$(값)의 구조
- expr은 수식연산 실행 명령어
 
ex>
#!/bin/sh
 
x=$(string value)
y=2
z=$(expr $y + 4)
 
echo "x is $x"
echo "z is $z"
 
결과>
x is string value
y is 6
 
 
7. 비교
1) 숫자
x -eq y   x가 y와 같은지 체크
x -ne y   x가 y와 같지 않은지 체크
x -gt y   x가 y 보다 큰지 체크
x -lt y   x가 y 보다 작은지 체크
( -le : 작거나 같은지 / -ge 크거나 같은지 )
2) 문자
x = y   문자열 x가 문자열 y와 같은지 체크
x != y  문자열 x가 문자열 y와 다른지 체크
-n x   문자열 x가 널 문자가 아니면 true로 간주함
-z x   문자열 x가 널 문자이면 true로 간주함.
[출처] Shell Script 기초_(변수, #!/bin/sh, 주석, 출력(echo), 값 비교)|작성자 birhday
