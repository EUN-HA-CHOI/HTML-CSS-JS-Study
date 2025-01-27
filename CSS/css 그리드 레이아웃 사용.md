## CSS 그리드 레이아웃 사용하기  

* CSS 그리드 레이아웃에서 사용하는 용어  
  가로 방향 줄row , 세로 방향 칼럼column 사용  

* CSS 그리드 레이아웃 항목을 배치하는 속성  
  * 그리드 컨테이너를 지정하는 display 속성  
    레이아웃을 지정할 때 먼저 그리드를 적용할 요소의 바깥 부분을 그리드 컨테이너로 만들어야 함.  
    -> 속성값  
     : grid(블록 레벨 요소로 배치)  
     : inline-grid(인라인 레벨 요소로 배치)
   
  * 칼럼과 줄을 지정하는 grid-template-columns, grid-template-rows 속성  
    컨테이너 안에 항목을 배치할 때 칼럼과 줄의 크기와 개수를 정하기 위해 사용  
    
   ```css
   #wrapper{
        display:grid;   /*그리드 컨테이너 지정*/
        grid-template-columns: 200px 200px 200px;  /*너비가 200px인 칼럼 3개*/
        grid-template-rows:100px;  /*줄 높이 100px*/
      }
   ```
   ```html
   <body>
    <div id="wrapper">
      <div class="items">Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet, reprehenderit.Lorem                ipsum dolor, sit amet consectetur adipisicing elit. </div>
      <div class="items">Lorem ipsum dolor, sit amet consectetur adipisicing elit.Lorem ipsum dolor, sit amet              consectetur adipisicing elit</div>
      <div class="items">Lorem ipsum dolor sit amet.Lorem ipsum dolor, sit amet consectetur adipisicing                    elit</div>
      <div class="items">Lorem ipsum dolor sit.Lorem ipsum dolor, sit amet consectetur adipisicing elit</div>
      <div class="items">Lorem, ipsum dolor.</div>
    </div>
  </body>
    ```
    
    <img width="300" alt="스크린샷 2022-06-23 오후 3 13 59" src="https://user-images.githubusercontent.com/97012561/175228115-3b06db9f-c3ad-4221-b840-0872ab0cecad.png">
    
    
* 상대적인 크기를 지정하는 fr 단위  
  * 반응형 웹 디자인에는 px 단위를 사용하면 항상 크기가 고정되므로 적합하지 않다.  
  그래서 상대적인 크기를 지정할 수 있는 fr(fraction)단위 사용  
  * ex.3개의 너비가 같은 칼럼 -> `grid-template-columns: 1fr 1fr 1fr`   

* 값이 반복될 때 줄여서 표현할 수 있는 repeat() 함수   
  * ex. `grid-template-columns: 1fr 1fr 1fr` -> `grid-template-columns: repeat(3, 1fr)`   

* 최솟값과 최댓값을 지정하는 minmax() 함수  
  * minmax() 함수를 사용하면 줄 높이를 고정하지 않고 최솟값과 최댓값을 사용해서 유연하게 지정할 수 있다.  
  * `grid-template-rows: minmax(100px, auto); /*줄 높이는 최소 100px*/`   

* 자동으로 칼럼 개수를 조절하는 auto-fill, auto-fit 값  
  * repeat() 함수를 사용해서 크기가 같은 칼럼을 반복할 때  
   `grid-template-columns: repeat(3, 1fr)` ->  `grid-template-columns: repeat(auto-fit,200px)`
  * 화면이 넓어지면 칼럼 개수가 많아지고 반대로 화면이 좁아지면 칼럼 개수가 줄어든다.  
 
 * 그리드 항목의 간격을 지정하는 grid-column-gap, grid-row-gap, grid-gap 속성  
    * grid-column-gap : 칼럼과 칼럼 사이 간격 지정  
    * grid-row-gap : 줄과 줄 사이 간격 지정  
    * grid-gap : 칼럼과 줄 사이의 간격을 한꺼번에 지정  
  
