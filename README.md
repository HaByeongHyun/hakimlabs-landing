# Hakim Labs Landing

조직 소개용 정적 랜딩 페이지. `hakimlabs.com`에 배포.

## 목적

- Google Play Console 개발자 계정 **조직 웹사이트** 필드 검증 통과
- Hakim Labs 조직 정보 및 제품 리스트 노출
- 단일 HTML 파일 (빌드 파이프라인 없음)

## 스택

- 순수 HTML + Tailwind CSS (CDN)
- Google Fonts (Inter)
- 빌드 불필요, 의존성 없음

## 로컬 미리보기

```bash
# Python 기본 서버
python3 -m http.server 8080

# 또는 npx
npx serve .
```

브라우저에서 `http://localhost:8080` 접속.

## 배포 (Cloudflare Pages)

1. 이 레포를 GitHub에 푸시 (`hakimlabs-landing`)
2. Cloudflare 대시보드 → `Workers & Pages` → `Create` → `Pages` → `Connect to Git`
3. 빌드 설정:
   - **Framework preset**: `None`
   - **Build command**: (비워두기)
   - **Build output directory**: `/`
4. `Save and Deploy` → 30초 내 `hakimlabs-landing.pages.dev` 발급
5. `Custom domains` → `hakimlabs.com` 추가 → DNS 자동 설정 → SSL 자동 발급

## 편집

`index.html` 한 파일만 수정하면 됩니다. 제품 추가 시 Products 섹션에 카드 복사해서 붙여넣기.

## 연락

admin@hakimlabs.com
