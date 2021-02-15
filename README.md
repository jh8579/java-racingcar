# java-racingcar
자동차 경주 게임 미션 저장소

## 기능 명세

## 우아한테크코스 코드리뷰
* [온라인 코드 리뷰 과정](https://github.com/woowacourse/woowacourse-docs/blob/master/maincourse/README.md)

# 문자열 덧셈기

## 기능 명세
* 입력 문자열이 빈 문자열 또는 null 값인지 확인한다.
* 쉼표(,)를 구분자로 사용하여 두 숫자의 합을 반환한다.
* 커스텀 구분자를 지정할 수 있도록 한다. (예 : “//;\n1;2;3” => 6)
* string 자체가 바로 정수로 변환될 수 있는지 확인한다.
* 콜론을 구분자로 사용한다.
* 음수가 포함되어 있는 경우 예외를 발생시킨다.

# 자동차 경주

## 기능 명세
* 필요한 객체 - Car, Car 리스트를 관리하는 객체, Round 관리하는 객체, RandomUtil, InputUtil, OutputView, GameRunner, GameController
* 자동차 이름 입력 / 시도 횟수 력력
* 자동차에 이름을 부여 -> 자동차 생성자로 초기화
* 자동차를 전진 멈춤 -> GameController 관리
* 원하는 범위 랜덤값 생성
* 각 라운드별 자동차 움직임 출력
* Car 리스트 우승자 선정 -> 복수 우승자 가능
* 우승자 출력

## 테스트 케이스
* 사용자 입력 예외처리 테스트
  * 시도 횟수 예외 처리
  * 자동차 이름 예외 처리
* 자동차 움직임/멈춤 테스트
* 자동차 움직임 출력 테스트
* 랜덤값 범위 테스트
* 우승자 선정 테스트

## 2차 리팩토링
* domain과 view 역할을 명확하게 분리
  - InputUtils와 input을 위한 출력을 InputView 하나로 합침
  - 모든 출력은 기존 PrintUtils -> OutputView 에서 모두 담당
  - view 패키지로 InputView, OutputView 이동
