## 요소 주변의 여백을 설정하는 margin 속성  
 `margin: <크기> | <백분율> | auto`

* margin 속성을 사용하여 웹 문서를 가운데 정렬하기  

* 마진 중첩 이해하기  

* 콘텐츠와 테두리 사이의 여백을 설정하는 padding 속성  
  

## 웹 문서의 레이아웃 만들기  
* 배치 방법 결정하는 display 속성  
  -블록 레벨 요소와 인라인 레벨 요소를 서로 바꿔서 사용 가능.
  -웹 문서의 내비게이션을 만들면서 메뉴 항목을 가로로 배치할 때 많이 사용하고, 이미지를 표 형태로 배치할 수 있다.  
  -문서 레이아웃을 만들 때 자주 사용하는 속성

|    종류      |                        설명                     |
|-------------|------------------------------------------------|
| block | 인라인 레벨 요소를 블록 레벨 요소로 만든다.                    |
| inline | 블록 레벨 요소를 인라인 레벨 요소로 만든다.                    |
| inline-block| 인라인 레벨,블록 레벨 요소의 속성을 모두 갖음,마진과 패딩 설정|  


* 왼쪽이나 오른쪽으로 배치하는 float 속성  
  -이미지를 표시하여 주변에 텍스트가 둘러싸도록 할 수 있다.  
  
|    종류      |  설명           |
|-------------|----------------|
| left | 요소를 문서 왼쪽에 배치     |
| right |  요소를 문서 오른쪽에 배치 |
| none| 기본값|  

``` css
<style>
   img {
     float: left; /*왼쪽에 떠 있게*/
     margin-right:40px;
   }
</style>
```
<img width="350" alt="스크린샷 2022-05-27 오후 1 21 05" src="https://user-images.githubusercontent.com/97012561/170628504-61c28cd9-9afa-4451-94b0-b2c319c41348.png">

* float 속성을 해제하는 clear 속성  
  -float 속성이 더 이상 유효하지 않다고 알려 주는 속성.

```css 
<style>
div {
 padding:20px;
 margin:10px;
}
#box1 {
  background:#ffd800;
  float:left;      /* 왼쪽으로 플로팅 */
} 
#box2 {
  background:#0094ff;
  float:left;       /* 왼쪽으로 플로팅 */
}
#box3 {
  background: #00ff21;   /*float 속성을 지정하지 않았으므로 웹 브라우저의 기본 흐름으로 배치됨*/
}
#box4 {
  background:#a874ff;
  clear:left;        /* 플로팅 해제 */
}
</style>		
```
<img width="400" alt="스크린샷 2022-05-30 오후 12 04 11" src="https://user-images.githubusercontent.com/97012561/170909706-8b48b7e9-5d28-4b74-bcee-10cd2bdefe1f.png">  

