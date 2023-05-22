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

## Manual Setup

Install `next`, `react` and `react-dom` in your project:

```bash
npm install next react react-dom
# or
yarn add next react react-dom
# or
pnpm add next react react-dom
```

Open `package.json` and add the following `scripts`:

```json
"scripts": {
  "dev": "next dev",
  "build": "next build",
  "start": "next start",
  "lint": "next lint"
}
```

These scripts refer to the different stages of developing an application:

- `dev` - Runs [`next dev`](/docs/api-reference/cli.md#development) to start Next.js in development mode
- `build` - Runs [`next build`](/docs/api-reference/cli.md#build) to build the application for production usage
- `start` - Runs [`next start`](/docs/api-reference/cli.md#production) to start a Next.js production server
- `lint` - Runs [`next lint`](/docs/api-reference/cli.md#lint) to set up Next.js' built-in ESLint configuration

Create two directories `pages` and `public` at the root of your application:

- `pages` - Associated with a route based on their file name. For example, `pages/about.js` is mapped to `/about`
- `public` - Stores static assets such as images, fonts, etc. Files inside `public` directory can then be referenced by your code starting from the base URL (`/`).

Next.js is built around the concept of [pages](/docs/basic-features/pages.md). A page is a [React Component](https://react.dev/learn/your-first-component) exported from a `.js`, `.jsx`, `.ts`, or `.tsx` file in the `pages` directory. You can even add [dynamic route](/docs/routing/dynamic-routes) parameters with the filename.

Inside the `pages` directory, add the `index.js` file to get started. This is the page that is rendered when the user visits the root of your application.

Populate `pages/index.js` with the following contents:

```jsx
function HomePage() {
  return <div>Welcome to Next.js!</div>
}

export default HomePage
```

After the set up is complete:

- Run `npm run dev` or `yarn dev` or `pnpm dev` to start the development server on `http://localhost:3000`
- Visit `http://localhost:3000` to view your application
- Edit `pages/index.js` and see the updated result in your browser

So far, we get:

- Automatic compilation and [bundling](/docs/advanced-features/compiler.md)
- [React Fast Refresh](https://nextjs.org/blog/next-9-4#fast-refresh)
- [Static generation and server-side rendering](/docs/basic-features/data-fetching/overview.md) of [`pages/`](/docs/basic-features/pages.md)
- [Static file serving](/docs/basic-features/static-file-serving.md) through `public/` which is mapped to the base URL (`/`)

In addition, any Next.js application is ready for production from the start. Read more in our [Deployment documentation](/docs/deployment.md).

## Related

For more information on what to do next, we recommend the following sections:

<div class="card">
  <a href="/docs/basic-features/pages.md">
    <b>Pages:</b>
    <small>Learn more about what pages are in Next.js.</small>
  </a>
</div>

<div class="card">
  <a href="/docs/basic-features/built-in-css-support.md">
    <b>CSS Support:</b>
    <small>Built-in CSS support to add custom styles to your app.</small>
  </a>
</div>

<div class="card">
  <a href="/docs/api-reference/cli.md">
    <b>CLI:</b>
    <small>Learn more about the Next.js CLI.</small>
  </a>
</div>
