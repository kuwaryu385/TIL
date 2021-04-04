##HTTPリクエスト302について

**[問題]**  
springboot testでレスポンスのHTTPステータスコードの判定のところでリダイレクトの場合はどのように実装するか分からなかった。

**[解決方法やコマンド]**  

通常はステータスコード200は

```java:title
status().isOk
```
でテスト

リダイレクトの場合は302（GETの場合）値を変更しないでそのまま移動する感じ。


```java:title
  (status().found())
```



**[参考URL]**  

https://developer.mozilla.org/ja/docs/Web/HTTP/Status

https://developer.mozilla.org/ja/docs/Web/HTTP/Status/302  
