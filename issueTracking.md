
# Issue Tracking

## 개요
github에서 제공하는 issue 기능을 통해 프로젝트를 진행하면서 일어나는 크고 작은 이슈, 개발진행사항, 개발자간의 커뮤니케이션, 개선사항 등을 관리할 수 있습니다. 좀 더 효율적인 issue사용을 위해 이슈와 관련된 컨벤션을 정의하였습니다.


## Issue와 Project 그리고 라벨의 활용
일반적으로 이슈를 생성할 해당 레포지토리에 들어와서 issue탭을 클릭하여 작성합니다. 허나 이번 프로젝트에서는 [Project](https://github.com/orgs/telework-freaks/projects)에서 `Todo`보드에 issue제목을 생성하고 `Convert to Issue`기능을 통하여 해당 issue를 생성한 목적과 세부사항을 작성합니다. 또한 issue에는 라벨을 추가할 수 있습니다. 라벨을 이용하여 해당작업이 어떤 목적을 가지고 있는지 빠르게 판단이 가능하다고 생각하여 라벨을 사용하기로 하였습니다.

### Project란?
issue를 정리하고 pull request할 때 `프로젝트 보드`를 사용할 수 있습니다. 또한 레포지토리 또는 organization 전체에서 `워크 플로우`관리가 가능합니다.

> 현재 ondolbang-v2 프로젝트를 진행중이므로 전체 issue와 pull request를 관리하기위해 ondolbang-v2라는 프로젝트가 생성되있고, 효율적인 issue관리를 위해 주차별로 프로젝트를 생성합니다. 주차별 프로젝트 이름은 YYMMDD(210301) - YYMMDD(210307)양식으로 정의합니다.

### 라벨 종류
-	feature - 기능관련
	-	new - 새로운 기능을 추가
	-	refactor - 기존에 있는 기능을 수정, 변경
	-	documentation - 문서화 작업
- problem - 버그관련
	-	bug - 큰 장애가 발생하지 않는 오류
	-	urgent - 빠른 시일내에 해결해야 하는 오류
	-	critical - 서비스에 치명적인 오류
> 현재 8개의 라벨을 정의하였으며 필요시 추가될 수 있습니다.


## Pull request
우리 프로젝트는 pull request를 작업의 최소 단위로 사용합니다. 이에 따라 issue와 pull request 를 1대1로 대응시켜 관리합니다. 해당 관계를 명확히 하기 위해 issue와 pull request의 이름을 통일시키는 규칙을 뒀습니다.

```
ex)
<issue>
[Add]: 랜딩 페이지에 최근 본 항목 링크 추가

- 랜딩 페이지의 메인로고 다음에 위치
- pc 기준 3 * 3 그리드를 사용
...

<pull request>
#1: [Add]: 랜딩 페이지에 최근 본 항목 링크 추가

- RecentView 컴포넌트 추가
- Landing 컴포넌트에 RecentView 컴포넌트 추가
...
```

issue 메시지의 제목은 [[commitMessageConvention.md]](https://github.com/telework-freaks/ondolbang-v2-technote/blob/main/commitMessageConvention.md)에 기술한 것과 같이 `Add, Update, Refactor` 등의 작업 내용을 의미하는 키워드와 작업내용을 한 문장으로 요약하여 작성합니다. issue 메시지의 내용은 해당 작업의 디테일을 위 예시와 같이 간략히 설명합니다. pull request 메시지의 제목에는 해당 PR이 완료한 작업에 해당하는 issue의 번호를 먼저 쓰고, issue의 제목을 작성합니다. 내용에는 완료한 작업 내용을 간략히 설명합니다. pull request 메시지의 내용 부분에는 해당 작업에서 변경된 사항을 위 예시와 같이 `코드 측면`에서 기술합니다. 최종 merge 이전에 팀원이 해당 PR을 검토하고 이상없음이 확인되면 변경점을 저장소에 merge합니다.

