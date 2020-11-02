##Code Review

라이브러리없이 짠 회원가입페이지

\*구현한 기능:

-영문소문자, 숫자, 특수문자 1개 이상 포함한 10자리
이상의 아이디/12자리 이상의 비밀번호 validation & validation에 따라 border색 바뀌는 inputbox

-아이디중복체크버튼

-아이디중복체크, 전체 form validation 결과에 따라 메시지 띄우는 modal

-윤년 반영되는 생년월일 seletbox

-글자수 count되고 300자 limitaion있는 자기소개 textarea

\*도움되었던 강의링크

정규표현식 이용한 validation:
https://youtu.be/NrzFle7RD0g

\*피드백

-코드 리팩토링 tip

1. 직접적으로 value값을 변화시키는 함수를 제외한 나머지 함수는 util폴더로 빼고, import해서 사용한다. (적용)

2. state를 관리하는 메인container에서는 value값만 다뤄주고, 부수적인 config는 각 컴포넌트 파트별로 다뤄준다(적용되어야 할 부분)

-bootstrap : 잘 짜인 css를 가져다 쓸수있음.

\*수정하면 좋을것:

form구조:
form 각 영역에 대한 isRequire 체크라던지 순수한 인풋데이터만 다뤄야할때 filter처리 해줘야 해서 에러가 많이 났음. form구조를 더 깔끔하게 효율적으로 짜는 방법 알면 좋을듯.

##TIL

[20.10.30]

\*코드 리팩토링

- 각종 변수명 수정

- function 정리&분리
  :전체 form validation함수,생년월일change함수 etc.

\*에러 해결

- css class명 수정, 전체 렌더링될 때 버튼박스도 같이 렌더링되는 문제 해결
