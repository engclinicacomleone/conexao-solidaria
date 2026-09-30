# Arquitetura e organização do projeto

## Objetivo

A organização do Conexão Solidária foi estruturada buscando separar as diferentes responsabilidades da aplicação e facilitar sua manutenção e evolução.

Durante o desenvolvimento, a estrutura inicialmente voltada à interface foi ampliada para acomodar comportamentos dinâmicos em JavaScript, tornando necessária uma divisão mais clara entre estrutura, apresentação, recursos visuais e lógica da aplicação.

## Organização de diretórios

O projeto adota uma separação dos arquivos de acordo com suas responsabilidades.

A estrutura contempla diretórios específicos para:

- documentos HTML;
- folhas de estilo CSS;
- arquivos JavaScript;
- imagens e recursos visuais.

Essa organização evita a concentração de arquivos com finalidades diferentes em um único diretório e facilita a localização dos recursos durante o desenvolvimento.

## Separação de responsabilidades

A arquitetura do projeto procura manter três responsabilidades principais separadas:

**Estrutura**

O HTML define a estrutura semântica e os elementos fundamentais da aplicação.

**Apresentação**

O CSS é responsável pela identidade visual, organização dos layouts, responsividade e estados visuais dos componentes.

**Comportamento**

O JavaScript controla a interatividade, manipulação do DOM, navegação, validação, persistência local e demais comportamentos dinâmicos.

Essa separação contribui para reduzir dependências desnecessárias e tornar o código mais compreensível.

## Organização do JavaScript

Com o aumento das funcionalidades, a lógica JavaScript foi dividida em módulos menores.

Entre as responsabilidades separadas durante o desenvolvimento estão:

- roteamento da aplicação;
- geração de templates;
- tratamento de formulários;
- armazenamento e recuperação de dados.

Essa abordagem segue o princípio de responsabilidade única, evitando a concentração de toda a lógica da aplicação em um único arquivo.

## Comunicação entre módulos

Os módulos JavaScript utilizam mecanismos de `import` e `export` para compartilhar apenas as funcionalidades necessárias.

Essa abordagem permite que cada módulo mantenha uma responsabilidade específica enquanto disponibiliza interfaces controladas para outras partes da aplicação.

O objetivo é reduzir o acoplamento e tornar futuras alterações menos propensas a gerar efeitos inesperados em funcionalidades não relacionadas.

## Fluxo simplificado da aplicação

De forma conceitual, o funcionamento da aplicação pode ser representado pelo seguinte fluxo:

`ação do usuário → evento → lógica JavaScript → processamento → atualização do DOM`

Quando existe persistência de dados, o fluxo pode incluir:

`interface → JavaScript → localStorage → JavaScript → interface`

Na navegação SPA, o fluxo segue aproximadamente:

`navegação → roteador → identificação da rota → template → atualização do conteúdo`

Esses fluxos ajudam a compreender como as diferentes partes da aplicação se relacionam.

## Manutenibilidade

A organização adotada busca facilitar:

- identificação da responsabilidade de cada arquivo;
- localização de erros;
- reutilização de funcionalidades;
- alteração isolada de componentes;
- expansão progressiva da aplicação;
- leitura do código por outros desenvolvedores.

A modularização também prepara o projeto para futuras mudanças de arquitetura conforme novas tecnologias forem estudadas.

## Limitações atuais

O projeto foi desenvolvido como aplicação acadêmica front-end e, portanto, sua arquitetura possui limitações intencionais.

Atualmente, não existe uma infraestrutura completa de back-end, banco de dados remoto ou autenticação de usuários.

O `localStorage` é utilizado para fins de persistência local e demonstração dos conceitos estudados, não devendo ser interpretado como substituto de uma camada de persistência adequada para uma aplicação em produção.

## Evolução futura

A arquitetura poderá evoluir conforme novos conhecimentos forem incorporados ao projeto.

Entre as possibilidades estão:

- integração com APIs;
- implementação de back-end;
- utilização de banco de dados;
- autenticação e autorização;
- adoção de ferramentas de build;
- implementação de testes automatizados;
- utilização futura de frameworks front-end quando tecnicamente justificável.

A evolução deverá preservar o princípio de separação de responsabilidades adotado desde as etapas iniciais.
