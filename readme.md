<div align="center">
  <h1>TDD Testes Unitários com MOCKITO>
  <p>
	 Um app simples para aplicar-mos os testes Unitários🤿 ☕ <br>
	  Desenvolvido com 💙 por Jefferson Cesar de Souza.<br>
	  Como Portifólio em meu Git
  </p>
</div>

## ⚙️ Funcionalidades 


## 🛠️ Tecnologias utilizadas

- Java 1.8
- Spring Boot Starter Web com thymeleaf, Springsecurity5, 
thymeleaf-extras-java8time, spring-boot-starter-data-jpa

>> Banco de dados h2database para testes apenas.

- App será feito em Java 1.8 utilizando Maven e Selenium para os Testes

>> Banco de Dados local ( ainda estou decidindo )



## 🖥️ Application.properties

#### Configurações properties
````
# datasource
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.url=jdbc:h2:mem:leiloes
spring.datasource.username=sa
spring.datasource.password=

# jpa
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=create-drop
````

#### Arquivo data.sql para banco automático
````
INSERT INTO `users` (`user_id`, `email`, `enabled`, `username`, `role`, `password`) VALUES
(1,	'fulano@gmail.com',	1,	'fulano',	'USER',	'$2a$10$8MeF8YTUTv22DVthkhOs3.WGT4W1Wp1xRXcRxTM12MgDzRviDpw7i'),
(2,	'ciclano@gmail.com',	1,	'ciclano',	'USER',	'$2a$10$8MeF8YTUTv22DVthkhOs3.WGT4W1Wp1xRXcRxTM12MgDzRviDpw7i'),
(3,	'beltrano@gmail.com',	1,	'beltrano',	'USER',	'$2a$10$8MeF8YTUTv22DVthkhOs3.WGT4W1Wp1xRXcRxTM12MgDzRviDpw7i');

INSERT INTO `leilao` (`id`, `data_abertura`, `nome`, `valor_inicial`, `usuario_user_id`) VALUES
(1,	'2020-08-03',	'Tablet Xpto 3',	5.00,	1),
(2,	'2020-08-03',	'Computador Z3',	500.00,	3);

INSERT INTO `lance` (`id`, `data`, `valor`, `leilao_id`, `usuario_user_id`) VALUES
(1,	'2020-08-04',	10.00,	1,	3),
(2,	'2020-08-04',	15.00,	1,	2);
````

#### Arquivo pom.xml
````
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.3.1.RELEASE</version>
		<relativePath /> <!-- lookup parent from repository -->
	</parent>
	<groupId>br.com.alura</groupId>
	<artifactId>leilao</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>leilao</name>

	<properties>
		<maven.compiler.version>3.8.1</maven.compiler.version>
		<maven.surefire.version>2.22.1</maven.surefire.version>
		<java.version>1.8</java.version>
	</properties>

	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-thymeleaf</artifactId>
		</dependency>
		<dependency>
			<groupId>org.thymeleaf.extras</groupId>
			<artifactId>thymeleaf-extras-springsecurity5</artifactId>
		</dependency>

		<dependency>
			<groupId>org.thymeleaf.extras</groupId>
			<artifactId>thymeleaf-extras-java8time</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-validation</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-security</artifactId>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-devtools</artifactId>
			<scope>runtime</scope>
			<optional>true</optional>
		</dependency>

		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>

		<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<configuration>
					<encoding>UTF-8</encoding>
					<source>${java.version}</source>
					<target>${java.version}</target>
				</configuration>
			</plugin>
		</plugins>
	</build>

</project>
````

Configurar:

#### Variáveis de memória
````
-Dspring.profiles.active=test
````


## 📒 Conteúdos  

**Testes Automatizados**: [Com Selenium](https://github.com/JeffeDev)

**FrontEnd**: Bootstrap e Thymeleaf 




## 🎯 O que o projeto faz:
  - [X] Aplicação de testes unitários



## 📸 Screenshots
####  📌 Selenium




## ❔ Dúvidas?!
Se tiver alguma dúvida sobre este repositório, envie para jeffe.info@gmail.com




