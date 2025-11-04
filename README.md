# Vue 2 → Vue 3 전환

---

## Vue 2 → Vue 3 매핑 요약
- 상태 관리: `data()` → `ref` / `reactive`
- 파생 데이터: `computed` 옵션 → `computed()` 함수
- 메서드: `methods` → `setup` 내부 함수
- 감시자: `watch` 옵션 → `watch()` 함수
- 라이프사이클 훅 매핑

| Vue 2                           | Vue 3                       | 사용 방식                      |
|---------------------------------|-----------------------------|--------------------------------|
| `beforeCreate`, `created`       | `setup()` 내부에서 바로 실행        | 단순 `console.log` 등         |
| `beforeMount`                   | `onBeforeMount`             | UI 마운트 직전 로그           |
| `mounted`                       | `onMounted`                 | 마운트 후 초기 동작           |
| `beforeUpdate`                  | `onBeforeUpdate`            | 갱신 직전 로그                |
| `updated`                       | `onUpdated`                 | 갱신 후 로그                  |
| `beforeDestroy`/`beforeUnmount` | `onBeforeUnmount`           | 언마운트 직전 로그           |
| `destroyed`/`unmounted`         | `onUnmounted`               | 언마운트 후 로그             |

---

## 동작 확인용 스크린샷
| components              | 실행 화면 |
|---------------------| --------- |
| E01Instance         | ![E01Instance](./screenshots/E01Instance.png) |
| E02Reactive         | ![E02Reactive](./screenshots/E02Reactive.png) |
| E03Binding          | ![E03Binding](./screenshots/E03Binding.png)   |
| E04Directives       | ![E04Directives](./screenshots/E04Directives.png) |
| E05ParentComponent  | ![E05ParentComponent](./screenshots/E05ParentComponent.png) |
| E06ParentComponent  | ![E06ParentComponent](./screenshots/E06ParentComponent.png) |
| E07OptionsApi       | ![E07OptionsApi](./screenshots/E07OptionsApi.png) |
| E08CompositionApi   | ![E08CompositionApi](./screenshots/E08CompositionApi.png) |
| E09CompositionApi   | ![E09CompositionApi](./screenshots/E09CompositionApi.png) |
| E10Ref              | ![E10Ref](./screenshots/E10Ref.png) |
| E11Reactive         | ![E11Reactive](./screenshots/E11Reactive.png) |
| E12RefComponent     | ![E12RefComponent](./screenshots/E12RefComponent.png) |
