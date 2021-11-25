## 구현이 필요한 기능

### 컴퓨터가 생각할 숫자 결정하기
> 1부터 9사이의 세 개의 숫자를 임의로 결정해야한다.
- [MissionUtils 라이브러리](https://github.com/woowacourse-projects/javascript-mission-utils#mission-utils) 의 Random.pickNumberInRange를 사용해 구한다.
```js
Random.pickNumberInRange(1, 10); // 1
```

### 유저가 제시한 숫자를 판정하기
> 입력한 값을 컴퓨터가 생각한 숫자와 비교하여 힌트 또는 정답을 출력한다.
- 입력된 숫자가 형식을 만족하는지 확인하는 `validateNumber` 메서드
- **3개의 숫자** 형식을 만족하는 경우
  - 같은 수가 같은 자리에 있으면 `스트라이크`
  - 같은 수가 다른 자리에 있으면 `볼`
  - 같은 수가 없으면 `낫싱`
  - 정확히 일치하는 경우엔 게임을 종료하고 재시작 버튼을 노출시킨다.
- 형식을 만족하지 않는 경우
  - `alert`로 에러 메시지를 보여주고, 다시 입력하도록 한다.
  - 잘못된 값이 입력되어 있던 폼은 비워준다.

### 현재 상태를 결과 영역에 표시하기
> 현재 상태에 따라 결과 영역에 적절한 값을 출력한다.
- 유저가 **오답**을 입력한 경우
  - 스트라이크, 볼, 낫싱의 결과를 결과 영역에 출력한다.
- 유저가 **정답**을 입력한 경우
  - 축하 메시지와 함께 게임을 재시작 할 수 있는 버튼을 노출한다.
- 유저가 재시작 버튼을 클릭한 경우
  - 결과 영역에 출력된 메시지들을 지운다.

### 게임 재시작하기
> 게임을 재시작 할 수 있도록 현재 상태와 정답을 초기화 시킨다.
- **[컴퓨터가 생각할 숫자 결정하기]** 에서 만든 메서드를 통해 정답을 초기화 한다.
- **[현재 상태를 화면에 표시하기]** 에서 만든 메서드를 통해 결과 영역의 메시지들을 지운다.