# Markdown extended Syntax

## Contents
* Tables
* Task List Items
* Strikethrough
* Autolinks
* Disallowed Raw HTML  

<br><br>
## Tables
확장된 Markdown 문법에서는 표를 만들 수 있다.

    | Syntax      | Description |
    | ----------- | ----------- |
    | Header      | Title       |
    | Paragraph   | Text        |
위와 같이 |와 세 개 이상의-를 활용하여 표를 만들 수 있다. 위 코드를 탭 없이 나타내면 아래와 같이 표로 표현된다.  

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |  

<br>

표를 만들 때는 칸의 크기를 일일이 맞춰주지 않아도 자동으로 완성된다.
> ex1)  
> 
>       | Syntax      | Description |
>       | -------- | ----------- |
>       | Header | Title |
>       | Paragraph  | Text     |

위 코드를 공백없이 나타내면 아래와 같이 자동으로 규격이 맞춰진다는 것을 알 수 있다.  
 | Syntax      | Description |  
 | -------- | ----------- |  
 | Header | Title |  
 | Paragraph  | Text       |  

<br>

표를 만들 때는 때에 따라 정렬을 할 수 있다.  
정렬을 하려면 :과 세 개 이상의 -를 사용하면 된다.   
> ex2)  
> 
>       | Syntax    | Description | Test Text |  
>       | :---      | :-------:   | ------:  |  
>       | Header    | Title       | Heres this |  

위 코드를 공백없이 나타내면 다음과 같다.  
| Syntax    | Description | Test Text |
| :---      | :-------:   | ------:  |
| Header    | Title       | Heres this |

위 코드와 표를 보고 정렬 방법을 직관적으로 알 수 있다.  
정렬하고자 하는 방향에 :을 찍고 -를 세 개 이상 입력하면 정렬할 수 있다.  
가운데 정렬을 하고 싶다면 -기호 세 개 이상과 그 양 옆에 :을 찍어주면 된다.  

<br>

표 안에서 |기호를 사용하고 싶다면 Escaping 문자를 사용하면 된다.   
> ex3)  
>       | f\|oo  |
>       | ------ |
>       | b `\|` az |
>       | b **\|** im |  

위 예시를 공백없이 작성하면 아래와 같다.  

| f\|oo  |
| ------ |
| b `\|` az |
| b **\|** im |


<br>

표를 만들 때 몇 가지 주의 점이 있다.  

* 테이블에 포함하기 위해서는 시작할 때 반드시 |로 시작하여야 한다.  
* 헤더 행의 셀 수는 구분 기호 행과 일치해야 한다. 
* 테이블 행의 셀 수보다 적은 수의 셀이있는 경우 빈 셀이 삽입되고 더 큰 경우 초과는 무시된다.  

<br><br>
## Tesk List Items  
Markdown  확장 문법에서는 작업 목록 항목을 만들 수 있다.  
체크 박스는 대괄호와 대괄호 안에 공백 또는 x문자로 구성된다.  

- [ ] foo  
- [x] bar  

작업 목록 항목을 중복하여 만들 수도 있다.  

- [x] foo  
    - [ ] bar
    - [x] baz  
- [ ] bim  

경우에 따라 작업 목록을 활성화할 수도 있다.  

<br><br>
## Strikethrough  
Markdown 확장 문법에서 글자의 가운데에 수평선을 그어 취소 선으로 표현할 수 있다.   
>ex1)  
>~~Markdown은 재미 없다.~~  
>공부하다 보니 재미있다!  


<br><br>
## Autolinks  
Markdown 확장 문법에서는 URL을 괄호 없이 자동으로 링크 변환을 한다.  

ex1)  
```
[Markdown basic syntax](https://www.markdownguide.org/basic-syntax/)  
<https://www.markdownguide.org/basic-syntax/>  
https://www.markdownguide.org/basic-syntax/
```

위 코드를 `없이 입력하면 다음과 같이 나타난다.  
[Markdown basic syntax](https://www.markdownguide.org/basic-syntax/)  
<https://www.markdownguide.org/basic-syntax/>  
https://www.markdownguide.org/basic-syntax/

괄호 없이도 자동 링크화 되는 것을 확인 할 수 있다.  
자동 링크를 인식하기 위해 GFM은 확장 검사를 한다.  
그 방법은 링크화 될 텍스트 형식에 따라 다르다.  

* www를 검사할 때는 www. 다음에 발견되는 유효 도메인의 형식을 검사한다. 그러면 자동으로 http가 삽입된다.  
* 확장된 이메일 자동 링크는 이메일 주소가 텍스트 노드 내에서 인식된다.  

따라서 경우에 맞게 활용하면 GFM에서 자동으로 링크를 생성해준다.  


<br><br>
## Disallowed Raw HTML  
Markdown 기본 문법을 공부할 때 배웠듯이 상황에 따라 HTML을 혼용하는 것은 바람직한 방법이다.  
하지만 GFM에서 HTML을 사용할 때 Markdown 컨텐츠 맥락에 맞지 않다고 판단되는 경우 HTML 태그의 실행을 막아주는 기능이 존재한다.  
> ex1)  
> <strong> <title> <style>
> <blockquote>
>   <xmp> is disallowed.  <XMP> is also disallowed.
> </blockquote>  

위 예시와 같이 몇몇 태그는 텍스트 그대로 출력이 된다.  
이러한 태그는 정해져 있으니 알아 두 도록 하자.  

* <title>
* <textarea>
* <style>
* <xmp>
* <iframe>
* <noembed>
* <noframes>
* <script>
* <plaintext>

이 외의 모든 HTML태그는 혼용하여 사용할 수 있다.  
