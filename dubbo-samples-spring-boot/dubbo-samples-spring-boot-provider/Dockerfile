# 使用轻量级的 JRE 镜像（根据你的 Java 版本选择）
FROM eclipse-temurin:17-jre-alpine

# 设置工作目录
WORKDIR /app

# 将 Maven 打包好的 jar 拷贝进去
COPY target/*.jar dubbo-samples-spring-boot-provider-1.0-SNAPSHOT.jar

# 设置 JVM 参数（如内存优化）
ENV JAVA_OPTS="-Xms512m -Xmx512m"

# 启动命令
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -jar dubbo-samples-spring-boot-provider-1.0-SNAPSHOT.jar"]