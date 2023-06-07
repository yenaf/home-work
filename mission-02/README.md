# mission-02

> 로그인 UI 만들어보기

## 1. 결과
![로그인UI완성](https://github.com/yenaf/nhlogis/assets/115360074/4e20ef86-a6f6-4238-ba7b-d0f424ef8f34)

## 2. 마크업 설계
![로그인마크업설계](https://github.com/yenaf/nhlogis/assets/115360074/9a94f707-877f-4e26-918e-1439df53c8c2)


## 3. 마크업 구조 분석
```html
  <div class="loginShadow"> //그림자영역
    <div class="innerContainer"> //로그인 상자 영역
      <h2>로그인</h2>
      <form action="/" method="post" class="loginForm" > 
        <fieldset>
          <legend>로그인, 회원가입, 아이디 비밀번호 찾기</legend>
          <div class="loginGroup"> //form 요소안의 요소들을 그룹핑하기 위한 div
            <div class="login"> //아이디 입력서식, 비밀번호 입력서식, 로그인버튼을 묶음
              <span> // label, input을 그룹핑하기위해 span요소를 사용
                <label for="userId">아이디</label>
                <input type="text" id="userId" required placeholder="euid@euid.dev"/>
              </span>
              <span>
                <label for="userPass">비밀번호</label>
                <input type="password" id="userPass" required placeholder="8자리 이상" minlength="8"/>
              </span>
              <button type="submit" >로그인</button>
            </div>
            <div class="join_Find"> //회원가입, 아이디 비밀번호 찾기내용 묶는 div
              <span> // 링크요소와 아이콘을 묶기위해 span요소 사용
                <a href="#"><i class="xi-angle-right"></i>회원가입</a>
              </span>
              <span>
                <a href="#"><i class="xi-angle-right"></i>아이디 비밀번호 찾기</a>
              </span>
            </div>
          </div>
        </fieldset>
      </form>
    </div>
  </div>
```

- position 속성을 그림자로 활용하기 위해 div 요소 안에 div 요소를 한 번 더 배치함.
- 아이디, 비밀번호를 각각 span으로 묶은 건 단락의 의미인 p 요소보다는 단순 그룹핑의 목적으로 쓰기 위해 span 요소를 사용함.
- 아이디, 비밀번호는 반드시 입력되어야 하는 값이기 때문에 input 속성에 required 속성을 넣음.
- 회원가입, 아이디 비밀번호 찾기는 단순히 버튼이 아니라 회원가입 창, 아이디 비밀번호 찾기 창으로 넘어가기 때문에 링크 요소를 사용.

## 4. 어려웠던 점
- h2 태그를 form 요소 안에 넣을까 밖에 빼둘까 고민함. form 요소 밖에 빼서 div 전체의 제목으로 쓰고, form 요소 안에는 legend 태그를 사용해서 form에 대한 설명을 한 다음 숨김 처리함.
- 피그마에 있는 시안대로 하려고 너비 값 주는데 자꾸 안 나와서 계속 고민함. 문제는 폰트였다. 폰스 설정 전 기본 폰트 너무 커서 계속 텍스트가 넘쳤던 것. 피그마 시안안에 있던 프리텐다드 폰트를 쓰니 해결됐다. 주어진 것을 잘 살펴보자.
- input의 입력창을 시안처럼 나란히 놓고 싶어서 label의 너비 값을 줬는데 전혀 해결되지 않았다. label은 인라인 요소이기 때문에 내용의 길이만큼만 너비를 차지해서 display: inline-block 속성을 주어서 해결할 수 있었다.





