# Markdown extended Syntax

## Contents
* Tables
* Task List Items
* Strikethrough
* Autolinks
* Disallowed Raw HTML  

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
 | Paragraph  | Text     |

표를 만들 때는 때에 따라 정렬을 할 수 있다.  
정렬을 하려면 :과 세 개 이상의 -를 사용하면 된다.   

> ex2)  
> 
>       | Syntax    | Description | Test Text |
>       | :---      | :-------:   | ------:  |
>       | Header    | Title       | Here`s this | >       | Paragraph | Text        | And more  |


위 코드를 공백없이 나타내면 다음과 같다.

| Syntax    | Description | Test Text |
| :---      | :-------:   | ------:  |
| Header    | Title       | Here`s this |
| Paragraph | Text        | And more  |

위 코드와 표를 보고 정렬 방법을 직관적으로 알 수 있다.  
정렬하고자 하는 방향에 :을 찍고 -를 세 개 이상 입력하면 정렬할 수 있다.  
가운데 정렬을 하고 싶다면 -기호 세 개 이상과 그 양 옆에 :을 찍어주면 된다.  

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
>~~Markdown은 재미 없다.~~ 공부하다 보니 재미있다!  


<br><br>
## Autolinks  


<br><br>
## Disallowed Raw HTML  
