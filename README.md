# 3DButton

CSS를 이용해 3D 버튼을 만들어 보았습니다.

![3DButton](https://user-images.githubusercontent.com/61913417/106631724-5dfe3880-65c0-11eb-8558-3d230b951cd3.gif)

### 구상 과정과 구현
- 메뉴를 3D 상자 형태로 만들고 싶다!
1. 메뉴에 transform-style: preserve-3d 속성을 이용해 3D 공간에 배치시킨다.
2. 메뉴에 가상요소 선택자를 사용하여 똑같은 크기로 만들고 이것도 마찬가지로 3D 공간에 배치시킨다.
3. rotateX(90deg) 속성을 주게 되면 3D 공간에 배치했으므로 X 축으로 90도 돌아가서 누운 형태가 되므로 우리 눈에는 보이지 않게 된다.
4. 그리고 translateZ(1em)을 사용하여 메뉴의 맨 위에 붙여 상자 형태로 만든다.  
	--> X 축으로 높였으니까 Z축을 줘야 위로 높히거나 아래로 낮출 수 있다, 메뉴의 크기를 2em으로 주고 눞혔으므로 정 가운데에 위치해서 누워있는셈이므로 절반의 값이 1em을 줘서 위로 붙였다. 그러므로 상자의 형태가 만들어 졌다.
- hover시 상자가 돌아가는 효과를 내고 싶다!
1. 상자의 형태를 만들어 놨으므로 a에 hover를 주고 전체가 돌아가게 만들어 준다.
2. rotateX(-90deg)를 줘서 앞쪽으로 돌아가게 만들어 원래 메뉴가 접히고 위에 붙혀놨던 요소가 나오면서 보여지게 된다.  
--> 위에서 rotateX(90deg)를 주면 눞혀져서 안보이게 됐지만 이번에는 눞히는게 아니라 앞쪽으로 돌리는 효과를 낼 것이므로 마이너스 값을 줘야 한다.
