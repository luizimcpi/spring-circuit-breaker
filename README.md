# spring-circuit-breaker

Exemplo de arquitetura de micro serviço configurada com spring que utiliza o circuit breaker (Hystrix - Netflix)

Requirements:
```
Maven
JDK 8
```
Primeiro
```
Na IDE de preferência -> Run as EurekaServerApplication.java
```
Segundo
```
Na IDE de preferência -> Run as BookStoreAppApplication.java
```
Terceiro
```
Na IDE de preferência -> Run as ReadingAppApplication.java ou execute mvn spring-boot:run d root directory of the application
```
ou
```
Execute o comando -> mvn spring-boot:run dentro do diretório de cada aplicação através do terminal
```

Acessar o Dashboard do Hystrix
```
http://localhost:8080/hystrix
Preencha a URL solicitada com:
http://localhost:8080/hystrix.stream
```
Requests de Exemplo (Executar no POSTMAN ou INSOMNIA):
```
Primeiro request: http://localhost:8080/to-read
```
```
Segundo request http://localhost:8080/to-buy
```

* Faça as requests normalmente com todos os serviços no ar, após verificar que está tudo funcionando, derrube a aplicação BookStoreAppApplication e comece as requests novamente após 20 tentativas o circuito irá abrir (open) você poderá confirmar isso através do dashboard do Hystrix.


