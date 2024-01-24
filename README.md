# deploy-demo01

使用 deploy.sh 進行部屬

官方資料：https://v3.vitejs.dev/guide/static-deploy.html#github-pages

# 步驟

1. 建立 deploy.sh 檔
```sh
#!/usr/bin/env sh

# abort on errors
set -e

# build
npm run build

# navigate into the build output directory
cd dist

# place .nojekyll to bypass Jekyll processing
echo > .nojekyll

# if you are deploying to a custom domain
# echo 'www.example.com' > CNAME

git init
git checkout -B main
git add -A
git commit -m 'deploy'

# if you are deploying to https://<USERNAME>.github.io
# git push -f git@github.com:<USERNAME>/<USERNAME>.github.io.git main

# if you are deploying to https://<USERNAME>.github.io/<REPO>
# git push -f git@github.com:<USERNAME>/<REPO>.git main:gh-pages

cd -
```

2. vite.config.js 中， base 屬性設定為儲存庫名稱
```sh
base: "/<REPO>/"
```

3. 部屬指令
```sh
sh deploy.sh
```
