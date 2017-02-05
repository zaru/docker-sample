```
$ docker build -t ruby2-sample .
$ docker run --rm -v "$PWD":/app -w /app ruby2-sample bundle install --path vendor/bundle
```
