# base

Next.js + Tailwind CSS 기반의 정적 베이스 프로젝트  
(React / TypeScript / ESLint 포함, 안정 버전 기준)

---

## 📦 필수 패키지 설치 (호환 안정 버전)

```bash
# 1. 핵심 패키지
npm install next@15.3.4 react@18.3.1 react-dom@18.3.1

# 2. TailwindCSS + PostCSS
npm install -D tailwindcss@3.4.1 postcss@8.4.38 autoprefixer@10.4.19
npx tailwindcss init -p

# 3. TypeScript + 타입
npm install -D typescript@5.4.5 @types/react@18.2.64 @types/react-dom@18.2.17

# 4. ESLint
npm install -D eslint@8.57.0 eslint-config-next@15.3.4
```

---

## 📁 필수 디렉토리/파일 생성

```bash
mkdir -p src/app
touch src/app/layout.tsx src/app/page.tsx src/app/globals.css
touch next.config.ts tsconfig.json
```

---

## 📄 필수 코드

### ✅ src/app/globals.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

### ✅ src/app/layout.tsx

```tsx
export default function RootLayout({ children }: { children: React.ReactNode }) {
  return (
    <html lang="ko">
      <body>{children}</body>
    </html>
  );
}
```

---

### ✅ src/app/page.tsx

```tsx
export default function Home() {
  return (
    <main className="text-3xl font-bold text-center mt-20">
      Hello, world!
    </main>
  );
}
```

---

## 🚀 실행 방법

```bash
npm run dev
```

---

이 프로젝트는 정적 안내형 웹사이트의 기본 뼈대로,  
Vercel 또는 GitHub Pages 정적 배포용으로 사용됩니다.