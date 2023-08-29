# 안녕 메롱

---
<h1>라라라라라리</h1>
---

## 라면 끓이는 법
1. 물을 끓인다.
2. 건더기와 스프, 라면사리를 넣는다.
3. 5분 뒤 맛있게 먹기!
---
## 오늘의 장보기 메뉴
- 양파
- 마늘
- 당근
---
# ``````오늘 해결해야 하는 문제``````
```javascript
if(input.trim().length > 0){

                //let search = { [`${sel_val}`]: input };
                //let search = sel_val+"="+input;

                //서버 호출 (비동기식)
                $.ajax({
                    url: "http://makeup-api.herokuapp.com/api/v1/products.json", //호출하고자_하는_서버경로
                    data: {[`${sel_val}`]: input},//"brand="+comp, //서버로_보내고자_하는_파라미터(인자) *입력창갯수만큼 가능*
                    type: "get", //전송방식(get/post)
                    dataType: "json" //서버로부터_응답되어오는_자원(return되는_자료형)
                }).done( function(data){
                    //요청에 성공했을 때 수행하는 곳
                    //data가 서버로부터 전달되어오는 return값이다.
                    console.log(data);
                    let msg_actual = put(data);