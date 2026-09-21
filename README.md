# 감나무 한가위

HTML, CSS, SVG, JavaScript를 `index.html`에 담은 추석 인사 페이지입니다.
별도 패키지 설치, 빌드, 서버, 환경 변수 없이 Vercel에 정적 사이트로 배포할 수 있습니다.
글꼴은 Google Fonts에서 불러옵니다.

## 터미널에서 배포

Node.js와 npm이 설치된 환경에서 이 프로젝트 폴더를 열고 실행합니다.

```sh
npx vercel@latest login
npx vercel@latest --prod
```

처음 배포할 때는 사용할 계정을 선택하고, 새 프로젝트를 만들거나 기존 프로젝트에 연결합니다.
새 프로젝트 이름은 `gamnamu-chuseok`처럼 영문 소문자와 하이픈으로 입력하세요.
현재 폴더명은 한글이므로 프로젝트 이름으로 그대로 사용하지 마세요.
코드 위치는 현재 폴더인 `./`를 선택합니다.
배포가 끝나면 터미널에 사이트 주소가 표시됩니다.

이후 페이지를 수정한 뒤 같은 폴더에서 `npx vercel@latest --prod`를 실행하면 다시 배포됩니다.

## Git 저장소로 배포

1. 숨김 파일을 포함한 프로젝트 파일을 GitHub 등의 Git 저장소에 올립니다.
2. Vercel에서 새 프로젝트를 만들고 해당 저장소를 가져옵니다.
3. Root Directory를 `index.html`과 `vercel.json`이 있는 폴더로 지정합니다.
4. 다음 설정을 확인한 뒤 Deploy를 누릅니다.

| 설정 | 값 |
| --- | --- |
| Framework Preset | Other |
| Build Command | 비워 둠 |
| Install Command | 비워 둠 |
| Output Directory | `.` |
| Environment Variables | 필요 없음 |

`vercel.json`에 위 설정이 저장되어 있습니다. `npm run build`나 `dist` 폴더를 지정할 필요가 없습니다.

## 로컬 확인

`index.html`을 브라우저에서 직접 열거나, Python 3가 설치되어 있다면 다음 명령을 실행합니다.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

브라우저에서 [로컬 페이지](http://127.0.0.1:8000)를 엽니다. 종료하려면 터미널에서 Ctrl+C를 누릅니다.

공식 문서: [정적 사이트 빌드 설정](https://vercel.com/docs/builds/configure-a-build), [CLI 배포](https://vercel.com/docs/cli/deploy).
