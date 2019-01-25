FROM websphere-liberty:webProfile7
COPY server.xml /config/server.xml
COPY server.env /config/server.env
COPY CustomerOrderServicesApp/target/CustomerOrderServicesApp-0.1.0-SNAPSHOT.ear /config/apps
COPY ProductSearchServiceApp/target/ProductSearchServiceApp-0.1.0-SNAPSHOT.ear /config/apps
COPY db2lib/db2jcc4.jar /liberty/wlp/usr/shared/resources
COPY db2lib/db2jcc_license_cu.jar /liberty/wlp/usr/shared/resources

RUN /opt/ibm/wlp/bin/installUtility install  --acceptLicense \
    appSecurity-2.0 \
    ejbLite-3.1 \
    ldapRegistry-3.0 \
    localConnector-1.0 \
    jaxrs-1.1 \
    jdbc-4.1 \
    jpa-2.0 \
    jsp-2.3 \
    servlet-3.1
