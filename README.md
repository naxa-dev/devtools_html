# devtools_html (Developer Tools Hub)

브라우저에서 바로 쓰는 **개발자용 미니 도구 모음(HTML/JS)** 프로젝트입니다.  
각 도구는 `views/` 아래의 페이지로 구성되어 있고, Node 서버(`app.js`)가 라우팅/정적 파일 제공을 담당합니다.

> 이 레포는 “개발할 때 자주 필요한 툴 페이지들을 한 곳에 모아두고, 로컬/서버에서 바로 띄워 쓰는 것”을 목표로 합니다.

---

## 데모/실행 화면
<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/6a183abb-43c8-42e9-86ea-7da433258d20" width="100%"></td>
    <td><img src="https://github.com/user-attachments/assets/2f358637-fe60-47ce-b238-19250ca50c2c" width="100%"></td>
  </tr>
</table>


---

## 프로젝트 구조

```
devtools_html/
├─ app.js               # Node 서버 진입점 (라우팅/정적 제공)
├─ package.json         # 의존성 및 실행 스크립트
├─ views/               # 각 도구 페이지(HTML 템플릿)
├─ static/              # 정적 리소스 (css/js/img 등)
└─ assets/              # 공용 리소스(도구 UI에서 사용하는 파일)
```

- **`views/`**: 도구별 화면(페이지). 새로운 도구를 추가하면 보통 여기에 HTML을 추가합니다.
- **`static/`, `assets/`**: 공통 스타일/스크립트/이미지 등을 둡니다.
- **`app.js`**: 로컬 실행 시 서버 역할(라우팅/정적 파일 서빙).

---

## 요구 사항

- Node.js (권장: LTS)
- npm (또는 yarn/npm)

---

## 로컬 실행

### 1) 설치
```bash
npm install
```

### 2) 실행
레포에 정의된 스크립트가 있는 경우(권장):

```bash
npm run dev
# 또는
npm start
```

스크립트가 따로 없다면(가장 기본):

```bash
node app.js
```

### 3) 접속
서버가 뜨면 브라우저에서 아래로 접속합니다.

- `http://localhost:PORT`
- PORT는 콘솔 로그 또는 환경변수로 확인/설정합니다.

예시:

```bash
# Windows (PowerShell)
$env:PORT=3000; node app.js

# macOS/Linux
PORT=3000 node app.js
```



---
