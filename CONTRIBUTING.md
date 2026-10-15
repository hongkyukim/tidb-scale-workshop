# Contributing Guide

## 저장소 기여 방법

### 버그 리포트

1. [GitHub Issues](../../issues) 확인 (중복 방지)
2. [Bug Report Template](../.github/ISSUE_TEMPLATE/bug_report.md) 사용
3. 스크린샷, 에러 메시지, 재현 단계 포함

### Feature 요청

1. [Feature Request Template](../.github/ISSUE_TEMPLATE/feature_request.md) 사용
2. 명확한 제목과 설명 작성
3. 관련된 Lab 또는 Task 언급

### Pull Request

1. Fork 및 branch 생성
   ```bash
   git checkout -b feature/my-improvement
   ```

2. 변경사항 적용

3. 커밋 메시지 (conventional commits)
   ```
   feat: add Lab 05 indexing example
   fix: correct SQL syntax in Lab 02
   docs: update README with new section
   ```

4. PR 생성 및 설명 작성

## 코딩 스타일

- **Python**: PEP 8 준수
- **SQL**: 대문자 키워드 (SELECT, FROM, WHERE)
- **문서**: Markdown, 한글/영문 혼용

## 테스트

모든 변경사항은 테스트를 포함해야 합니다:

```bash
# Lab 테스트 실행
cd labs/lab-XX
pytest tests/test_requirements.py -v

# 전체 프로젝트 테스트
cd project
pytest tests/ -v
```

---

감사합니다! 🙏
