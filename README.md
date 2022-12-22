# Projeto RPG :snowflake: 

### Plataforma para jogar RPG com amigos.

<p align="center">
  <img src="https://media.tenor.com/i2AeJZKldpUAAAAC/pen-pen-evangelion.gif" />
</p>

# Arquitetura e Stack :tiger:
Feito com um conjunto de serviços estruturados em uma arquitetura de microsserviços e orientado a eventos 

Os serviços estão organizados em arquitetura de camadas hexagonal, clique para ver o [modelo](https://user-images.githubusercontent.com/86073233/209199986-478711fc-afd2-47ae-8887-4e2a700dc5f9.png).    
  
  
> ## Detalhes de stack   
> ***A implementação do serviço de autenticação é feita em [Java 17](https://docs.oracle.com/en/java/javase/17/) usando [Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/).*** 
> - A persistência de dados deste serviço é feita em um banco relacional [MySQL](https://dev.mysql.com/doc/). [Modelo de Dados]()  
> 
> ***A implementação do serviço de sessões é feita em [JavaScript](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript) usando [NodeJS](https://nodejs.org/en/docs/).***  
> - A persistência de dados deste serviço é feita em um banco não relacional [MongoDB](https://www.mongodb.com/docs/). [Modelo de Dados](). 
>  
> ***Os serviços estão integrados a um message broker, implementado com [RabbitMQ](https://www.rabbitmq.com/documentation.html).***  
> 
> No Front-end será usada as seguintes tecnologias:
> - HTML
> - CSS com Sass, Tailwind
> - JS com React  
> ***[Bibliotecas Usadas]()***

# Desenvolvimento :whale2: 

## Regras de Negócio :mailbox:

### Cadastramento
> Para se cadastrar o usuário deverá informar o seu email.  
> Caso o email seja verificado o usuário poderá informar o seu nome, o seu apelido, o seu avatar, sua senha e opcionalmente seu número de celular.

### Login
> Para se logar o usuário deverá informar o seu apelido ou email e sua senha.  
Caso a autenticação de duas fatores esteja ativada o usuário receberá um código pelo celular ou email para seguir no sistema.

### Amigos e Mensagens
> Todo usuário cadastrado pode ter amigos e enviar mensagens ou convites de jogos.  
Para adicionar um amigo deverá informar o seu apelido.

### Personagens
> O usuário pode deixar personagems criados para poder entrar em jogos novos.  
Cada personagem tem seu avatar próprio e ficha com história e atributos

### Jogo
> O usuário pode entrar em um jogo já em andamento ou novo.   
Para entrar no jogo o usuário deverá ter um personagem criado

### Criação de Jogo
> O usuário pode criar um jogo como mestre.  
Para criar será necessário escolher o livro de regras e as configurações específicas.

### Sessões
> O usuário pode entrar em sessões de jogos do qual foi convidado independendente se a sessão está fechada ou não.   
Se a sessão estiver fechada o usuário será limitado na sessão podendo apenas editar seu personagem.

## Estudo de Caso :symbols:

![image](https://user-images.githubusercontent.com/86073233/209179978-bb23657a-1c26-4b5c-9465-fd0057764349.png)

