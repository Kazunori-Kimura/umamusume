```sh
npx create-next-app umamusume
cd umamusume
# git の初期化
git init
# 各種パッケージのインストール
npm install --save-dev typescript @types/node @types/react
npm install --save-dev eslint typescript @typescript-eslint/parser @typescript-eslint/eslint-plugin eslint-config-react-app eslint-plugin-flowtype eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react eslint-plugin-react-hooks prettier rimraf
npm install --save-dev sass
# 設定ファイルの生成
mkdir .vscode
touch .vscode/settings.json
touch .vscode/extensions.json
touch .editorconfig
touch .eslintignore
touch .prettierignore
touch .prettierrc.js
# src フォルダに各ファイルを移動
mkdir src
mv pages src/
mv styles src/
# 拡張子の変更 (.js -> .tsx, .css -> .scss)
mv src/pages/_app.js src/pages/_app.tsx
mv src/pages/index.js src/pages/index.tsx
mv src/styles/globals.css src/styles/globals.scss
mv src/styles/Home.module.css src/styles/Home.module.scss
# おもむろに build すると tsconfig.json, next-env.d.ts が生成される
npx next build
```
