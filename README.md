# pingpong


#### 핑퐁게임을 강화학습을 통해 사용자와 대결을 할 수 있도록 인공지능을 학습

<img src="https://user-images.githubusercontent.com/87750521/132180844-f241a145-35b5-4d07-beb6-de9ddfb2f924.png" width="450" height="340">


### 구조
1. AI VS User 구조의 게임으로 구성
2. DQNAgent를 직접 구성하고 학습모델을 만들어서 강화학습
3. 학습이 완료된 모델 테스트

### 학습
- 게임의 끝이 정확하게 정의 되어있지 않기에 5000프레임이 1Epesode로 지정하는데 실점하였을 때 Epesode를 강제 종료
- 1픽셀이 움직일 때마다 1stap이 소모된는것으로 5000step이 1Epesode가 됨
- 공이 자신의 벽에 닿아 상대에게 점수를 주지 않는 것이 학습목표
- 150번째 Epesodes가 넘어가면서 5000step, 최대 스탭을 유지하기 시작
- 240번째 Epesodes이상의 학습 모델을 가지고 테스트시 실점이 거의 없이 사람과 핑퐁게임 유지가 가능하게 됨

### 결과
 - 학습이 처음부터 원활하게 이루어지지 않아 Epesode와 step, 보상값에 대한 설정을 여러가지로 테스트하고 그 중 가장 좋다 생각되는 설정으로 학습
 - 처음에는 200step, 시작하자마자 실점하여 게임이 종료되는 경우가 많았지만 150번째 Epesodes부터 게임을 유지하는 step이 길어짐
 - 240번째 Epesodes이후의 학습모델은 비슷한 성능을 보여주고 사람과 테스트를 진행하였을 때 실점하지 않고 원활한 게임이 



