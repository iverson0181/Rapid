# Rapid

## Very easy automatic code generation
#### 非常容易地自动生成代码
#### 非常に簡単な自動コード生成

## See the video link below
#### 请看以下视频链接
#### 以下のビデオリンクをご覧ください。

> https://www.bilibili.com/video/BV1XT411M7rZ/?vd_source=5540375a2c7c12747e7298f4e6f5ddad

## Refer to the java demo for usage. It is very simple and fast
#### 用法请参考java的demo，非常简单快速
#### javaのデモを参考に、非常に簡単な使い方をしてください

## Not limited to any programming language, All can be used with confidence, home must choose
#### 不局限于任何编程语言, 都能用得放心，居家必选
#### プログラミング言語に限定されない, ご家庭の必需品

## Welcome interested friends to contribute excellent templates
#### 欢迎有兴趣的朋友仔贡献优秀的模板
#### ご興味のある方からの優れたテンプレートのご投稿をお待ちしております

## Template API (Optional)

#### Configuration files
#### 配置文件
#### コンフィギュレーションファイル
>> template.yml will override application.yml for the same properties
```
src/main/resources/application.yml
src/main/resources/template/template.yml
```


#### The default template parameters are the following
#### 默认模板参数有以下
#### デフォルトのテンプレートパラメーターは以下の通りです
```
tableComment    # Comments on the table
tableFileds     # A list of fields of the table
className       # The name of the class generated by this table
objectName      # The name of the instant generated by this class
domainName      # your package domain
tableName       # database table
packagePath   # Your package's base directory
author          # author 
version         # version
```
##### Using iterations like this
##### 这样使用迭代
##### このようにイテレーションを使うことで
```
[# th:each="field : ${tableFileds}"]
/** [(${field.extra})]  */
@Field("[(${field.key})]")
private [(${field.type})] [(${field.field})];

[/]
```
##### Mock Table Demo For Mysql
```
CREATE DATABASE rapid_dev;
CREATE TABLE rapid_dev.`order` (
	id int auto_increment primary key,
	name varchar(40) not null 
)
ENGINE=InnoDB
COMMENT='order comment';
```
