# Java 스터디
기본기가 중요하다. 기본서를 통해 문법 숙지 및 활용

<br>

## 📒 책 소개
Do it! 자바 완전 정복

<br>

## ⏱️ 공부 기간
2023.10.26 ~ 2023.12.26

<br>

## 📌 주차 별 학습

#### 1주차(10.26 ~ 10.28) : 자바 시작하기, 자료형, 연산자
#### 2주차(10.29 ~ 11.04) : 제어문과 제어 키워드, 참조 자료형
#### 3주차(11.05 ~ 11.11) : 클래스와 객체, 클래스 내부 구성 요소
#### 4주차(11.12 ~ 11.18) : 클래스 외부 구성 요소, 자바 제어자, 클래스의 상속과 다형성
#### 5주차(11.19 ~ 11.25) : 자바 제어자, 이너 클래스와 이너 인터페이스
#### 6주차(11.26 ~ 12.02) : 예외 처리, 쓰레드(1/2), 쓰레드(2/2)
#### 7주차(12.03 ~ 12.09) : 제네릭, 컬렉션 프레임 워크(1/2), 
#### 8주차(12.10 ~ 12.16) : 컬렉션 프레임 워크(2/2), 람다식
#### 9주차(12.17 ~ 12.23) : 자바 입출력(1/2), 자바 입출력(2/2)

<br>

## 💡 학습 내용

### 1. 자바 시작하기

### == 프로그래밍 언어 == 

<br>

고급언어:   C, C++, JAVA <br>
기계어:    2진 데이터(010101001) 컴퓨터가 직접 알아들을 수 있는 언어 <br>
어셈블리어: 기계어와 1대1로 대응 <br>

자바 8에서 람다식, 인터페이스 내의 정적 메서드, 디폴트 메서드 등 중요한 버전!

자바는 어떻게 높은 점유율을 얻으면서 개발자에게 사랑받게 되었을까?
1. 플랫폼 독립성
2. 객체지향 언어
3. 함수형 코딩 지원
4. 분산 처리 지원
5. 멀티 쓰레드 지원
etc..

<br>

> 플랫폼 독립성이란?

.exe .app .sh 확장자를 가진 파일들은 플랫폼 종속성이다

자바도 .class는 자바 가상 머신(JVM) 덕분에 플랫폼 독립성을 이루었다

당연히도 각 플랫폼마다 각각 자바 가상 머신을 설정해야된다

<br>

> 자바 개발 도구 JDK? 자바 실행 환경 JRE?

JDK는 자바를 이용해 프로그램을 개발하는 데 필요한 도구를 모아 둔 집합
JRE는 완성된 프로그램을 실행하는데 필요한 환경

자바 가상 머신 ⊂ 자바 개발 환경 ⊂ 자바 개발 도구 

<br>

> 자바 소스 코드의 실행 과정

.java 소스 파일 생성  <br>
=>(파일 저장시 자동 컴파일) .class 바이트 코드 파일 생성  <br>
=>(실행) JVM 메모리 할당  <br>
=>(메서드 영역에 클래스 로딩) main()메서드 실행

<br>

> 메모리 영역?

1. 메서드 영역 == 클래스 영역 == 정적 영역 == 상수 영역
2. 스택 영역
3. 힙 영역

<br><br>

__자바의 기본 구조__

```
public class P_1027 {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

<br>

__주석__

```
public class P_1027 {
    public static void main(String[] args) {
        //System.out.println("Hello World");
    }
}
```

<br>

> 패키지 선언부

패키지를 지정하면 반드시 첫 줄에 패키지 선언이 와야한다 <br>
BUT 
<br>
패키지를 지정하지 않았으면, 디폴트 패키지를 사용한다면 __패키지 선언이 생략된다__

<br>

> 클래스 선언부
```
class  : 클래스라는 것을 알려주는 java 키워드
P_1027 : 클래스명
```

public은 다른 패키지에서도 사용할 수 있는 접근 지정자
<br>
접근지정자는 9장에서 추가로 학습한다

1. 클래스명 == 소스 파일명
2. 하나의 소스 파일에 최대 1개의 public 클래스만 존재

<br>

> main() 메서드

```
void : 리턴 타입
main : 메서드 명
```

static은 정적 메서드를 가르킴(전체코드 위에 있음)

<br>

바이트코드(.class)가 메서드 영역에 로딩되면 JVM은 main() 메서드 부터 찾는다

<br>

> 출력 방법

```
public class P_1027 {
    public static void main(String[] args) {
        System.out.println("");  // 1
        System.out.print();      // 2
        System.out.printf();     // 3
    }
}
```


<br>
<br>

---


### 2. 자료형

### == 변수와 자료형 == 

<br>

> 자료형 선언

컴파일언어는 변수를 사용하기 전에 반드시 자료형 선언

__주의__
1. 자료형 사용하기 전에 반드시 자료형 선언
2. 자료형은 반드시 한번만 선언

<br>

> 변수 선언과 함께 값 대입하기

```
int a = 3
```

<br>

> 변수 선언과 값 대입 분리하기

```
int a;
a = 3;
```

<br>

> 자료형

기본 자료형 : boolean, byte, short ,int, long, float, double, char 
<br>
참조 자료형 : 배열, 클래스, 인터페이스

<br>

> 구분 이유?

기본자료형과 참조 자료형의 값 저장 방식이 다르다

<br>

> 메모리 구조

1. 클래스(class) 영역
2. 정적(static) 영역 -> 변수들이 저장되는 공간
3. 상수 영역
4. 메서드(method) 영역 -> 객체들이 저장되는 공간

<br>

> 실제 데이터값의 저장 위치

기본 자료형 : 스택 메모리에 생성된 공간에 실제 변숫값을 저장한다
참조 자료형 : 실제 데이터값은 힙 메모리에 저장하고, 스택 메모리의 변수공간에는 실제 변숫값이 저장된 힙 메모리의 위칫값을 저장한다.

<br>

부울대수 자료형 - boolean
<br>
정수 자료형 - byte, short, int, long 각각 1byte, 2byte, 4byte, 8byte

<br>

> 자동 타입 변환(Auto type casting)

```
    byte a = 3;
    short b = 3;
    int c = 3;
    long d = 3L;
    long e = 3;  // 자동 타입 변환 -> __업캐스팅__
    byte f = 30; // 저장할 수 없는 범위의 정숫값이 입력되면 int 인식 -> 오류 발생
```

<br>

> 타입 변환(Type casting)

```
    int value1 = (int)5.3; (int)5.3 = 5
    long value2 = (long)10;
    float value3 = (float)5.8;
    double value4 = (double)16;

    long value5 = 10L;
    long value6 = 10l;
    float value7 = 5.8F;
    float value8 = 5.8f;
```

> 기본 자료형 간의 연산

CPU 연산 최소 단위가 int이므로 int보다 작은 자료형도 일단 int로 읽어와서 연산 수행


