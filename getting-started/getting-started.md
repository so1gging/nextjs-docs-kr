---
description: Get started with Next.js in the official documentation, and learn more about all our features!
---

> Next.js 13 은 최근에 릴리즈 되었습니다. [더 알아보기](https://nextjs.org/blog/next-13) 혹은 [13 버전으로 업그레이드하기](https://nextjs.org/docs/upgrading#upgrading-from-12-to-13) 에서 알아보세요.
> 13버전은 `page` directory 처럼 동작하는 [`app` directory](https://beta.nextjs.org/docs/app-directory-roadmap) 와 같은 beta 기능을 도입합니다.
> 13버전에서 `pages` 기능을 사용할 수 있지만, 새로운 `app` 기능을 사용해 볼 수 있습니다. [새로운 beta 문서를 알아보기](https://beta.nextjs.org/docs).

# 시작하기

Next.js 문서에 오신 것을 환영합니다 !

Next.js 가 처음이신 경우, 우리는 [학습 과정](https://nextjs.org/learn/basics/create-nextjs-app) 을 보시는 것을 추천합니다.
퀴즈가 포함된 대화형 과정은 Next.js를 사용하기 위해 알아야 할 모든 것을 알려줍니다.

만약 Next.js에 관련하여 질문(어느것이여도 상관없습니다!)이 있다면, 언제든 [GitHub Discussions](https://github.com/vercel/next.js/discussions)의 커뮤니티로 오셔서 질문해주세요!

#### 시스템 요구사항

- [Node.js 16.8.0](https://nodejs.org/) or 최신버전
- MacOS, Windows (including WSL), and Linux 에서 지원합니다.

## 자동설정

우리는 `create-next-app` 을 사용하여 새로운 Next.js 를 만들기를 권장합니다. `create-next-app` 은 모든 것을 자동적으로 설치할 수 있어요. (굳이 빈 폴더를 만들 필요가 없습니다. `create-next-app` 이 만들어 줄거에요.)

프로젝트를 만들고, 실행하세요:
```bash
npx create-next-app@latest
# or
yarn create next-app
# or
pnpm create next-app
```

TypeScript로 시작하고 싶으시다면, `--typescript` 플래그를 추가하세요:

```bash
npx create-next-app@latest --typescript
# or
yarn create next-app --typescript
# or
pnpm create next-app --typescript
```

설치가 완료된 후:

- 개발서버 `http://localhost:3000`에 접속할 수 있도록 `npm run dev` or `yarn dev` or `pnpm dev` 를 실행하세요.
- `http://localhost:3000` 를 방문해서 당신의 어플리케이션을 구경하세요.
- `pages/index.js` 를 수정하고, 업데이트된 당신의 브라우저를 확인하세요.

`create-next-app` 을 사용하는 방법에 대한 더 많은 정보는 [`create-next-app` documentation](/docs/api-reference/create-next-app.md)에서 볼 수 있습니다.

## 수동 설정

`next` , `react` , `react-dom` 를 당신의 프로젝트에 설치하세요:

```bash
npm install next react react-dom
# or
yarn add next react react-dom
# or
pnpm add next react react-dom
```

`package.json` 을 열고 `scripts` 를 추가하세요:

```json
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```

이 스크립트들은 어플리케이션에서의 서로다른 개발단계를 나타냅니다: 

- `dev` - [`next dev`](/docs/api-reference/cli.md#development) 실행은 Next.js의 개발서버를 시작하는 것과 같아요.
- `build` - [`next build`](/docs/api-reference/cli.md#build) 실행은 운영서버 사용을 위한 어플리케이션 빌드단계예요.
- `start` - [`next start`](/docs/api-reference/cli.md#production) 실행은 Next.js의 운영서버를 시작하는 것과 같아요.
- `lint` - Runs [`next lint`](/docs/api-reference/cli.md#lint) 실행은 Next.js의 내장된 ESLint 실행과 같아요.

어플리케이션의 최상위에 `pages`와 `public` 두 개의 폴더를 만듭시다: 

- `pages` - 파일이름들을 기반으로 경로와 연결됩니다. 예를들어, `pages/about.js` 는 `/about` 와 연결되죠.
- `public` - 이미지나 폰트 등의 정적 에셋들의 저장소라고 보면 돼요. `public` 폴더 내의 파일들은 기본 URL인 (`/`) 을 시작하는 코드에서 참조할 수 있어요.

Next.js 는 [pages](/docs/basic-features/pages.md) 개념을 기반으로 구축되었습니다. 
페이지는 `pages` 속의 `.js`, `.jsx`, `.ts`, `.tsx` 확장자를 가진 [React Component](https://react.dev/learn/your-first-component) 로 이루어져 있습니다.
파일이름과 함께 [동적 경로](/docs/routing/dynamic-routes)로 파라미터를 추가할 수도 있습니다.


`pages` 폴더로 들어가서, 시작하기위한 `index.js` 파일을 추가합시다.
이 페이지는 사용자가 당신의 어플리케이션을 방문했을 때 가장 첫번째로 보여질 페이지 입니다.

`pages/index.js` 를 아래와 같은 내용으로 채워봅시다:

```jsx
function HomePage() {
  return <div>Welcome to Next.js!</div>
}

export default HomePage
```

설치가 완료된 후:

- 개발서버 `http://localhost:3000`에 접속할 수 있도록 `npm run dev` or `yarn dev` or `pnpm dev` 를 실행하세요.
- `http://localhost:3000` 를 방문해서 당신의 어플리케이션을 구경하세요.
- `pages/index.js` 를 수정하고, 업데이트된 당신의 브라우저를 확인하세요.

지금까지, 우리는:

- 자동 컴파일 and [빌드](/docs/advanced-features/compiler.md)
- [빠른 새로고침 반응](https://nextjs.org/blog/next-9-4#fast-refresh)
- [정적 생성 및 서버 측 렌더링](/docs/basic-features/data-fetching/overview.md) of [`pages/`](/docs/basic-features/pages.md)
URL (`/`) 을 통해 매핑되는 `public/` 통한 [정적파일 제공](/docs/basic-features/static-file-serving.md) 

추가로, 어느 Next.js 어플리케이션이든 처음으로부터 만들 준비가 되어있습니다. [Deployment documentation](/docs/deployment.md)에서 더 읽어보세요.

## 관련되어서

다음에 할 것에 대한 정보를 제공할게요. 다음 섹션을 권장합니다:

<div class="card">
  <a href="/docs/basic-features/pages.md">
    <b>Pages:</b>
    <small>Next.js 에서 page가 무엇인지</small>
  </a>
</div>

<div class="card">
  <a href="/docs/basic-features/built-in-css-support.md">
    <b>CSS Support:</b>
    <small>당신만의 커스텀 스타일을 위한 내장 CSS 지원</small>
  </a>
</div>

<div class="card">
  <a href="/docs/api-reference/cli.md">
    <b>CLI:</b>
    <small>Next.js CLI에 대해서 더 알아보기</small>
  </a>
</div>
