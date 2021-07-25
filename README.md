# Context Api

- 동적으로 바뀌지 않을 데이터 상태관리(테마,스타일 등)
- 확정되지 않는 값을 저장하는데 적합하지 않으며, 최적화 관점에서 한계점이 명확함
- 동적으로 데이터를 변경시 제대로 변경되지 않는 문제점
- 많은 양의 데이터를 상태관리 할 시 코드가 지저분해지고 가독성이 떨어짐
- 다이나믹하게 상태관리를 할때 provider가 많이 사용됨

# Redux

- 정보의 생태계가 넓고 활용예시가 많음
- 러닝커브가 있고 간단한 상태관리에도 많은양의 코드를 사용함
- store에서 사용되는 정보가 바뀌었을 때 렌더되는 로직을 작성햐야함

# Recoil

- react에 전역상태 관리를 위한 라이브러리로 hook과 비슷하여 사용하기 쉬움
- 파생데이터를 사용하므로 컴포넌트에서 데이터를 변경하는 로직을 써주지 않아도됨
- 정보의 생태계가 작음
- 디버깅 툴 지원이 미비함
- hook으로만 사용가능
- SSR 문제가있어 해결하기위한 로직을 작성해야함

* Atom

- 데이터를 보관하는 작은 단위

* Selector

- 파생되는 아톰을 리턴함
- 아톰을 조합하여 리턴 가능

* useRecoilValue

- read only

* useRecoilState

- hook에서 useState사용이 비슷함

* useSetRecoilState

- 값을 변경하기 위한 함수를 리턴함

* useResetRecoilState

- 디폴트 값으로 변경

* useRecoilStateLoadable

- 비동기 selector를 읽기 위해 사용됨
- Loadable state객체를 반환함(Loadable은 최신 아톰 셀렉터 상태)

* useRecoilValueLoadable

- 비동기 selector를 읽기 위해 사용됨
- Loadable Value객체를 반환함(Loadable은 최신 아톰 셀렉터 상태)
