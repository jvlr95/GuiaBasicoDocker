**Guia Básico de Docker para Iniciantes**

Este guia oferece uma introdução ao Docker, abordando conceitos essenciais e comandos frequentemente utilizados.

### Instalação do Docker:

1. **Baixe e Instale o Docker:**
   ```bash
   curl -fsSL https://get.docker.com/ | sudo bash
   ```

2. **Adicione seu usuário ao grupo Docker:**
   ```bash
   sudo usermod -aG docker $USER
   ```

3. **Verifique a Instalação:**
   ```bash
   docker --version
   ```

### Manipulação de Imagens Docker:

1. **Pesquisar Imagens no Docker Hub:**
   ```bash
   docker search nginx
   ```

2. **Baixar uma Imagem:**
   ```bash
   docker pull nginx
   ```

3. **Listar Imagens Locais:**
   ```bash
   docker image ls
   ```

4. **Inspeção de Detalhes de uma Imagem:**
   ```bash
   docker image inspect nginx:latest | less
   ```

5. **Remover uma Imagem:**
   ```bash
   docker image rm --force nginx
   ```

6. **Limpar Imagens Não Utilizadas:**
   ```bash
   docker image prune -a
   ```

7. **Login no Docker Hub:**
   ```bash
   docker login
   ```

8. **Tag e Enviar Imagem para o Docker Hub:**
   ```bash
   docker image tag nginx:latest seu_usuario/nginx:latest
   docker push seu_usuario/nginx:latest
   ```

### Utilização de Containers Docker:

1. **Executar um Container:**
   ```bash
   docker run nginx
   ```

2. **Executar Container em Segundo Plano:**
   ```bash
   docker run --detach --name nginx nginx
   ```

3. **Iniciar, Parar e Reiniciar Containers:**
   ```bash
   docker container start nginx
   docker container stop nginx
   docker container restart nginx
   ```

4. **Executar Comandos em um Container em Execução:**
   ```bash
   docker container exec -it nginx bash
   ```

5. **Copiar Arquivos entre Host e Container:**
   ```bash
   docker container cp teste.txt nginx:/var
   docker container cp nginx:/etc/hosts .
   ```

6. **Manter Containers Ativos sem Processos Secundários:**
   ```bash
   docker container run -d --name debian debian:latest sleep 1d
   ```

Este guia oferece uma base sólida para começar a usar o Docker. À medida que você se familiariza com esses conceitos, poderá explorar recursos mais avançados e integrar o Docker em seus projetos. **Padronize a documentação no README para fácil referência.**
