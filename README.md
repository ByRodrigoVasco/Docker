# O que é o Docker?

Para responder essa pergunta primeiro, você precisa entender o que são Containers.

## Container


Containers são tipo uma máquina virtual, tem o sistema operacional e tudo mais, só que, diferente das máquinas virtuais, eles não simulam o computador inteiro, mas sim criam um ambiente isolado que finge ser uma máquina virtual.

Geralmente, esses containers também rodam a versão mais enxuta possível do software. Teoricamente, você pode instalar um sistema operacional como o Ubuntu com tudo que tem direito em um container, mas o que os profissionais costumam fazer é construir uma versão mais leve do sistema operacional, que só faz uma coisa.

É uma unidade padrão de software que empacotam componentes de software em um sistema de arquivos completo, que contem TUDO necessário para a execução: códito, runtime, ferramentas de sistema - qualquer coisa que possa ser instalada em um servidor. isso garante que o software sempre irá executar da mesma forma, independente do seu ambiente.

### Caracterizando um container

Um container será um ambiente de virtualização

* Com menos consumo de processamento
* Com menor custo de manutenção e configuração
* Com menor tempo de inicialização e finalização

![ImageContainers](assets/images/imageContainer.png)

Contêiner: instância de uma imagem do docker

## Docker

Docker é uma forma de construir e rodar esses containers, salvar em templates, etc...

Ele é uma plataforma de código aberto que usa contêiners para empacotar aplicações e suas dependências, garantindo que elas sejam executadas de forma consistente em qualquer ambiente. O Docker permite que os desenvolvedores criem, testem e implantem aplicativos de maneira rápida e eficiente, independentemente do sistema operacional ou infraestrutura subjacente.


![ImageDocker](assets/images/imageDocker.png)

* ### Client - interface de linha de comando para interagir com o docker host

 Os comandos do Docker são usados para criar, gerenciar e interagir com contêineres e imagens. Eles permitem que os desenvolvedores construam, testem e implantem aplicativos de maneira rápida e eficiente, independentemente do sistema operacional ou infraestrutura subjacente.


* ### Docker Host - onde os containers rodam

O docker host é o ambiente onde os contêineres são executados. Ele pode ser um servidor físico, uma máquina virtual ou um serviço de nuvem. O Docker host é responsável por gerenciar os recursos do sistema e garantir que os contêineres sejam executados de forma eficiente.

* ### Registry - repositório de imagens 

O registry é um repositório de imagens do Docker, onde os desenvolvedores podem armazenar e compartilhar suas imagens. O Docker Hub é o registro público mais popular, mas também existem registros privados que as empresas podem usar para armazenar suas imagens de forma segura.

## Imagem
Uma imagem é um pacote com todas as dependências e informações necessárias para criar um container. Você pode pensar em uma imagem como um modelo para criar containers. As imagens são construídas em camadas, onde cada camada representa uma modificação ou adição feita à imagem base.

* Imagem = classe

*  container = objeto

## Comandos básicos do Docker

| Comando | Descrição |
| --- | --- |
| docker run | inicia um container a partir de uma imagem |
| docker build | constrói uma imagem a partir de um Dockerfile |
| docker pull | baixa uma imagem do repositório |
| docker push | envia uma imagem para o repositório |
| docker ls | lista os containers em execução |
| docker ls -a | lista todos os containers, incluindo os parados |
| docker stop | para um container em execução |
| docker start | inicia um container parado |
| docker rm | remove um container |
| docker exec | executa um comando em um container em execução |



## Flags importantes
* --name - dá um nome ao container
* -it - roda o container em modo interativo, permitindo acesso ao terminal do container
* -di - roda o container em segundo plano, liberando o terminal (detached mode)
* -p - mapeia as portas do container para as portas do host
* --name - dá um nome ao container
* --rm - remove o container automaticamente após a execução

##### **detached mode:** modo em que o container roda em segundo plano, permitindo que o terminal seja liberado para outras tarefas. O container continua rodando mesmo após o terminal ser fechado. Para acessar o terminal do container em detached mode, é necessário usar o comando "docker exec -it <container_name> bash" ou "docker attach <container_name>".

##### **Dica:** *Use docker container rm -f [id do container]* para forçar a remoção de um container que está em execução. Cuidado: isso interrompe o processo imediatamente!

## Subindo a primeira aplicação



## Dockerfile



## Assuntos extras para estudar

### Orquestradores de contêineres
- **Docker Swarm:** ferramenta de orquestração de contêineres do Docker, que permite gerenciar um cluster de hosts Docker e implantar aplicativos em contêineres de forma escalável e resiliente.

- **Kubernetes:** plataforma de código aberto para automação de implantação, dimensionamento e gerenciamento de aplicativos em contêineres, que suporta uma ampla variedade de ferramentas de contêinerização, incluindo o Docker. O Kubernetes é amplamente utilizado para orquestrar e gerenciar aplicativos em contêineres em ambientes de produção.