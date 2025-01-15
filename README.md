# plugin-oauth2

Halo 2.0 的 OAuth2 第三方登录插件(for Liteyuki Passport)。

遵循GPL3.0许可从[上游仓库](https://github.com/halo-sigs/plugin-oauth2)fork修改分发

这里提供一个可以对接任意OAuth2协议的第三方登录的方法

参考[halo-sigs/plugin-oauth2/issues/23](https://github.com/halo-sigs/plugin-oauth2/issues/23)

但是这个issue并没有解决我的问题，但是给我提供了尝试的思路，直接新增不起效果，但是可以尝试更改现有的配置

## 修改和接入其他provider的方法

定位到[src/main/resources/extensions/auth-provider.yaml](src/main/resources/extensions/auth-provider.yaml)文件
参考着改一个你的OAuth2第三方登录的信息

然后定位到[src/main/resources/extensions/client-registrations.yaml](src/main/resources/extensions/client-registrations.yaml)，按照提示填入你的OAuth2第三方登录的配置

使用jdk17编译，然后打包jar

```bash
./gradlew build
```

最后在[built/libs](built/libs)目录下找到生成的jar文件，上传到你的Halo博客的插件管理页面即可
