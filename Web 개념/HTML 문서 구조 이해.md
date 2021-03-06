## HTML 문서 구조 이해

#### DOM 이란?

>DOM(Document Object Model)은 웹 페이지에 대한 인터페이스입니다. 기본적으로 여러 프로그램들이 페이지의 콘텐츠 및 구조, 그리고 스타일을 읽고 조작할 수 있도록 API를 제공합니다. 



#### 웹 페이지는 어떻게 만들어질까?

>웹 브라우저가 원본 HTML 문서를 읽어들인 후, 스타일을 입히고 대화형 페이지로 만들어 뷰 포트에 표시하기까지의 과정을 "Critical Rendering Path"라 합니다. 
>
>- 첫 번째 단계에서 브라우저는 읽어들인 문서를 파싱하여 최종적으로 어떤 내용을 페이지에 렌더링할지 결정
>
>-  두번째 단계에서 브라우저는 해당 렌더링을 수행합니다.
>
>첫 번째 과정을 거치면 __랜더 트리__가 생성됩니다.
>
>렌더 트리는 웹 페이지에 표시될 HTML 요소들과 이와 관련된 스타일 요소들로 구성됩니다. 브라우저는 렌더 트리를 생성하기 위해 다음과 같이 두 모델이 필요
>
>- DOM(Document Object Model) - HTML 요소들의 구조화된 표현
>- CSSOM(Cascading Style Sheets Object Model) - 요소들과 연관된 스타일 정보의 구조화된 표현

#### DOM은 어떻게 생성될가?

>DOM은 원본 HTML 문서의 객체 기반 표현 방식입니다. 둘은 서로 비슷하지만, DOM이 갖고 있는 근본적인 차이는 단순 텍스트로 구성된 HTMl 문서의 내용과 구조가 객체 모델로 변환되어 다양한 프로그램에서 사용될 수 있다는 점
>
>DOM의 개체 구조는 "노드 트리"로 표현됩니다. 하나의 부모 줄기가 여러개의 자식 나뭇가지를 갖고 있고, 또 각각의 나뭇가지는 잎들을 가질 수 있는 나무와 같은 구조로 이루어져 있기 때문입니다. 
>
>__DOM은 HTML이 아닙니다__ : DOM은 HTML 문서로부터 생성되지만 항상 동일하지 않습니다. 
>
>브라우저 뷰 포트에 보이는 것은 렌더 트리로 DOM과 CSSOM의 조합입니다. 렌더 트리는 오직 스크린에 그려지는 것으로 구성되어 있어 DOM과 다릅니다.



#### 요약 정리

>DOM은 HTML 문서에 대한 인터페이스입니다. 첫째로 뷰 포트에 무엇을 렌더링 할지 결정하기 위해 사용되며, 둘재로는 페이지의 콘텐츠 및 구조, 그리고 스타일이 자바스크립트 프로그램에 의해 수정되기 위해 사용됩니다.
>



#### 문서 구조

>- WWW(World Wide Web)
>  - 인터넷, 컴퓨터, 웹 브라우저를 통해 글자, 이미지, 동영상, 음성 등의 데이터를 사용자에게 제공하거나, 사용자와 컴퓨터 또는 사용자 상호 간에 소통하게 해주는 서비스
>  - 익스플로러, 크롬, 사파리, 파이어 폭스등
>- __서버와 클라이언트__
>  - 클라이언트가 웹 페이지의 주소(URL) 입력
>  - 서버는 요청을 받은 데이터를 클라이언트의 컴퓨터에 전송
>  - 클라이언트의 웹 브라우저는 서버가 전송한 데이터를 해석하여 화면에 표시
>- __웹의 서버와 클라이언트 환경__
>  - 데이터 센터
>    - 자신이 보유한 서버와 네트워크를 기업이나 기관에 임대하는 서비스를 제공
>  - 웹 서버
>    - 인터넷과 같은 네트워크를 통해 클라이언트가 요청하는 서비스를 제공하는 컴퓨터
>  - 클라이언트
>    - 원격의 웹 서버에 서비스를 요청하는 컴퓨터 또는 컴퓨터 사용자를 의미
>  - 웹 사이트와 웹 페이지
>    - 웹 사이트 : 인터넷 프로토콜 기반의 네트워크에서 도메인 이름(domain name) 만으로 구성된 URL이 나태내는 웹 페이지의 묶음
>    - 웹 페이지 : 웹 브라우저에서 보는 각각의 화면
>  - 웹 호스팅 
>    - 인터넷 전문 업체가 자신이 보유한 웹 서버와 네트워크를 이용하여 홈페이지를 구축할 수 있도록 서버상의 사용자 계정과 디스크 공간을 임대하는 서비스
>  - IP 주소와 DNS
>    - IP 주소 : 다른 컴퓨터와 구별되도록 갖는 고유한 주소
>    - DNS(domain name system) : ip 주소와 그것에 대응하는 도메인 이름의 쌍으로 구성된 정보를 가지고 있음



#### HTML 관련 태그

>- 너무 많아서 다 외우지 말고 필요할 때 마다 인터넷 검색을 하는게 맞다고 생각



#### URL과 경로

>__절대 경로__
>
>- http://로 시작하는 주소
>- 인터넷상에 하나밖에 없는 유일무이한 고유한 경로를 의미
>- 최상위 디렉토리가 반드시 포함된 경로를 의
>
>__상대 경로로 나타내기__
>
>- 현재 폴더의 위치를 기준으로 대상 파일이나 폴더의 위치를 지정
>- 절대 경로보다 서버의 폴더 구조나 도메인 변경 및 웹 페이지 제작 수정에 편리
>- 일반적으로 상대 경로를 더 많이 사용



#### 테이블 태그

>```html
><!-- 밑의 방식으로 테이블 생성함 -->
><table>
>    <tr> 
>    	<th></th> 
>    </tr>
></table>
>```
>
>__셀 병합__
>
>```html
><th colspan ="2"></th>
><td rowspan="2"></td>
>
>```



#### 웹 브라우저의 HTML문서 렌더링 과정

>1. 불러오기
>   - 로더가 서버로부터 전달 받는 리소스 스트림을 읽는 과정. 읽으면서 어떤 파일인지, 데이터인지 파일을 다운로드 할 것인지 등을 결정한다.
>2. 파싱(Phasing)
>   - 웹 엔진이 가지고 있는 HTML/XML 파서가 문서를 파싱해서 DOM Tree를 만든다
>3. 렌더링 트리 만들기
>   - DOM Tree는 내용을 저장하는 트리로 자바스크립트에서 접근하는 DOM객체를 쓸 때 이용하는 것이고 별도로 그리기 위한 트리가 만들어져야 하는데 그것이 렌더링 트리다.
>4. CSS 결정
>   - CSS는 선택자에 따라서 적용되는 태그가 다르기 떄문에 모든 CSS 스타일을 분석해 태그에 스타일 규칙이 적용되게 결정한다.
>5. 레이아웃
>   - 렌더링 트리에서 위치나 크기를 가지고 있지 않기 때문에 객체들에게 위치와 크기를 정해주는 과정을 레이아웃이라고 함
>6. 그리기
>   - 렌더링 트리를 탐색하면서 그리기



#### CSS는 위에 Script는 아래에?

>웹 브라우저의 렌더링 순서를 이해하면 이해가 가는 말이다. 문서를 파싱해서 DOM Tree를 만들어도 __스타일 규칙이 없으면 렌더링 할 수가 없다.__ 즉, 최대한 빨리 스타일 규칙을 알아야 렌더링트리가 완전히 만들어지므로 스타일시트 파일을 모두 다운로드시키기 위해 <head></head> 태그 사이에 놓는 것이다.(인터프리터에서 html파일 위에서 아래로 읽음)
>
>자바스크립트는 왜 아래에 놓아야 성능이 좋아질까 ? 
>
>자바스크립트는 DOM 객체를 이용해서 컴포넌트들을 조작하는데  <head></head>태그 사이 처럼 상단에 놓게 되면 HTML 파서가 파싱을 멈추고 스크립트파일을 읽기 때문이다.
>
>파싱을 멈추고 읽기 때문에 위에서 스크립트파일이 많거나 파일이 크면 읽는 시간이 오래걸려 사용자 입장에서 웹페이지가 느리게 보이게 되므로 느리다고 느낄 수 있다. 심지어 잘 못 코딩했을 경우 HTML 파싱보다 자바스크립트 파일이 먼저 실행되서 적용이 안되는 모습도 볼 수 있다. 따라서 일반적으로 </body>태그 위에 스크립트를 모아둔다.