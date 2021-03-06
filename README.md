# java 

### class
```
동일한 속성과 행위를 수행하는 객체의 집합
객체 : 필드, 메소드
```

<br>

### 접근 제어자
```
접근 제어자를 통해 변수, 메소드, 생성자에 대한 접근 권한을 지정할 수 있다.
종류는 public, private, protected, default가 존재한다. 
```
<img width="876" alt="접근제어자" src="https://user-images.githubusercontent.com/99054659/164952723-526a1bbb-cd3b-4c8c-9927-e354984cdbcd.png">

<br>

### static
```
static - class method
no static - instance method
```

static은 클래스에 고정된 멤버로서 클래스 로더가 클래스를 로딩하면 메모리에 할당 시켜준다. <br><br>
사용이유 : 전역적으로 쉽게 재사용하는 멤버나 잘 변하지 않는 변수, 메소드들에 주로 사용된다. <br>
만들어 놓고 클래스 호출, 객체 생성을 따로 할 필요없이 바로바로 사용할 수 있기 떄문에 사용성이 좋다. <br>
하지만 static은 메모리 자원을 할당해놓고 사용하는 것이기 떄문에 너무 많이 사용한다면 메모리를 많이 차지하게 되어 프로그램이 무거워질 수 있다.

<br>

### OOP(Object Oriented Programming)
```
문제를 여러 개의 객체 단위로 나눠 작업하는 방식으로, 객체들이 서로 유기적으로 상호작용하는 프로그래밍 이론이다.
```
장점
1. 코드 재사용성 증가
2. 생산성 향상
3. 유지보수의 우수성

<br>

단점
1. 개발속도가 느림
2. 실행속도가 느림
3. 코딩 난이도 상승

<br>

### 인스턴스(instance)란

설계도를 바탕으로 소프트웨어 세계에 구현된 구체적인 실체 즉, 객체를 소프트웨어에 실체화 하면 그것을 '인스턴스'라고 부른다. <br>
실체화된 인스턴스는 메모리에 할당된다.

<img width="757" alt="인스턴스" src="https://user-images.githubusercontent.com/99054659/164957609-7f1bf93d-20db-45c2-943e-91f0c5736f64.png">

<br>

### 상속(inheritance)란
```
부모가 자식에게 물려주는 행위로서 부모(상위) 클래스의 멤버를 자식(하위) 클래스에 물려주어 자식 클래스가 갖고 있는 것처럼 사용
```

장점
1. 코드 중복 감소
2. 유지 보수 시간 감소

<br> 

### this

```
현재 클래스 안의 개체를 가져오는 참조 변수 
```

<br>

### super
```
자식 클래스에서 부모 클래스 개체를 가져오는데 사용하는 참조 변수
```

<br>

### Overloading
```
두 메서드가 같은 이름을 갖고 있으나 인자의 수자 자료형이 다른 경우
```

<br>

### Overriding
```
상위 클래스의 메서드의 이름과 용례와 같은 함수를 하위 클래스에서 재정의하는 것
```

<br>

### Interface 
```
동일한 목적 하에 동일한 기능을 수행하게끔 강제하는 것
자바의 다형성을 극대화하여 개발코드 수정을 줄이고 프로그램 유지보수성을 높이기 위해
인터페이스를 사용한다.
```

<br>

### Exception
```
프로그램 실행 시 아래와 같은 다양한 오류가 발생할 수 있다.
- 파일을 읽는 프로그램을 실행시켰으나 파일을 찾을 수 없는 경우
- 문자열을 숫자로 변환하는 프로그램을 실행했으나 숫자로 변환할 수 없는 문자열인 경우
- 배열의 범위를 벗어나는 경우
```

<br>

```
public class trycatchTest {
 
    public static void main(String[] args) {
    
        // try : 안에 있는 코드들이 에러가 발생하는 경우 catch문으로 전달합니다.
        try {
            int [] num = new int[3];
        
            System.out.println("num 배열의 최대 길이는 3입니다.");
        
            num[4] = 0;
            System.out.println("num[4] 에 값을 입력했습니다.");
            
        // catch : try에서 발생한 예외처리를 진행합니다.
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("배열 길이가 맞지 않습니다.");
            
        // finally : 예외처리가 발생여부를 떠나 무조건 실행하도록 하는 구문
        } finally {
            System.out.println("배열을 다시 선언합니다");
            int [] num = new int[5];
            
            num[4] = 0;
            
            System.out.println(num[4]);
        }
        
        System.out.println("프로그램을 종료합니다");
    }
}

```

















