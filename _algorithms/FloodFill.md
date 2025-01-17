### 개념

* 주어진 시작점으로부터 연결된 영역을 찾는 알고리즘
  예) 3D Matrix 에서 특정 위치 (x, y, z) 와 연결된 영역의 부피를 찾는 알고리즘


---
### 구현

* [DFS](DFS.md) 또는 [BFS](BFS.md) 를 활용하여 구현

### 구현 비교 - BFS, DFS

**시간 복잡도**
* 이론적으로는 둘 다 맵의 총 칸 수 만큼 탐색해야되므로 O(N) 만큼 소요됨
* 그러나 BFS 는 인접한 노드를 연속적으로 탐색하기 때문에 Cache 효율이 좋을 수 있음
  반면, DFS 는 한 방향으로 깊게 탐색할 경우 stack 깊이에 따라 메모리 접근 패턴이 불규칙해져서 Cache 효율이 떨어질 수 있음

**공간 복잡도**
* 제공된 맵의 형태에 따라 달라질 수 있음
* 깊은 레벨의 탐색이 필요한 맵의 경우 DFS 사용 시, Stack 이 깊어질 수 있음
* BFS 는 초기에 넓은 영역을 탐색할 경우 많은 요소가 Queue 에 저장될 수 있으므로 더 많은 메모리를 사용할 수도 있음
* 결론적으로, 정답은 없음


---
### 유형

* [마법사 상어와 파이어스톰](https://www.acmicpc.net/problem/20058)에서 얼음의 최대 크기를 구하는 조건에 Flood Fill 사용됨