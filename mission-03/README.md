# mission-03
> 관련사이트 영역 만들기

## 1. 결과
![mission-03](https://github.com/yenaf/nhlogis/assets/115360074/ee4fa01e-a73c-452e-a1e9-804185614eef)

## 2. 마크업 구조 분석
```html
<div class="gradient"> //gradient 배경색깔을 주기위한 div
    <aside class="newEvent">
      <h2>신규 <span>이벤트</span></h2>
    </aside>

    <aside class="relatedSite">
      <h2>관련 <span>사이트</span></h2>
      <div class="relatedSite-Wrapper"> //늘어나는 효과, 테두리, 흰색배경
        <ul class="relatedSite-List"> //움직이는 list
          <li>
            <a href="#" class="relatedSite-link">제로베이스</a>
          </li>
          <li>
            <a href="#" class="relatedSite-link">MDN</a>
          </li>
          <li>
            <a href="#" class="relatedSite-link">웹접근성 연구소</a>
          </li>
          <li>
            <a href="#" class="relatedSite-link">Web Standards</a>
          </li>
          <li>
            <a href="#" class="relatedSite-link">W3C</a>
          </li>
        </ul>
      </div>
    </aside>
</div>
```
- aside  보조적컨텐츠 섹션. 웹페이지의 메인콘텐츠와 관련된 사이드의 정보, 광고등 부분적인 정보를 나타낼때 사용함.

## 3. 어려웠던 점
- animation 사용이 어려워 trnasition으로만 구현을 했다 (animation은 추가로 공부할것)
- list를 호버했을때 배경 부분의 영역과 list부분의 영역이 각자 다르게 움직여서 어떻게 구현해야할지 고민함. transition을 똑같이 쓰고 시간만 다르게 구현.
- height : auto를 주면 transition을 썼을때 인식하지않는다. 반드시 크기를 줄것.