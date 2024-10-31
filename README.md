# java-lotto-precourse

# 콘솔 로또 게임

로또 게임을 콘솔 환경에서 즐길 수 있는 Java 애플리케이션입니다.

## 목차
- [프로젝트 소개](#프로젝트-소개)
- [시스템 요구사항](#시스템-요구사항)
- [시작하기](#시작하기)
- [프로젝트 구조](#프로젝트-구조)
- [기능 목록](#기능-목록)

## 프로젝트 소개
이 프로젝트는 사용자가 콘솔 환경에서 로또 게임을 즐길 수 있도록 구현된 애플리케이션입니다. 실제 [로또 게임](https://namu.wiki/w/%EB%A1%9C%EB%98%90%206/45)과 유사한 규칙을 따르며, 사용자 친화적인 인터페이스를 제공합니다.

```
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43] 
[3, 5, 11, 16, 32, 38] 
[7, 11, 16, 35, 36, 44] 
[1, 8, 11, 31, 41, 42] 
[13, 14, 16, 38, 42, 45] 
[7, 11, 30, 40, 42, 43] 
[2, 13, 22, 32, 38, 45] 
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```

## 시스템 요구사항
- JDK 21 이상
- Gradle 8.x 이상

## 시작하기

#### 프로젝트 클론
```bash
git clone https://github.com/[username]/java-lotto-7.git
cd java-lotto-7
```

#### 빌드
```bash
./gradlew build
```

#### 실행
```bash
./gradlew run
```
또는 IDE에서 `Application` 클래스의 `main()` 메서드를 직접 실행할 수 있습니다.

## 프로젝트 구조
(완성시킨다음 구조 넣기) 

## 기술 스택
- Java 21
- Gradle
- [mission-utils](https://github.com/woowacourse-projects/mission-utils) (1.2.0)

#### 코드 컨벤션
- Google Java Style Guide를 따릅니다.
- 메서드와 클래스에 적절한 주석을 추가해주세요.
- 테스트 코드 작성을 권장합니다.

## 기능 목록
- [ ] 로또 번호는 1~45까지의 숫자(정수)로 이루어져 있다.
- [x] 1개의 로또는 중복되지 않는 6개 숫자로 이루어져 있다.
  - [x] 숫자가 6개가 아니라면, 예외를 반환한다.
  - [x] 숫자가 중복이 되면, 예외를 반환한다.
  - [ ] 로또 번호는 오름차순으로 정렬한다.
- [ ] 당첨 번호는 1~45까지의 숫자(정수) 6개 + 보너스 번호 1개로 이루어져 있다.
  - [ ] 번호가 6개가 아니라면 예외를 반환한다.
  - [ ] 번호는 1~45 사이가 아니라면 예외를 반환한다.
  - [ ] 번호가 중복이 되면, 예외를 반환한다.
  - [ ] 보너스 번호는 1~45 사이가 아니라면 예외를 반환한다.
  - [ ] 보너스 번호가 당첨 번호 6개에 포함되는 값이라면 예외를 반환한다.
- [ ] 당첨 기준은 등수, 번호 일치 개수, 상금으로 이루어져 있다.
  - [ ] 5개 번호가 일치한다면, 보너스 번호가 있는지 확인한다.
- [ ] 로또 구입 금액을 입력하면 구입 금액에 해당하는 만큼 로또를 발행한다.
  - [ ] 로또 구입 금액이 1,000원 단위가 아니라면 예외를 반환한다.
- [ ] 당첨 내역을 알려준다.
  - [ ] 당첨 번호와 보너스 번호를 통해 로또 번호 몇 개가 일치하는지 계산한다.
- [ ] 수익률을 계산한다.
