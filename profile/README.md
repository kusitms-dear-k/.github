## 💘 팀 소개

[대학생IT경영학회 큐시즘](https://www.instagram.com/kusitms_official/) 31기 **"오케이-크"** 팀입니다!<br>

<div align="center">

| **황유림** | **황동준** | **이현지** | **정인아** | 
| :------: |  :------: | :------: | :------: | 
| [<img src="https://avatars.githubusercontent.com/u/156565796?v=4" height=150 width=150> <br/> @ummiih](https://github.com/ummiih) | [<img src="https://avatars.githubusercontent.com/u/114459629?v=4" height=150 width=150> <br/> @nebulaBdj](https://github.com/nebulaBdj) | [<img src="https://avatars.githubusercontent.com/u/110108243?v=4" height=150 width=150> <br/> @Amepistheo](https://github.com/Amepistheo) | [<img src="https://avatars.githubusercontent.com/u/150119998?v=4" height=150 width=150> <br/> @InaJeong73](https://github.com/InaJeong73) | 
| `프론트 리더`  | `프론트` | `백엔드 리더` | `백엔드` |

</div>

## 🍰 디어케이 로고
<div align="center">
<img src="https://github.com/user-attachments/assets/c24d420d-8f58-4e10-9f1b-1998d7fd1a98" height=150 width=150>
</div>

## 📢 API 명세서
[디어케이 API 명세서](http://223.130.155.249:8080/swagger-ui/index.html)<br><br>

## 🌱 ERD
![image](https://github.com/user-attachments/assets/2de8c9d4-0b89-4507-bb9a-6ffc94888187)

## 🛠️ 시스템 아키텍처
![아키텍처](https://github.com/user-attachments/assets/d6fd0075-d54a-4082-b00e-6ddb7af37f72)

## 🤔 질문사항
### 프론트엔드 3가지

1. 컴포넌트 개발 단계에서 Storybook을 도입하려 하는데, 실무에서 효과적인 사용 패턴이 있을까요?
    - 특히:
    - 다양한 상태(로딩, 에러, 비활성화)의 컴포넌트를 체계적으로 관리하는 방법
    - Autodocs를 활용한 문서 자동화 시 프로퍼티 타입 정의 팁
    - QA 과정에서 Storybook을 협업 도구로 활용한 사례
   측면에서 궁금합니다.

2. 테스트 피라미드 구조에서 각 계층(Jest-단위, RTL-통합, Playwright-E2E)의 명확한 책임 분배 기준은 어떻게 설정해야 할까요?
    - 예를 들어:
    - 단위 테스트에서 커버해야 할 최소 유즈 케이스
    - 통합 테스트 시 모의(mocking) 범위 설정 원칙
    - E2E 테스트에서 주의해야 할 플레이크니스(flakiness) 감소 전략
   측면에서 궁금합니다.

3. 서비스 특성상 제품을 공급하는 사장님과 사용하는 소비자에 대한 권한 처리를 해야하는데 실무에서는 어떤식으로 권한처리를 하는지 어떤 방식이 효율적인지 궁금합니다

<div style="font-family: Arial, sans-serif; line-height: 1.6; font-size: 15px;">

  <h3> 백엔드 3가지</h3>

  <!-- 1. 가게 - 디자인 - 옵션 -->
  <div style="margin-bottom: 30px;">
    <h4>1. 가게 - 케이크 디자인 - 옵션 연관관계</h4>
    <p>
      하나의 <strong>가게(store)</strong>는 여러 개의 <strong>케이크 디자인(design)</strong>을 가집니다.
    </p>
    <p>각 케이크 디자인은 아래와 같은 <strong>선택 옵션</strong>들을 포함합니다:</p>
    <ul>
      <li>시트맛 (예: 초코, 바닐라 등)</li>
      <li>크림맛 (예: 초코, 바닐라 등)</li>
      <li>크기 (예: 도시락 케이크, 1호 케이크, 2호 케이크 등)</li>
    </ul>
    <p style="margin-top: 10px;">
      👉 현재 <strong>테이블 간 연관관계 설정이 적절한지</strong> 확인하고 싶습니다.<br />
      혹시 <strong>더 단순화할 수 있는 구조</strong>가 있다면 제안 부탁드립니다!
    </p>
  </div>

  <br>

  <!-- 2. 주문서 질문 구조 -->
  <div style="margin-bottom: 30px;">
    <h4>2. 주문서 - 공통 질문 및 개별 질문 처리</h4>
    <p>
      가게에 주문을 할 때, 공통적으로 필요한 질문은 <code>common_question</code> 테이블에 고정 저장됩니다.<br />
      각 가게는 추가로 자체적인 질문을 설정할 수 있으며,<br />
      실제 주문서에 표시되는 질문들은 모두 <code>order_question</code> 테이블에 저장됩니다.
    </p>

  <div style="margin-top: 10px;">
  <strong>💡 예시:</strong>
  <div style="margin-top: 5px;">
    <p><strong>공통 질문:</strong></p>
    <p>- 이름이 무엇인가요?<br />- 어떤 디자인을 주문하시나요?</p>
    <p><strong>추가 질문:</strong></p>
    <p>- 원하는 케이크 모양은?(원형, 하트 등)<br />- 기타 요청사항을 말씀해주세요.</p>
  </div>
</div>

<p style="margin-top: 10px;">
      👉 이런 구조가 <strong>확장성과 관리 측면에서 적절한지</strong> 궁금합니다.<br />
      더 나은 설계 방식이 있다면 제안 부탁드립니다!
    </p>

  </div>

  <br>

  <!-- 3. 통합검색 기준 -->
<div>
  <h4>3. 통합검색 정확도 및 정렬 기준</h4>
  <p>
    예: 사용자가 <strong>“상도동 봉천동 생일 케이크”</strong>라고 검색할 경우,<br />
    → 해당 키워드를 모두 포함한 <strong>가게 및 디자인</strong>을 <strong>정확도 순</strong>으로 우선 노출해야 합니다.
  </p>

  <div style="margin-top: 10px;">
    <strong>✅ 지원하는 필터 조건:</strong>
    <p>- 당일 주문 가능 여부</p>
    <p>- 지역 리스트 (예: 상도동, 봉천동 등)</p>
    <p>- 주문 가능한 날짜 범위 (예: 2025-04-30 ~ 2025-05-03)</p>
    <p>- 최소 금액 / 최대 금액</p>
    <p>- 도시락 케이크 여부</p>
  </div>

  <div style="margin-top: 10px;">
    👉 위 <strong>키워드 + 필터 조건</strong>을 바탕으로 <strong>정확도를 어떻게 계산할지</strong>와 <strong>결과를 어떤 기준으로 정렬할지</strong>에 대한 의견을 듣고 싶습니다!
  </div>
</div>


</div>
