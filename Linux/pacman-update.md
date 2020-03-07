# Pacman


## 1. 更新时出现文件已存在

出现 错误为:

```
conflicting files:
npm: /usr/lib/node_modules/npm/node_modules/minizlib/node_modules/minipass/LICENSE already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/minizlib/node_modules/minipass/README.md already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/minizlib/node_modules/minipass/index.js already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/minizlib/node_modules/minipass/package.json already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/npm-registry-fetch/node_modules/safe-buffer/LICENSE already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/npm-registry-fetch/node_modules/safe-buffer/README.md already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/npm-registry-fetch/node_modules/safe-buffer/index.d.ts already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/npm-registry-fetch/node_modules/safe-buffer/index.js already exists in filesystem
npm: /usr/lib/node_modules/npm/node_modules/npm-registry-fetch/node_modules/safe-buffer/package.json already exists in filesystem
```

解决

目前我的操作是强制更新解决的

```
sudo pacman -S npm --overwrite /path/to/npm
```
