# 🌐 USGS Earthquake Globe

USGS 공개 지진 데이터를 3D 지구본으로 시각화하는 실시간 대시보드입니다.

## 기능

- **3D Globe**: 최근 7일간 M2.5+ 지진을 지구본 위 마커로 표시 (드래그 회전, 확대/축소)
- **상세 패널**: 마커 클릭 시 규모·위치·발생 시간(KST)·깊이·USGS 링크 확인
- **시간 슬라이더**: 7일 × 3시간 단위(56구간)로 필터링, KST 날짜 경계 기준
- **Daily Record**: 날짜별(KST) 지진 발생 건수 집계, 오늘/어제 비교 및 변화율
- **TEST 패널**: Slow / 401 / 403 / Rate Limit / Offline / Schema Change synthetic fixture로 오류 상태 테스트

## 데이터 출처

[USGS Earthquake Hazards Program](https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/2.5_week.geojson) — `M2.5+ Past 7 Days` GeoJSON Feed (별도 API Key 불필요)

## 실행 방법

정적 파일 하나로 구성되어 있어 별도 빌드 없이 바로 실행됩니다.

```bash
# 로컬에서 바로 열기
open index.html

# 또는 GitHub Pages로 배포된 주소로 접속
```

## 기술 스택

- Vanilla JavaScript, Three.js (3D Globe), OrbitControls
- `localStorage` (Daily Record 저장)
- 별도 서버/빌드 도구 없음 — 단일 `index.html`

## 참고

- 모든 시간은 Asia/Seoul(KST) 기준으로 표시됩니다.
- 로그인/회원가입/서버 DB 없음 — 순수 프론트엔드 프로젝트입니다.
