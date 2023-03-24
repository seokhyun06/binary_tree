# 자료구조 비선형구조
일렬로 나열하지 않아 자료 순서나 관계가 복잡한 구조를 의미이다.

# 트리(tree)
정점(Node)과 선분(branch)를 이용하여 사이클을 이루지 않도록 구성한 그래프(Graph)의 특수한 형태이다.
![그림01](https://user-images.githubusercontent.com/122009563/227128905-00e9cd8c-43aa-4559-8e7d-3602220f1104.jpg)

# 1-1) 이진 트리(Binary_Tree)
- 모든 노드들의 자식 노드가 두 개 이하인 트리를 의미하는데, 다음은 이진 트리의예다.
- 이런 이진 트리에서는 서브 트리가두 개 이하기 때문에 서브 트리는 왼쪽 서브 트리와 오른쪽 서브 트리로 구분한다.

![image](https://user-images.githubusercontent.com/122009563/227128194-e9fa7e88-7fd4-493e-aabd-1ba4898e6914.png)
![image](https://user-images.githubusercontent.com/122009563/227396541-7a392b6e-4bff-4473-ad03-30b0488b2034.png)

# 이진 트리 용어
- 디그리(Degree) : 차수로 각 노드에서 뻗어 나온 가지의 수
  -> A=3, B=2, C=1, D=3
- 단말 노드(Terminal Node, = 잎(Leaf) 노드 ) : 자식이 없는 노드 즉, Degree(차수)가 0인 노드
  -> K L, F, G, M, I, J
- 비단말 노드(Non-Terminal Node) : 자식이 하나라도 있는 노드, Degree(차수)가 0이 아닌 노드
  -> A, B, C, D, E, H
- 조상 노드(Ancestors Node) : 임의의 노드에서 근 노드에 이르는 경로상에 있는 노드들
  -> M의 조상 노드는 H, D, A
- 자식 노드(Son Node) : 어떤 노드에 연결된 다음 레벨의 노드들
  -> D의 자식 노드는 H, I, J
- 부모 노드(Parent Node) : 어떤 노드에 연결된 이전 레벨의 노드들
  -> E, F의 부모 노드는 B
- 형제 노드(Brother Node, Sibling) : 동일한 부모를 갖는 노드들
  -> H의 형제 노드는 I, J 
   
![image](https://user-images.githubusercontent.com/122009563/227394139-8c6e3699-6993-4cdc-93dc-84b6e3ad7dde.png)

# 이진 트리 탐색(Binary Search Tree)
- 이진 탐색 트리(binary search tree)는 데이터의 삽입, 삭제, 탐색 등이 자주 발생하는 경우에 효율적인 구조로
- 이진 트리이면서 같은 값을 갖는 노드가 없어야 한다.
- 왼쪽 서브 트리에 있는 모든 데이터는 현재 노드의 값보다 작다. 
- 오른쪽 서브 트리에 있는 모든 노드의 데이터는 현재 노드의 값보다 크다.
- 데이터 탐색은 루트에서부터 시작된다. 
- 루트 노드의 데이터와 찾으려는 데이터를 비교하여 같으면 탐색은 성공 종료
- 루트 노드가 작으면 루트 노드의 오른쪽 
- 루트 노드가 크면 루트 노드의 왼쪽 

![image](https://user-images.githubusercontent.com/122009563/227395301-0b95cf8e-d6c2-4b51-b638-23acf35b5c52.png)

데이터가 6인 노드를 탐색하는 과정을 살펴보면 => 7->3->6

# 이진 트리 삽입
- 이진 탐색 트리에서의 삽입은 탐색 동작을 통해 이루어진다. 
- 탐색에 성공하면 삽입은 실패하는데, 이는 이진 탐색 트리는 같은 데이터를 갖는 노드가 없어야 하기 때문이다. 
- 반면에 탐색에 실패하면 삽입을 할 수 있으며, 탐색에 종료된 지점의 데이터를 값으로 하는 노드가 삽입된다. 
- 삽입할 위치는 루트 노드에서부터 시작되며 삽입할 노드의 데이터가 비교하는 노드의 데이터보다 작으면 왼쪽 서브 트리로 진행하고 크면 오른쪽 서브 트리로 진행한다.

![image](https://user-images.githubusercontent.com/122009563/227393646-08ad0200-7b30-418f-8a89-b46f22b15724.png)

# 이진 트리 삭제
- 이진 탐색 트리에서 노드를 삭제하는 동작은 삭제할 노드의 위치에 따라 세 가지로 구분된다.
- 삭제할 노드가 단말 노드인 경우 부모 노드에서 삭제할 노드를 가리키는 링크를 제거하면 된다. 
- 데이터가 6인 노드를 삭제하려면 부모 노드인 데이터가 7인 노드에서 삭제할 노드를 가리키는 링크를 제거
      
![image](https://user-images.githubusercontent.com/122009563/227392101-5663d8af-c4ef-4a91-9fd1-9861e200cd31.png)

# 이진 트리(binary_tree) Node Java Code
![image](https://user-images.githubusercontent.com/122009563/227391636-89ce56a5-2a5b-4f92-b36e-1702dc004298.png)
