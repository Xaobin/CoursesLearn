
## Curso de Docker

<a name="inicio"></a>



1. [**Introdução ao Docker**](#item1)
   - O que é Docker?
   - Conceito de containers e imagens.
   - Diferenças entre Docker e máquinas virtuais.

2. [**Instalação e Configuração**](#item2)
   - Como instalar Docker no seu sistema operacional.
   - Testando se a instalação foi feita corretamente.

3. [**Comandos Básicos**](#item3)
   - Criar e executar containers.
   - Listar, parar e remover containers.
   - Trabalhar com imagens no Docker Hub.

4. [**Dockerfile**](#item4)
   - O que é um Dockerfile?
   - Criando uma imagem personalizada com Dockerfile.
   - Entendendo os principais comandos no Dockerfile.

5. [**Volumes e Persistência**](#item5)
   - Como persistir dados em containers.
   - Criar e gerenciar volumes.

6. [**Redes no Docker**](#item6)
   - Configuração básica de redes.
   - Conexão entre containers.

7. [**Docker Compose**](#item7)
   - O que é Docker Compose?
   - Criando arquivos `docker-compose.yml` para gerenciar múltiplos containers.
   - Exemplos práticos de uso.

8. [**Ambiente de Produção**](#item8)
   - Melhores práticas para deploy com Docker.
   - Escalabilidade e orquestração com ferramentas como Kubernetes.

9. [**Resolução de Problemas**](#item9)
   - Como depurar containers.
   - Análise de logs e gerenciamento de erros comuns.

10. [**Segurança com Docker**](#item10)
    - Configuração de segurança básica.
    - Limitação de acesso e permissões.


<a name="item1"></a>

**Introdução ao Docker**.

### O que é Docker?
Docker é uma plataforma de código aberto projetada para ajudar desenvolvedores a criar, empacotar e executar aplicativos em containers. Esses containers incluem tudo o que o aplicativo precisa para funcionar, como bibliotecas, dependências e o próprio código. Isso garante que a aplicação rode de forma consistente, independentemente do ambiente.

### Conceito de Containers e Imagens
- **Containers**: São ambientes isolados e portáteis onde as aplicações são executadas. Pense neles como "mini-computadores" virtuais, mas muito mais leves.
- **Imagens**: São modelos imutáveis usados para criar containers. Elas contêm as instruções para montar o container, incluindo o sistema operacional base e os arquivos necessários.

### Diferenças entre Docker e Máquinas Virtuais (VMs)
Uma dúvida comum ao começar é a diferença entre Docker e VMs. Aqui estão os pontos principais:
- Containers compartilham o mesmo kernel do sistema operacional host, enquanto VMs possuem sistemas operacionais próprios.
- Docker é mais leve e inicia containers em segundos, enquanto VMs tendem a consumir mais recursos e demoram mais para iniciar.
- Containers são mais adequados para desenvolvedores e equipes ágeis, enquanto VMs são amplamente usadas para virtualização tradicional.


[Voltar para Início](#inicio)

<hr>
<a name="item2"></a>

Vamos explorar o item 2 do seu **dockercurso**: **Instalação e Configuração do Docker**.

### Como instalar o Docker
A instalação pode variar dependendo do sistema operacional que você está utilizando. Aqui está um guia geral:

#### Para Windows:
1. **Baixe o instalador**: Acesse o [site oficial do Docker](https://www.docker.com/) e faça o download do Docker Desktop para Windows.
2. **Instale o software**: Execute o instalador e siga as instruções.
3. **Configuração**: Após a instalação, reinicie o sistema se necessário. Inicie o Docker Desktop e verifique se está funcionando.

#### Para macOS:
1. **Download**: Baixe o Docker Desktop no [site oficial do Docker](https://www.docker.com/).
2. **Instale**: Arraste o aplicativo para a pasta Aplicativos e abra-o.
3. **Configuração**: Verifique se o Docker está funcionando corretamente.

#### Para Linux:
1. **Use o gerenciador de pacotes**: Dependendo da sua distribuição, instale o Docker com os seguintes comandos:
   - Para Ubuntu: 
     ```bash
     sudo apt update
     sudo apt install docker.io
     ```
   - Para Fedora:
     ```bash
     sudo dnf install docker
     ```
2. **Verifique a instalação**: Rode o comando `docker --version` para confirmar a instalação.

---

### Testando a instalação
Depois de instalar o Docker, é importante garantir que está funcionando corretamente:
1. **Verifique a versão**: Use o comando:
   ```bash
   docker --version
   ```
   Isso exibirá a versão instalada.

2. **Rode o container de teste**: Execute o comando:
   ```bash
   docker run hello-world
   ```
   Ele baixa uma imagem e inicia um container simples que exibe uma mensagem de sucesso.

3. **Confirmando o funcionamento**: Se tudo estiver correto, você verá uma mensagem no terminal confirmando que o Docker está configurado.

[Voltar para Início](#inicio)


<hr>
<a name="item3"></a>

**item 3: Comandos Básicos do Docker**.

Aprender os comandos básicos é essencial para começar a usar o Docker no dia a dia. Aqui estão os mais importantes:

---

### Trabalhando com Containers
1. **Criar e executar um container:**
   ```bash
   docker run nome-da-imagem
   ```
   - Exemplo: 
     ```bash
     docker run ubuntu
     ```
     Este comando cria e executa um container baseado na imagem `ubuntu`.

2. **Iniciar um container já existente:**
   ```bash
   docker start id-ou-nome-do-container
   ```

3. **Parar um container:**
   ```bash
   docker stop id-ou-nome-do-container
   ```

4. **Remover um container:**
   ```bash
   docker rm id-ou-nome-do-container
   ```

---

### Trabalhando com Imagens
1. **Baixar uma imagem do Docker Hub:**
   ```bash
   docker pull nome-da-imagem
   ```
   - Exemplo:
     ```bash
     docker pull nginx
     ```

2. **Listar imagens disponíveis localmente:**
   ```bash
   docker images
   ```

3. **Remover uma imagem local:**
   ```bash
   docker rmi nome-ou-id-da-imagem
   ```

---

### Inspecionar Containers
1. **Listar todos os containers:**
   ```bash
   docker ps
   ```
   - Para listar os containers parados:
     ```bash
     docker ps -a
     ```

2. **Ver os logs de um container:**
   ```bash
   docker logs id-ou-nome-do-container
   ```

3. **Inspecionar detalhes de um container:**
   ```bash
   docker inspect id-ou-nome-do-container
   ```

4. **Acessar um container em execução (modo interativo):**
   ```bash
   docker exec -it id-ou-nome-do-container bash
   ```

[Voltar para Início](#inicio)

<hr>
<a name="item4"></a>

Vamos falar sobre o **item 4 - Dockerfile**. Essa é uma parte essencial para criar imagens personalizadas no Docker!

---

### O que é um Dockerfile?
Um **Dockerfile** é um arquivo de texto simples que contém um conjunto de instruções que o Docker usa para construir uma imagem. Cada linha no Dockerfile representa uma etapa na criação da imagem, como instalar dependências, copiar arquivos ou definir variáveis de ambiente.

---

### Criando um Dockerfile
1. **Estrutura básica de um Dockerfile**:
   Aqui está um exemplo simples:
   ```dockerfile
   # Escolha uma imagem base
   FROM ubuntu:latest

   # Instale pacotes necessários
   RUN apt-get update && apt-get install -y curl

   # Copie arquivos locais para o container
   COPY meu-arquivo.txt /app/

   # Defina o diretório de trabalho
   WORKDIR /app

   # Comando padrão ao executar o container
   CMD ["echo", "Olá, Docker!"]
   ```

---

### Principais comandos no Dockerfile
- **FROM**: Define a imagem base para o container. Exemplo: `FROM ubuntu:latest`.
- **RUN**: Executa comandos durante a construção da imagem. Exemplo: `RUN apt-get update`.
- **COPY**: Copia arquivos do host para o container. Exemplo: `COPY arquivo.txt /app/`.
- **WORKDIR**: Define o diretório de trabalho dentro do container.
- **CMD**: Especifica o comando padrão que será executado quando o container iniciar.

---

### Construindo a Imagem com um Dockerfile
Depois de criar o Dockerfile, você pode construir uma imagem usando o comando:
```bash
docker build -t nome-da-imagem .
```
- O `-t` permite dar um nome à sua imagem.
- O `.` indica que o Dockerfile está no diretório atual.

---

### Testando a Imagem
Após criar a imagem, você pode executar um container com ela:
```bash
docker run nome-da-imagem
```

---

O Dockerfile é uma ferramenta poderosa que ajuda a automatizar e padronizar a construção de imagens. Se quiser, podemos praticar criando um Dockerfile juntos para um projeto específico! 🚀

<hr>
<a name="item5"></a>

Item 5: **Volumes e Persistência no Docker**. Este tópico é essencial para lidar com dados que precisam permanecer mesmo depois que um container é encerrado.

---

### Por que utilizar volumes?
Por padrão, os dados criados dentro de um container são temporários e desaparecem quando o container é removido. Para preservar esses dados, usamos **volumes**, que são áreas de armazenamento criadas e gerenciadas pelo Docker fora do ciclo de vida do container.

---

### Tipos de Volumes no Docker
1. **Volumes Gerenciados pelo Docker**:
   - Criados e mantidos automaticamente pelo Docker.
   - São ideais para armazenamento persistente.

2. **Bind Mounts**:
   - Permitem vincular um diretório específico do sistema host ao container.
   - Útil para desenvolvimento local onde os arquivos podem ser alterados diretamente.

---

### Comandos Básicos para Trabalhar com Volumes
1. **Criar um volume:**
   ```bash
   docker volume create nome-do-volume
   ```

2. **Listar volumes existentes:**
   ```bash
   docker volume ls
   ```

3. **Remover um volume:**
   ```bash
   docker volume rm nome-do-volume
   ```

---

### Usando Volumes com Containers
Ao executar um container, você pode montá-lo em um volume para persistir os dados:
```bash
docker run -v nome-do-volume:/diretorio-dentro-do-container nome-da-imagem
```
- Exemplo:
  ```bash
  docker run -v meu-volume:/app/data ubuntu
  ```

---

### Exemplos Práticos
1. **Criando e testando um volume**:
   - Crie o volume:
     ```bash
     docker volume create meu-volume
     ```
   - Use o volume em um container:
     ```bash
     docker run -v meu-volume:/data ubuntu bash -c "echo 'Olá, Volume!' > /data/mensagem.txt"
     ```
   - Verifique os dados persistidos acessando o container novamente:
     ```bash
     docker run -v meu-volume:/data ubuntu cat /data/mensagem.txt
     ```

---

### Vantagens dos Volumes
- Persistência de dados independente dos containers.
- Compartilhamento de dados entre múltiplos containers.
- Fácil backup e migração de dados.

Volumes são uma ferramenta fundamental para gerenciar dados em aplicações Docker.


[Voltar para Início](#inicio)
<hr>
<a name="item6"></a>

**item 6  - Redes no Docker**. Este é um aspecto importante para configurar a comunicação entre containers ou entre containers e o mundo externo.

---

### Introdução às Redes no Docker
O Docker possui um sistema de redes integrado que permite:
- Conectar containers entre si.
- Controlar o tráfego de entrada e saída.
- Isolar aplicações para segurança e organização.

---

### Tipos de Redes no Docker
1. **bridge (padrão)**:
   - É a rede padrão criada pelo Docker.
   - Usada quando você quer que vários containers se comuniquem em uma mesma máquina.

2. **host**:
   - Faz com que o container use diretamente a rede do host, sem isolamento.
   - Útil para performance ou quando o isolamento de rede não é necessário.

3. **none**:
   - Remove totalmente a conexão de rede.
   - Usada quando você não quer nenhuma comunicação de rede para o container.

4. **rede personalizada**:
   - Permite criar redes específicas e configurar detalhes como sub-redes e gateways.
   - Ideal para ambientes mais complexos.

---

### Comandos Básicos para Trabalhar com Redes
1. **Listar redes disponíveis:**
   ```bash
   docker network ls
   ```

2. **Criar uma rede personalizada:**
   ```bash
   docker network create nome-da-rede
   ```

3. **Conectar um container a uma rede:**
   ```bash
   docker network connect nome-da-rede id-ou-nome-do-container
   ```

4. **Desconectar um container de uma rede:**
   ```bash
   docker network disconnect nome-da-rede id-ou-nome-do-container
   ```

5. **Remover uma rede:**
   ```bash
   docker network rm nome-da-rede
   ```

---

### Exemplo Prático
1. Crie uma rede personalizada:
   ```bash
   docker network create minha-rede
   ```

2. Inicie dois containers conectados à mesma rede:
   ```bash
   docker run -dit --name container1 --network minha-rede ubuntu
   docker run -dit --name container2 --network minha-rede ubuntu
   ```

3. Verifique a conectividade entre os containers:
   - Acesse o primeiro container:
     ```bash
     docker exec -it container1 bash
     ```
   - Instale o `ping` (se necessário) e teste:
     ```bash
     apt update && apt install -y iputils-ping
     ping container2
     ```

---

### Vantagens de Configurar Redes no Docker
- **Isolamento**: Cada aplicação pode ter sua própria rede isolada.
- **Escalabilidade**: É fácil conectar novos containers à rede existente.
- **Configuração personalizável**: Flexibilidade para configurar IPs, sub-redes e regras.

Redes são fundamentais para aplicações que dependem de múltiplos serviços comunicando-se entre si, como uma aplicação web com backend e banco de dados. 

[Voltar para Início](#inicio)
<hr>
<a name="item7"></a>

**item 7: Docker Compose**. O Docker Compose é uma ferramenta extremamente útil para gerenciar e orquestrar múltiplos containers, especialmente em aplicações que possuem vários serviços.

---

### O que é Docker Compose?
Docker Compose é uma ferramenta que permite definir e gerenciar ambientes multi-container usando um único arquivo de configuração chamado `docker-compose.yml`. Com ele, você pode especificar como seus containers interagem, suas dependências e configurações de forma simples e organizada.

---

### Vantagens do Docker Compose
- **Simplicidade**: Gerencie vários containers com comandos únicos.
- **Automação**: Criação e inicialização automática de todos os serviços necessários.
- **Portabilidade**: Compartilhe o arquivo `docker-compose.yml` com sua equipe para replicar o ambiente em qualquer lugar.

---

### Estrutura de um Arquivo `docker-compose.yml`
Aqui está um exemplo básico de um arquivo `docker-compose.yml` para uma aplicação web simples:

```yaml
version: '3'

services:
  web:
    image: nginx
    ports:
      - "8080:80"
  app:
    image: python:3.9
    volumes:
      - ./app:/app
    working_dir: /app
    command: python app.py
```

Neste exemplo:
- Definimos dois serviços: `web` (um servidor nginx) e `app` (um aplicativo Python).
- O serviço `web` mapeia a porta 8080 do host para a porta 80 no container.
- O serviço `app` utiliza um volume para montar o diretório local `./app` no caminho `/app` dentro do container.

---

### Principais Comandos do Docker Compose
1. **Iniciar os serviços definidos no arquivo `docker-compose.yml`:**
   ```bash
   docker-compose up
   ```
   - Use `-d` para rodar em modo "detached" (em segundo plano):
     ```bash
     docker-compose up -d
     ```

2. **Parar os serviços:**
   ```bash
   docker-compose down
   ```

3. **Reiniciar containers específicos:**
   ```bash
   docker-compose restart nome-do-servico
   ```

4. **Verificar o status dos serviços:**
   ```bash
   docker-compose ps
   ```

---

### Exemplo Prático
Imagine que você tem um site com um backend (Python) e um banco de dados (MySQL). Aqui está um arquivo `docker-compose.yml` para configurar isso:

```yaml
version: '3'

services:
  backend:
    image: python:3.9
    volumes:
      - ./backend:/backend
    working_dir: /backend
    command: python server.py
    ports:
      - "5000:5000"

  db:
    image: mysql:5.7
    environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: minha_app
    ports:
      - "3306:3306"
```

Com este arquivo, você pode rodar `docker-compose up` e ter todo o ambiente configurado automaticamente.

---

O Docker Compose é uma ferramenta poderosa para simplificar o trabalho com aplicações que exigem múltiplos serviços. 

[Voltar para Início](#inicio)
<hr>
<a name="item8"></a>

**item 8: Ambiente de Produção com Docker**. Este passo é crucial para garantir que suas aplicações sejam escaláveis, seguras e eficientes quando implantadas em um ambiente de produção.

---

### Melhores Práticas para Deploy com Docker
1. **Utilizar Imagens Otimizadas**:
   - Prefira imagens leves, como as baseadas em Alpine Linux, para reduzir o uso de recursos e o tempo de inicialização.
   - Exemplo:
     ```dockerfile
     FROM node:alpine
     ```

2. **Configurar Variáveis de Ambiente**:
   - Use variáveis de ambiente para definir configurações de produção sem expor dados sensíveis. Por exemplo:
     ```yaml
     environment:
       - DATABASE_URL=jdbc:mysql://db:3306/producao
     ```

3. **Gerenciar Recursos**:
   - Limite o uso de CPU e memória para evitar que containers consumam recursos excessivos:
     ```bash
     docker run --memory="512m" --cpus="1" nome-da-imagem
     ```

4. **Manter Logs Organizados**:
   - Direcione os logs para ferramentas externas como ELK Stack ou AWS CloudWatch para monitoramento centralizado.

---

### Escalabilidade e Orquestração
Para gerenciar múltiplos containers em produção, é essencial usar ferramentas de orquestração. **Kubernetes** e **Docker Swarm** são as opções mais populares.

1. **Kubernetes**:
   - Permite criar clusters de containers altamente escaláveis.
   - Garante disponibilidade com balanceamento de carga e auto-recuperação de serviços.

2. **Docker Swarm**:
   - Uma alternativa mais simples ao Kubernetes.
   - Fácil de configurar para implantações menores.

---

### Segurança em Produção
1. **Reduzir Permissões**:
   - Execute containers com o menor privilégio possível:
     ```bash
     docker run --user 1000 nome-da-imagem
     ```

2. **Atualizar Imagens**:
   - Certifique-se de que as imagens utilizadas estejam sempre atualizadas para evitar vulnerabilidades.

3. **Isolamento de Rede**:
   - Utilize redes personalizadas e evite expor portas desnecessárias.

---

### Exemplo de Deploy em Produção com Docker Compose
Aqui está um exemplo de configuração simplificada para produção usando o `docker-compose.yml`:

```yaml
version: '3.8'

services:
  app:
    image: minha-app:latest
    deploy:
      replicas: 3
      resources:
        limits:
          cpus: '1.0'
          memory: 512M
    environment:
      - NODE_ENV=production
    networks:
      - rede-producao

networks:
  rede-producao:
    driver: bridge
```

Nesse exemplo, a aplicação:
- Usa 3 réplicas para garantir alta disponibilidade.
- Possui limites de recursos configurados para proteger o host.
- Está conectada a uma rede isolada para maior segurança.

---

Ambientes de produção exigem atenção especial, e as boas práticas garantem que suas aplicações sejam confiáveis, escaláveis e seguras.

[Voltar para Início](#inicio)
<hr>
<a name="item9"></a>

**item 9: Resolução de Problemas no Docker**. Entender como identificar e corrigir problemas é essencial para trabalhar com containers de forma eficiente.

---

### Problemas Comuns no Docker
1. **Containers não iniciam**:
   - Pode ocorrer por conflitos de configuração ou dependências faltantes.
   - Solução: Verifique os logs do container para identificar o erro.

2. **Imagens muito grandes**:
   - Imagens mal otimizadas podem consumir muito espaço.
   - Solução: Utilize imagens base mais leves e elimine arquivos desnecessários no Dockerfile.

3. **Conexão de rede falhando**:
   - Containers podem não se comunicar corretamente devido a configurações de rede.
   - Solução: Verifique a rede dos containers e reconecte se necessário.

4. **Erro ao montar volumes**:
   - Pode acontecer por permissões ou caminhos incorretos.
   - Solução: Certifique-se de que o caminho no host existe e tem as permissões corretas.

5. **Recursos insuficientes**:
   - Containers podem consumir muita CPU/memória, afetando o desempenho do host.
   - Solução: Configure limites de recursos ao criar ou executar containers.

---

### Comandos Úteis para Depuração
1. **Visualizar os logs do container**:
   ```bash
   docker logs nome-ou-id-do-container
   ```
   Isso ajuda a entender o que está acontecendo dentro do container.

2. **Inspecionar detalhes de um container**:
   ```bash
   docker inspect nome-ou-id-do-container
   ```
   Exibe informações detalhadas, como configurações de rede e volumes.

3. **Verificar o uso de recursos**:
   ```bash
   docker stats
   ```
   Mostra o consumo de CPU e memória em tempo real.

4. **Testar conectividade de rede**:
   Acesse o container e use o comando `ping` para verificar a conexão:
   ```bash
   docker exec -it nome-do-container ping nome-de-outro-container
   ```

---

### Passos para Resolver Problemas
1. **Isolamento**: Comece isolando o problema (rede, volume, imagem, etc.).
2. **Logs e Inspeção**: Use os comandos de logs e inspeção para identificar detalhes do erro.
3. **Recriação**: Caso não consiga corrigir, recrie o container ou imagem para eliminar possíveis falhas.
4. **Documentação**: Consulte a documentação oficial do Docker e fóruns online (como Stack Overflow) para buscar soluções específicas.

---

### Dicas Adicionais
- **Backup Regular**: Sempre mantenha backups de dados importantes em volumes.
- **Ambiente de Teste**: Teste mudanças em um ambiente separado antes de aplicar em produção.
- **Atualizações**: Certifique-se de estar usando a versão mais recente do Docker para evitar bugs corrigidos.

---

Com essas técnicas, você estará pronto para identificar e resolver problemas de forma eficaz!

[Voltar para Início](#inicio)
<hr>
<a name="item10"></a>

**item 10: Segurança com Docker**. A segurança é um componente crítico ao usar containers, especialmente em ambientes de produção, onde dados sensíveis e operações em larga escala estão envolvidos.

---

### Práticas Fundamentais de Segurança com Docker

1. **Executar Containers com Permissões Restringidas**:
   - Por padrão, os containers podem ter permissões de superusuário, o que pode ser arriscado.
   - Solução: Execute containers como usuários não privilegiados.
     ```bash
     docker run --user 1000 nome-do-container
     ```

2. **Utilizar Imagens Seguras e Confiáveis**:
   - Baixe imagens somente de fontes confiáveis, como o Docker Hub oficial ou repositórios verificados.
   - Verifique se há vulnerabilidades nas imagens usando ferramentas como o `docker scan`:
     ```bash
     docker scan nome-da-imagem
     ```

3. **Limitar o Acesso a Dados Sensíveis**:
   - Use variáveis de ambiente para gerenciar segredos, mas, para maior segurança, utilize ferramentas como `Docker Secrets` para armazenar informações confidenciais.

4. **Configuração de Rede**:
   - Evite expor serviços diretamente ao público se não for necessário.
   - Use redes personalizadas para isolar containers e limitar a comunicação.

5. **Manter o Docker Atualizado**:
   - Atualize regularmente o Docker para a versão mais recente, que corrige bugs e vulnerabilidades.

---

### Proteções Adicionais

1. **Habilitar Perfis AppArmor ou SELinux**:
   - Use controles de acesso baseados no kernel para reforçar a segurança dos containers.

2. **Isolar Recursos do Host**:
   - Configure limites para evitar que containers consumam recursos excessivos:
     ```bash
     docker run --memory="512m" --cpus="1" nome-do-container
     ```

3. **Habilitar Somente Recursos Necessários**:
   - Desative privilégios desnecessários com o parâmetro `--cap-drop`:
     ```bash
     docker run --cap-drop ALL nome-do-container
     ```

---

### Auditorias e Monitoramento
- **Auditar Logs**:
  Verifique logs regularmente para identificar atividades suspeitas:
  ```bash
  docker logs nome-do-container
  ```

- **Ferramentas de Monitoramento**:
  Utilize ferramentas como Falco, Aqua Security ou Sysdig para monitorar o comportamento dos containers e identificar possíveis ameaças.

---

### Exemplo de Configuração Segura
Aqui está um exemplo de como rodar um container com configurações seguras:
```bash
docker run \
  --user 1000 \
  --read-only \
  --memory="512m" \
  --cap-drop ALL \
  --network minha-rede-segura \
  minha-imagem-segura
```

Nesse exemplo:
- O container roda como um usuário sem privilégios.
- A opção `--read-only` impede alterações não autorizadas no sistema de arquivos.
- Limites de memória e CPU evitam sobrecarga no host.

---

Segurança é um processo contínuo, e seguir essas práticas ajuda a proteger suas aplicações e dados. 


[Voltar para Início](#inicio)

