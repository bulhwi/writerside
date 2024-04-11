# 정리

## Curl (Client URL)
curl(client url) 명령어는 프로토콜들을 이용해 URL 로 데이터를 전송하여 서버에 데이터를 보내거나 가져올때 사용하기 위한 명령줄 도구 및 라이브러리이다. 쉽게말해 예를들어 자바스크립트 환경에서 REST API(http)를 테스트하고싶다면 보통 ajax, fetch 를 이용해 요청을 보내는 것과 같이, SHELL(커맨드라인 환경)에서 REST API(http) 테스트 하고 싶으면 curl 명령어를 이용하면 된다 라고 이해하면 된다.

## Curl 명령어
```Shell
$ curl [options...] <url>
$ curl --help all 
```

| 명령어                      | 설명                                                              |
|--------------------------|-----------------------------------------------------------------|
| -k, --insecure           | https 프로토콜에서 SSL 인증서에 대한 검증없이 연결                                |
| -i, --head               | HTTP 헤더만 보여주고 컨텐츠는 표시하지 않음                                      |
| -D, --dump-header [file] | HTTP 헤더를 file에 기록 (덤프)                                          |
| -L, --location           | --max-redirs 옵션 뒤에 숫자로 몇 번의 리디렉션까지 따라갈 것인지를 적을 수 있다.<br/>기본 값은 50이다. |

## Write content
%product% supports two types of markup: Markdown and XML.
When you create a new help article, you can choose between two topic types, but this doesn't mean you have to stick to a single format.
You can author content in Markdown and extend it with semantic attributes or inject entire XML elements.

## Inject XML
For example, this is how you inject a procedure:

<procedure title="Inject a procedure" id="inject-a-procedure">
    <step>
        <p>Start typing and select a procedure type from the completion suggestions:</p>
        <img src="completion_procedure.png" alt="completion suggestions for procedure" border-effect="line"/>
    </step>
    <step>
        <p>Press <shortcut>Tab</shortcut> or <shortcut>Enter</shortcut> to insert the markup.</p>
    </step>
</procedure>

## Add interactive elements

### Tabs
To add switchable content, you can make use of tabs (inject them by starting to type `tab` on a new line):

<tabs>
    <tab title="Markdown">
        <code-block lang="plain text">![Alt Text](new_topic_options.png){ width=450 }</code-block>
    </tab>
    <tab title="Semantic markup">
        <code-block lang="xml">
            <![CDATA[<img src="new_topic_options.png" alt="Alt text" width="450px"/>]]></code-block>
    </tab>
</tabs>

### Collapsible blocks
Apart from injecting entire XML elements, you can use attributes to configure the behavior of certain elements.
For example, you can collapse a chapter that contains non-essential information:

#### Supplementary info {collapsible="true"}
Content under a collapsible header will be collapsed by default,
but you can modify the behavior by adding the following attribute:
`default-state="expanded"`

### Convert selection to XML
If you need to extend an element with more functions, you can convert selected content from Markdown to semantic markup.
For example, if you want to merge cells in a table, it's much easier to convert it to XML than do this in Markdown.
Position the caret anywhere in the table and press <shortcut>Alt+Enter</shortcut>:

<img src="convert_table_to_xml.png" alt="Convert table to XML" width="706" border-effect="line"/>

## Feedback and support
Please report any issues, usability improvements, or feature requests to our
<a href="https://youtrack.jetbrains.com/newIssue?project=WRS">YouTrack project</a>
(you will need to register).

You are welcome to join our
<a href="https://jb.gg/WRS_Slack">public Slack workspace</a>.
Before you do, please read our [Code of conduct](https://plugins.jetbrains.com/plugin/20158-writerside/docs/writerside-code-of-conduct.html).
We assume that you’ve read and acknowledged it before joining.

You can also always email us at [writerside@jetbrains.com](mailto:writerside@jetbrains.com).

<seealso>
    <category ref="wrs">
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/markup-reference.html">Markup reference</a>
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/manage-table-of-contents.html">Reorder topics in the TOC</a>
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/local-build.html">Build and publish</a>
        <a href="https://plugins.jetbrains.com/plugin/20158-writerside/docs/configure-search.html">Configure Search</a>
    </category>
</seealso>