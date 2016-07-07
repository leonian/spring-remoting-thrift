**The repository is deprecated, moved to https://github.com/superhj1987/awesome-libs/blob/master/doc/spring-remoting-thrift.md**

# spring-remoting-thrift
thrift rpc support in spring: ThriftServiceExporter;ThriftFactoryBean

## Github Url

[https://github.com/superhj1987/spring-remoting-thrift](https://github.com/superhj1987/spring-remoting-thrift)

## Usage

### Server

    <bean name="/api/appService"
          class="ome.srhang.libs.spring.remoting.thrift.ThriftServiceExporter">
        <property name="serviceInterface" value="***">
        </property>
        <property name="service">
            <ref bean="***"/>
        </property>
    </bean>

### Client

    <bean id="thriftAppService"
          class="me.srhang.libs.spring.remoting.thrift.ThriftProxyFactoryBean">
        <property name="serviceUrl">
            <value>${api.url}</value>
        </property>
        <property name="serviceInterface"
                  value="***"/>
    </bean>
