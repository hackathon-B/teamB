# ベースイメージ
FROM node:20-bullseye

# 作業ディレクトリの設定
WORKDIR /app

# 依存関係ファイルのコピー
COPY package.json package-lock.json ./

# 依存関係のインストール
RUN npm install npm@latest && npm install

# アプリケーションのコピー
COPY . . 

# 開発サーバーを起動
# CMD ["npm", "run", "dev"]