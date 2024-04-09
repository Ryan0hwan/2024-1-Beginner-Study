# 브랜치 관리의 필요성
* 서로의 작업에 영향을 주지 않기 위해선 브랜치의 분리가 필요
* 각 브랜치가 어떤작업을 위해 존재하는가
* main브랜치는 항상 안전하게 관리할 것

# 브랜치 보호 규칙
* 승인 없이 Pull Request를 병합할 수 없도록 제한 가능
* 특정 브랜치에 Push 가능자를 제한 가능

# Git Flow(2010년 Vincent Driessen이 고안한 방법
* Main Branches(main(master), develop)
* Supporting branches(feature, release, hotfix)

1. main
프로젝트 생성 시 기본으로 생성되는 브랜치.
영원히 존재하며, 병합될 때마다 제품의 새로운 버전이 탄생
main대신 master라는 이름이 사용되기도 하나, 최근 유행은 main

2. develop
영원히 존재하는 두 번째 브랜치
feature브랜치의 기반.

3. feature
develop 브랜치에서 분기하여 작업

4. release
배포 준비를 위한 브랜치
자잘한 버그를 수정하고 QA작업을 함
develop 브랜치에서 분기하여 main브랜치로 병합

5. hotfix
배포 환경에서 즉각적인 수정이 필요한 경우 사용
main브랜치에서 분기됨
main과 develop모두에 병합이 필요함

But, 배포가 수시로 이루어지는 현 시대의 웹.앱과는 부적합.
이를 고안한 Vincent Drissen도 GitHub Flow 전략 추천

# Github Flow
Main과 Feature 브랜치만 사용

1. Main
항상 배포 가능상태로 유지. main으로 병합 전, 충분한 테스트 필요

2. feature
Git Flow와 달리, 이외 브랜치들 구분하지 않음, 그만큼 코드리뷰가 중요하겠지.
main에서 분기하여 다시 main으로 병합.
브랜치의 목적을 이름에 잘 담아야함



# 개발자의 Attitude
* convention을 만들어 사용하자. [긴 시간이 지나도 의도파악이 쉽도록]
* 구글링을 꼼꼼히 할 것
* public repository에 있는 코드는 곧 내 얼굴이다.
* "좋은"질문을 잘 하자
