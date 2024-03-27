<!-- 목표 : 다양한 태그를 활용해 예시 화면의 기능 만들어보기 -->
<!-- - 복습할 개념 체크 리스트
    - [ ]  <br> 태그
    - [ ]  <h1> ~ <h6> 태그
    - [ ]  <select> 태그
    - [ ]  <list> 태그 -->
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="x-ua-compatible" content="IE=Edge" />
    <title>태그 더 사용해보기</title>
  </head>
  <body>
    <!-- disabled와 selected태그를 이용해 선택 할 수없는 설명 창을 만들 수도 있다. -->
    <!-- onchange와 script function을 활용해 다양한 반응을 만들 수 있다. -->
    <fieldset>
      <legend>
        <h2>다양한 동물들</h2>
      </legend>
      <select id="selectBox" name="selectBox" onchange="changeBox()">
        <option disabled selected>맘에 드는 동물을 고르세요.</option>
        <option value="cat">고양이</option>
        <option value="dog">강아지</option>
        <option value="gorilla">원숭이</option>
        <option value="noting">맘에 드는게 없다</option>
      </select>
      <br />
      <ol>
        <h2>포유류의 특징</h2>
        <li>털이 많다.</li>
        <li>일반적으로 지성이 높다.</li>
        <li>수유를 한다.</li>
      </ol>
    </fieldset>
    <script>
      function changeBox() {
        let select = document.getElementById("selectBox");
        let selectValue = select.options[select.selectedIndex].value;
        // jquery에서 단축화 할 수 있지만 js의 경우 긴문항을 사용해야한다.
        if (selectValue == "cat") alert("고양이는 까칠하죠");
        if (selectValue == "dog") alert("강아지는 착하죠");
        if (selectValue == "gorilla") alert("진심 인가요?");
        if (selectValue == "noting") alert("맘에드는게 없으신가봐요");
      }
    </script>
  </body>
</html>
