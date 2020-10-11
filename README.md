병렬 프로그래밍
===========
#### Executor.execute (진행시켜! (나몰라라...)) vs ExecutorService.submit (공손하게 제출하면서 진행상황 및 종료여부를 확인할 수 있는 Future 를 돌려줌)
```
Executor.execute 와 ExecutorService.submit 은 예외 처리 전략에 차이가 있다.  
Executor.execute 의 기본 처리 전략은 예외 발생 시 UncaughtExceptionHandler 가 stacktrace 를 콘솔에 출력한다. (custom handler 사용 가능) 
ExecutorService.submit 는 Future 의 get 메소드 호출 시 ExecutionException 발생시킨다.
```

**의문점**
``` 
ExecutorService 의 <T> Future<T> submit(Runnable task, T result) 는 왜 존재할까? 설계 목적이 뭘까? 
```

```java
public interface ExecutorService {
    <T> Future<T> submit(Runnable task, T result);
}
```
#### 용어 정리
- 처리량(throughput): 병렬로 
========================  
You can use the [editor on GitHub](https://github.com/Yungdi/Yungdi.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Yungdi/Yungdi.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

<mxfile host="www.draw.io" modified="2019-11-22T07:27:25.069Z" agent="Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.97 Safari/537.36" etag="tIJoxi5KbqdbIRYhcwSA" version="12.2.9" type="github" pages="1">
  <diagram name="Page-1" id="97916047-d0de-89f5-080d-49f4d83e522f">
    <mxGraphModel dx="1426" dy="794" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1.5" pageWidth="1169" pageHeight="827" background="#ffffff" math="0" shadow="0">
      <root>
        <mxCell id="0"/>
        <mxCell id="1" parent="0"/>
        <mxCell id="Gr3s9tRPsxVrafdJNDCz-60" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="2" target="Gr3s9tRPsxVrafdJNDCz-59">
          <mxGeometry relative="1" as="geometry"/>
        </mxCell>
        <mxCell id="2" value="programming study" style="rounded=1;fillColor=#10739E;strokeColor=none;shadow=1;gradientColor=none;fontStyle=1;fontColor=#FFFFFF;fontSize=14;" parent="1" vertex="1">
          <mxGeometry x="672" y="205.5" width="200" height="60" as="geometry"/>
        </mxCell>
        <mxCell id="Gr3s9tRPsxVrafdJNDCz-59" value="java" style="rounded=1;fillColor=#10739E;strokeColor=none;shadow=1;gradientColor=none;fontStyle=1;fontColor=#FFFFFF;fontSize=14;" vertex="1" parent="1">
          <mxGeometry x="672" y="345.5" width="200" height="60" as="geometry"/>
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
