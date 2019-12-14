# 미션 3 : 블랙잭 게임

## 기능 목록

- 플레이어의 이름 입력 요청
  - 쉼표 기준으로 분리
  - ',,' 입력시(이름이 빈칸) 재입력 요청
- 플레이어에게 배팅 금액 입력 요청
  - 플레이어 수 만큼 반복
  - 숫자가 아닌 값 입력시 재입력 요청
  - 0 이하의 수 입력시 재입력 요청
- 플레이어와 딜러에게 임의의 카드 2장씩 분배
  - 딜러 먼저 2장, 플레이어1 2장, ... 의 방식
- 사용된 카드는 리스트에서 배제
- 카드의 합
  - king,queen,jack은 각각 10
  - 2~9는 그대로 2~9
  - ace의 경우 :
    - 1일 때와 11일 때 모두 계산해서, '21-합' 의 크기가 더 작은 경우로 설정
    - ace의 값을 11로 했을때, 합이 21을 넘기는 경우 무조건 ace의 값은 1로 설정
    - 카드를 새로 받을 때마다 1로 계산할지 11로 계산할지 선택
- 카드를 처음 주었을 때, 블랙잭(카드의 합이 21)이 나온 경우
  - 딜러만 블랙잭인 경우 : 모든 플레이어의 배팅 금액 0으로 설정, 게임 종료
  - 플레이어만 블랙잭인 경우 : 블랙잭인 플레이어의 배팅 금액*1.5 로 설정, 게임 종료
  - 딜러와 플레이어 모두 블랙잭인 경우 : 배팅 금액 그대로, 게임 종료
- 플레이어에게 카드를 받을지 요청
  - 카드의 합이 21이 넘지 않는 경우, n을 입력할때까지 요청
  - y,n이 아닌 값을 입력하는경우 재요청
- 플레이어의 카드 합 > 21
  - 배팅금액 0으로 설정
- 딜러가 처음 받은 2장의 카드 합
  - 합<17 : 1장 더
  - 합>17 : 더 받지 않음
- 결과
  - 딜러의 카드 합이 21 초과 : 모든 플레이어의 배팅 금액 그대로
  - 그 외의 경우 : 21 이하면서 21과 가장 가까운 값인 사람 승리
    - 승리자의 배팅금액만 그대로, 그 외는 0으로 설정
- 플레이어의 배팅 금액이 줄어드는 경우 
  - 줄어든 금액은 모두 딜러의 수익

## 프로그래밍 요구사항

- 중복 코드 제거
- 자바 코드 컨벤션 준수
- 3항 연산자 금지
- else 예약어 금지
- 함수 길이 최대 10라인
- 인덴트 최대 1
- 함수의 인자 최대 3개