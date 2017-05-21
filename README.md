## css-drawing-Character


#### 라이언(Ryan)
1. - - [라이언 HTML 구조잡기](https://github.com/u4bi/css-drawing-Character/commit/b75791729b4da6566911f5fef11939477e04c87d)
   - 각 div 구조의 클래스 정의
   - **`ryan` : 라이언 전체영역**
   - **`ear left, ear right` : 왼쪽 귀 오른쪽 귀**
     - `선택자와 선택자 사이에 공백은?`
     - `하위요소를 설정함을 의미`
   - **`face` : 라이언의 얼굴**
  
  _[html]_
  ```{html}
   <!-- HTML 구조 잡기-->
   
   <div class="ryan"> <!-- 라이언 -->
   
     <div class="ear left"></div> <!-- 왼쪽 귀 -->
     <div class="ear right"></div><!-- 오른쪽 귀 -->
    
     <div class="face"> <!-- 라이언의 얼굴-->
    
     </div>
    
   </div>
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfLTVJNVJrRkx0RE0)

2. - - [라이언 귀 스타일 정의](https://github.com/u4bi/css-drawing-Character/commit/77790f2bba48c262e1fba98d304aaafbb364a9e8)
   - **`.ryan .ear` : 양쪽 귀에 공동으로 들어갈 스타일 요소**
      - `앱솔루트, 탑0, 높이너비92px, 보더10px검은색 줄선`
      - `보더반지름100%, 배경색 주황계열` 
   - **`ryan .ear.left` : 왼쪽 귀 스타일요소**
      - `좌측 기준에서 54px 떨어진 곳에 배치`
   - **`ryan .ear.right` : 오른쪽 귀 스타일요소**
      - `우측 기준에서 54px 떨어진 곳에 배치`
   - `하위 다중 클래스 사용할 경우에는?`
   - `공백없이 바로 붙여 사용해야함`
     - `예: ear.right {}`

  _[css]_
  ```{css}
   /* 귀 공통 스타일 */
   .ryan .ear {
     position: absolute;
     top: 0;
     width: 92px;
     height: 92px;
     border: 10px solid #000;
     border-radius: 100%;
     background: #d59729;
   }
  
  /* 왼쪽 귀 위치 */
   .ryan .ear.left {
     left: 54px;
   }
  
  /* 오른쪽 귀 위치 */
   .ryan .ear.right {
     right: 54px;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfaXhJUUhsS1Q3OXc)

3. - - [라이언의 전체 영역 스타일 잡기](https://github.com/u4bi/css-drawing-Character/commit/b2bf2728680ca6058e93e8e25de10aad8ffcb841)
   - **`.ryan` : 라이언의 전체 영역**
      - `릴렉티브로 설정, 마진의 너비 50px 마진의 높이는 auto`
   - **`*와 after before` : <html> 영역**
      - `박스 사이징을 보더 박스로 설정`
   - **`body` : <body> 영역**
      - `배경을 진한 보라색으로 설정`   

  _[css]_
  ```{css}
   /* html */  
   *, *:after, *:before{
     box-sizing: border-box;
   }
   
   /* body */
   body{
     background: #313654;
   }
   
   /* 라이언의 전체 영역 */
   .ryan{
     position: relative;
     margin: 50px auto;
     width: 400px;
     height: 380px;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfOUVfZ2Z5RFY1TGs)

4. - - [라이언 얼굴 스타일 정의](https://github.com/u4bi/css-drawing-Character/commit/cf8d5d1525a2b5be60b324ef87bbc566d44cbb85)
   - 라이언 영역안에서 바로 아래 붙는 원을 그림
   - **`.ryan .face` : 라이언의 얼굴 원형**
     - `앱솔루트, 그 바로 아래 딱 붙기 위해 바텀 0, 높이400px, 너비367px`
     - `보더반지름100%, 보더10px검은색 줄선, 배경색 주황계열`
  
  _[css]_
  ```{css}
   .ryan .face{
     position: absolute;
     bottom: 0;
     width: 400px;
     height: 367px;
     border-radius: 100%;
     border: 10px solid #000;
     background: #d59729;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfLTRPU1Z6UkxycTA)

5. - - [라이언 눈썹 스타일 정의](https://github.com/u4bi/css-drawing-Character/commit/39249752686658323ccd14c6bef8f36dfdebe9d2)
   - **`.ryan .eyebrow` : 양쪽 눈썹에 공통으로 들어갈 스타일 요소**
     - `앱솔루트, 탑106px, 너비78px, 높이14px, 보더반지름14px, 배경색 검은계열`
   - **`.ryan .eyebrow.left` : 왼쪽 눈썹 스타일 요소**
     - `좌측 기준에서 68px 떨어진 곳에 배치`
   - **`.ryan .eyebrow.right` : 오른쪽 눈썹 스타일 요소**
     - `우측 기준에서 68px 떨어진 곳에 배치`
  
  _[html]_
  ```{html}
   <div class="face"> <!-- 라이언의 얼굴-->
   
     <div class="eyebrow left"></div> <!-- 왼쪽 눈썹 -->
     <div class="eyebrow right"></div> <!-- 오른쪽 눈썹 -->
     
   </div>
  ```
  _[css]_
  ```{css}
   /* 눈썹 공통 스타일 */
   .ryan .eyebrow {
     position:absolute;
     top: 106px;
     width: 78px;
     height: 14px;
     border-radius: 14px;
     background: #000;
   }

   /* 왼쪽 눈썹 위치 */
   .ryan .eyebrow.left{
     left: 68px;
   }

   /* 오른쪽 눈썹 위치*/
   .ryan .eyebrow.right{
     right: 68px;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfZlRTbmRBREI5NXc)

6. - - [라이언 눈 스타일 정의](https://github.com/u4bi/css-drawing-Character/commit/28f60a455ca80a90a823c9b221f2dbe028496f40)
   - **`.ryan eye` : 양쪽 눈에 공통으로 들어갈 스타일 요소**
      - `앱솔루트, 탑147px, 너비높이26px, 보더반지름100%, 배경색 검은계열`
   - **`.ryan .eye.left` : 왼쪽 눈 스타일 요소**
     - `좌측 기준에서 68px 떨어진 곳에 배치`
   - **`.ryan .eye.right` : 오른쪽 눈 스타일 요소**
     - `우측 기준에서 68px 떨어진 곳에 배치`
  
  _[html]_
  ```{html}
   <div class="face"> <!-- 라이언의 얼굴-->
     
     ... <!-- 왼쪽 눈썹 -->
     ... <!-- 오른쪽 눈썹 -->
     
     <div class="eye left"></div> <!-- 왼쪽 눈 -->
     <div class="eye right"></div> <!-- 오른쪽 눈 -->
     
   </div>
  ```
  _[css]_
  ```{css}
  /* 눈 공통 스타일 */
   .ryan .eye {
     position: absolute;
     top: 147px;
     width: 26px;
     height: 26px;
     border-radius: 100%;
     background: #000;
   }

   /* 왼쪽 눈 위치 */
   .ryan .eye.left{
     left: 98px;
   }
   
   /* 오른쪽 눈 위치 */
   .ryan .eye.right{
     right: 98px;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfWGQ3ZDBLdEY0ckk)

7. - - [라이언 코 스타일 정의](https://github.com/u4bi/css-drawing-Character/commit/d3473500f5a1ed9e84a064c64ec82470d2dbdb9d)
   - **`.ryan .nose` : 가운데 코에 들어갈 스타일 요소**
     - `앱솔루트, 탑 184, 좌측 기준에서 50% 떨어진 곳에 배치`
     - `마진 레프트축 -16px(코의 너비만큼 땡김)`
     - `너비32px, 높이33px, 보더반지름100%, 배경색 검은계열`

  _[html]_
  ```{html}
   <div class="face"> <!-- 라이언의 얼굴-->
     
     ... <!-- 왼쪽 눈 -->
     ... <!-- 오른쪽 눈 -->
     
     <div class="nose"></div> <!-- 코 -->
     
   </div>
  ```
  _[css]_
  ```{css}
  /* 코 위치 */
   .ryan .nose {
     position: absolute;
     top: 184px;
     left: 50%;
     margin-left: -16px;
     width: 32px;
     height: 33px;
     border-radius: 100%;
     background: #000;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfUUlfVk1qbUlCRU0)

8. - - [라이언 코 border-radius 속성 수정](https://github.com/u4bi/css-drawing-Character/commit/6c4ea73da37bcfbb1f17945b5a1f5ec77a33e8ab)
   - 코를 좀더 자연스럽게 하기 위함
   - **`border-radius` : 속성값 수정**
     - `(변경전) 100% -> (변경후) 80% 80% 100% 100%;`  
     - `해당 속성은 왼쪽위, 오른쪽위, 오른쪽아래, 왼쪽 아래`
     - `시계 방향으로 진행함`
  
  _[css]_   
  ```{css}
  /* 코 위치 */
   .ryan .nose {
   
     etc...
     
     border-radius: 80% 80% 100% 100%;
     
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfcTliYmhPTWJuTkE)

9. - - [라이언 입 스타일 정의](https://github.com/u4bi/css-drawing-Character/commit/38c81c69ac8892d67dac84a989d8b8e75a96ae55)
   - **`.ryan .mouth` : 양축 부분 입에 공통으로 들어갈 스타일 요소**
     - `앱솔루트, 탑191px, 너비73px, 높이68px`
     - ` 보더10px검은색 줄선, 보더반지름100%, 배경색 검은계열`
   - **`.ryan .mouth.left` : 좌측 부분 입 스타일 요소**
     - `좌측 기준에서 127px 떨어진 곳에 배치`
   - **`.ryan .mouth.right` : 우측 부분 입 스타일 요소**
     - `우측 기준에서 127px 떨어진 곳에 배치`

  _[html]_   
  ```{html}
   <div class="face"> <!-- 라이언의 얼굴-->
     
     <div class="mouth left"></div> <!-- 입 좌측부분 -->
     <div class="mouth right"></div> <!-- 입 우측부분 -->
     
   </div>
  ```
  _[css]_
  ```{css}
   /* 입 공통 스타일 */
   .ryan .mouth {
     position: absolute;
     top: 191px;
     width: 73px;
     height: 68px;
     border: 10px solid #000;
     border-radius: 100%;
     background: #fff;
   }

   /* 입 좌측 부분 위치 */
   .ryan .mouth.left {
     left: 127px;
   }

   /* 입 우측 부분 위치 */
   .ryan .mouth.right {
     right: 127px;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfUHhPcWxiQkdhOFU)

10. - - [nose 클래스와 mouth 클래스의 쌓힘 순서 조정](https://github.com/u4bi/css-drawing-Character/commit/7db8c5d590fe4d4e6c6e2d29f6640dcded5ca969)
   - **`.ryan .nose { z-index }` : 코의 렌더링 순서**
     - `z-index의 속성값을 1로 조정` 
     - `얼굴의 뒤 -1 / 입의 뒤 0 / 입의 앞 1`
     - `참고`: http://www.w3schools.com/cssref/pr_pos_z-index.asp
  
  _[css]_
  ```{css}
   /* 코 위치 */
   .ryan .nose {
   
      etc...
     
      z-index: 1;
     
   }  
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfM3pleUpubndqejQ)

11. - - [라이언의 입부분에 content속성을 가진 before 요소 추가](https://github.com/u4bi/css-drawing-Character/commit/de97208a02cb179c4586aac8189c3393a1d26da1)
   - 입을 좀더 자연스럽게 하기 위한 작업
   -  `입 중앙의 검은 줄선을 흰색 배경을 가진 content 속성으로 덮는다.`
   - **`ryan .mouth:before` : before 통해 content속성의 가상요소 추가**
     - ` 콘텐츠 문자열 공백, 앱솔루트, 너비5px,높이5px, 배경색 빨간계열(임시)`
     - `z-index 1로 설정 (이 가상요소가 위로 쌓힘)`
  
  _[css]_
  ```{css}
  /* 입 공통 before 가상요소 */
   .ryan .mouth:before {
      content: "";
      position: absolute;
      width: 5px;
      height: 5px;
      background: red; /* 테스트를 위한 색상 추후 #fff로 변경 */
      z-index: 1;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfQ3R2VTl3ckFIUkE)

12. - - [라이언의 입부분에 추가된 content 속성의 스타일 요소 정의](https://github.com/u4bi/css-drawing-Character/commit/2b2b5fd674725bfc65c4f3d30da4cc94ceeadd99)
   - 흰 배경의 content 속성을 알맞는 크기로 조정해 검은선 덮기
   - **`ryan .mouth:before` : 입의 가상요소에 공동으로 추가된 content 속성**
     - `탑2px, 너비30px, 높이33px`
     - `회전 -45도, 배경색 하얀계열`
   - **`.ryan .mouth.left:before` : 좌측 부분 입 before 가상요소**
     - `좌측 기준에서 29px 떨어진 곳에 배치`
   - **`.ryan .mouth.right:before` : 우측 부분 입 before 가상요소**
     - `우측 기준에서 29px 떨어진 곳에 배치`
  
  _[css]_
  ```{css}
   /* 입 공통 before 가상요소 */
   .ryan .mouth:before {
    
      etc...
    
      width: 30px;
      height: 33px;
      -webkit-transform: rotate(-45deg);
      transform: rotate(-45deg);
      background: #fff;
      
   }
   
   /* 입 좌측 부분 before 가상요소 */
   .ryan .mouth.left:before {
      left: 29px;
   }

   /* 입 우측 부분 before 가상요소 */
   .ryan .mouth.right:before {
      right: 29px;
   }
  ```
![Alt text](http://drive.google.com/uc?export=view&id=0B3XkfYbZArSfTDJwYmZCcXZrakk)

13. - - [라이언의 코를 입에 추가된 가상요소의 앞으로 조정](https://github.com/u4bi/css-drawing-Character/commit/45facb88157e63f8660355f5395133b8f8fdbe75)
   - 입의 가상요소가 코를 덮고 있는데 코를 위로 쌓음
   - **`.ryan .nose { z-index }` : 코의 렌더링 순서**
     - `z- index의 속성값을 2로 수정`
     - `얼굴의 뒤-1 /입의 뒤 0/입의 앞 1 /가상요소의 앞 2`
  
  _[css]_
  ```{css}
   /* 코 위치 */
   .ryan .nose {
   
      etc...
     
      z-index: 2;
     
   }  
  ```
  
  ###### 도움을 주신 zineeworld(http://zinee-world.tistory.com) 님에게 감사드립니다.
  ###### 더 많은 CSS 드로잉 작품은 [이곳](http://zinee-world.tistory.com/category/CSS%20Drawing/Gallery)에서 확인하실 수 있습니다.