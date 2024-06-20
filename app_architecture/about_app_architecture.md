공식문서 링크<br/>
[https://developer.android.com/topic/architecture](https://developer.android.com/topic/architecture)

<br/>

## Guide to app arhciteture

<br/>

### Mobile app user experiences

<img src="https://github.com/suojae3/android_kotlin_docs/assets/126137760/638a1ff4-fc03-41b2-9d62-af9ca6bf6da3" width="450">

<br/>
<br/>

#### 🔫 안드로이드는 다양한 컴포넌트들로 구성되어 있다.(그중 주요 4대 컴포넌트는 아래와 같다)
- `activities`: 사용자 인터페이스(UI)를 구성하는 화면(사용자와 애플리케이션이 상호작용할 수 있는 단일 화면)
- `fragments`: 전체 UI에서 어딘가에 반복적으로 재사용 가능한 부분
- `services`: 사용자와 상호작용하지 않고 백그라운드에서 오래 실행되는 작업을 수행할 수 있는 애플리케이션 구성 요소
- `content provider`: 다른 애플리케이션의 데이터에 접근이 필요할 때 사용하게 되는 컴포넌트(ex: 사진첩)
- 이러한 컴포넌트들은 `app manifest`에 정보를 담게된다.
  
<br/>

#

### Common architectural principles

#### 🔫 Separation of concerns
- UI관련 요소에는 UI 핸들링 로직만 담겨 있어야한다.


#### 🔫 Drive UI from data models
- UI는 데이터 모델링에 따라 바뀌어야한다. 즉 데이터모델이 UI에 의존하는 것이 아니라 UI가 데이터모델에 의존해야한다.
- 위와같이 설계해야 데이터가 UI라이프사이클로부터 독립적일 수 있다. (OS가 메모리가 부족하면 UI라이프사이클에 관여하기 때문)
- 따라서 OS가 앱을 강제종료시키더라도 데이터모델은 이로부터 독립적이여야한다.
- 네트워크 환경 여부와도 독립적이여야한다. (OS가 관여할 수 있는 영역이기 때문에)


#### 🔫 Single source of truth
- SSOT는 데이터를 소유하고 있는 객체로 오직 SSOT만이 데이터를 수정할 수 있다.
- 외부에서 참조가 아닌 SSOT 자체에서 변환을 끝내야하기 때문에 SSOT는 "불변"타입의 데이터를 뿌리게된다.
- 즉 인풋으로 이벤트가 SSOT에 들어오면 SSOT 내부 블랙박스에서 데이터를 조작한뒤 아웃풋으로 불변 데이터 모델을 뿌리는 방식이다.
- 



#### 🔫 Unidirectional Data Flow



<<br/>


### Recommended app architecture


#### 🔫 Modern App Architecture


<br/>

### Manage dependencies between components






