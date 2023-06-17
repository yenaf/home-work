# mission-05
이미지 스프라이트(image sprite) 기법으로 인기사이트 영역 만들기


## 1. 결과
![mission-05](https://github.com/yenaf/nhlogis/assets/115360074/b3a89fa2-ec03-4a38-8c3d-8bfefc23a79c)



## 2. 마크업 구조 분석
```html
  <section class="favorite">
    <h2 class="favorite-title">인기<span class="accent-color"> 사이트</span></h2>
    <ol class="favorite-list">
      <li class="favorite-item spriteUp">
        <span class="favorite-rank">1</span>
        W3C
      </li>
      <li class="favorite-item spriteDown">
        <span class="favorite-rank">2</span>
        Web Standards
      </li>
      <li class="favorite-item spriteMiddle">
        <span class="favorite-rank">3</span>
        CSS ZenGarden
      </li>
      <li class="favorite-item spriteUp">
        <span class="favorite-rank">4</span>
        MDN
      </li>
    </ol>
    <a href="#" class="favorite-more"><i class="xi-plus"></i>더보기</a>
  </section>
```

- 인기 사이트의 순위는 순서가 있는 순차리스트이기때문에 ol태그를 사용했다.
- rank 이미지는 li태그의 이미지 스프라이트 기법으로 배경처리했다.

## 3. 어려웠던 점
- background-position으로 이미지를 제 위치에 놓게 하는것이 어려움이 있었다. 위치는 li태그의 제일 오른쪽에 위치하기때문에 키워드값을쓰거나 100% 값을 쓰면 오른쪽에 배치됐고, 피그마 시안에서 이미지의 위아래 간격을 보고 키워드 값과 px값을 사용했다.


- 더보기의 a태그를 같은 위치에있는 h2 제목태그의 블록에 배치하면 편리할거 같아서 h2에 position:relative를 사용하고, a태그에 position:absolute를 사용했는데 바깥영역(body)으로 배치가 되었다. 마크업을 다시 살펴보니 h2는 a링크요소의 형제요소여서 적용이 되지 않는다는 것을 알았다.position: absolute는 가장 가까운 위치 지정 조상 요소에 대해 상대적으로 배치하며, 조상 중 위치 지정 요소가 없다면 초기 컨테이닝 블록을 기준으로 삼는다.