# Wildfly 10.x - Spring 4.x sample applications.

Need to edit or create some existing WildFly modul configuration.

1. Edit ..\org\apache\cxf\impl\main\module.xml

<?xml version="1.0" encoding="UTF-8"?>
<module xmlns="urn:jboss:module:1.3" name="org.apache.cxf.impl">

    <properties>
        <property name="jboss.api" value="private"/>
    </properties>

    <resources>
        <resource-root path="cxf-rt-bindings-coloc-3.1.6.jar"/>
        <resource-root path="cxf-rt-bindings-object-3.1.6.jar"/>
        <resource-root path="cxf-rt-bindings-soap-3.1.6.jar"/>
        <resource-root path="cxf-rt-bindings-xml-3.1.6.jar"/>
        <resource-root path="cxf-rt-databinding-aegis-3.1.6.jar"/>
        <resource-root path="cxf-rt-databinding-jaxb-3.1.6.jar"/>
        <resource-root path="cxf-rt-features-clustering-3.1.6.jar"/>
        <resource-root path="cxf-rt-frontend-jaxws-3.1.6.jar"/>
        <resource-root path="cxf-rt-frontend-simple-3.1.6.jar"/>
        <resource-root path="cxf-rt-management-3.1.6.jar"/>
        <resource-root path="cxf-rt-security-3.1.6.jar"/>
        <resource-root path="cxf-rt-security-3.1.6-jandex.jar"/>
        <resource-root path="cxf-rt-security-saml-3.1.6.jar"/>
        <resource-root path="cxf-rt-transports-http-3.1.6.jar"/>
        <resource-root path="cxf-rt-transports-http-hc-3.1.6.jar"/>
        <resource-root path="cxf-rt-transports-jms-3.1.6.jar"/>
        <resource-root path="cxf-rt-transports-local-3.1.6.jar"/>
        <resource-root path="cxf-rt-wsdl-3.1.6.jar"/>
        <resource-root path="cxf-rt-ws-addr-3.1.6.jar"/>
        <resource-root path="cxf-rt-ws-mex-3.1.6.jar"/>
        <resource-root path="cxf-rt-ws-policy-3.1.6.jar"/>
        <resource-root path="cxf-rt-ws-rm-3.1.6.jar"/>
        <resource-root path="cxf-tools-common-3.1.6.jar"/>
        <resource-root path="cxf-tools-java2ws-3.1.6.jar"/>
        <resource-root path="cxf-tools-validator-3.1.6.jar"/>
        <resource-root path="cxf-tools-wsdlto-core-3.1.6.jar"/>
        <resource-root path="cxf-tools-wsdlto-databinding-jaxb-3.1.6.jar"/>
        <resource-root path="cxf-tools-wsdlto-frontend-jaxws-3.1.6.jar"/>
        <resource-root path="cxf-services-ws-discovery-api-3.1.6.jar"/>
        <resource-root path="cxf-xjc-boolean-3.0.5.jar"/>
        <resource-root path="cxf-xjc-bug986-3.0.5.jar"/>
        <resource-root path="cxf-xjc-dv-3.0.5.jar"/>
        <resource-root path="cxf-xjc-ts-3.0.5.jar"/>
        <resource-root path="cxf-xjc-runtime-3.0.5.jar"/>
    </resources>

    <dependencies>
        <module name="asm.asm" />
        <module name="javax.api" />
        <module name="javax.annotation.api" />
        <module name="javax.jms.api" />
        <module name="javax.jws.api" />
        <module name="javax.mail.api" />
        <module name="javax.resource.api" />
        <module name="javax.servlet.api" />
        <module name="javax.wsdl4j.api" />
        <module name="javax.xml.bind.api" services="import"/>
        <module name="com.sun.xml.bind" services="import"/>
        <module name="javax.xml.soap.api" />
        <module name="javax.xml.stream.api" />
        <module name="javax.xml.ws.api" />
        <module name="org.apache.commons.lang" />
        <module name="org.apache.httpcomponents"/>
        <module name="org.apache.neethi" />
        <module name="org.apache.velocity" />
        <module name="org.apache.xml-resolver" />
        <module name="org.apache.ws.xmlschema" />
        <module name="org.apache.ws.security" />
        <module name="org.apache.santuario.xmlsec" />
        <module name="org.codehaus.woodstox" />
        <module name="org.joda.time" />
        <module name="org.opensaml" />
        <module name="org.apache.cxf" export="true">
          <imports>
            <include path="META-INF/cxf"/>
            <include path="META-INF"/>
          </imports>
          <exports>
            <include path="META-INF/cxf"/>
            <include path="META-INF"/>
          </exports>
        </module>
        <module name="org.apache.cxf.ws-security" export="true" services="export">
          <imports>
            <include path="META-INF/cxf"/>
            <include path="META-INF"/>
          </imports>
          <exports>
            <include path="META-INF/cxf"/>
            <include path="META-INF"/>
          </exports>
        </module>
        <module name="org.apache.cxf.services-sts" export="true" services="export">
          <imports>
            <include path="META-INF/cxf"/>
            <include path="META-INF"/>
          </imports>
          <exports>
            <include path="META-INF/cxf"/>
            <include path="META-INF"/>
          </exports>
        </module>
        <module name="org.springframework.spring" export="true" services="export" />
    </dependencies>
</module>
