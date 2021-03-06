## 스프링 타입 컨버터 소개
* @RequestParam 등 스프링엔 다양한 타입 변환 기능 제공
* Converter를 통해 S -> T, T -> S 타입 변환 구현 가능

## 컨버전 서비스 - ConversionService
* 다양한 Converter를 등록하여 사용

## 스프링에 Converter 적용하기
* WebConfig를 통해 Converter를 넣은 ConversionService등록
* 컨트롤러의 @RequestParam등에서 타입 변환시에 Converter가 자동으로 사용됨

## 뷰 템플릿에 컨버터 적용하기
* thymeleaf에서 ${{number}}, th:field 등으로 자동으로 객체 -> 문자로 변환

## 포맷터 - Formatter
* 객체 <-> 문자 + Locale(현지화)
* parse(), print()

## 포맷터를 지원하는 컨버전 서비스
* DefaultFormattingConversionService에서 Converter, Formatter등록하여 사용 가능

## 포맷터 적용하기
* WebConfig에 addFormatter()를 통해 등록후 글로벌하게 사용 가능

## 스프링이 제공하는 기본 포맷터
* 데이터 클래스에서 @NumberFormat(pattern = "###,###")등을 붙여 문자가 들어올때 자동 형변환 가능