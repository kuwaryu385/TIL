# Warファイルがデプロイ出来なかったときの対応

**[問題]**
はじめて作成したWebアプリをWarファイルにデプロイしようとしたとき
にページが表示されず404エラーが表示された。

**[原因]**
SpringBootServletInitializerクラスを配置していなかった。

**[解決方法やコマンド]**
* SpringBootServletInitializerクラスを配置した。
* これを実装することでWarファイルからSpringApplication,Servlet,Filter,ServletContextInitializerBeenをサーバーにバインドするだとか。
* 必要になるのは、warファイルを作成してデプロイする場合のみだそうです。



```java:mainクラス配下に実装
//mainクラス配下に実装

import org.springframework.boot.builder.SpringApplicationBuilder;
import org.springframework.boot.web.servlet.support.SpringBootServletInitializer;

public class ServletInitializer extends SpringBootServletInitializer {

	@Override
	protected SpringApplicationBuilder configure(SpringApplicationBuilder application) {
		return application.sources(SimpleStressCheckerApplication.class);
```

**[参考文献]**
クラスSpringBootServletInitializer
https://docs.spring.io/spring-boot/docs/current/api/org/springframework/boot/web/servlet/support/SpringBootServletInitializer.html
