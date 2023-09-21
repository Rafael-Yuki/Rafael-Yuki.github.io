# Projeto Jekyll Padrão

Este é um projeto Jekyll padrão hospedado no GitHub Pages.

## Clonar o Projeto

Para começar a trabalhar neste projeto localmente, siga estas etapas:

1. Clone o repositório para o seu ambiente de desenvolvimento:

   ```bash
   git clone https://github.com/Rafael-Yuki/Rafael-Yuki.github.io.git
   ```

2. Navegue até o diretório do projeto:

   ```bash
   cd Rafael-Yuki.github.io
   ```

## Configurar o Ambiente Local

Para configurar o ambiente local e executar o projeto, siga estas etapas:

1. **Requisitos Prévios**:

   Certifique-se de ter o Ruby e o Jekyll instalados em seu sistema. Se você não tiver, siga as instruções na [documentação oficial do Jekyll](https://jekyllrb.com/docs/installation/) para a instalação.

2. **Instalar as Dependências**:

   Instale as dependências do projeto usando o Bundler. Execute o seguinte comando no diretório do projeto:

   ```bash
   bundle install
   ```

## Executar o Projeto Localmente

Depois de configurar o ambiente, você pode executar o projeto localmente usando o seguinte comando:

```bash
bundle exec jekyll serve
```

Isso iniciará o servidor de desenvolvimento Jekyll e você poderá acessar o projeto em seu navegador em `http://localhost:4000`.

## Contribuir

Se você quiser contribuir para este projeto, siga estas etapas:

1. Faça um fork deste repositório em sua própria conta do GitHub.
2. Clone o repositório forked para o seu ambiente de desenvolvimento.
3. Crie uma nova branch para suas alterações:

   ```bash
   git checkout -b minha-branch
   ```

4. Faça as alterações desejadas e commit-as:

   ```bash
   git commit -m "Minhas alterações"
   ```

5. Envie as alterações para o seu repositório forked:

   ```bash
   git push origin minha-branch
   ```

6. Abra um Pull Request no repositório original e aguarde a revisão.

## Licença

Este projeto está sob a licença [MIT](LICENSE).
```

Certifique-se de substituir `https://github.com/Rafael-Yuki/Rafael-Yuki.github.io.git` pela URL do seu repositório GitHub, se for diferente. Este README.md fornece informações detalhadas para clonar, configurar o ambiente local, executar o projeto e contribuir para o seu projeto Jekyll padrão no GitHub Pages.
```

7. Fluxo de trabalho do projeto Jekyll com GitHub Pages, integração do ESLint e CodeQL:

1. **Gatilhos (Triggers)**:
   - O workflow é acionado por eventos como push (envio de código) e pull requests (solicitações de recebimento de código) na branch principal (`main`).
   - Isso garante que o workflow seja executado sempre que houver mudanças no código-fonte do projeto.

2. **Configuração Inicial**:
   - O ambiente de execução é configurado como `ubuntu-latest`.
   - São definidas permissões para acessar o código do repositório e fazer implantações.

3. **Checkout do Código**:
   - O código-fonte do repositório é clonado, obtendo a versão mais recente da branch `main`.

4. **Construção do Site Jekyll**:
   - O ambiente é configurado para construir um site Jekyll.
   - Dependências como Ruby e Bundler são instaladas.
   - As gemas necessárias para o Jekyll são instaladas.
   - O comando `bundle exec jekyll build` é usado para construir o site, gerando os arquivos no diretório `./_site`.

5. **Análise de Qualidade do Código com ESLint**:
   - O ESLint é instalado, configurado e usado para analisar o código JavaScript/TypeScript em busca de problemas de qualidade.
   - Os resultados são formatados em um arquivo SARIF para análise posterior.

6. **Análise de Segurança com CodeQL**:
   - A análise de segurança com o CodeQL é realizada, identificando possíveis vulnerabilidades no código.
   - Os resultados são formatados em um arquivo SARIF para análise posterior.

7. **Upload de Artefatos**:
   - O site construído (no diretório `./_site`) e os resultados das análises do ESLint e CodeQL são enviados como artefatos.

8. **Implantação no GitHub Pages**:
   - A implantação no GitHub Pages é feita usando uma ação específica.
   - O site construído no passo 4 é implantado, tornando-o publicamente acessível na URL do GitHub Pages.

9. **Resultado**:
   - O site Jekyll é construído, testado quanto à qualidade do código com ESLint, e verificado quanto à segurança com o CodeQL.
   - Após a implantação bem-sucedida, o site está disponível publicamente no GitHub Pages.

Esse fluxo de trabalho automatizado garante que o site Jekyll seja construído e implantado com eficiência, enquanto verifica a qualidade e a segurança do código por meio das análises do ESLint e CodeQL.
