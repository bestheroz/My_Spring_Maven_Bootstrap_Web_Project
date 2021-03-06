
## A customized Spring framework including the latest versions of Maven, DB-MyBatis, and Bootstrap.

> 최신 버전의 Maven, DB-MyBatis, Bootstrap을 포함하여 사용자 정의 된 스프링 프레임워크입니다.

## The UI framework uses Bootstrap, mostly expressed in jsp and ajax.

> UI 프레임워크는 Bootstrap을 사용하였으며 대부분 jsp와 ajax로 표현되어 있습니다.

## Base on Java8, tomcat9.

> 자바 8, 톰캣 9 기반

    <?xml version="1.0" encoding="UTF-8"?>
    <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
        <modelVersion>4.0.0</modelVersion>
        <groupId>com.github.bestheroz</groupId>
        <artifactId>My_Spring_Legacy_MyBatis_jQuery_Web_Project</artifactId>
        <name>My_Spring_Legacy_MyBatis_jQuery_Web_Project</name>
        <packaging>war</packaging>
        <version>1.0.0-BUILD-SNAPSHOT</version>
        <properties>
            <m2eclipse.wtp.contextRoot>/ROOT</m2eclipse.wtp.contextRoot>
            <java-version>1.8</java-version>
            <springframework-version>5.1.8.RELEASE</springframework-version>
            <spring-security-version>5.1.5.RELEASE</spring-security-version>
            <aspectj-version>1.9.4</aspectj-version>
            <slf4j-version>1.7.26</slf4j-version>
            <logback-version>1.2.3</logback-version>
            <jdbcdslogexp2-version>2.1</jdbcdslogexp2-version>
            <ddal-sqlparser-version>3.0.3</ddal-sqlparser-version>
            <gson-version>2.8.5</gson-version>
            <joda-time-version>2.10.3</joda-time-version>
            <lang3-version>3.9</lang3-version>
            <mybatis-version>3.5.1</mybatis-version>
            <mybatis-spring-version>2.0.1</mybatis-spring-version>
            <HikariCP-version>3.3.1</HikariCP-version>
            <common-io-version>2.6</common-io-version>
            <tika-version>1.21</tika-version>
            <commons-codec-version>1.12</commons-codec-version>
            <junit-version>5.5.0</junit-version>
            <servlet-api-version>4.0.1</servlet-api-version> <!-- tomcat9 : 4.0.1 tomcat8.5 : 3.1.0, tomcat7 : 3.0.1 -->
            <servlet.jsp-api-version>2.3.3</servlet.jsp-api-version> <!-- tomcat9 & tomcat 8.5 : 2.3.3, tomcat7 : 2.2.1 -->
            <jstl-version>1.2</jstl-version>
            <ziplet-version>2.4.1</ziplet-version>
            <lucy-version>1.6.3</lucy-version>
            <poi-version>4.1.0</poi-version>
            <pdfbox-version>2.0.16</pdfbox-version>
            <boxable-version>1.5</boxable-version>
            <mockito-version>2.27.0</mockito-version>
            <hamcrest-version>1.3</hamcrest-version>
            <h2database-version>1.4.199</h2database-version>
            <!-- maven 빌드 및 ant 배포 관련 -->
            <maven-eclipse-plugin-version>2.10</maven-eclipse-plugin-version>
            <maven-compiler-plugin-version>3.8.1</maven-compiler-plugin-version>
            <exec-maven-plugin-version>1.6.0</exec-maven-plugin-version>
            <maven-war-plugin-version>3.2.3</maven-war-plugin-version>
            <maven-antrun-plugin-version>1.8</maven-antrun-plugin-version>
            <org.apache.ant-version>1.10.6</org.apache.ant-version>
            <jsch-version>0.1.55</jsch-version>
            <ant-contrib-version>1.0b3</ant-contrib-version>
        </properties>
    
        <dependencies>
            <!-- Spring -->
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-webmvc</artifactId>
                <version>${springframework-version}</version>
            </dependency>
            <dependency>
                <artifactId>spring-jdbc</artifactId>
                <groupId>org.springframework</groupId>
                <version>${springframework-version}</version>
            </dependency>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-aop</artifactId>
                <version>${springframework-version}</version>
            </dependency>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-test</artifactId>
                <version>${springframework-version}</version>
            </dependency>
    
            <!-- spring security (https) -->
            <!-- <dependency> -->
            <!-- <groupId>org.springframework.security</groupId> -->
            <!-- <artifactId>spring-security-core</artifactId> -->
            <!-- <version>${spring-security-version}</version> -->
            <!-- </dependency> -->
            <!-- <dependency> -->
            <!-- <groupId>org.springframework.security</groupId> -->
            <!-- <artifactId>spring-security-web</artifactId> -->
            <!-- <version>${spring-security-version}</version> -->
            <!-- </dependency> -->
            <!-- <dependency> -->
            <!-- <groupId>org.springframework.security</groupId> -->
            <!-- <artifactId>spring-security-config</artifactId> -->
            <!-- <version>${spring-security-version}</version> -->
            <!-- </dependency> -->
    
            <!-- AspectJ -->
            <dependency>
                <groupId>org.aspectj</groupId>
                <artifactId>aspectjrt</artifactId>
                <version>${aspectj-version}</version>
            </dependency>
            <!-- aop-Logging 사용관련 -->
            <dependency>
                <groupId>org.aspectj</groupId>
                <artifactId>aspectjweaver</artifactId>
                <version>${aspectj-version}</version>
            </dependency>
    
            <!-- Logging -->
            <dependency>
                <groupId>org.slf4j</groupId>
                <artifactId>slf4j-api</artifactId>
                <version>${slf4j-version}</version>
            </dependency>
            <dependency>
                <groupId>org.slf4j</groupId>
                <artifactId>jcl-over-slf4j</artifactId>
                <version>${slf4j-version}</version>
                <scope>runtime</scope>
            </dependency>
    
            <!-- logback -->
            <dependency>
                <groupId>ch.qos.logback</groupId>
                <artifactId>logback-core</artifactId>
                <version>${logback-version}</version>
            </dependency>
            <dependency>
                <groupId>ch.qos.logback</groupId>
                <artifactId>logback-classic</artifactId>
                <version>${logback-version}</version>
            </dependency>
    
            <!-- sql log util -->
            <dependency>
                <groupId>org.jdbcdslog</groupId>
                <artifactId>jdbcdslogexp2</artifactId>
                <version>${jdbcdslogexp2-version}</version>
            </dependency>
            <!-- Sql formatter -->
            <dependency>
                <groupId>studio.raptor</groupId>
                <artifactId>ddal-sqlparser</artifactId>
                <version>${ddal-sqlparser-version}</version>
            </dependency>
    
            <!-- gson -->
            <dependency>
                <groupId>com.google.code.gson</groupId>
                <artifactId>gson</artifactId>
                <version>${gson-version}</version>
            </dependency>
    
            <!-- Joda Time -->
            <dependency>
                <groupId>joda-time</groupId>
                <artifactId>joda-time</artifactId>
                <version>${joda-time-version}</version>
            </dependency>
    
            <!-- For StopWatch, ExceptionUtils, StringUtils -->
            <dependency>
                <groupId>org.apache.commons</groupId>
                <artifactId>commons-lang3</artifactId>
                <version>${lang3-version}</version>
            </dependency>
    
            <!-- myBatis -->
            <dependency>
                <groupId>org.mybatis</groupId>
                <artifactId>mybatis</artifactId>
                <version>${mybatis-version}</version>
            </dependency>
            <dependency>
                <groupId>org.mybatis</groupId>
                <artifactId>mybatis-spring</artifactId>
                <version>${mybatis-spring-version}</version>
            </dependency>
    
            <!-- db connection pool 이용 -->
            <dependency>
                <groupId>com.zaxxer</groupId>
                <artifactId>HikariCP</artifactId>
                <version>${HikariCP-version}</version>
            </dependency>
            <!-- jdbc -->
            <dependency>
                <groupId>oracle.jdbc</groupId>
                <artifactId>jdbc</artifactId>
                <version>12.2.0.1</version>
                <scope>system</scope>
                <systemPath>${project.basedir}/src/main/webapp/WEB-INF/lib/ojdbc8.jar</systemPath>
            </dependency>
    
            <!-- 파일 검증(확장자, MimeType) -->
            <dependency>
                <groupId>org.apache.tika</groupId>
                <artifactId>tika-core</artifactId>
                <version>${tika-version}</version>
            </dependency>
            <dependency>
                <groupId>commons-io</groupId>
                <artifactId>commons-io</artifactId>
                <version>${common-io-version}</version>
            </dependency>
    
            <!-- 암호화관련(Base64, AES..) -->
            <dependency>
                <groupId>commons-codec</groupId>
                <artifactId>commons-codec</artifactId>
                <version>${commons-codec-version}</version>
            </dependency>
    
            <!-- Test -->
            <dependency>
                <groupId>org.junit.jupiter</groupId>
                <artifactId>junit-jupiter-engine</artifactId>
                <version>${junit-version}</version>
                <scope>test</scope>
            </dependency>
            <dependency>
                <groupId>org.mockito</groupId>
                <artifactId>mockito-core</artifactId>
                <version>${mockito-version}</version>
                <scope>test</scope>
            </dependency>
            <dependency>
                <groupId>org.hamcrest</groupId>
                <artifactId>hamcrest-all</artifactId>
                <version>${hamcrest-version}</version>
                <scope>test</scope>
            </dependency>
    
            <!-- gzip compress filter -->
            <dependency>
                <groupId>com.github.ziplet</groupId>
                <artifactId>ziplet</artifactId>
                <version>${ziplet-version}</version>
            </dependency>
    
            <!-- @Inject -->
            <dependency>
                <groupId>javax.inject</groupId>
                <artifactId>javax.inject</artifactId>
                <version>1</version>
            </dependency>
    
            <!-- Servlet -->
            <dependency>
                <groupId>javax.servlet</groupId>
                <artifactId>javax.servlet-api</artifactId>
                <version>${servlet-api-version}</version>
                <scope>provided</scope>
            </dependency>
            <dependency>
                <groupId>javax.servlet.jsp</groupId>
                <artifactId>javax.servlet.jsp-api</artifactId>
                <version>${servlet.jsp-api-version}</version>
                <scope>provided</scope>
            </dependency>
            <dependency>
                <groupId>javax.servlet</groupId>
                <artifactId>jstl</artifactId>
                <version>${jstl-version}</version>
            </dependency>
    
            <!-- XSS Filter -->
            <dependency>
                <groupId>com.navercorp.lucy</groupId>
                <artifactId>lucy-xss</artifactId>
                <version>${lucy-version}</version>
            </dependency>
    
            <!-- Create Excel -->
            <dependency>
                <groupId>org.apache.poi</groupId>
                <artifactId>poi</artifactId>
                <version>${poi-version}</version>
            </dependency>
            <dependency>
                <groupId>org.apache.poi</groupId>
                <artifactId>poi-ooxml</artifactId>
                <version>${poi-version}</version>
            </dependency>
    
            <!-- Create Pdf -->
            <dependency>
                <groupId>org.apache.pdfbox</groupId>
                <artifactId>pdfbox</artifactId>
                <version>${pdfbox-version}</version>
            </dependency>
            <dependency>
                <groupId>com.github.dhorions</groupId>
                <artifactId>boxable</artifactId>
                <version>${boxable-version}</version>
            </dependency>
    
            <!-- 임시DB h2 -->
            <dependency>
                <groupId>com.h2database</groupId>
                <artifactId>h2</artifactId>
                <version>${h2database-version}</version>
            </dependency>
    
            <!-- 여기까지 표준프레임워크에서 정의한 library -->
            <!-- 여기까지 표준프레임워크에서 정의한 library -->
            <!-- 여기까지 표준프레임워크에서 정의한 library -->
    
        </dependencies>
    
        <profiles>
            <profile>
                <id>local</id>
                <properties>
                    <resources>resources-local</resources>
                </properties>
                <activation>
                    <activeByDefault>true</activeByDefault>
                </activation>
            </profile>
            <profile>
                <id>dev</id>
                <properties>
                    <maven.test.skip>true</maven.test.skip>
                    <is.dual.server>false</is.dual.server>
                    <resources>resources-dev</resources>
                    <ftp.serverIp1>111.222.111.222</ftp.serverIp1>
                    <ftp.path>/data1/services/project/docbase</ftp.path>
                    <ftp.id>username</ftp.id>
                    <ftp.passwd>password</ftp.passwd>
                    <tomcat.home>/tomcat8</tomcat.home>
                    <tomcat.id>wasadmin</tomcat.id>
                    <tomcat.passwd>TLSEKD!tpsxjwas</tomcat.passwd>
                </properties>
            </profile>
            <profile>
                <id>real</id>
                <properties>
                    <maven.test.skip>true</maven.test.skip>
                    <is.dual.server>false</is.dual.server>
                    <resources>resources-real</resources>
                    <ftp.serverIp1>111.222.111.222</ftp.serverIp1>
                    <ftp.serverIp2>111.222.111.222</ftp.serverIp2>
                    <ftp.path>/data1/services/project/docbase</ftp.path>
                    <ftp.id>username</ftp.id>
                    <ftp.passwd>password</ftp.passwd>
                </properties>
            </profile>
        </profiles>
    
        <build>
            <finalName>ROOT</finalName>
            <resources>
                <resource>
                    <directory>${project.basedir}/src/main/java</directory>
                    <includes>
                        <include>**/*Mapper.xml</include>
                    </includes>
                </resource>
                <resource>
                    <directory>${project.basedir}/src/main/resources</directory>
                </resource>
                <resource>
                    <directory>${project.basedir}/src/main/${resources}</directory>
                </resource>
            </resources>
    
            <plugins>
                <plugin>
                    <artifactId>maven-eclipse-plugin</artifactId>
                    <version>${maven-eclipse-plugin-version}</version>
                    <configuration>
                        <additionalProjectnatures>
                            <projectnature>org.springframework.ide.eclipse.core.springnature</projectnature>
                        </additionalProjectnatures>
                        <additionalBuildcommands>
                            <buildcommand>org.springframework.ide.eclipse.core.springbuilder</buildcommand>
                        </additionalBuildcommands>
                        <downloadSources>true</downloadSources>
                        <downloadJavadocs>true</downloadJavadocs>
                    </configuration>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-compiler-plugin</artifactId>
                    <version>${maven-compiler-plugin-version}</version>
                    <configuration>
                        <source>${java-version}</source>
                        <target>${java-version}</target>
                        <compilerArgument>-proc:none</compilerArgument>
                        <!-- <debug>true</debug> -->
                        <showWarnings>true</showWarnings>
                        <showDeprecation>true</showDeprecation>
                    </configuration>
                </plugin>
                <plugin>
                    <groupId>org.codehaus.mojo</groupId>
                    <artifactId>exec-maven-plugin</artifactId>
                    <version>${exec-maven-plugin-version}</version>
                    <configuration>
                        <mainClass>org.test.int1.Main</mainClass>
                    </configuration>
                </plugin>
                <plugin>
                    <groupId>org.apache.maven.plugins</groupId>
                    <artifactId>maven-war-plugin</artifactId>
                    <version>${maven-war-plugin-version}</version>
                    <!--				<configuration>-->
                    <!--					<warSourceExcludes>%regex[resources/(?!inc/).*]</warSourceExcludes>-->
                    <!--				</configuration>-->
                </plugin>
                <!-- 배포 플러그인 -->
                <!--			<plugin>-->
                <!--				<groupId>org.apache.maven.plugins</groupId>-->
                <!--				<artifactId>maven-antrun-plugin</artifactId>-->
                <!--				<version>${maven-antrun-plugin-version}</version>-->
                <!--				<configuration>-->
                <!--					<tasks>-->
                <!--						<taskdef resource="net/sf/antcontrib/antlib.xml" />-->
    
                <!--						<echo>war deploy #1 start</echo>-->
                <!--						<scp file="${project.build.directory}/ROOT.war" todir="${ftp.id}@${ftp.serverIp1}:${ftp.path}" password="${ftp.passwd}" trust="true" sftp="true" filemode="777" dirmode="777" />-->
                <!--						<echo>war deploy #1 finish</echo>-->
    
                <!--						<if>-->
                <!--							<equals arg1="${resources}" arg2="resources-dev" />-->
                <!--							<then>-->
                <!--								<echo>tomcat #1 Restart start</echo>-->
                <!--								<sshexec host="${ftp.serverIp1}" trust="yes" username="${tomcat.id}" password="${tomcat.passwd}" timeout="20000" failonerror="false"-->
                <!--									command="${tomcat.home}/bin/shutdown.sh; sleep 10; rm -rf ${ftp.path}/ROOT/; sleep 3; ${tomcat.home}/bin/startup.sh" />-->
                <!--								<echo>tomcat #1 Restart finish</echo>-->
                <!--							</then>-->
                <!--							<else>-->
                <!--								<echo>Skip to Restart tomcat #1 in "real" enviroment</echo>-->
                <!--							</else>-->
                <!--						</if>-->
                <!--						<if>-->
                <!--							<equals arg1="${is.dual.server}" arg2="true" />-->
                <!--							<then>-->
                <!--								<echo>war deploy #2 start</echo>-->
                <!--								<scp file="${project.build.directory}/ROOT.war" todir="${ftp.id}@${ftp.serverIp2}:${ftp.path}" password="${ftp.passwd}" trust="true" sftp="true" filemode="777" dirmode="777" />-->
                <!--								<echo>war deploy #2 finish</echo>-->
                <!--								<if>-->
                <!--									<equals arg1="${resources}" arg2="resources-dev" />-->
                <!--									<then>-->
                <!--										<echo>tomcat #2 Restart start</echo>-->
                <!--										<sshexec host="${ftp.serverIp2}" trust="yes" username="${tomcat.id}" password="${tomcat.passwd}" timeout="20000" failonerror="false"-->
                <!--											command="${tomcat.home}/bin/shutdown.sh; sleep 10; rm -rf ${ftp.path}/ROOT/; sleep 3; ${tomcat.home}/bin/startup.sh" />-->
                <!--										<echo>tomcat #2 Restart finish</echo>-->
                <!--									</then>-->
                <!--									<else>-->
                <!--										<echo>Skip to Restart tomcat #2 in "real" enviroment</echo>-->
                <!--									</else>-->
                <!--								</if>-->
                <!--							</then>-->
                <!--							<else></else>-->
                <!--						</if>-->
                <!--					</tasks>-->
                <!--				</configuration>-->
                <!--				<executions>-->
                <!--					<execution>-->
                <!--						<phase>install</phase>-->
                <!--						<goals>-->
                <!--							<goal>run</goal>-->
                <!--						</goals>-->
                <!--					</execution>-->
                <!--				</executions>-->
                <!--				<dependencies>-->
                <!--					<dependency>-->
                <!--						<groupId>org.apache.ant</groupId>-->
                <!--						<artifactId>ant</artifactId>-->
                <!--						<version>${org.apache.ant-version}</version>-->
                <!--					</dependency>-->
                <!--					<dependency>-->
                <!--						<groupId>org.apache.ant</groupId>-->
                <!--						<artifactId>ant-jsch</artifactId>-->
                <!--						<version>${org.apache.ant-version}</version>-->
                <!--					</dependency>-->
                <!--					<dependency>-->
                <!--						<groupId>com.jcraft</groupId>-->
                <!--						<artifactId>jsch</artifactId>-->
                <!--						<version>${jsch-version}</version>-->
                <!--					</dependency>-->
                <!--					<dependency>-->
                <!--						<groupId>ant-contrib</groupId>-->
                <!--						<artifactId>ant-contrib</artifactId>-->
                <!--						<version>${ant-contrib-version}</version>-->
                <!--					</dependency>-->
                <!--				</dependencies>-->
                <!--			</plugin>-->
            </plugins>
        </build>
    </project>


## The default log of the framework

> 프레임워크의 기본 로그

	14:56:39.730 [INFO ] com.mycompany.standard.context.logging.MyRequestLoggingFilter.beforeRequest(22) === <GET>/sample/admin/member/adminMember.view, parameters={}
	14:56:39.731 [INFO ] Interceptor.preHandle(RequestFacade, CompressingHttpServletResponse, HandlerMethod) START ....... Execute Time ....... : 00:00:00.000
	14:56:39.731 [INFO ] Interceptor.preHandle(RequestFacade, CompressingHttpServletResponse, HandlerMethod) E N D ....... Execute Time ....... : 00:00:00.000 - return Value(boolean) : true
	14:56:39.731 [INFO ] AdminMemberController.view() START ....... Execute Time ....... : 00:00:00.000
	14:56:39.732 [INFO ] AdminMemberController.view() E N D ....... Execute Time ....... : 00:00:00.000 - return Value(String) : "/sample/admin/member/AdminMember"
	14:56:39.757 [INFO ] com.mycompany.standard.common.interceptor.Interceptor.afterCompletion(71) === /sample/admin/member/adminMember.view ....... Request Complete Execute Time(include JSP) viewName : /sample/admin/member/AdminMember ....... : 00:00:00.025

## Added work (View detail url: [https://blog.naver.com](https://blog.naver.com/PostList.nhn?blogId=bestheroz&from=postList&categoryNo=92))

> 추가된 작업 (상세보기 url: [https://blog.naver.com](https://blog.naver.com/PostList.nhn?blogId=bestheroz&from=postList&categoryNo=92))

1. Communication between the server and the client treats the java.util.Date type as a Long(timestamp) value.
 
 > 서버와 클라이언트 간 통신에서 java.util.Date형 을 Long(Time Stamp) 값으로 처리.

2. added trace-log.

 > 추적로그를 추가하였습니다.
 
3. Variable-bound DB SQL Logging.
 
 > 변수 바인딩된 DB SQL 로그 남기기.
  
4. Automatic generation of SQL using @SelectProvider, @InsertProvider, @UpdateProvider, @DeleteProvider.
 
 > @SelectProvider, @InsertProvider, @UpdateProvider, @DeleteProvider 을 이용한 SQL 자동생성.
 
5. java.util.Date -> org.joda.time.LocalDateTime

## Add in the future.. Give feedback. :)

> 향후 추가될.. 의견주세요 :)

 1. ....
 
 2. ....
 
 3. ....
 
 
