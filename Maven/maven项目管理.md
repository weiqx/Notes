[视频链接]（https://www.bilibili.com/video/BV1Ah411S7ZE?p=18&spm_id_from=pageDriver）



**maven基础**

- Maven简介
- 下载与安装
- Maven基础概念
- 第一个Maven项目（手工制作）
- 第一个Maven项目（idea 生成）
- 依赖管理
- 生命周期与插件



### 1 maven简介

maven是一个项目管理工具，将项目开发和管理过程

POM （Project Object Model）:项目对象模型）:项目对象模型

项目构建

依赖管理

统一开发结构

maven项目目录结构



![1625558397334](C:\Users\86568\AppData\Roaming\Typora\typora-user-images\1625558397334.png)







### 2 maven下载与安装



###### 环境变量配置

- 依赖Java ，需要配置JAVA_HOME 

- 设置MAVEN 自身的运行环境，需要配置MAVEN_HOME

- 测试环境配置结果

  cmd   里面输入   `mvn`

```java
D:\Enviroment\apache-maven-3.6.0  -- maven的安装目录，新建系统变量MAVEN_HOME

%MAVEN_HOME%\bin		-- 编辑环境变量  
```



### 3 Maven基础概念

POM （Project Object Model）:项目对象模型

仓库：

坐标：组织ID  项目ID  版本号

**本地仓库设置**

```xml
Default: ${user.home}/.m2/repository  -- settings文件 本地仓库默认位置
C:\Users\86568\.m2\repository     -- 本地仓库默认位置

<localRepository>D:\maven\repository</localRepository>  -- 自己手动配置的本地仓库位置
```



**远程仓库设置**

Maven默认连接的仓库位置

```xml
<repositories>
	<repository>
        <id>central</id>
        <name>Central Repository</name>
        <url>https://repo.maven.apache.org/maven2</url>  -- 默认在国外的网站
        <layout>default</layout>
        <snapshots>
        	<enabled>false</enabled>
        </snapshots>
    </repository>
</repositories>
```



**镜像仓库配置**

在setting文件中配置阿里云镜像仓库

```xml
<mirrors>
    <!--配置具体的仓库下的镜像  -->
    <mirror>
        <!-- 词镜像的唯一标识符，用来区分不同的mirror 元素 -->
        <id>nexus-aliyun</id>
        <!-- 对哪种仓库进行 -->
        <mirrorOf>central</mirrorOf>
        <!-- -->
        <name>Nexus aliyun</name>
        <!-- URL -->
        <url>http://maven.aliyun.com/nexus/content/groups/public</url>
    </mirror>
</mirrors>
```



小结：

- 配置本地仓库
- 配置阿里镜像仓库（资源从哪里来）
- setting文件的区别















### 4 第一个Maven项目（手工制作）

Maven工程目录结构

![1625640186137](C:\Users\86568\AppData\Roaming\Typora\typora-user-images\1625640186137.png)

Maven项目构建命令

```bash
mvn compile    # 编译
mvn clean      # 清理
mvn test	   # 测试
mvn package    # 打包
mvn install    # 安装到本地仓库
```



```java
mvn compile  -- dos 命令

cls   -- 清空cmd控制台

mvn clean   -- 
```



### 5 第一个Maven项目（idea 生成）

配置**Maven**

![1625640247805](C:\Users\86568\AppData\Roaming\Typora\typora-user-images\1625640247805.png)





### 6 依赖管理

依赖管理：依赖范围、依赖范围传递性

依赖传递：

可选依赖：

排除依赖：



### 7 生命周期与插件







