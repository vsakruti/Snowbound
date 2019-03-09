FROM alfresco/alfresco-share:6.1.0-RC3

ARG TOMCAT_DIR=/usr/local/tomcat

RUN mkdir -p $TOMCAT_DIR/amps_share

COPY amps_share/snowbound-share-0.2.amp $TOMCAT_DIR/amps_share

RUN java -jar $TOMCAT_DIR/alfresco-mmt/alfresco-mmt*.jar install \
    $TOMCAT_DIR/amps_share/snowbound-share-0.2.amp \
	$TOMCAT_DIR/webapps/share -directory -nobackup -force