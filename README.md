# Java
#### 인프런 <예제로 공부하는 JAVA100>
java 공부 및 자료구조와 알고리즘

문제.1  자바 학습을 위한 환경설정에 대한 내용이다.  순서를 올바르게 맞춰보시오.
-------------------------------------------------------------------------------------------
	1. JDK를 설치한다.
	2. 소스코드 편집기(에디터) 자바가 실행될 수 있도록 환결설정을 해준다.
	3. 내 pc가 32비트인지 64비트인지 확인한다.
	4. 편리한 자바 소스코드 작성을 위한 자신에게 맞는 소스코드 편집기(에디터)를 설치한다.
	5. 내 pc 내 어떤 디렉토리에서도 자바가 실행될 수 있도록 패스 설정을 한다.

	정답 : 3 - 1 - 5 - 4 - 2

문제.2 내 pc에 JDK를 설치하고 어떤 디렉토리에서도 자바가 실행될 수 있도록 패스 설정을 하시오.
	그런 후 "명령 프롬프트" 모드에서  java 라고 입력하여 아래 결과처럼 나오도록 한다.
	
	
	
		정답 : 비트 확인 -> 오라클 공식 홈페이지에 접속 후 Java SE의 JDK를다운 -> 검색창에 고급 시스템 설정 검색 후 환경 변수라는 메뉴를 클릭 하여 패스 설정을 해줌
		 
![image](https://user-images.githubusercontent.com/69742511/158386323-dca1ab7b-d0c0-4d28-b2a6-1ef24b232da0.png)

문제.3  명령 프롬프트 창에서 javac -version을 입력하고 엔터치면 에러가 나는데 그 이유를 설명하시오.

	정답 : 패스설정을 할 때 시스템 변수의 Path 안에 JDK 경로를 설정해 줘야하는데 이 설정이 안되어 있어서 오류가 발생함.

문제.4 
	1. 자바 코드가 작성이 되어져서 최종 실행이 되는 과정을 설명하시오.
	2. 파이썬 언어와 비교해서 설명해보시오.
	3. 자바와 파이썬으로 작성한 코드를 저장할 때 확장자는 어떻게 저장하는지 말해보시오.
	
	정답 : 
		[1] 자바 언어(컴파일 언어)
			자바 코드 작성(Test.java) -> 자바 코드 컴파일(Compile)(Test.class) -> 자바 코드 실행(Run)(Test)
			
			참고 : javac는 Compile할 때 사용되며, Compile 후 Test.class 파일을 생성함
			
		[2] 파이썬 언어(인터프리터 언어)
			파이썬 코드 작성(Test.py) -> 파이썬 코드 실행(Run)

문제.5 자바 소스 코드 작성 및 실행을 위한 Tool(Notepad++)을 설치하고 자바 코드 실행을 하기위한 옵션 설정을 하시오.
 정답 : 노트패드++ 공식 사이트에서 다운을 받고 plugins에서 설정해주면 됨
	Plugins는 컴파일 하도록 해주는 설정을 할 수 있음

문제.6 자바의 기본적인 코드를 작성한 것인데 에러가 많이 나온다. 에러를 모두 찾아서 수정하시오.

	[code]
	public class java100_variable_HelloWorld {
			public static void main(string[] args) {
				system.out.println('Hello World~')
			}
		}
	정답 : 
	[code]
	public class Java100_variable_HelloWorld {
			public static void main(String[] args) {
				System.out.println("Hello World~");
			}
		}
	

문제.7 자바의 기본적인 코드 구성에서 각 키워드를 간략히 설명하시오.
	[code]
	public class java100_variable_HelloWorld {
			public static void main(String[] args) {
				System.out.println("Hello Java~^_^");
			}
		}
	
	정답 :  
	[code]
	접근제어자 클래스선언 클래스이름 {
			접근제어자 static 반환타입 메서드명(파라미터) {
				구현할 코드 작성
			}
		}
	
	접근제어자 : public, private, protected, default // 클래스나 메서드에 접근할 수 있는 범위를 지정
		Private -> protected -> public 순서
		Public : 접근 제한이 없음
		Private : 권한이 있을때만 사용 가능
	
	클래스선언 : class // 객체를 생성하는 틀, 프레임, 공장
	
	클래스이름 : 카멜케이스(단어와단어 사이의 구분을 대문자로)
	
	메서드이름 : 메서드란? 함수(어떤 특정한 동작이나 작업, 행위 등을 수행하는 것.)
	
	파라미터 : 메서드에 들어가는 인자값

문제.8 자바의 메인 메서드를 작성한 코드에서 틀린 곳을 찾아서 모두 수정하시오.

	[파일명 : Java100_variable_HelloWorld3.java]
	public class Java100_variable_HelloWorld {
		public void main_method(String[] gaddonge) {
			System.out.println("Hello World~");
		}
	}

	정답 :
	[파일명 : Java100_variable_HelloWorld3.java]
	public class Java100_variable_HelloWorld {
		public static void main(String[] gaddonge) {
			System.out.println("Hello World~");
		}
	}
	
	메인메서드(main()) : 
		1. 만약 다르게 작성하면 기본 메서드(main())를 찾을 수 없다라고 에러 발생 함.
		2. Java 프로그램이 실행되면 제일 먼저 메인 메서드를 찾아서 실행.
		3. 길게 작성된 소스에서 그 프로그램의 시작이 어딘지 알 수 없으면 안되르모 시작점을 알려주는 용도
	
	파라미터스 :
		1. 메서드(함수) 호출시 하나 or 둘 이상의 파라미터 값을 넣어서 호출할 수 있음. 이러한 인수(파라미터)들의 값을 저장할 변수들을 명시.
		2. String(문자열) --> [ ](배열) --> args(변수명)
		Args는 하나의 변수명일 뿐이므로 임의의 이름을 지정해도 무방.
	
	반환할타입 :
		return type--> 반환할 값이 있냐? 없냐? --> 없으면 void(빈 공간,empty)
		Void 메서드(함수)는 호출하면 결과로써 특별히 반환되는 값은 없이 수행되는 메서드.
	
