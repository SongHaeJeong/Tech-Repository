## JavaScript

__자바 스크립트 정의__

>- 클라이언트쪽에서 독립적으로 실행되는 프로그램을 작성하기 위한 스크립트 언어
>- 플랫폼에 독립적
>- 모든 웹 브라우저에서 동일한 실행 결과를 얻을 수 있음



__자바 스크립트 특성__

>- 웹 문서(XHTML, HTML)에 끼워서 사용하는 스크립트 언어
>- 웹 브라우저에서 자바스크립트 해석기가 웹 문서를 실행할 때 프로그램 코드를 해석하는 인터프리터 언어의 형태
>- 자료형(premitive, reference data type) 조사를 철저하게 하지 않음
>- 클래스를 정의, 클래스를 상속할 수 없다
>- 객체를 정의하여 사용할 수는 있다.
>- 소스가 노출되어 보안성이 없다.
>- 컴포넌트 기반
>- 다양한 프로그래밍 언어 및 여러 데이터베이스와의 인터페이스로 생성된 서버측 프로그램과 긴밀히 통할될 수 있다
>- 웹 브라우저와 여타 프로그램에 내장되어 사용되는 스크립트 언어
>- 웹 브라우저와 같은 특정 환경 내에서 실행되기 때문에, 파일이나 메모리 관리 등이 필요
>- 웹 페이지 내의 엘리먼트를 생성/제거하고, 속성을 변경한다 



__자바스크립트의 기능__

>- 웹 문서에 동적으로 움직일 수 있는 프로그램적인 요소를 추가
>- 어떤 이벤트에 대한 반응을 할 수 있도록 웹 문서를 구성
>- 웹 문서 내의 XHTML 요소의 내용을 읽거나 변경
>- 클라이언트의 정보를 서버에 보내기 전에 먼저 검증
>- 클라이언트가 어떤 웹 브라우저를 사용하는지 알아내어 사용자의 웹 브라우저에 맞는 웹 문서를 호출하는 맞춤형 서비스를 제공
>- 클라이언트 컴퓨터에 쿠키를 새로 만들거나 생성된 쿠키를 삭제 및 회수할 수 있다.



__자바스크립트의 장점과 단점__

>- 작업 속도가 빠르다.
>  - 자바스크립트는 HTML 파일 내에서 작성할 수 있으므로 개발 속도가 빠르다
>  - 자바, C/ C++ 등 프로그래밍 언어의 기본적인 틀을 그대로 갖추고 있어 사용자로부터 익숙한 작업 가능
>- 운영체제의 제한을 받지 않음
>- 배우기 쉬움
>- 소스 코드가 노출된다.
>- 한정된 객체와 객체 함수다.



__식별자__

>- 이름을 붙일 때 사용하는 단어, 변수와 함수 이름 등으로 사용
>  - 키워드 사용 안됨
>  - 특수 문자는 _와 $만 허용
>  - 숫자로 시작하면 안됨
>  - 공백은 입력하면 안됨
>- 식발자 사용 규칙
>  - 생성자 함수의 이름은 항상 대문자로 시작
>  - 변수, 함수, 속성 , 메소드의 이름은 항상 소문자로 시작
>  - 여러 단어로 된 식별자는 각 단어의 첫글자로 대문자로함



__조건문__

>- if 기본 형태 :
>
>```javascript
>if(<불 표현식>){
>
>}
>
>example
>let input = 32;
>if(input % 2 == 0) {
>    console.log("작수입니다.!")
>}
>
>
>if(<불 표현식>){
>    // 불 표현식이 참일 때 실행할 문장
>}else{
>    // 불 표현식이 거짓일 때 실행할 문장
>}
>```
>
>
>
>- switch 조건문 기본 형태 :
>
>```javascript
>switch (<비교할 값>){
>	case <값>:
>		<문장>
>		break;
>	default :
>		<문장>
>		break;
>}
>```
>
>
>
>- 삼항 연산자
>
>```javascript
><불 표현식> ? <참> : <거짓>
>```
>
>
>
>

