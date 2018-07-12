# common-dependency

当前版本 | `1.5.6.RELEASE`
--- | ---

公共依赖项目。本项目中集成了业务开发常用的库、框架的依赖，并对版本冲突的依赖进行了处理。


项目采用与springboot相同的多版本管理方案，通过多个分支以及tag的方式进行管理。项目发布的版本号原则上与springboot保持一致。

你的项目可以使用 `common-dependency` 作为 parent, 这样间接地以`common-build` 为ancestor.

```
<parent>
    <groupId>net.sealake</groupId>
    <artifactId>common-dependency</artifactId>
    <version>${common-dependency.version}</version>
</parent>
```

或者在 `dependencyManagement` 中import它.

```
<!-- 以 common-build 为parent是可选的 -->
<parent>
    <groupId>net.sealake</groupId>
    <artifactId>common-build</artifactId>
    <version>${common-build.version}</version>
</parent>

<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>net.sealake</groupId>
            <artifactId>common-dependency</artifactId>
            <version>${common-dependency.version}</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

## References
1. [common-build项目](https://github.com/sealake/common-build)

