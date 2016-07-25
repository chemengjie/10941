创建项目
mvn archetype:generate -DgroupId=com.hand -DartifactId=javatest -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false -DarchetypeCatalog=local

进行编译
mvn clean compile


执行程序
mvn exec:java -Dexec.mainClass="com.hand.App" -Dexec.args="arg0 arg1 arg2"



mvn clean compile exec:java -Dexec.mainClass="com.hand.App" -Dexec.args="arg0 arg1 arg2"
maven创建Web项目

mvn archetype:generate -DgroupId=com.hand -DartifactId=webtest1 -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false -DarchetypeCatalog=local



<plugins>
      <plugin>
                <groupId>org.eclipse.jetty</groupId>
                <artifactId>jetty-maven-plugin</artifactId>
                <version>9.2.11.v20150529</version>
                <configuration>
                    <webAppConfig>
                        <allowDuplicateFragmentNames>true</allowDuplicateFragmentNames>
                    </webAppConfig>
                </configuration>
            </plugin>
    </plugins>
运行项目
mvn jetty:run