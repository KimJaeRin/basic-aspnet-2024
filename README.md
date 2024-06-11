# basic-aspnet-2024
IoT 개발자과정 ASP.NET 리포지토리

## 1일차
- 웹기술 개요
    - World Wide Web은 인터넷의 하나의 Part
    - Full-Stack
        - Front-end : 웹사이트 화면으로 사람들에게 보이는 부분 기술
        - Back-End : 웹사이트 뒤에서 동작하는 서버기술
        - Server-Operation : HW, OS, SW등 운영(클라우드)
- 업무용 웹 사이트 참조
    - https://www.ecount.com/kr/ECK/ECK004M_CN.aspx

- Front-end(필라이언트)
    - HTML5
    - CSS3
    - Javascript(ECMAScript 6)

- Back-end(서버)
    1. Java - Spring, Spring Boot, JSP, EJB ...
    2. Javascript - Node.js, Express ...
    3. Python - Django, Flask, fastAPI ...
    4. C# - ASP.NET
    5. Ruby - Ruby on rails
    6. C - cgi, fastCGI ...
    7. PHP - 

- 개발
    - 프론트엔드 전부 + 백엔드 여러개 중 하나 + DB
    - 웹 브라우저에서 F12(개발자도구)
    - VS Code 플러그인
        - HTML Code Snippet 
        - Live Server

- HTML5
    - XML이 웹페이지 구성하기 위한 선행기술, 너무 복잡해서 간략화 시킨 것
    - Hyper Text Markup Language 
    - 기본적으로 확장자 .html  
    - Tip! lorem 탭, 긴 샘플 텍스트 생성됨
    - 기본태그(body에 사용)
        - h1 ~ h6 : 제목(마크다운 #, ##와 동일)
        - p : 일반문장
        - div : 그룹화 구분자, 아주 중요(CSS 연계 디자인)
        - img : 이미지 표현
        - br : 한 줄 내리기(엔터)
        - 특수문자 : & ; 사이에 영문자로 표시(너무 많음!)
        - strong 또는 b : 볼드체
        - em : 이탤릭체
        - mark : 형광펜 효과
        - u, strike: 밑줄, 취소선
        - a : 웹페이지 링크(중요)
        - ul, ol > li : 순서없는 목록, 순번있는 목록
        - table, tr, th, td : 테이블 만드는 태그
        - audio, video : 오디오, 비디오
        - object, embed : 객체 추가

    - HTML + CSS + Javascript
        - 내부 스타일, 외부 스타일, 인라인 스타일
        - 내부 스크립트, 외부 스크립트, 인라인 스크립트

    - 오류, 디버그
        - F12 개발자도구로 활용

    - 양식태그(body > form안에 사용 필수)
        - front-end 입력한 내용이 back-end로 보내기위한 관문
        - form 을 반드시 사용
        - input
            - type="text" : 텍스트박스
            - type="password" : 비밀번호박스
            - type="button" : 일반버튼
            - type="submit" : 제출(!) 
            - Checkbox : 체크박스
            - radio : 라디오 버튼
            - file : 파일 업로드
            - image : 이미지(img와 유사)
            - reset : 폼 내의 입력양식태그 값 초기화
            - hidden : 숨김값(유용)
        - textarea : 여러행 텍스트 입력
        - select, option : 콤보박스
        - fieldset : 그룹박스
        - submit 클릭 loopback(값 전달)발생
        - 값 전달 방법
            - GET : URL 뒤 ? 다음에 key=value&key=value ... 데이터 전달
            - POST : 화면 뒤로 숨겨서 데이터 전달
    - 공간구분 태그
        - span : 한줄로 공간구성
        - div : 행간으로 블록지정 공간구성

## 2일차
- HTML5
    - 시맨틱 웹 : 시맨틱 태그로 화면을 구조를 잡는 웹구성 방식
    - header, main, content, nav, footer, aside, section, article ... 구조태그(화면에
    안나타남) 사용
    - 시맨택 태그를 div로 바꿔도 똑같이 동작하기 때문에 요새는 많이 사용안함. 걷어내고
    있는 추세

- CSS3
    - 웹 디자인 핵심, Cascading Style Sheets
    - 상단에서부터 <body> 부터 하위에 태그들에 계속해서 적용되는 스타일이라는 뜻
    - 선택자에게 주어지는 디자인 속성
    - 선택자(selector)
    - 속성(property)
    - 배경, 폰트
    - 레이아웃
        - HTML 만으로는 화면 레이아웃이 만들어지지 않음
        - 중앙정렬, 원트루, 고정바...
    - 반응형 웹(Responsive web)
        - 메타태그 viewport를 사용하면 그때부터 반응형 웹
        ```html
        <meta name='viewport' content='width=device-width, initial-scale=1'>
        ```
        - @media 태그 : 디바이스 종류별로 

- Javascript

## 3일차
   - 바닐라스크립트 : 완벽하게 기본에 충실한 자바스크립트
   - 기본적으로 클라이언트(웹 브라우저에서 프론트엔드에 표시) 베이스
   - Node.js : 자바스크립트로 백엔드를 구현(파이썬과 유사)
   - 특징
       - 자료형 선언이 없음. var 변수 선언
       - 인터프리터 언어(not Compile Lang)
       - 확장자 .js
       - 속도가 컴파일 언어에 비해서 느림
       - VS Code도 자바스크립트로 만든 앱
       - 문장끝 ; 은 생략가능, but 최대한 쓸 것
       - 정수와 실수를 구분하지 않음
       - 0으로 나눠도 예외가 발생하지 않음
       - 파이썬과 동일하게 ', " 모두 사용
       - 완전히 동일함을 비교하는 === 연산자
       - 변수선언시 let(일반), var(지역변수), const(상수)
       - HTML 태그과 연계(DOM) 중요 !!!

- DOM(Document Object Model) !!!!!
    - 실행 순서!
    - HTML에 있는 모든 요소텔 제어할 수 있음
    - HTML 애니메이션, 게임, 통신 모두 가능
    - 이벤트 on- 으로 시작
        - onload : 화면이 다 랜더링되면 그 다음 발생    
        - onfocus : 객체에 마우스를 클릭해서 포커스가 가면 발생
        - onclick : 객체를 마우스로 클릭하면 발생
        - ondbclick : 더블클릭
        - onmousemove : 마우스를 이동하면 발생
        - onmouseover : 객체 위에 마우스가 올라가면 발생
        - onkeydown, onkeypress : 객체에서 키보드를 타이핑하면 발생
        - ...

- jQuery
    - 자바 스크립트 라이브러리
    - js를 매우 편리하게 사용할 수 있도록 도와주는 서포트 라이브러리
    - 순식간에 웹개발 업계를 장악했던 라이브러리
    - 사용빈도가 줄고는 있지만 아직도 80%정도의 웹사이트가 사용 중
    - js 파일 다운로드 후 사용하거나, CDN 링크를 사용하면됨(추천)

## 4일차(24-06-03)
- HTML + CSS + js(jQuery) 응용 
    - jQuery 응용
        - javascript와 jQuery를 혼용해도 상관없음
        - jQuery로 코딩 편할때와  javascript로 편할때가 있음  
    - Bootstrap 
        - 오픈소스 CSS 프레임워크
        - 트위터 블루프린트 -> 부트스트랩
        - 현재 전세계에서 가장 각광받는 프레임워크 중 하나
        - CSS를 동작시키기 위해서는 Javascript도 포함
        - 소스 다운로드 받아서 사용(1), CDN으로 링크만 사용(2), 2번이 훨씬 편리 But 네트워크 연결 되어있어야 함
        - Bootstrap은 화면사이즈를 12등분
        - container 밑에 마치 table 처럼 div를 구분해서 사용
        - container > row > col div 태그 클래스 정의
    - Bootstrap학습에 시간을 들이는게 아님. Copyleft가 정석
        - https://getbootstrap.com/docs/5.3/getting-started/introduction/ 참조
        - https://getbootstrap.com/docs/5.3/examples/ 스니펫 활용 추천
    - 무료 테마(template)가 잘되어있음
    - https://startbootstrap.com/

- 웹페이지 클로닝
    -  핀터레스트 타입 웹페이지 만들기(진행중)

## 5일차
- HTML + CSS + js(jQuery) 응용
    - 웹페이지 클로닝
        - 핀터레스트 타입 + 부트스트랩 웹페이지 만들기(완료)
     
          https://github.com/hugoMGSung/basic-aspnet-2024/assets/59336331/643a9b13-c062-49a6-a712-aadfc4c7b292

        - Codehal 유튜버 로그인 웹페이지 튜토리얼 따라하기

          <img src="https://raw.githubusercontent.com/hugoMGSung/basic-aspnet-2024/main/images/an0001.png" width="730" alt="Codehal 로그인창 따라하기">

          <!-- ![이미지](https://raw.githubusercontent.com/hugoMGSung/basic-aspnet-2024/main/images/an0001.png) -->

## 6일차
- HTML + CSS + js(jQuery) 응용
    - 웹페이지 클로닝
        - Codehal 슬라이더 애니메이션 웹페이지 튜토리얼 따라하기(완료)


- 개인 웹페이지 클로닝
    - 

    https://github.com/KimJaeRin/basic-aspnet-2024/assets/158007433/88f6d0de-bf4f-4f3b-a22e-1cdb8dcd8fdd



## 9일차
- ASP.NET
    - 역사
        - 1990년대 MS가 웹 서버기술로 ASP(Active Server Page)를 배포. like JSP(Java Server Page)
        - ASP는 .NET으로 된 언어가 아닌, VB Script를 사용. 확장자(.asp)
        - 개발이 무지 쉬워서 많이 사용
        - 스파게티 코드 : HTML + CSS + JAVA Script + VB Script 합쳐서 만든 페이지
        - 유지보수 어렵고 성능이 나쁨

        - 2000년대 MS가 .NET Framework를 발표.
        - C#, VB.NET, C++.NET 등의 새로운 언어를 배포, 여기에 맞춰서 웹서버 기술을 다시만듬
        - 가장 큰 장점은 윈폼 개발하는 것 처럼 웹개발을 할 수 있음.
        - 초창기에 스파게티 코드를 거의 그대로 사용, 성능↓
        - 2009년 ASP.NET MVC(Model View Controller 디자인패턴) 공표, 성능은 좋아짐.
        - 하지만, 윈도우에서만 동작
        - 모든 OS 플랫폼에서 동작할 수 있는 .NET Core를 재출시
        - 거기에 웹 서버기술을 또 다시 만듦 -> ASP.NET Core

    - .NET Core(현재는 .NET 9.0, Core라는 이름은 사용하지않음)의 장점
        - 빠르고 오픈소스
        - 크로스 플랫폼, OS에 종속받지 않음
        - 성능 
    
    - ASP.NET 종류
        - **ASP.NET Core 웹앱(MVC) : 가장 기본적인 프론트앤드(HTML, CSS, JS .cshtml) + 백엔드(C#.aspx.cs) 웹개발**
        - **ASP.NET Core 웹 API : 데이터포털, 네이버, 카카오, 영화 API 사이트를 만드는 백엔드(프론트엔드가 없어서 화면이 없음)**
        - Js(Vue, Angular, React) 프론트앤드 + ASP.NET Core 백엔드
        - Edge용 웹 드라이버 테스트 : 엣지 브라우저에 종속된 테스트용
        - ASP.NET Core gRPC 서비스 : 고성능 원격 프로시저 호출(스트리밍 호출) 서비스
        - Blazor - Js 프론트엔드를 따라서 C# 컴포넌트 기반으로 개발하는 웹개발 방식 웹사이트 개발
        - Razor - 프론트엔드 개발에 C# 코드가 특화되서 사용되는 웹사이트 개발방식
        - .NET Aspire - Blazor 프론트엔드 + Redis + 웹 API 백엔드

    - 참조사이트
        - https://learn.microsoft. com/ko-kr/aspnet/core/?view=aspnetcore-3.1
        - https://github.com/dotnet
        - https://mixedcode.com/
        - https://github.com/gilbutITbook/006824

    - ASP.NET Core 웹앱(Model-View-Controller)
        - 현재 기본적인 웹개발의 가장 표준
        - Java 계열도 Spring (Boot) MVC로 개발
        - MVC 개념도

            <img Src="" width="730">

        - 프론트엔드가 예전엔 스파게티코드가 무지 심했다면, 현재는 스파게티코드가 최소화 되어있음.
        - IIS Express Server : VS에서 ASP.NET 웹사이트를 운영하는 개발용 웹서버
        - index.* : 웹사이트 가장 대문되는 페이지 이름
        - 파일 저장시 핫다시로드(HotReload) 체크
        - @로 시작하는 C#구문. Tag helper, Html helper로 HTML 구문 내에 C# 코드를 적어서 활용하는 방법 = Razor 구문
        - Action == HTML에서 Form태그 내의 submit버튼 / 링크를 클릭
        - 액션이 발생한 이후 처리하는 매서드의 결과를 ActionResult
        - 콘솔 서버로그 잘 확인할것, 프로세스가 종료되면 웹사이트 실행 안됨
    
    - 데이터베이스 연동방법
        - DB first - 가장 전통적인 DB 연동방식. DB설계, DB구축, C#과 연동
        - Code first - 최근 트렌드가 되는 DB 연동방식. C# 엔티티 클래스 작성, DB연결 설정 후 실행하면 DB에 테이블이 생성
        - EntityFramework를 사용하면 아주 손쉽게 구축가능

    - EntityFramework(Core)
        - Microsoft. EntityFrameworkCore
        - Microsoft. EntityFrameworkCore. Tools
        - Microsoft. EntityFrameworkCore. SqlServer

    - Code first 구현순서
        - ASP.NET 프로젝트 생성
        - EF 패키지 설체
        - 엔티티 클래스 작성
        - appsettings.json 에 DB연결문자열 추가
    