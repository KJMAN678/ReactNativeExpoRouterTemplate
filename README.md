### Devin

- [Devin's Machine](https://app.devin.ai/workspace) でリポジトリ追加

#### 1.Git Pull
- そのまま

#### 2.Configure Secrets
```sh
# 環境変数用のファイル作成
$ touch .envrc

# .envrc に下記を入力. xxx は適宜更新

export HOGE=hoge

# 環境変数を読み込む
$ direnv allow
```

- ローカル用
```sh
$ brew install direnv
```
#### 4.Maintain Dependencies
```sh
$ docker compose up -d
$ docker compose down
$ docker compose build
```

#### 5.SetUp Lint
```sh
$ docker compose run --rm frontend npx expo lint
```

#### 6.SetUp Tests
- no tests ran in 0.00s だと Devin の Verify が通らないっぽい
```sh
$ docker compose run --rm frontend npm run test
```

#### 8.SetUp App
```sh
$ http://localhost:8081/ がフロントエンドのURL
```

#### 9.Additional Notes
- 必ず日本語で回答してください
を入力

### package-json, package-json-lock のアプデ
```sh
$ cd frontend
$ npx npm-check-updates -u
$ npx npm-check-updates -u --target minor
$ npx npm-check-updates -u --target patch
$ npm install
cd ..
```

### 参考

- [【2025年最新版】Expo/React Nativeの開発環境を構築する ExpoとExpo Routerをセットアップ](https://zenn.dev/arafipro/books/rn-2025-newest-expo-setup/viewer/02_expo-setup)
- 
