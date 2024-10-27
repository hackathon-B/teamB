# Dockerfile
# Python3.11が使えるUvicorn-Gunicornイメージ
FROM tiangolo/uvicorn-gunicorn:python3.11

# メンテナー情報をラベルに追加
LABEL maintainer="Sebastian Ramirez <tiangolo@gmail.com>"

# requirements.txtをコンテナ内の/tmpにコピー
COPY requirements.txt /tmp/requirements.txt

# 依存関係をキャッシュを使わずにインストール
RUN pip install --no-cache-dir -r /tmp/requirements.txt

# ローカルの ./appをコンテナ内の /appにコピー
COPY ./app /app

# 作業ディレクトリを /app に設定
WORKDIR /app