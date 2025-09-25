# Python 3.13 업그레이드 실행계획

## 1. 환경 준비
- Python 3.12.11 가상환경(현재 환경) 사용 및 활성화
- 기존 requirements.txt 및 의존성 최신화

## 2. 코드 호환성 점검 및 수정
- print, exception, import 등 Python 2/3 호환성 코드 제거
- deprecated/변경된 표준 라이브러리 함수 및 문법 수정
- `distribute` 등 더 이상 사용하지 않는 레거시 패키지 제거 및 `setuptools`로 대체

## 3. 패키지 메타데이터 및 빌드 시스템 현대화
- `setup.py`, `MANIFEST.in` 등 최신 표준에 맞게 수정
- 필요시 `pyproject.toml` 추가
- `guachi.egg-info` 등 불필요한 파일 정리

## 4. 문서 및 테스트 코드 점검
- Sphinx 문서 빌드가 Python 3.12.11 환경에서 정상 동작하는지 확인
- `guachi/tests/` 내 테스트 코드가 Python 3.12.11 환경에서 정상 동작하는지 점검 및 필요시 수정

## 5. 자동화 및 검증
- CI/CD(예: GitHub Actions)에서 Python 3.13 테스트 추가
- 모든 테스트 통과 확인

## 6. 결과 정리 및 문서화
- 업그레이드 내역 및 변경점 README 또는 CHANGELOG에 기록

---

각 단계별로 세부 작업을 진행하며, 필요시 추가적인 마이그레이션 도구 활용 및 코드 리뷰를 병행합니다.
