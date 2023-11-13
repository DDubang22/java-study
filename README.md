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

<br>

> 같은 기본 자료형 간의 연산 결과

| 연산                        | 결과         |
|----------------------------|------------|
| byte 자료형 + byte 자료형     | int 자료형    |
| short 자료형 + short 자료형   | int 자료형    |
| int 자료형 + int 자료형       | int 자료형    |
| long 자료형 + long 자료형     | long 자료형   |
| float 자료형 + float 자료형   | float 자료형  |
| double 자료형 + double 자료형 | double 자료형 |

<br>

> 서로 다른 기본 자료형 간 연산 결과

| 연산                        | 결과         |
|----------------------------|------------|
| byte 자료형 + short 자료형    | int 자료형   |
| byte 자료형 + int 자료형      | int 자료형    |
| short 자료형 + long 자료형     | long 자료형   |
| int 자료형 + float 자료형     | float 자료형   |
| long 자료형 + float 자료형   | float 자료형  |
| float 자료형 + double 자료형 | double 자료형 |


<br>
<br>

---


### 3. 연산자

### == 연산자의 종류 == 

<br>

> 산술 연산자 : +, -, *, /, % (사칙연산 및 나머지 연산) 

<br>

> 증감 연산자 : ++, -- (값이 1씩 증가 및 감소)

<br>

> 비트 연산자 : &, | ~, ^ (비트 AND, OR, NOT, XOR)

<br>

> 시프트 연산자 : >>, <<, >>> ( 비트 단위의 이동)

<br>

> 비교 연산자 : <, >, <=, >=, ==, != ( 값의 크기 비교)

<br>

> 논리 연산자 : &&, ||, !, ^

<br>

> 대입 연산자 : =. +=. -=. *=, /=, &=. |=, >>=, <<=. >>>= ( 산술 연산 결과의 대입)

<br>

> 삼항 연산자 : (참 또는 거짓) ? x : y (참일 때 x, 거짓일 때 y)


<br>

<hr/>

### 4. 제어문

### 제어문 : 프로그램의 처리 순서를 바꾸는 것

<br>

> 선택 제어문 : if, switch

<br>

> 반복 제어문 : for, while, do-while

<br>

> 제어 키워드 : break, continue

<br>

<hr/>

### 5. 배열

### 1차원 배열

<br>

> 배열 : 동일한 자료형을 묶어 저장하는 참조 자료형

생성할 때 크기를 지정해야되고, 한 번 크기를 지정하면 절대 변경할 수 없는 특징을 가지고 있다.

<br>

> 배열 생성하기

```
int[] a;
double[] a;
String[] a;
```

<br>

> 모든 참조 자료형 객체는 힙메모리 생성 힙 메모리에 생성된다

```
new int[3];
new String[5];
```

> 배열 자료형 변수에 객체 대입하기

```
int[] a = new int[3];
```

```
int[] a;
a = new int[3];
```

>> 객체에 값 입력하기

index는 0부터 시작한다, 예를 들어 방이 3개면 0,1,2다.

```
int[] a = new in[3]
a[0] = 3;
a[1] = 4;
a[2] = 5;
```

<br>

배열의 저장 공간에 값을 대입하거나 읽을 때, 없는 인덱스를 사용하면 예외(Exception) 발생하고 프로그램은 종료된다.

```
System.out.println(a[2]);  // 5 출력
System.out.println(a[-1]); // 예외 발생 
System.out.println(a[3]);  // 예외 발생
```

<br>

> 배열의 길이

배열 참조 변수.length

<br>

### 2차원 정방 행렬 배열

가로 및 세로 방향의 2차원으로 데이터를 저장하는 배열이 2차원 배열이다.

```
// 배열의 선언 방법 1
int[][] array1 = new int[3][4];
int[][] array2;
array2 = new int[3][4];


// 배열의 선언 방법 2
int array3[][] = new int[3][4];
int array4[][];
array4 = new int[3][4];



// 배열의 선언 방법 3
int[] array5[] = new int[3][4];
int[] array6[];
array6 = new int[3][4];
```

<br>

> 배열 객체를 생성하고 값 대입하기

```
 int[][] a = new int[2][3];

a[0][0] = 1; a[0][1] = 1; a[0][2] = 1;
a[1][0] = 1; a[1][1] = 1; a[1][2] = 1;
```

<br>

### 문자열을 저장하는 String

> 객체 생성 방법

```
String 참조 변수명 = new String("문자열");
```

```
// String 객체 생성 1
String str1 = new String("hello");

// String 객체 생성 2
String str2 = "안녕하세요";
```

```
// 문자열 리터럴에 따른 생성 문자열 객체의 공유
public class P_1113 {
    public static void main(String[] args) {
        String str1 = new String("안녕");
        String str2 = "안녕";
        String str3 = "안녕";
        String str4 = new String("안녕");

        System.out.println(str1 == str2);
        System.out.println(str2 == str3);
        System.out.println(str3 == str4);
        System.out.println(str4 == str1);

        /** 출력 값
         *  false
         *  true
         *  false
         *  false
         */
    }
}
```

```
// 문자열의 '+' 연산자
public class P_1113 {
    public static void main(String[] args) {
        String str1 = "안녕" + "하세요";

        String str2 = "안녕";
        str2 += "하세요";

        String str3 = "안녕" + 3;
        String str4 = "안녕" + String.valueOf(3);

        System.out.println("str1 = " + str1);
        System.out.println("str2 = " + str2);
        System.out.println("str3 = " + str3);
        System.out.println("str4 = " + str4);

        /**
         *  str1 = 안녕하세요
         *  str2 = 안녕하세요
         *  str3 = 안녕3
         *  str4 = 안녕3
         */
    }
}
```

<br>

> String 클래스의 주요 메서드

| /                  | retrun type | method                                 | explanation                                                                                                      |
|---------------------|:-----------:|----------------------------------------|------------------------------------------------------------------------------------------------------------------|
| 문자열<br>길이         |     int     | length()                               | 문자열 길이                                                                                                      |
| 문자열<br>검색         |     char    | charAt(int index)                      | index 위치에서의 문자                                                                                            |
| 문자열<br>검색         |     int     | indexOf(int ch)                        | 문자열에 포함된 문자 또는 문자열의 위치를 앞에서부터 검색했을 때 일치하는 인덱스 값 (fromIndex는 검색 시작 위치) |
| 문자열 검색         |     int     | indexOf(int ch, int fromIndex)         | ``                                                                                                               |
| 문자열<br>검색         |     int     | indexOf(String str)                    | ``                                                                                                               |
| 문자열<br>검색         |     int     | indexOf(String str, int fromIndex)     | ``                                                                                                               |
| 문자열<br>검색         |     int     | lastIndexOf(int ch)                    | 문자열에 포함된 문자 또는 문자열의 위치를 앞에서부터 검색했을 때 일치하는 인덱스 값 (fromIndex는 검색 시작 위치) |
| 문자열<br>검색         |     int     | lastIndexOf(int ch, int fromIndex)     | ``                                                                                                               |
| 문자열<br>검색         |     int     | lastIndexOf(String str)                | ``                                                                                                               |
| 문자열<br>검색         |     int     | lastIndexOf(String str, int fromIndex) | ``                                                                                                               |
| 문자열<br>변환 및<br>검색 |    float    | String.valueOf(boolean b)              | boolean, char, int, long, float, double 값을 문자열로 변환하기 위한 정적 메서드                                  |
| 문자열<br>변환 및<br>검색 |    float    | String.valueOf(char c)                 | ``                                                                                                               |
| 문자열<br>변환 및<br>검색 |    float    | String.valueOf(int i)                  | ``                                                                                                               |
| 문자열<br>변환 및<br>검색 |    float    | String.valueOf(long l)                 | ``                                                                                                               |
| 문자열<br>변환 및<br>검색 |    float    | String.valueOf(float f)                | ``                                                                                                               |
| 문자열<br>변환 및<br>검색 |    float    | String.valueOf(double d)               | ``                                                                                                               |
| 문자열<br>변환 및<br>검색 |    double   | concat(String str)                     | 문자열 연결(String 객체의 + 연산과 동일)                                                                         |
| 문자열<br>배열<br>변환    |    char[]   | toCharArray()                          | 문자열을 char[]로 변환                                                                                           |

<br>

• length() : 문자열의 길이를 리턴한다 <br>
• charAt() : 문자열에서 특정 인덱스를 위치해 있는 문자를 알아 낸다. <br>
• indexOf() : 문자열에서 특정 문자나 특정 문자열을 앞에서부터 찾아 위칫값을 알아낸다. <br>
• lastIndexOf() : 문자열에서 특정 문자나 특정 문자열을 뒤에서부터 찾아 위칫값을 알아낸다. <br>
• String.valueOf() : 기본 자료형을 문자열로 바꾸는 정적 메서드다. <br>
• concat() : 2개의 문자열을 연결한다. + 연산자와 동일한 기능을 수행한다. <br>
• toCharArray() : 문자열을 char배열로 변환한다. 자바 입출력 과정에서 주로 사용한다. <br>

<br>

| ////               | return type | method                                                            | explanation                                                                                                                  |
|------------------|-------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 문자열 수정      | String      | toLowerCase()                                                     | 영문 문자를 모두 소문자로 변환                                                                                               |
| 문자열 수정      | String      | toUpperCase()                                                     | oldChar 문자열을 newChar 문자열로 대체한 문자열 생성                                                                         |
| 문자열 수정      | String      | replace(char oldChar, char newChar)                               | beginIndex부터 끝까지의 문자열 생성                                                                                          |
| 문자열 수정      | String      | substring(int beginIndex) substring(int beginIndex, int endIndex) | beginIndex부터 endIndex - 1 위치까지의 문자열 생성                                                                           |
| 문자열 수정      | String[]    | split(String regex) split(String,regex, int limit)                | regex 기준으로 문자열을 분할한 문자열 배열을 생성(regex 구분 기호는 "\|" 기호로 여러 개 사용 가능, limit는 분할의 최대 개수) |
| 문자열 수정      | String      | trim()                                                            | 문자열의 앞뒤 공백 제거                                                                                                      |
| 문자열 내용 비교 | boolean     | equals()                                                          | 문자열의 실제 내용 비교 (==는 메모리 번지(stack) 비교)                                                                       |
| 문자열 내용 비교 | boolean     | equalsIgnoreCase(String anotherString)                            | 대소문자 구분 없이 문자열의 실제 내용 비교                                                                                   |

<br>
• toLowerCase(): 영문 문자를 모두 소문자로 변환한다. <br>
• toUpperCase(): 영문 문자를 모두 대문자로 변환한다. <br>
• replace(): 일부 문자열을 다른 문자열로 대체한다. <br>
• substring(): 문자열의 일부만을 포함하는 새로운 문자열 객체를 생성한다. <br>
• split(): 특정 기호를 기준으로 문자열을 분리한다. <br>
• trim(): 문자열의 좌우 공백을 제거한다. <br>
• equals(): 두 문자열의 위칫값이 아닌 실제 데이터값을 비교한다. 이때 대소문자를 구분한다. <br>
• equalsIgnoreCase(): 두 문자열의 위칫값이 아닌 실제 데이터값을 비교한다. <br>

<br>

<hr/>

### 6. 클래스와 객체

객체(Object)는 사용할 수있는 실체

> 클래스

객체를 만들기 위한 설계도

> 객체지향 문법 요소 : 클래스(Class)와 인터페이스(Interface)

> 클래스 : 일반 클래스와 추상 클래스(abstract class)

<br>

> 클래스 구조

```
class 클래스명 {
    ...
}
```

```
package ...;            // 1. 패키지
import  ...;            // 2. 임포트
class  클래스명 {...}     // 3. 외부 클래스

public class A { // <- A 파일명과 동일해야됨
    int a = 3;              // 1. 필드
    double abc() {...};     // 2. 메서드
    A() {...};              // 3. 생성자
    class 클래스명 {...}      // 4. 이너 클래스
}
```

<br><br>

> 클래스 외부 구성요소 : 패키지, 임포트, 외부 클래스

1. 패키지 : 

프로젝트 생성할 때 패키지를 지정했다면 이 구성 요소에 패키지명이 포함되며, 반드시 주석을 제외하고 첫 번째 줄에 위치해야 한다. 클래스의 생성 과정에서 패키지를 생성하지 않았다면, 즉 디폴트 패키지를 사용하면 생략된다.
<br>

2. 임포트 : 

다른 패키지의 클래스를 사용하고자 할 때 포함된다.

3. 외부 클래스 : <

클래스의 외부에 또 다른 클래스가 또 포함될 수 있다. 즉 1개의 .java 파일에 여러 개의 클래스가 포함될 수 있다는 것이다. 단, 외부 클래스에는 public 키워드를 붙일 수 없다.


<br>

> 클래스 내부 구성요소 : 필드, 메서드, 생성자, 이너 클래스

1. 필드 :

클래스의 특징(속성)을 나타내는 변수다.

2. 메서드 :   

클래스가 지니고 있는 기능(함수)를 나타낸다.

3. 생성자 :

생성자는 클래스의 객체를 생성하는 역할을 담당한다.

4. 이너 클래스 : 

클래스의 내부에도 클래스가 포함될 수 있다.

<br>

> 클래스와 객체 구분하기

비유를 하자면 클래스는 붕어빵 기계, 객체를 __붕어빵기계__ 로 찍어낸 붕어빵이라고 비유한다.   
우리가 붕어빵을 먹고 싶은데 붕어빵 기계를 먹을 수는 없다   
붕어빵하고 속 안 팥을 먹고 싶으면 찍어낸 붕어빵을 먹어야 한다 당연한 소리다.   
이것을 바꿔서 __클래스__ 와 __객체__ 로 설명하겠다.   

클래스에서 객체를 만드는 과정은 __생성자__ 가 수행한다. 위에서 언급한적 있다.   
클래스의 생성자로 __객체__ 를 만드는 과정을 __인스턴스화__ 라고 한다. 영어로는 instantiation   
인스턴스화로 만들어진 __객체__ 를 __인스턴스__ 라고 한다. 영어로는 __instance__   

__객체__ 안에는 클래스의 내부 구성요소(4가지) 중 __생성자__ 를 제외한 나머지 요소가 포함돼 있는데 __인스턴스 멤버__ 라고한다.   

__클래스는 바로 사용할 수 없고 반드시!! 객체를 생성해 객체 안에 있는 필드, 메서드 및 이너 클래스를 사용해야 한다.__   

> 객체의 생성과 활용

조금 더 깊게 들어가보자.  

> 객체 생성하기.

```
클래스명 참조 변수명 = new 생성자();

A a = new A();
```

참조 변수명은 실제 데이터를 저장하는 것이 절대 아니다. 헷갈리지 말자.   
실제 데이터가 있는 __힙 메모리의 위칫값__ 을 가리키는 변수다.   
new 키워드로 힙 메모리에 할당해 주는 것이다.   

실제 데이터를 저장하고 있는 객체를 힙 메모리의 어느 위치에 넣었는지를 알려 주지 않으면 그 객체를
쓸 방법이 없다, 그래서 위치값을 변수에 넣어서 알려주는 것이다.   
__A()생성자로 만든 객체를 힙 메모리에 넣고, 위칫값을 A타입의 참조 변수 a에 저장하라!__   

> 포인트 연산자

자바에서는 힙 메모리에 직접 접근할 수 있는 방법이 없으며, 위치 정보를 포함하고 있는 참조 변수를 이용해야 접근 가능할 수 있다.   

```
A a = new A();
System.out.println(a.m); // 필드 활용
a.print();               // 메서드 활용
```

<br>

<hr/>

### 7. 클래스 내부 구성 요소

> 필드와 지역 변수 구분

필드 : 클래스에 포함된 변수   
지역변수 : 메서드에 포함된 변수   

큰 차이점은 __메모리의 위치__ 이다   
필디는 힙 메모리의 객체내부, 지역변수는 스택 메모리에 생성된다.   
스택메모리에 저장되는 변수는 JVM에 자동으로 관리하지만, 힙 메모리 객체안에 생성되는 필드는 객체가 사라지지 않는 한 절대 삭제되지 않는다.   

또 다른 차이점은 필드와 지역 변수의 초깃값이다.   
필드는 직접 초기화하지 않아도 강제로 초기화한다.   
반면, 지역 변수는 직접 초기화하지 않으면 저장 공간이 그대로 있어 값 출력할 때 오류가 발생한다.   

<br>
<br>

> 메서드






