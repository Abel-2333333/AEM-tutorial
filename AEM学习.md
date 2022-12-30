# AEM学习

## 1. 生成demo工程

### 配置maven环境

参考链接: https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-17454.html?lang=en

拷贝上面链接中的内容并追加如下配置到settings.xml中

```xml
<activeProfiles>
    <activeProfile>adobe-public</activeProfile>
</activeProfiles>
```

### 生成工程(两种命令)

1. 创建一个空文件夹
2. 切换到该文件夹路径, 输入下面两个命令中的其中一个

①

```sh
mvn org.apache.maven.plugins:maven-archetype-plugin:2.4:generate -DarchetypeGroupId=com.adobe.granite.archetypes -DarchetypeArtifactId=aem-project-archetype -DarchetypeVersion=18 -DarchetypeCatalog=https://repo.adobe.com/nexus/content/groups/public/
```

②

```sh
mvn archetype:generate -DarchetypeGroupId=com.adobe.aem -DarchetypeArtifactId=aem-project-archetype -DarchetypeVersion=36 -DappId=aemdemo -DartifactId=aemdemo -DgroupId=com.adobe.aem.demo -DappTitle=aemDemo -Dpackage=com.adobe.aem.demo -DaemVersion=6.5.12 -DincludeDispatcherConfig=n
```

