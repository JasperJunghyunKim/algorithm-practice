### 개념

- Breadth First Search
- [그래프](Graph.md) 의 모든 노드를 체계적으로 탐색하는 알고리즘 중 하나로, 시작 정점으로부터 가까운 정점을 우선적으로 방문하고 멀리 떨어진 정점을 나중에 방문하는 방식
- 이를 위해 큐(Queue)를 사용하여 이미 방문한 정점들을 순차적으로 저장하고, 가장 먼저 방문한 정점을 기준으로 인접한 정점들을 탐색
- 모든 노드에 접근하기 때문에 [완전탐색](Exhaustive%20Search.md) 의 한 종류로 볼 수도 있으나, 구체적으로, BFS 는 효율적인 방법으로 문제를 해결하기 위해 사용됨
- [FloodFill](FloodFill.md) 알고리즘을 구현하는 방법으로 사용되기도 함
  이때, 그래프는 일반적으로 인접 행렬 형태로 사용됨


### ⚠️ 주의

* BFS와 [Dijkstra](Dijkstra.md) 사용 구분
	* BFS는 모든 간선의 가중치가 양수이며 가중치가 동일한 경우 
	* Dijkstra : 모든 간선이 양수이며 가중치가 다를 경우


---
### 구현 Queue

```Python
bfs_visited = [START_V]
bfs_to_visit = deque([START_V])

while bfs_to_visit:
	cur_v = bfs_to_visit.popleft() # queue
	for next_v in range(1, NUM_V + 1):
		if graph[cur_v][next_v] == True and next_v not in bfs_visited:
			bfs_visited.append(next_v)
			bfs_to_visit.append(next_v)

print(*bfs_visited)
```


---
### 유형

1. [BFS, DFS 구현](https://www.acmicpc.net/problem/1260)
2. [숨바꼭질](https://www.acmicpc.net/problem/1697)
   문제 조건을 그래프로 구현했을 때, BFS 로 접근할 수 있음을 파악하는 것이 핵심
3. 연결 요소 파악
   바이러스가 퍼질 때, 어떤 컴퓨터가 살아남는지
4. 최단 경로 찾기
5. 미로 찾기


---
### 참고

### 정리중