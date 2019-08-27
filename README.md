# 오늘의 '마음의소리' (오마소)

오늘의 '마음의소리' (오마소) 사이트의 데이터를 관리하는 저장소입니다.  
https://dailylist.github.io/channels/2085301/

각 회차의 기본 정보, 태그 등 정보를 JSON 형태로 관리하고 있습니다.

누구든지 수정 참여 할 수 있습니다.

## 데이터 수정 방법
주의: 아래 사용하는 에피소드 번호는 '마음의소리' 번외편 추가등 이유로 '마음의소리' 만화 안에 또는 제목에 표시한 회차 번호와 다릅니다.

259번 이후부터 4개씩 차이남.  
259번 = 255회  
260번 = 256회  
...  
그전에는 0~3개 차이남.

참고: [회차 관련 특이사항](https://namu.wiki/w/%EB%A7%88%EC%9D%8C%EC%9D%98%EC%86%8C%EB%A6%AC#s-12.1)

### 태그 수정
`/data/extend/xxx.json` 파일을 열고,
안에 있는 대응하는 회차의 `tags`의 값에 태그를 추가하고 삭제하면 됩니다.

예: [1101-1200.json](https://github.com/dailylist/dailylist-2085301-data/blob/draft/data/extend/1101-1200.json)
```json
...
"1182": {
  "tags": "조철왕,자전거,학교,썸타다"
},
...
```

### 관련 에피소 수정
`/data/extend/xxx.json` 파일을 열고,
안에 있는 대응하는 회차의 `related`의 값에 에피소드 번호를 추가하고 삭제하면 됩니다.

예:
```json
...
"704": {
  "tags": "특집,N00화 특집,...",
  "related": "346,347"
},
...
```
서로 관련 된 회차는, 한곳에만 추가하면 됩니다.
위에 같은 경우, 704에 346을 추가했으면, 346에서 704를 추가하지 않아도 됩니다.

### 새로운 에피소드 추가
`data/basic/xxx.json` 파일에 새로운 에피소드 정보 추가합니다.

지금은 스크립트로 일괄 추가하고 있습니다.

### 대표 이지지 수정
`data/ogimg/xxx.json` 파일에 대응하는 에피소드 정보 수정합니다.

## 데이터 사용하는 branch

- master: 아직 사용 안 함.
- main: 빌드할 때 사용 함.
- draft: 수정, 테스트 시 사용 함.
  - 테스트 후, main으로 merge 함.

----
(끝)
