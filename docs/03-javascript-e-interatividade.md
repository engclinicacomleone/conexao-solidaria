# JavaScript e interatividade

## Objetivo

Nesta etapa, o Conexão Solidária evoluiu de uma interface predominantemente estática para uma aplicação web com comportamentos dinâmicos implementados em JavaScript.

O desenvolvimento teve como foco a manipulação do DOM, o gerenciamento de eventos, a navegação em página única, a geração dinâmica de componentes, a validação de formulários, a persistência local de dados e a organização modular do código.

## Single Page Application

A navegação da aplicação foi estruturada seguindo o conceito de Single Page Application (SPA).

Em vez de realizar o recarregamento completo da página a cada interação, o JavaScript controla a navegação e atualiza dinamicamente a região principal da interface.

A implementação utiliza recursos da History API do navegador, incluindo:

- `pushState()` para registrar mudanças de navegação;
- `popstate` para responder às ações de avançar e voltar do navegador;
- interceptação de eventos de navegação;
- atualização dinâmica do conteúdo exibido.

Essa abordagem permite manter a estrutura principal da aplicação enquanto apenas o conteúdo necessário é atualizado.

## Manipulação do DOM

O Document Object Model (DOM) é utilizado como principal mecanismo de comunicação entre a lógica JavaScript e os elementos apresentados ao usuário.

A aplicação utiliza JavaScript para:

- localizar elementos da interface;
- alterar conteúdos;
- criar componentes dinamicamente;
- modificar classes e estados visuais;
- responder às ações realizadas pelo usuário;
- atualizar a interface sem recarregar todo o documento.

Essa etapa permitiu compreender a relação entre a estrutura HTML e o comportamento da aplicação.

## Templates dinâmicos

Partes da interface são geradas dinamicamente a partir de estruturas de dados JavaScript.

Arrays de objetos podem ser processados utilizando métodos como:

- `map()`;
- `join()`;
- Template Literals.

Com isso, os dados são transformados em componentes visuais sem a necessidade de repetir manualmente estruturas HTML semelhantes.

O fluxo pode ser representado de forma simplificada como:

`dados → processamento JavaScript → template → interface`

Essa abordagem melhora a reutilização e facilita futuras alterações nos componentes.

## Gerenciamento de eventos

A interatividade da aplicação é baseada no monitoramento de eventos gerados pelo usuário.

Entre os eventos considerados estão:

- cliques;
- navegação;
- envio de formulários;
- alterações em campos;
- ações realizadas em elementos criados dinamicamente.

Em situações necessárias, `preventDefault()` é utilizado para impedir o comportamento padrão do navegador e permitir que a própria aplicação controle determinada ação.

Também foi utilizada delegação de eventos para lidar de maneira eficiente com elementos inseridos dinamicamente no DOM.

## Validação de formulários

Os formulários possuem rotinas de validação executadas antes do processamento dos dados.

Entre as verificações realizadas estão:

- campos obrigatórios;
- valores vazios;
- espaços em branco;
- formatos inválidos;
- consistência dos dados informados.

Quando uma inconsistência é identificada, a interface fornece feedback visual ao usuário.

Essa abordagem busca impedir o processamento de dados inadequados e melhorar a experiência de utilização da aplicação.

## Persistência com localStorage

Para simular a persistência de informações sem a necessidade de um back-end, foi utilizado o `localStorage` do navegador.

Os dados estruturados em JavaScript são convertidos para JSON antes do armazenamento:

`JSON.stringify()`

Quando recuperados, são novamente transformados em estruturas JavaScript:

`JSON.parse()`

O fluxo utilizado pode ser representado como:

`objeto JavaScript → JSON → localStorage → JSON → objeto JavaScript`

Essa implementação permite preservar determinadas informações mesmo após o recarregamento da página.

## Modularização

À medida que a aplicação ganhou novas responsabilidades, o código JavaScript foi separado de acordo com suas funcionalidades.

A estrutura considera módulos responsáveis por diferentes partes do comportamento da aplicação, como:

- roteamento;
- templates;
- formulários;
- persistência de dados.

A comunicação entre módulos utiliza recursos de `import` e `export`.

Essa separação reduz o acoplamento entre funcionalidades e facilita leitura, manutenção, testes e evolução do código.

## Testes e depuração

Durante o desenvolvimento foram realizados testes voltados principalmente aos fluxos de interação da aplicação.

Entre os cenários avaliados estavam:

- entradas inválidas em formulários;
- campos contendo apenas espaços;
- comportamentos inesperados de navegação;
- persistência e recuperação de dados;
- funcionamento dos eventos;
- atualização dinâmica da interface.

As ferramentas de desenvolvimento do navegador foram utilizadas para inspeção do DOM, análise do console e identificação de comportamentos incorretos.

Os problemas identificados foram analisados, corrigidos e novamente testados.

## Aprendizados

Esta etapa demonstrou como JavaScript conecta dados, comportamento e interface em uma aplicação web.

Além da implementação das funcionalidades, tornou-se evidente a importância de separar responsabilidades, compreender o fluxo dos eventos e utilizar métodos de depuração de forma sistemática.

A experiência também estabeleceu uma base prática para compreender futuramente frameworks e bibliotecas JavaScript, já que muitos desses recursos abstraem conceitos fundamentais trabalhados diretamente nesta implementação.

## Próximas melhorias

Como evolução técnica do projeto, poderão ser explorados:

- ampliação dos testes automatizados;
- tratamento mais estruturado de erros;
- melhoria das mensagens de validação;
- refinamento da arquitetura modular;
- gerenciamento mais robusto do estado da aplicação;
- integração futura com APIs e serviços de back-end;
- estudo de frameworks baseados nos fundamentos implementados em Vanilla JavaScript.
