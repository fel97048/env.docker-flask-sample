# Flaskを使ったアプリのDockerイメージ作成手順書

## Flaskアプリケーションの作成

1. Pythonの仮想環境を作成
```
> python3 -m venv env.docker-flask-sample
> cd env.docker-flask-sample
> source bin/activate
```

2. 仮想環境にFlaskをインストール
```
> pip3 install flask
```

3. appディレクトリを作成
```
> mkdir app
```

4. app/app.pyファイルを作成し内容は以下とする
```
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World</p>"

if __name__ == '__main__':
    app.run()
```

5. 試しに実行してブラウザから http://127.0.0.1:5000 にアクセス
```
> python app/app.py
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on http://127.0.0.1:5000
Press CTRL+C to quit
```


