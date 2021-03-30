# SE_woo

# ***Overview***
존 그루버(John Gruber)의 기본 구문의 원래 설계 문서에 설명은 매일 매일 필요한 많은 요소를 추가하지만 어떤 사람들에게는 충분하지 않았다. 그래서 확장 구문이 추가되었다.

여러 개인과 조직은 테이블, 코드 블록, 구문 강조, URL 자동 연결 및 각주와 같은 추가 요소를 추가하여 기본 구문을 확장했다. 이러한 요소는 기본 Markdown 구문을 기반으로 하는 경량 마크업 언어를 사용하거나 호환되는 Markdown 프로세서에 확장을 추가하여 활성화 할 수 있다.

# ***Availability***
모든 Markdown 애플리케이션이 확장 구문 요소를 지원하는 것은 아니다. 응용 프로그램에서 사용중인 경량 마크업 언어가 사용하려는 확장 구문 요소를 지원하는지 여부를 확인해야 한다. 그렇지 않은 경우 마크다운 프로세서에서 확장을 활성화 할 수 있다.

# ***Lightweight Markup Languages***
Markdown의 상위 집합인 몇 가지 경량 마크업 언어가 있다. 여기에는 Gruber의 기본구문이 포함되며 테이블, 코드 블록, 구문 강조 표시, URL 자동 연결 및 각주와 같은 추가 요소를 추가하여 이를 기반으로 한다. 가장 널리 사용되는 대부분의 Markdown 응용 프로그램은 다음과 같은 경량 마크 업 언어 중 하나를 사용한다.

- [CommonMark](https://commonmark.org)
- [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/)
- [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/)
- [MultiMarkdown](https://fletcherpenney.net/multimarkdown/)
- [R Markdown](https://rmarkdown.rstudio.com)

# ***Markdown Processors***
대부분은 확장 구문 요소를 활성화하는 확장을 추가 할 수 있다. 자세한 내용은 프로세서 설명서를 확인하라.
[dozens of Markdown processors](https://github.com/markdown/markdown.github.com/wiki/Implementations)

# ***Tables***
표를 추가하려면 세 개 이상의 하이픈(---)을 사용하여 각 열의 헤더를 만들고 파이프 (|)를 사용하여 각 열을 구분한다.  
선택적으로 테이블의 양쪽 끝에 파이프를 추가할 수 있다.  
예시는 아래와 같다. (셀 너비는 다를 수 있다.)

\| Syntax      | Description |  
\| ----------- | ----------- |  
\| Header      | Title       |  
\| Paragraph   | Text        |  

출력은 다음과 같다.
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

# ***Alignment***
머리글 행 내 하이픈의 왼쪽, 오른쪽 또는 양쪽에 콜론(:)을 추가하여 열의 텍스트를 왼쪽, 오른쪽 또는 가운데로 정렬 할 수 있다.

예시는 아래와 같다.  

\| Syntax      | Description | Test Text     |  
\| :---        |    :----:   |          ---: |  
\| Header      | Title       | Here's this   |  
\| Paragraph   | Text        | And more      |  

출력은 다음과 같다.
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

# ***Formatting Text in Tables***
표 내의 텍스트 서식을 지정할 수 있다.  
예를 들어 링크, 코드(코드 블록이 아닌 백틱(`)의 단어 또는 구문만) 및 강조를 추가할 수 있다.

제목, 인용구, 목록, 수평 규칙, 이미지 또는 HTML 태그는 추가할 수 없다.

# ***Escaping Pipe Characters in Tables***
HTML 문자코드(\&#124;)를 사용하여 테이블에 파이프(|)문자를 표시할 수 있다.

# ***Fenced Code Blocks***
기본 Markdown 구문을 사용하면 공백 4개 또는 탭 1개로 줄을 들여 쓰기 하여 코드 블록을 만들 수 있다. 그게 불편하다면 차단된 코드 블록을 사용해보자. 마크다운 프로세서 또는 편집기에 따라 코드 블록 앞뒤의 줄에 세 개의 백틱 (```) 또는 세 개의 물결표 (~~~)를 사용한다.  
제일 좋은 부분은 어떤 줄도 들여 쓸 필요가 없다. 예시는 아래와 같다.

\```  
{  
  "firstName": "John",  
  "lastName": "Smith",  
  "age": 25  
}  
\```

출력은 다음과 같다.
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

# ***Syntax Highlighting***
많은 Markdown 프로세서는 분리 코드 블록에 대한 구문 강조를 지원한다.  
이 기능을 사용하면 코드가 작성된 모든 언어에 대해 색상 강조 표시를 추가할 수 있다.  
구문 강조를 추가하려면 분리 코드 블록 앞의 백틱 옆에 언어를 지정하라.

예시는 아래와 같다.  

\```json  
{  
  "firstName": "John",  
  "lastName": "Smith",  
  "age": 25  
}  
\```

출력은 다음과 같다
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

# ***Footnotes***
각주를 사용하면 문서 본문을 어지럽히지 않고 메모와 참조를 추가 할 수 있다.  
각주를 생성하면 각주 참조를 추가한 위치에 링크가 있는 위 첨자 번호가 나타난다.  
독자는 링크를 클릭하여 페이지 하단의 각주 내용으로 이동할 수 있다.

각주 참조를 만들려면 괄호([^1])안에 캐럿과 식별자를 추가한다.  
식별자는 숫자 또는 단어 일 수 있지만 공백이나 탭은 포함 할 수 없다.  
식별자는 각주 참조를 각주 자체와 만 연관시킨다.  
출력에서 ​​각주는 순차적으로 번호가 매겨진다.

콜론과 텍스트 ([^1]: My footnote.)와 함께 대괄호 안에 다른 캐럿과 숫자를 사용하여 각주를 추가한다. 문서 끝에 각주를 넣을 필요가 없다.  
목록, 블록 따옴표 및 표와 같은 다른 요소 내부를 제외하고 어디에나 둘 수 있다.

예시는 아래와 같다.

Here's a simple footnote,[^1] and here's a longer one.[^bignote]  

[^1]: This is the first footnote.  

[^bignote]: Here's one with multiple paragraphs and code.

Indent paragraphs to include them in the footnote.

\`{ my code }`

Add as many paragraphs as you like.

출력은 다음과 같다.

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

# ***Heading IDs***
많은 Markdown 프로세서는 제목에 대한 사용자 지정 ID를 지원한다. 일부 Markdown 프로세서는 자동으로 추가한다. 사용자 지정 ID를 추가하면 제목에 직접 연결하고 CSS로 수정할 수 있다. 사용자 지정 머리글 ID를 추가하려면 머리글과 같은 줄에서 사용자 지정 ID를 중괄호로 묶는다.

예시는 아래와 같다.

\### My Great Heading {#custom-id}

HTML은 아래와 같다.

\<h3 id="custom-id">My Great Heading\</h3>

# ***Linking to Heading IDs***
숫자 기호 (#) 다음에 사용자 지정 머리글 ID가 있는 표준 링크를 만들어 파일에서 사용자 지정 ID가 있는 머리글에 연결할 수 있다.

예시는 아래와 같다.

\[Heading IDs](#heading-ids)

출력은 다음과 같다.

[Heading IDs](#heading-ids)

# ***Definition Lists***
일부 Markdown 프로세서를 사용하면 용어 정의 목록과 해당 정의를 만들 수 있다.  
정의 목록을 만들려면 첫 번째 줄에 용어를 입력하고 다음 줄에 콜론과 공백 및 정의를 입력한다.

예시는 다음과 같다.

First Term  
: This is the definition of the first term.

Second Term  
: This is one definition of the second term.  
: This is another definition of the second term.  

출력은 다음과 같다.  
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

# ***Strikethrough***
단어의 가운데에 수평선을 넣어 취소할 수 있다.  
단어를 취소하려면 단어 앞뒤에 두 개의 물결표 기호 (~~)를 사용한다.

예시는 아래와 같다.

\~~The world is flat.~~ We now know that the world is round.

출력은 다음과 같다.

~~The world is flat.~~ We now know that the world is round.

# ***Task Lists***
작업 목록을 사용하면 확인란이 있는 항목 목록을 만들 수 있다.  
작업 목록을 지원하는 Markdown 응용 프로그램에서는 콘텐츠 옆에 확인란이 표시된다.  
작업 목록을 만들려면 작업 목록 항목 앞에 대시(-) 및 공백([ ])이있는 대괄호를 추가한다.  
확인란을 선택하려면 대괄호 ([x]) 사이에 x를 추가한다.

예시는 아래와 같다.

\- [x] Write the press release  
\- [ ] Update the website  
\- [ ] Contact the media  

출력은 다음과 같다.

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

# ***Emoji***
마크다운 파일에 이모티콘을 추가하는 방법에는 두 가지가 있다.  
이모티콘을 복사하여 마크다운 형식의 텍스트에 붙여 넣거나 이모티콘 단축 코드를 입력하는 것이다.

# Copying and Pasting Emoji
대부분의 경우 [Emojipedia](https://emojipedia.org) 와 같은 소스에서 그림 이모티콘을 복사하여 문서에 붙여넣을 수 있다.  
많은 Markdown 응용 프로그램은 Markdown 형식의 텍스트에 이모지를 자동으로 표시한다.  
Markdown 애플리케이션에서 내보낸 HTML 및 PDF 파일은 이모티콘을 표시해야한다.

# Using Emoji Shortcodes
일부 Markdown 애플리케이션에서는 이모티콘 단축 코드를 입력하여 이모티콘을 삽입할 수 있다.  
콜론으로 시작하고 끝나며 그림 이모티콘의 이름이 포함된다.

예시는 아래와 같다.

Gone camping! :tent: Be back soon.

That is so funny! :joy:

# ***Automatic URL Linking***
많은 Markdown 프로세서는 자동으로 URL을 링크로 변환한다.  

예시는 아래와 같다.

http://www.example.com

출력은 다음과 같다.

http://www.example.com

# ***Disabling Automatic URL Linking***
URL이 자동으로 연결되는 것을 원하지 않는 경우 URL을 백틱이 있는 코드 로 표시하여 링크를 제거할 수 있다.

예시는 아래와 같다.

\`http://www.example.com\`

출력은 다음과 같다.

`http://www.example.com`
