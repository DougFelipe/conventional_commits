# Controle de Versão e Conventional Commits

Este repositório é dedicado ao estudo e aplicação de práticas de Controle de Versão e Conventional Commits, fundamentais para a colaboração eficiente e gestão de projetos de software. 

Aqui é explorada a importância do Controle de Versão, o papel dos commits no desenvolvimento de software, e como a adoção de Conventional Commits pode melhorar significativamente a clareza e utilidade das mensagens de commit, servindo como um recurso de consulta aqueles que desejam adotar padrões de commits que facilitam a manutenção e colaboração em projetos de software.


- [Controle de Versão e Conventional Commits](#controle-de-versão-e-conventional-commits)
  - [Por que o Controle de Versão é Importante?](#por-que-o-controle-de-versão-é-importante)
- [Commit e Controle de Versão](#commit-e-controle-de-versão)
  - [Importância dos Commits no Desenvolvimento de Software](#importância-dos-commits-no-desenvolvimento-de-software)
- [Conventional Commits](#conventional-commits)
  - [Para que servem?](#para-que-servem)
  - [Importância no Desenvolvimento de Software e Controle de Versão](#importância-no-desenvolvimento-de-software-e-controle-de-versão)
- [Como Utilizar Conventional Commits](#como-utilizar-conventional-commits)
- [Tipos de Conventional Commits](#tipos-de-conventional-commits)
  - [feat: Novas Funcionalidades](#1-feat-novas-funcionalidades)
  - [fix: Correções de Bugs](#2-fix-correções-de-bugs)
  - [docs: Documentação](#3-docs-documentação)
  - [refactor: Refatoração](#4-refactor-refatoração)
  - [test: Testes](#5-test-testes)
  - [perf: Performance](#6-perf-performance)
  - [style: Estilo](#7-style-estilo)
  - [build: Processo de Build](#8-build-processo-de-build)
  - [ci: Integração Contínua](#9-ci-integração-contínua)
  - [config: Configurações](#10-config-configurações)
  - [access: Acessibilidade](#11-access-acessibilidade)
  - [data: Manipulação de Dados](#12-data-manipulação-de-dados)
  - [security: Segurança](#13-security-segurança)
  - [dependency: Dependências](#14-dependency-dependências)
  - [chore: Tarefas Diversas](#15-chore-tarefas-diversas)
  - [revert: Reverter](#16-revert-reverter)
  - [merge: Fusão de Branches](#17-merge-fusão-de-branches)
  - [release: Lançamentos](#18-release-lançamentos)
  - [cleanup: Limpeza de Código](#19-cleanup-limpeza-de-código)
  - [experiment: Experimentações](#20-experiment-experimentações)
- [Boas Práticas](#boas-práticas)
- [Referências Úteis](#referências-úteis)


## Controle de Versão e Conventional Commits

O Controle de Versão registra alterações em um arquivo ou conjunto de arquivos ao longo do tempo, permitindo que você recupere versões específicas posteriormente. Essa prática é fundamental no desenvolvimento de software, onde muitos desenvolvedores estão manipulando o mesmo código-fonte.

### Por que o Controle de Versão é Importante?

- **Colaboração Eficiente**: Facilita o trabalho simultâneo de vários desenvolvedores em um único projeto, minimizando conflitos de código.
  
- **Histórico Completo**: Cada alteração feita no repositório é rastreada, incluindo o autor, a descrição da alteração e a data, o que simplifica a compreensão da evolução do projeto.
  
- **Gestão de Releases**: Permite marcar pontos específicos na história do projeto como importantes (releases) facilitando o gerenciamento de versões estáveis.
  
- **Desfazer Alterações**: Oferece a possibilidade de reverter para versões anteriores do projeto, o que é crucial para a correção de erros ou a descontinuação de funcionalidades indesejadas.
  
- **Experimentação e Branching**: Os desenvolvedores podem criar ramificações (branches) isoladas para experimentar novas ideias sem afetar o código principal, promovendo a experimentação segura.
  
- **Recuperação de Desastres**: Em caso de falhas críticas ou perda de dados, o sistema de controle de versão atua como uma rede de segurança, permitindo uma recuperação rápida e eficaz para estados anteriores estáveis do software.
  
- **Integração e Deploy**: Modernos sistemas de controle de versão estão frequentemente integrados com pipelines de CI/CD (Integração Contínua/Delivery Contínuo), automatizando testes e deploy, o que aumenta a eficiência e a confiabilidade do lançamento de novas versões do software.
  
- **Escalabilidade**: À medida que os projetos de software crescem em complexidade e tamanho de equipe, o controle de versão se torna ainda mais crucial. Ele suporta a expansão sem sacrificar a organização ou a integridade do projeto.

O Controle de Versão é essencial para o desenvolvimento de software moderno, promovendo a colaboração, a segurança e a eficiência no gerenciamento de projetos.

## Commit e Controle de Versão 

Um "commit" é uma gravação de alterações feitas no código-fonte ou em arquivos de um projeto de software em um repositório de controle de versão. Ele atua como uma "fotografia" do estado atual do projeto, permitindo que os desenvolvedores documentem o progresso e façam anotações sobre as mudanças realizadas. Cada commit inclui uma mensagem explicativa que fornece contexto sobre o que foi alterado e por quê, facilitando a compreensão do histórico do projeto. 

Commits são fundamentais no desenvolvimento de software, atuando como marcos individuais que documentam a evolução de um projeto. Eles são mais do que simples atualizações; cada commit encapsula um progresso significativo ou uma correção essencial, tornando-o uma parte intrínseca da narrativa do desenvolvimento.

### Importância dos Commits no Desenvolvimento de Software

- **Documentação Precisa**: Cada commit oferece uma descrição detalhada do que foi alterado, servindo como uma documentação precisa que facilita o entendimento das modificações realizadas ao longo do tempo.

- **Responsabilidade**: Ao associar cada conjunto de alterações a um autor específico, os commits fomentam um ambiente de responsabilidade, onde cada contribuição pode ser atribuída a um indivíduo.

- **Milestones de Desenvolvimento**: Os commits podem ser utilizados como pontos de referência para o progresso do projeto, ajudando na organização de tarefas e na definição de objetivos claros de desenvolvimento.

- **Facilitação de Revisões**: Os commits permitem que as revisões de código sejam mais estruturadas e focadas, já que cada commit é uma unidade de mudança que pode ser analisada isoladamente.

- **Suporte à Colaboração Assíncrona**: Em um ambiente de trabalho distribuído, os commits permitem que os membros da equipe contribuam e atualizem o projeto em seus próprios horários, mantendo a continuidade do desenvolvimento.

## Conventional Commits

*Conventional Commits* são convenções de nomenclatura para mensagens de *commit* que enfatizam com clareza as modificações realizadas. Essa abordagem padroniza as mensagens de *commit*, tornando-as mais informativas e fáceis de entender.

Eles são estruturados de forma a destacar o tipo de mudança feita, o escopo da mudança, e uma descrição clara da alteração ou adição.

### Para que servem?

- **Comunicação Clara**: Proporcionam uma visão imediata do tipo de alterações incluídas em um *commit*, facilitando a revisão de código e o entendimento rápido das mudanças.

### Importância no Desenvolvimento de Software e Controle de Versão

- **Histórico Organizado**: Contribuem para um histórico de projeto mais organizado e pesquisável, permitindo que desenvolvedores compreendam rapidamente a natureza das alterações.
  
- **Facilitação de Rollbacks**: Em casos de necessidade de reverter mudanças, a clareza nas mensagens de *commit* permite identificar rapidamente quais *commits* devem ser revertidos ou ajustados.
  
- **Integração Contínua**: Com mensagens padronizadas, é possível automatizar partes do processo de integração contínua, como a execução de testes específicos com base no tipo de *commit*.
  
- **Melhoria na Colaboração**: A padronização de mensagens melhora significativamente a colaboração em equipe, pois todos os membros têm expectativas claras sobre a estrutura e o conteúdo das mensagens de *commit*.
  
- **Gerenciamento de Versões Semânticas**: Facilita o uso de versões semânticas ao permitir que ferramentas automatizadas incrementem números de versão com base no tipo de alterações indicadas pelas mensagens de *commit*.

Adotar *Conventional Commits* é uma prática que reforça a disciplina e a clareza no registro de mudanças, beneficiando não apenas o processo de desenvolvimento individual, mas também a colaboração em equipe e a gestão eficaz do ciclo de vida do software.


## Como Utilizar Conventional Commits

1. **Estrutura da Mensagem**: Cada mensagem de commit deve ter um cabeçalho, composto por um tipo, um escopo opcional, e uma descrição.

- A estrutura básica é: `<tipo>[escopo opcional]: <descrição>`.

2. **Escopo**: Opcionalmente, inclua um escopo que esclareça o contexto da alteração. O escopo pode ser o nome de um módulo ou componente.

3. **Descrição**: A descrição deve ser concisa e explicar o motivo da alteração, não o que foi mudado.

##  Tipos de Conventional Commits

### 1) feat: Novas Funcionalidades
Adiciona novas funcionalidades ou melhorias significativas ao projeto.

#### Exemplos:
- feat(auth): implementa autenticação baseada em JWT
- feat(ui): adiciona tema escuro
- feat(api): suporta filtragem de dados na API de usuários

### 2) fix: Correções de Bugs
Corrige problemas no código que afetam o comportamento esperado do software.

#### Exemplos:
- fix(login): corrige redirecionamento após o login
- fix(cart): ajusta cálculo de total quando item é removido
- fix(email): resolve problema de codificação em e-mails enviados

### 3) docs: Documentação
Atualiza ou melhora a documentação do projeto.

#### Exemplos:
- docs(readme): atualiza instruções de instalação
- docs(changelog): adiciona notas de release para a versão 2.1
- docs(api): melhora documentação dos endpoints

### 4) refactor: Refatoração
Melhora a estrutura interna do código sem alterar seu comportamento externo.

#### Exemplos:
- refactor(cart): simplifica lógica de adição de itens
- refactor(utils): unifica funções de formatação de data
- refactor(api): separa rotas em diferentes arquivos para clareza

### 5) test: Testes
Adiciona ou altera testes automatizados.

#### Exemplos:
- test(auth): adiciona testes para o fluxo de autenticação
- test(ui): implementa testes para o novo componente de carrossel
- test(api): aumenta cobertura de testes para o controller de usuário

### 6) perf: Performance
Melhora a performance e eficiência do software.

#### Exemplos:
- perf(api): otimiza consulta de banco de dados para listagem de produtos
- perf(images): implementa lazy loading para imagens na homepage
- perf(build): reduz tamanho do bundle através de tree shaking

### 7) style: Estilo
Ajusta espaços em branco, formatação e outros elementos que não alteram o significado do código.

#### Exemplos:
- style(lint): corrige warnings de lint em vários arquivos
- style(format): aplica formatação com Prettier
- style(comments): remove comentários obsoletos

### 8) build: Processo de Build
Altera o sistema de build ou atualiza dependências externas.

#### Exemplos:
- build(webpack): atualiza para a versão mais recente do Webpack
- build(deps): atualiza React para a versão mais recente
- build(ci): adiciona etapa de lint ao pipeline de CI

### 9) ci: Integração Contínua
Modifica arquivos e scripts de CI/CD.

#### Exemplos:
- ci(github-actions): adiciona job para testes de integração
- ci(travis): corrige script de deploy
- ci(docker): otimiza Dockerfile para build mais rápido

### 10) config: Configurações
Modifica configurações do projeto.

#### Exemplos:
- config(eslint): adiciona regra para proibir uso de var
- config(prettier): ajusta largura máxima da linha para 100 caracteres
- config(editor): adiciona arquivo .editorconfig

### 11) access: Acessibilidade
Melhora a acessibilidade do software.

#### Exemplos:
- access(buttons): adiciona atributos aria a botões sem texto
- access(colors): ajusta contraste de cores para melhor leitura
- access(navigation): melhora navegação por teclado no menu principal

### 12) data: Manipulação de Dados
Gerencia e manipula dados.

#### Exemplos:
- data(schema): atualiza esquema do banco de dados para suportar novos campos
- data(migration): adiciona script de migração para a nova versão do esquema
- data(seed): adiciona dados de exemplo para desenvolvimento

### 13) security: Segurança
Melhora a segurança do software.

#### Exemplos:
- security(auth): corrige vulnerabilidade de injeção de SQL no login
- security(deps): atualiza bibliotecas com vulnerabilidades conhecidas
- security(https): força HTTPS em todas as páginas

### 14) dependency: Dependências
Gerencia dependências do projeto.

#### Exemplos:
- dependency(upgrade): atualiza lodash para a versão mais recente
- dependency(remove): remove biblioteca não utilizada xyz
- dependency(add): adiciona axios para requisições HTTP

### 15) chore: Tarefas Diversas
Realiza tarefas de manutenção que não se encaixam em outras categorias.

#### Exemplos:
- chore(cleanup): remove arquivos temporários
- chore(release): prepara para a versão 1.2.0
- chore(repo): atualiza .gitignore

### 16) revert: Reverter
Indica a reversão de um commit anterior.

#### Exemplos:
- revert: reverter "feat(login): add captcha to login form"
- revert: reverter "chore: update dependencies"
- revert: reverter "fix(cart): correct item count"

### 17) merge: Fusão de Branches
Representa a fusão de branches no projeto.

#### Exemplos:
- merge(feature/cool-feature): mescla branch de funcionalidade no main
- merge(hotfix/login): mescla correção de emergência no main
- merge(release/1.2): mescla branch de release no main

### 18) release: Lançamentos
Marca um novo lançamento ou versão do projeto.

#### Exemplos:
- release(1.2.0): lança versão 1.2.0
- release(2.0.0-beta): lança versão beta 2.0.0
- release(1.1.5): lança patch version 1.1.5

### 19) cleanup: Limpeza de Código
Remove código, arquivos ou dependências não utilizados ou obsoletos.

#### Exemplos:
- cleanup(unused-vars): remove variáveis não utilizadas
- cleanup(old-files): deleta arquivos antigos de design
- cleanup(deps): remove pacotes não utilizados

### 20) experiment: Experimentações
Realiza experimentações ou testes de novas ideias.

#### Exemplos:
- experiment(new-algo): testa novo algoritmo de recomendação
- experiment(feature-flag): adiciona flag de funcionalidade para teste
- experiment(ui): testa novo layout para a página inicial


## Boas Práticas

- **Mensagens Atômicas**: Cada commit deve representar uma mudança atômica e lógica. Não agrupe alterações não relacionadas.

- **Uso de Verbos no Imperativo**: Escreva a descrição do commit no imperativo: "Adiciona recurso", "Corrige bug", etc.

- **Mensagens Claras e Descritivas**: A descrição deve ser clara o suficiente para que, ao ler a mensagem do commit, outros membros da equipe possam entender o propósito da alteração sem ter que ler o código.

- **Consistência**: Adote um padrão consistente para as mensagens de commit em todo o projeto, facilitando a leitura do histórico de commits.

Ao seguir estas diretrizes, o uso de Conventional Commits ajuda a manter um histórico de commits claro e legível, facilita a geração automatizada de changelogs, e melhora a comunicação e colaboração dentro de equipes de desenvolvimento de software.


## Referências Úteis

- [Conventional Commits 1.0.0](https://www.conventionalcommits.org/pt-br/v1.0.0/)
- [Padrões de Commits Conventional Commits](https://medium.com/linkapi-solutions/conventional-commits-pattern-3778d1a1e657)
- [Padrões de Commits no GitHub](https://github.com/iuricode/padroes-de-commits)
- [Conventional Commits Cheat Sheet](https://kapeli.com/cheat_sheets/Conventional_Commits.docset/Contents/Resources/Documents/index)
- [Padronizando mensagens de commit com Conventional Commits](https://www.linkedin.com/pulse/conventional-commits-padronizando-mensagens-de-commit-diego-telles/?originalSubdomain=pt)
- [Simplificando o controle de versão com Conventional Commits](https://www.alura.com.br/artigos/simplificando-controle-versao-conventional-commits)
