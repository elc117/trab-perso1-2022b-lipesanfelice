![Spring](https://www.educative.io/v2api/editorpage/5669828520574976/image/6296864620544000)

# Spring Framework
* O Spring é um framework Java criado com o objetivo de facilitar o desenvolvimento de aplicações, explorando, para isso, os conceitos de Inversão de Controle e Injeção de Dependências (uma das maneiras de implementar a Inversão de Controle). Dessa forma temos uma tecnologia que nos fornece recursos necessários à grande parte das aplicações, como módulos para persistência de dados, integração, segurança, testes, desenvolvimento web, como também nos permite criar soluções menos acopladas, mais coesas e, consequentemente, mais fáceis de compreender e manter.
* A Inversão de Controle permite delegar a outro elemento o controle sobre como e quando um objeto deve ser criado e quando um método deve ser executado, por exemplo. Assim o controle sobre a execução de alguns comportamentos, passa a ser gerenciado por esse elemento, não cabendo mais aos programadores.
* Com a Injeção de Dependência a classe deixa de se preocupar em como resolver as suas dependências. Ela passa a manter o foco apenas no uso dos recursos das dependências para realizar as tarefas que precisa. E isso leva a uma das características mais conhecidas quando programamos com Spring: não precisamos utilizar o new para criar os objetos por ele gerenciados, pois isso passa a ser feito pelo framework.
Esse framework oferece diversos módulos que podem ser utilizados de acordo com as necessidades do projeto, como módulos voltados para desenvolvimento Web, persistência, acesso remoto e programação orientada a aspectos, um breve resumo dos principais módulos estará logo abaixo na decorrência do texto.

## Spring Boot
* O Spring Boot busca solucionar a complexidade da inicialização e gerenciamento de dependências de um projeto com Spring, além de tratar de maneira coesa e eficiente a questão da configuração, fazendo uso extensivo de Convention Over Configuration.
* Pode ser considerado um plugin para a ferramenta de building, seja ela o Maven ou o Gradle. Seus principais objetivos são gerenciar dependências de maneira opinativa e automática, e simplificar a execução do projeto em tempo de desenvolvimento e depuração.
* Possui a funcionalidade de empacotamento da sua aplicação em um JAR executável contendo todas as dependências necessárias, inclusive o Servlet Container, seja ele o Tomcat, Jetty ou mesmo Undertow, apesar de ainda ser possível empacotar um WAR da forma tradicional.
* O principal benefício do Boot, entretanto, é a configuração de recursos baseada no que se encontra no classpath. Se o POM de seu Maven inclui a dependência do JPA e o driver do PostgreSQL, ele irá criar uma unidade de persistência baseada no PostgreSQL.

## Spring Data
* A missão da Spring Data é fornecer um modelo de programação familiar e consistente baseado em Spring para acesso a dados, mantendo as características especiais do armazenamento de dados subjacente.
* Ele facilita o uso de tecnologias de acesso a dados, bancos de dados relacionais e não relacionais, estruturas de redução de mapas e serviços de dados baseados em nuvem. Este é um projeto guarda-chuva que contém muitos subprojetos específicos para um determinado banco de dados. Em suma ele disponibiliza os métodos necessários para realizar as operações de CRUD (Create, Read, Update e Delete) no banco de dados, além também de disponibilizar buscas utilizando ordenação e paginação.
* Dentro do Spring Data podemos encontrar frameworks como o Spring Data JDBC que facilita realizar operações no banco de dados utilizando a JDBC (Java Database Connectivity), temos também o Spring Data MongoDB que provê integração com o banco de dados NoSQL MongoDB, o Spring Data JPA que facilita o uso da JPA (Java Persistence API) dentro de aplicações Spring.

## Spring Cloud
* Fornece ferramentas para desenvolvedores criarem rapidamente alguns dos padrões comuns em sistemas distribuídos (por exemplo, gerenciamento de configuração, descoberta de serviço, disjuntores, roteamento inteligente, micro-proxy, barramento de controle, tokens únicos, bloqueios globais, eleição de liderança, distribuição sessões, estado do cluster). A coordenação de sistemas distribuídos leva a padrões padronizados então os desenvolvedores podem criar rapidamente serviços e aplicativos que implementam esses padrões. Eles funcionarão bem em qualquer ambiente distribuído, incluindo o próprio laptop do desenvolvedor, centros de dados bare metal e plataformas gerenciadas como o Cloud Foundry.

## Spring Security
* Um dos pontos cruciais durante o desenvolvimento de uma aplicação web é a sua segurança, a todo momento existem novas técnicas de invasão e formas da segurança de sua aplicação ser quebrada.
* É bem comum terceirizarmos as implementações de segurança de nossas aplicações para bibliotecas ou frameworks que foram desenvolvidas por especialistas na área de segurança e por conta disso que neste artigo iremos falar sobre o Spring Security.
* O Spring Security é uma biblioteca que fornece proteção, mas também autenticação, autorização e armazenamento de senhas. Sendo que trabalha com vários protocolos para autenticação. Para armazenar senhas em um banco de dados, ele tem opção de vários encoders. Também é possível utilizá-lo em projetos com Java EE, Spring Webflux, e Kotlin. Além disso, ele protege de ataques mais comuns como CSRF ou XSS.
* É uma estrutura que se concentra em fornecer autenticação e autorização para aplicativos Java. Como todos os projetos Spring, o poder real do Spring Security é encontrado na facilidade com que ele pode ser estendido para atender aos requisitos personalizados.

## Spring Web Flow
* Permite implementar os "fluxos" de um aplicativo da web. Um fluxo encapsula uma sequência de etapas que orientam um usuário durante a execução de alguma tarefa de negócios. Ele abrange várias solicitações HTTP, tem estado, lida com dados transacionais, é reutilizável e pode ser dinâmico e de longa duração por natureza.
* O ponto ideal para o Spring Web Flow são os aplicativos da Web com estado com navegação controlada, como check-in para um voo, solicitação de empréstimo, check-out do carrinho de compras ou até mesmo adicionar uma etapa de confirmação a um formulário.
* O Spring Web Flow fornece uma linguagem de definição de fluxo declarativa para fluxos de autoria em um nível mais alto de abstração. Ele permite que seja integrado a uma ampla gama de aplicativos sem nenhuma alteração (no modelo de programação de fluxo), incluindo Spring MVC, JSF e até mesmo aplicativos da Web de Portlet. 

## Spring MVB
* O Spring MVC é um framework que nos auxilia no desenvolvimento de aplicações web. Com ele, nós conseguimos ter facilidade e flexibilidade para trabalhar com requisições web.
* O Spring MVC é uma excelente implementação do padrão MVC. De forma resumida, MVC (acrônimo para Model-View-Controller) sugere uma maneira para você pensar na divisão de responsabilidades, principalmente dentro de um software web, dividindo as camadas em model, view, controller. Com ele podemos separar o código relativo à interface do usuário das regras de negócio.
* Ele já possui as principais funcionalidades que precisamos para o desenvolvimento: atender as requisições HTTP, delegar responsabilidades de processamento de dados para outros componentes e preparar as respostas HTTP, trabalha de forma síncrona, ou seja, processa requisições uma a uma, por ordem de chegada. Enquanto uma requisição não for finalizada, ele não processa a seguinte.

# Explicando exemplo deixado no GitHub
* O código tem o objetivo de mostrar como são implementadas algumas das funcionalidades dos modulos do spring framework, o exemplo foi retirado de um site e foi estudado, juntamente com outros exemplos, mas esse englobou alguns detalhes que me pareceram pertinentes e foram realizadas algumas modificações ao longo do estudo para entender melhor o comportamento do Spring Framework e como funcionavam os seus módulos, o que está totalmente de acordo o que eu havia proposto. Com os meus estudos criei o ApiService.java que consiste em uma adição que achei pertinente ao código, fiz isso com a intenção de completar as suas funcionalidades, mas logo falarei mais dela.
* O código consiste basicamente na criação de um API  é um conjunto de definições e protocolos usado no desenvolvimento e na integração de aplicações, utilizando alguns módulos do Spring Framework. O código faz um uso maior do Spring Boot, mas podemos observar alguns outros módulos do spring framework como o spring Data e o Spring Security.
* A adição que fiz foi criar o ApiService que consiste na implementação de um crud utilizando o spring Boot que aprendi em alguns tutorias que vi pela internet, com o objetivo de verificar se todos os métodos da classe pessoa estão funcionando (create, update, delete, post). Ele realiza a obtenção de todos os registros de usuários usando o método findAll(), obtenção de um registro específico usando o método findById(), salvando um registro específico usando o método save(), excluindo um registro específico usando o método deleteById() e atualiza um registro.
* Olhando para pasta security nós percebemos os diferentes papeis do Spring security, pois percebemos um processo de filtragem das informações e configurações dos métodos de autenticação e autorização. Podemos perceber a essência do Spring Security, pois nos textos acima é citado a função de armazenar senhas em banco de dados e ele é utilizado pra isso nesse programa e também claro para a parte de autenticação e autorização, pois estamos trabalhando com usuário e senha como forma de acessar o programa. 
* O Spring Boot reconhece como componentes da aplicação, todas as classes definidas no mesmo pacote da classe que contém o método main ou em um package “abaixo” do package, ou seja, como a classe está definida no pacote br.com.treinaweb.springbootapiexemplo, qualquer classe definida nele ou em um “subpackage” dele, será reconhecida pelo Spring Boot.
* As configurações do banco de dados estão no arquivo application.properties. Vale ressaltar que algumas modificações do Spring Boot podem ser feitas nesse arquivo, porém é recomendável manter somente as configurações do banco de dados se a experiência do programador com spring não for muito ampla.
* O arquivo pom. xml que contém o starter web e das dependências que foram definidas é considerado o coração de um projeto Maven. Com a configuração de poucos descritores é possível gerenciar dependências, centralizar documentação sobre o projeto e principalmente compilar e distribuir uma aplicação.
* O arquivo DemoApplication.java contém o nosso método main e este método será responsável por carregar todas dependências embutidas na aplicação, isso inclui o servidor web. Desta forma, para esta aplicação web não é necessário definir um arquivo war e adicioná-lo no servidor.
* Para criar o repositório foi necessário apenas estender da interface JpaRepository do Spring Data.

# Motivação
* Escolhi me aprofundar nesse assunto, pois sempre foi um interesse pessoal algum dia trabalhar com aplicativos ou sistemas grandes e nas minhas pesquisas eu descobri que o spring é utilizado por empresas como Netflix, Amazon e Ebay que são grandes, participam do meu cotidiano e eu já tinha um certo interesses em conhecer alguns métodos e ferramentas que eles usam. Outro motivo foi fato do Spring facilitar muito a programação por conta de todos os seus módulos que abrangem diversas áreas, isso me despertou o interesse, pois eu gostei de programar em java só que as vezes buscando tutoriais na internet eu achava os exemplos de código muito difíceis pela quantidade de informação e com os exemplos usando spring eu sinto que entendi melhor algumas funcionalidades.

# Referencias
* [Devemedia](https://www.devmedia.com.br)
* [Alura](https://www.alura.com.br)
* [GeekHunter](https://blog.geekhunter.com.br)
* [TreinaWeb](https://www.treinaweb.com.br)
* https://www.youtube.com/watch?v=JayflBOmTQQ
* https://www.devmedia.com.br/introducao-ao-spring-framework/26212 
* https://www.youtube.com/watch?v=gq4S-ovWVlM
* https://www.youtube.com/watch?v=Va3f_Yfsx5c
* https://www.youtube.com/watch?v=If1Lw4pLLEo
