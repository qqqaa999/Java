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
	
문제.9 자바 메인 메서드에서 static 키워드의 역할에 대해서 설명해보시오.
	- Static을 안쓰면 에러가 나는데 그 이유가 무엇인지도 같이 설명해보시오.
	
	정답 : 
		1. Static으로 선언된 함수(메서드)나 변수는 자바 버추얼 머신에서 인스턴스 객체의 생성 없이 호출을 할 수 있다
			i. 즉, 객체 생성없이 해당 함수(메서드)를 호출해서 사용할 수 있다
		2. 자바 프로그램을 실행하면 static으로 지정된 메서드를 찾아서 먼저 메모리에 할당시킨다.
		3. Static으로 지정된 메서드가 여러개인 경우 객체를 생성하는 것과 상관없이 모두 메모리에 할당 시킴
		4. 그런 후에, main으로 만들어진 메서드가 있는지를 찾아서 그 메서드를 가장 먼저 시작점의 메서드로써 호출함

문제.10 변수와 변수 선언이란 무엇이고, 변수의 용도와 왜 필요한지 설명해보시오.
	- 변수란?
	- 번수 선언이란?
	- 변수의 용도와 필요한 이유

	정답 : 
		1. 변수란 데이터를 저장하는 메모리 공간 그리고 변하는 수
		2. 변수 선언이란 변수를 사용하기 위해서는 먼저 변수의 자료형에 맞는 자료형을 선언을 해줘야 함.
		3. 변수의 용도 : 데이터를 저장
		4. 왜 필요한가 :  무언가를 저장하고 활용하기 위해서 필요하다.

문제.11 자바의 데이터타입(자료형)에 대해서 각 타입의 사이즈와 함께 설명해 보시오.
	- 정수형의 경우 사이즈와 범위도 말해보시오.
	
	정답 : 
		기본형 타입과 참조형 타입
		
		기본형 타입(Primitive Data Type) 8개
			정수형 : byte(1byte), short(2byte), int(4byte), long(4byte)
			실수형 : float(4byte), double(8byte)
			문자형 : char(2byte)<문자 한 개 , 문자열을 다루는 타입은 없음>
			부울형(논리형) : boolean(1btye) --> true, false
			
		참조형 타입(Reference Data Type) 기본형에 속하지 않은 데이터 형들
			클래스(class), 배열(array), 인터페이스(interface), 문자열(String/immutable)
			참조형 변수의 특징 : 데이터가 저장된 메모리의 주소 값을 저장하는 변수임
		기본형은 데이터가 메모리에 저장되지만 참조형은 데이터의 주소값을 메모리해 저장함
![image](https://user-images.githubusercontent.com/69742511/158618822-428af13a-0d87-42e2-b529-f8f5d7bfdeb5.png)
문제.12 자바의 Primitive Data Type의 Byte 크기와 Bit 크기를 출력하는 코드를 구현하시오.
	- 정수형 타입과 문자형 타입에 대해서만 구현함
	- 이때, 각 타입의 최댓갑과 최솟값도 같이 구하여 출력하시오.
	- 아래 결과에서 문자형의 최댓값, 최솟값이 제대로 출력이 안되었는데 그 이유를 설명하고 수정하시오

	[결과 출력]
	
	
	정답 : 
	
	문자형 최댓값, 최솟값의 경우 숫자 타입이 아니어서 출력이 안됬음.
	
문제.13 정수, 실수 ,문자형 타입의 변수 사용에서 틀린 곳을 찾아서 모두 수정하시오.
	- 에러가 안나더라도 올바르게 수정해주시오.
	
	
 정답 : 
	
	
문제.14 기본형 타입의 값을 초기화한 아래의 코드에서 틀린 곳을 찾아 수정하시오.
	byte b = 100;
	short s = 30000;
	int i = 2100000000;
	long l = 700000000000;
	float f = 9.8;
	double d = 3.14;
	char c = 'A'
	boolean bl = false;
	
	정답 :
		byte b = 100;
		short s = 30000;
		int i = 2100000000;
		long l = 700000000000L;
		float f = 9.8F;
		double d = 3.14;
		char c = 'A'
		boolean bl = false;

문제.15 정수형 변수를 문자형으로 형(Type) 변환시켜서 출력하면 어떤 결과가 나오는지 말해보시오.
	
	1.
		short a = 'A';
		System.out.println(a);
		
	2.
		short b = 90;
		System.out.println( (char)b );
	3.
		char c ='C';
		System.out.println( (short)c );
	
	정답 : 
		1. 65
		2. Z
		3. 68
문제. 16 System.out.print(), println(), printf() 등에 대해서 예제를 통해 설명해보시오.
	- 이때 10진수 10에 대해서 8진수 16진수로 각각 출력해보시오.

	정답 : 
		Systme.out.printf("10진수 10은 8진수로 %o 이고, 16진수로는 %x이다.", 10,10);
			§ 출력 : 10진수 10은 8진수로 12 이고, 16진수로는 A이다. 
		- print() : 줄 바꿈이 없음
		- println() : 출력이 끝나면 줄 바꿈
		- printf() : 지시자를 사용 <%d(정수), %f(소수점 형식), %c(문자), %s(문자열),  %b(bool), %n(줄바꿈), %e(지수), %o(8진수), %x(16진수)>
			§ System.out.printf("저는 %d살의 대학생입니다.",b);
			§ 소수점 출력 같은 경우는 %f에서 %.(소수점 자리를 적어주면됨)f
![image](https://user-images.githubusercontent.com/69742511/158619013-e20fb0d5-00b0-48c5-bc63-3aa37b0b398f.png)
문제.17 정수형(int)을 문자열(String)로 변환하여 정수의 자릿수를 구하는 코드를 구현해보시오.
	- 정수 12345를 입력하면 자릿구가 "5"로 출력되도록 한다.
	
	정답 : 
		public static void main(String[] args) {
				int num = 12345;
				System.out.println(String.valueOf(num).length());
				System.out.println(String.valueOf(num) + 1);
				System.out.println("1"+(num+1)); // String으로 시작하는 경우 뒤에 있는 입력값 들도
				// String 이라고 인식하여 출력 값 1123451로 출력이 됨
					// --> 뒤에 정수들을 정수로 인식하게 하고 싶으면 
					System.out.println("1"+(num+1)); 가로를 해주면 됨.
				// length()는 문자열과 배열만 사용가능.
				// String.valueOf(변수)는 문자열로 바꾸어줌.
				// Integer.valueOf(변수)는 정수로 바꾸어줌.
			}
		
		}

문제.18 수치 연산자에 대해서 설명해보시오.
	
	정답 :
		public static void j_18(String[] args) {
			int a,b,c,d;
			a=60;b=8;c=300;d=400;
			System.out.println("a+b="+a+b); // 문자열로 인식
			System.out.println("a+b="+(a+b)); // 더하기 +
			System.out.println("a+b="+(a-b)); // 빼기 -
			System.out.println("a+b="+(a*b)); // 곱하기 *
			System.out.println("a+b="+(a/b)); // 나누기 /
			System.out.println("a+b="+(a%b)); // 나머지 %
		}

문제.19 축약된 형태의 연산자를 사용하요 변수 a의 값을 증가시켜보시오.
	정답 :
		public static void j_19(String[] args) {
				int a = 0, b =100;
				a = a + 1;
				System.out.println(a); // 1
				a += 1;
				System.out.println(a); // 2
				a++;
				System.out.println(a); // 3
				// ++,-- 연산자는 1씩 증가시킴.
			}
	
	
문제.20  수치 연산자를 사용한 연산에서 소수점 결과가 예상과 다르게 나오는 것을 설명해 보시오.
	- 아래의 코드 결과가 올바르게 나오도록 수정해보시오.

	public static void j_20(String[] args) {
		int a = 60, b = 8;
		int rst1 = a/b;
		System.out.println(rst1);
	}

	정답 :
		public static void j_20(String[] args) {
				int a = 60, b = 8;
				int rst1 = a/b;
				System.out.println(rst1); // 7
				System.out.println((float)a/b); // 7.5
				float rst2 = a/b;
				System.out.println(rst2); // 7 리턴 받는 자료형이 실수여도 리턴 받기전에 정수로 연산을
										// 하고 난 뒤어서 7로 출력이 됨/
				float rst3 = (float)a / b;
				System.out.println(rst3); // 7.5
				// 어느 한쪽의 값을 실수로 바꾸어주면 해결.
				double rst4 = 60/8;
				System.out.println(rst4); // 7 자료형이 실수형이어도 연산값들이 정수면 7이 출력됨.
				double rst5 = 60/8.0;
				System.out.println(rst5); // 7.5
				// 즉, 자료형에 따라 입력 값을 잘 적어줘야됨.
			}

문제.21 관계 연산자에 대해서 설명해보시오.
	// [!] : 관계 연산자 : ==, !=, >, >=, <, <=
	
	정답 : 
		- 관계 연산자의 결과는 참(true)과 거짓(flase)이 됨.
		- == : 같다, != : 같지 않다, >,< : 방향에 있는 수가 더 크다, >=,<= : 크거나 같다.

문제.22 논리 연산자에 대해 설명해보시오.
	
	정답 : 
		- &&(and), ||(or), !(not)
![image](https://user-images.githubusercontent.com/69742511/158619668-0f43bcbd-38e8-4810-82eb-d01c7ea6c6bf.png)

조건문 if, else, else if

	- 문법 : if (A 비교 연산자 B) { true시 실행 코드 }
		else if (A 비교 연산자 B) { 상위 조건이 거짓이고 현재 조건이 참일 때 실행 코드 }
		else { false시 실행 코드 } 
	- Tip { }가 없으면 한줄만 포함이 됨. --> 그냥 무조건 { }을 해주자.
	
Switch
// 입력 변수 조건은 byte, short, int, char, String이어야 하며 break,default를 빼먹지 않도록 주의하여야 함.
	- 문법 : switch(입력변수) {
		case (입력값1):
			실행될 코드 작성
			break;
		case (입력값2):
			실행될 코드 작성
			break;
		default:
			case에 해당되는 값이 하나도 없을 때 기본적으로 실행되는 코드 작성
			break;
	}

삼항 연산자
	삼항 연사자란 조건의 참과 거짓에 따라 어떤 연산을 할지 정해주는것
	- 문법 :(조건문) ? 참 : 거짓;
	- Ex) 
	int a = 10, b =20;
	int c = a < b ? a + 1 : b + 1;
	System.out.println(c); // 출력 11
		
반복문
	자바의 반복문 종류
		1. for문   2.  while문   3.  do ~ while문   4.  향상된 for문
		
	1.  for문 : 
	for(int=i; i<10; i++){
		실행 코드
	}
	for(변수 초기식; 조건식; 증감식) {
		조건식--> 참인 동안 실행
	}

	2. While문 :
	While(조건) {
		실행 코드
	}
	
	3. Do~while문 :
	// do~while문은 조건에 상관 없이 한번은 실행 됨
	do{
		실행 코드
	}while(조건식)

	4. 향상된 for 문 : 
	for(변수 :  배열명){
		실행 코드
	}
	// 배열의 값 하나하나가 변수에 대입되며, 배열의 인덱스 길이 만큼 반복함

배열
	- 배열이란 동일한 데이터 타입의 값들을 하나의 배열명으로 저장시킬 수 있는 아주 편리한 구조임
	- 배열을 사용하면 변수 일일이 변수를 선언할 필요없이 한방에 선언이되며, 초기화 값도 한방에 셋팅해줌.
	
	- 배열 선언
		○ 데이터 타입 [] 배열명 = new 데이터타입 [배열크기];
		○ 데이터 타입 배열명[] = new 데이터타입 [배열크기];

	- 배열의 선언 --> 배열 크기 지정 --> 배열 공간의 값은 자동으로 초기화 셋팅 됨
		○ 정수형 0, 실수형 0.0

	- 배열 선언과 동시에 특정 값으로 초기화 하는 방법
		○ 데이터 타입 [] 배열명 = {값,값,값,…};
		○ 데이터 타입 [] 배열명 = new 데이터 타입 {값,값,값…};
		○ 데이터 타입 [] 배열명;
		배열명 = new 데이터타입 {값,값,값…};
	
주소값
	- 주소값은 다른 말로 참조 값이라고도 함
	- new 연산자 : 메모리 주소를 return을 시켜줌
		○ int [] arr = new int [] {1,2,3};
		// 같은 경우는 arr라는 변수명에 1,2,3의 주소 값을 넘겨줌
		// --> 변수명 사용하면 주소값을 불러와서 메모리 공간상에 있는 데이터를 불러옴. 
	- 주소값 출력 방법 : 변수명을 출력 시키면 주소값이 출력됨
		○ System.out.println(arr); --> 주소값 출력
		○ 참고로 정수형은 I@로 시작, 실수형은 D@로 시작함

문제 : 배열의 값들을 for문과 같은 반복문을 사용하지 않고 한꺼번에 출력하는 코드를 작성하시오.

	정답 : 
		1. Arrays.toString()  메서드를 사용하면됨.
			i. 사용법 : 
			import java.util.Arrays;
			int [] arr = {1,2,3,4,5};
			System.out.println(Arrays.toString(arr));
			--> 출력 결과 : [1,2,3,4,5] // 반복문을 사용하면 1,2,3,4,5가 출력 됨.
			--> [ ]의 차이 주의 할것

다중 배열 선언
		1. int [] a,b,c;
		2. int d[], e[], f[];
		○ 1번과 2번의 방법으로 여러개의 배열을 한번에 선언 할 수 있음.

2 차원 배열 선언
		1. int [] [] arr = {{1,3,5,},{2,4,6}};
			//이런식으로 배열 선언과 초기화를 하면 됨
			
문자 뽑기 메서드
	charAt(); 메서드 사용 --> 해당 인덱스에 있는 값을 반환 --> 단어를 한글자씩 저장할 수 있음.
	Ex : charAt(인덱스);
		String [] str = {"abc","ABC","알파벳"};
		System.out.println(str[0].chartAt(2)); --> c
		System.out.println(str[0].chartAt(2)); --> C
		System.out.println(str[0].chartAt(2)); --> 벳

문자열 뽑기 메서드
	substring(); 메서드 사용 --> 시작 인덱스부터 종료 인덱스의 값을 반환 -> 문자열을 저장할 수 있음
	EX : substring(시작,종료); 종료 인덱스는 출력에 포함이 안됌.
		String [] str = {"abc","ABC","알파벳"};
		System.out.println(str[0].substring(0)); --> abc
		System.out.println(str[0].substring(1,2)); --> B
		System.out.println(str[0].chartAt(1,3)); --> 파벳
	
배열 복사 메서드
	arraycopy() : System.arrayscopy(원본배열명, 원복 배열에서 복사 시작 인덱스, 복사배열명, 복사배열에서 복사 시작 인덱스, 복사 길이);
	사용법 : 
		import java.util.Arrays;
		int [] arr1 = {1,2,3};
		int [] arr2 = {1,2,3,4,5,6};
		System.arraycopy(arr1,0,arr2,3,3);
		System.out.println(Arrays.toString(arr2));
		// 출력 [1,2,3,1,2,3] 
		
배열 길이 구하기와 문자열 길이 구하기
		1. 배열 길이는 length;를 사용해서 구하면 됨
			i. arr.length; --> 길이 출력
		2. 문자열 길이는 length();를 사용해서 구하면 됨
			i. str.length(); --> 문자열 길이 출력

입력과 배열 문제
	사용자 입력을 받아 2차원 배열을 생성하고 값을 입력하는 코드를 구현하시오.
	----------------------------------------------------------
	행의 갯수를 입력하고 [Enter] 치세요 = 3
	열의 갯수를 입력하고 [Enter] 치세요 = 3
	1번째 행에 입력할 문자 3개를 차례대로 입력하고 [Enter] 치세요 = ㄱㄴㄷ
	2번째 행에 입력할 문자 3개를 차례대로 입력하고 [Enter] 치세요 = ㄹㅁㅂ
	3번째 행에 입력할 문자 3개를 차례대로 입력하고 [Enter] 치세요 = ㅅㅇㅈ
	---------------
	ㄱㄴㄷ
	ㄹㅁㅂ
	ㅅㅇㅈ
	--------------
	
	import java.util.Scanner;
	Scanner sc = new Scanner(System.in);
	System.out.print("행의 갯수를 입력하고 [Enter] 치세요 = ");
	int row = sc.nextInt();
	System.out.print("열의 갯수를 입력하고 [Enter] 치세요 = ");
	int col = sc.nextInt();
	String [] [] strar = new String [row][col];
	
	for(int i=0; i<col; i++){
		System.out.printf("%d번째 행에 입력할 문자%d개를 차례대로 입력하고 [Enter] 치세요 = ",i+1,row);
		String val = sc.next();
		if(val.length() == row) {
			for(int j=0;j<row;j++) {
				strar[i][j] = val.substring(j,j+1);
			}
		}
		else {
			System.out.println("문자 갯수를 잘못 입력하였습니다. 다시 입력해주세요.");
			i--;
		}
	}
	for(int i=0; i<strar.length;i++) {
		for(int j=0;j<strar[i].length; j++) {
			System.out.print(strar[i][j]);
		}
		System.out.println();
	}
	
	- 문자를 입력받을 땐 java.util.Scanner를 import 하고 
	- Scanner 객체명 = new Scanner(System.in) 를 하여 Scanner 객체를 생성해줘야됨 why? Scanner는 객체이기 때문
		○ System.in : 키보드에서 사용자로부터 키 입력을 받기 위해서는 System.in을 사용함 

	- Scanner 클래스의 메소드
	
	![image](https://user-images.githubusercontent.com/69742511/159166907-1017d64d-716d-4113-a5d5-fb2c0c1c733c.png)
