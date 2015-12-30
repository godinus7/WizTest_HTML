## HTML5  
  
## CSS3  
#### 태그선택자  
1. 태그 선택자 : 특정 태그를 선택할 때 사용  
```  
h1 { color: red; }  
```  
2. `*` 선택자 : 모든 태그를 선택할 때 사용  
```  
 * { margin: 0; padding: 0;}  
```  
3. `#`(id) 선택자 : 태그를 유일하게 구분짓는 id를 선택할 때 사용  
```  
#wrap { background-color: green; }  
<div id="wrap"> </div>   
```  
4. `.`(class) 선택자 : class 속성을 선택할 때 사용  
```  
.menu { width: 200px; }  
<div id="wrap" class="menu"> </div>  
<div id="content" class="menu"> </div>   
```  
5. `[]`속성 선택자 : 태그의 속성을 선택할 때 사용  
```  
input[type=text] { color: orange; }  
<input type="text" value="abc"></input>  
<input type="tel" value="010-1234-5678"></input>  
```  
6. `A>B`자손 선택자 : A의 바로 밑 하위 요소 B일때만 적용될 때 사용  
```  
div>h1 { color: red; }  
<div>  
	<h1>test</h1>  
</div>  
<div>  
	<ul>  
		<li><h1>menu1</h1></li>  
		<li>menu2</li>  
	</ul>  
</div>  
```  
7. `A B` 후손 선택자 : A의 하위 요소 중 B에 해당하면 적용, A 밑에 C 밑에 B가 있어도 적용  
```  
div h1 { color: red; }  
<div>  
	<h1>test</h1>  
</div>  
<div>  
	<ul>  
		<li><h1>menu1</h1></li>  
		<li>menu2</li>  
	</ul>  
</div>  
```   
8. 혼합 선택자 : 특정태그의 특정 클래스등 혼합하셔 사용  
```  
div li.menu { font-size: 16px; }  
<div>  
	<ul>  
		<li>menu1</li>  
		<li class="menu">menu2</li>  
		<li>menu3</li>  
	<ul>  
</div>  
```  
9. `A+B` 동위 선택자 : A태그와 동등한 위치에 있는 B태그 중 A의 바로 밑에 있는 B태그에만 적용하는 선택자.  
10. `A~B` 동위 선택자 : A태그와 동등한 위치에 있는 모든 B태그에 적용하는 선택자  
```  
<style>  
	h3~div {  
		font-size: 10px;  
		color: orange;  
	}  
	h3+div {  
		color: red;  
	}  
</style>  
<h3>Test</h3>  
<div>div1</div>  
<div>div2</div>  
<div>div3</div>  
```  