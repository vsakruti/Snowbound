FROM alfresco/alfresco-content-repository:6.1.0-RC7

ARG TOMCAT_DIR=/usr/local/tomcat

COPY snowbound/virtualviewer.war $TOMCAT_DIR/webapps/virtualviewer.war

RUN mkdir -p $TOMCAT_DIR/amps

COPY amps/snowbound-repo-0.2.amp $TOMCAT_DIR/amps/snowbound-repo-0.2.amp

RUN java -jar $TOMCAT_DIR/alfresco-mmt/alfresco-mmt*.jar install \
        $TOMCAT_DIR/amps/snowbound-repo-0.2.amp \
        $TOMCAT_DIR/webapps/alfresco -nobackup -force