FROM node

# アプリケーションディレクトリを作成する
WORKDIR /usr/src/server

# キャッシュを利用するために、package.jsonとpackage-lock.jsonのみをコピーし、
# 依存関係を先にインストール
COPY package*.json ./
RUN npm install

# アプリケーションコードをコンテナにコピー
COPY . .

EXPOSE 8080
CMD [ "npm", "run", "serve" ]