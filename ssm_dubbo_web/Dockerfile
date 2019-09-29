FROM tomcat:7.0

ARG JAR_FILE

#定义工作目录
ENV TOMCAT_BASE /usr/local/tomcat

#复制配置文件
COPY server.xml $TOMCAT_BASE/conf/

ADD target/${JAR_FILE} /usr/local/tomcat/webapps/

#给配置文件增加读权限
RUN chmod a+xr $TOMCAT_BASE/conf/server.xml

#删除默认的ROOT文件件
RUN rm -rf $TOMCAT_BASE/webapps/ROOT