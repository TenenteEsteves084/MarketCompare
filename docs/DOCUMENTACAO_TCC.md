# Documentação do TCC — MarketCompare

> **Rascunho técnico baseado nas informações atualmente disponíveis no repositório.** O repositório consultado contém os arquivos README, mas não contém o código-fonte descrito neles. Por isso, os detalhes de implementação e execução abaixo devem ser conferidos com a versão completa do projeto antes da entrega acadêmica.

## Identificação do trabalho

- **Título do projeto:** MarketCompare — comparação de preços entre mercados
- **Autor(a):** [preencher]
- **Instituição:** [preencher]
- **Curso:** [preencher]
- **Orientador(a):** [preencher]
- **Ano:** [preencher]

## 1. Resumo

O MarketCompare é descrito como uma aplicação web destinada à consulta e comparação de preços de produtos cadastrados em diferentes mercados. A proposta reúne as ofertas em um catálogo, permitindo pesquisar e filtrar produtos e identificar o menor preço registrado. Para usuários autenticados, o sistema também prevê o cadastro e o gerenciamento de produtos, além de uma lista de favoritos. A documentação do repositório informa que a aplicação utiliza Node.js e Express no backend, HTML, CSS e JavaScript no frontend, arquivos JSON para armazenamento de dados e Jest e Supertest para testes automatizados.

**Palavras-chave:** comparação de preços; aplicação web; catálogo de produtos; Node.js.

## 2. Contextualização e problema

A consulta de preços em diferentes estabelecimentos pode exigir que o consumidor acesse diversas fontes separadamente. A proposta do MarketCompare é centralizar os preços cadastrados em um catálogo, facilitando a consulta e a comparação das ofertas disponíveis.

> A contextualização acadêmica, os dados que demonstram a relevância do problema e as referências bibliográficas precisam ser complementados pelo(a) autor(a), de acordo com a pesquisa realizada no TCC.

## 3. Objetivos

### 3.1 Objetivo geral

Desenvolver uma aplicação web para consultar produtos e comparar preços cadastrados em diferentes mercados.

### 3.2 Objetivos específicos

- Disponibilizar um catálogo de produtos com busca, filtros e ordenação.
- Exibir os preços e mercados associados a cada produto para apoiar a comparação.
- Permitir que usuários autenticados cadastrem e gerenciem produtos.
- Oferecer funcionalidades de conta, autenticação e recuperação de senha.
- Testar os principais comportamentos da API.

## 4. Escopo funcional

| Recurso | Descrição | Acesso indicado no README |
| --- | --- | --- |
| Catálogo | Consultar produtos, pesquisar, filtrar por categoria ou mercado e ordenar por nome ou menor preço. | Público |
| Comparação de preços | Consultar os mercados e preços cadastrados para um produto. | Público |
| Cadastro de produto | Informar produto, mercado, endereço, cidade e preço. | Requer autenticação |
| Gestão de cadastros | Listar, editar e excluir produtos enviados pelo usuário autenticado. | Requer autenticação |
| Favoritos | Adicionar ou remover produtos dos favoritos da sessão. | Requer autenticação |
| Conta | Criar conta, entrar, sair e redefinir senha. | Público para os fluxos de conta |

## 5. Requisitos do sistema

### 5.1 Requisitos funcionais

1. O sistema deve apresentar um catálogo de produtos.
2. O sistema deve permitir buscar produtos e filtrar por categoria ou mercado.
3. O sistema deve permitir ordenar os resultados por nome ou menor preço.
4. O sistema deve apresentar os preços e os mercados cadastrados para um produto.
5. O sistema deve permitir que usuários autenticados cadastrem produtos e informações de preço e localização.
6. O sistema deve permitir que o usuário autenticado consulte, edite e exclua os próprios cadastros.
7. O sistema deve permitir adicionar e remover produtos dos favoritos.
8. O sistema deve oferecer cadastro, login, logout e redefinição de senha.

### 5.2 Requisitos não funcionais

- A aplicação deve ser acessível por navegador web.
- As telas de autenticação são descritas como responsivas e com temas claro e escuro.
- A API deve possuir testes automatizados para os principais fluxos descritos.
- A configuração de sessão deve permitir definir o segredo por variável de ambiente.

> Os requisitos não funcionais devem ser revisados com base no código e nos critérios efetivamente avaliados no trabalho.

## 6. Tecnologias e arquitetura descritas

Segundo o README em português:

- **Backend:** Node.js, Express e `express-session`.
- **Frontend:** HTML, CSS e JavaScript.
- **Persistência:** arquivos JSON.
- **Testes:** Jest e Supertest.

A organização lógica descrita separa páginas e API em rotas, regras de controle em controladores, operações auxiliares em serviços e dados em arquivos JSON. O frontend é descrito como composto por arquivos estáticos e páginas HTML.

### 6.1 Estrutura prevista no README

```text
backend/
  server.js
  src/
    controllers/
    data/
    routes/
    services/
  tests/
frontend/
  static/
  templates/
media/
```

**Observação:** essa estrutura é a que consta no README e não foi possível confirmá-la na árvore de arquivos atualmente visível no repositório.

## 7. Dados e limitações

O README informa que produtos e contas são armazenados em arquivos JSON e que as sessões usam o armazenamento em memória padrão do `express-session`. Essa configuração é apresentada como adequada para desenvolvimento local e demonstração, mas não para publicação em produção. O README também recomenda substituir configurações de demonstração e adotar armazenamento e configurações apropriados antes de disponibilizar o sistema publicamente.

As limitações devem ser descritas no TCC com base na implementação final, incluindo aspectos como persistência, segurança, atualização dos preços e cobertura dos dados disponíveis.

## 8. Instalação, execução e testes

As instruções abaixo são reproduzidas do README do projeto e dependem da presença dos diretórios e arquivos de código correspondentes:

```bash
cd backend
npm install
npm start
```

O README indica acesso local em `http://localhost:5000` e recomenda configurar `SESSION_SECRET` para definir o segredo das sessões.

Para executar os testes, a partir da pasta `backend/`:

```bash
npm test
```

A suíte é descrita como baseada em Jest e Supertest e cobre operações da API, incluindo listagem, busca, filtros, comparação de preços, cadastro, edição, exclusão e autenticação.

## 9. Testes e validação

O README descreve testes automatizados para a API. Para completar esta seção no TCC, registre:

- versão do Node.js utilizada;
- ambiente e procedimento de execução dos testes;
- quantidade de testes executados e resultados;
- cenários avaliados manualmente;
- limitações encontradas durante a validação.

Não foram incluídos resultados quantitativos nesta documentação porque eles não estão disponíveis nos arquivos consultados.

## 10. Considerações finais

O MarketCompare propõe centralizar a consulta de produtos e a comparação de preços cadastrados, combinando funcionalidades públicas de pesquisa com recursos de gestão associados a uma conta. A documentação existente descreve uma implementação web com API, interface, armazenamento em JSON e testes automatizados. As conclusões finais do TCC devem ser escritas após a validação da versão completa do sistema e relacionadas aos objetivos definidos pelo trabalho.

## 11. Informações a completar antes da entrega

- Dados de autoria, instituição, curso, orientação e ano.
- Problema de pesquisa, justificativa e referências bibliográficas.
- Metodologia adotada e etapas de desenvolvimento.
- Diagramas efetivamente elaborados (casos de uso, arquitetura, banco/dados ou fluxo).
- Capturas de tela e descrição dos fluxos finais.
- Resultados dos testes e avaliação com usuários, se realizada.
- Revisão das instruções de instalação conforme o código efetivamente entregue.
- Revisão do texto conforme o modelo e as normas exigidas pela instituição.
