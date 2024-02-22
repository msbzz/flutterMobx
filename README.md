# Gerenciando estados com Provider

Este projeto é fruto do curso de 'Flutter: aplicando gerenciamento de estados com MobX' da plataforma ALURA

## Introdução

  Dado aplicativo um aplicativo de delivery chamado Panucci Delivery, com layout pronto, será dada continuidade nas ações adicionar itens na sacola de compras e conferir o valor total na parte inferior da tela. Clicando no botão "Ver carrinho", seremoss redirecionados para a página de checkout, onde é possível validar os itens escolhidos e finalizar o pedido.

  Utilizaremos o gerenciador de estados MobX. Estudaremos conceitos como actions e observables (observáveis). Também aprendemos como recuperar as informações dos observáveis e transportá-los para toda nossa aplicação, utilizando provider.

<img src="info/app.inicial.png" alt="app inicial" style="width: 15%; display: block;"/>

## Ferramentas utilizadas

 - mobx: É uma biblioteca de gerenciamento de estado para Dart que permite que se crie stores para gerenciar o estado da aplicação de forma reativa, facilitando a comunicação entre os componentes da UI e o estado da aplicação. Com MobX, quando o estado é atualizado, todos os componentes que dependem desse estado são automaticamente re-renderizados.

- flutter_mobx: É o pacote que integra o MobX com o Flutter, fornecendo widgets e funcionalidades que permitem a reatividade do MobX dentro dos aplicativos Flutter. Ele oferece, por exemplo, o widget Observer, que é usado para observar as mudanças nos stores MobX e reconstruir automaticamente a UI quando o estado observado muda.

- provider: Biblioteca de gerenciamento de estado para Flutter, recomendada pela equipe do Flutter. Ela funciona com um mecanismo diferente do MobX, baseado em InheritedWidgets, para passar dados e gerenciar o estado através da árvore de widgets. O Provider é mais genérico e pode ser usado para injeção de dependência, além de gerenciamento de estado. Ele não é específico para MobX e pode ser usado com qualquer abordagem de gerenciamento de estado ou mesmo sem uma.

- mobx_codegen: Este pacote é uma parte importante do ecossistema MobX em Dart/Flutter, pois fornece a capacidade de user anotações em seu código com @observable, @action, @computed, etc., e o pacote gerará automaticamente o código boilerplate necessário para que essas anotações funcionem.  


- build_runner: Não é específico para MobX, mas é uma ferramenta essencial quando se usa mobx_codegen ou qualquer outra biblioteca que requer geração de código em Dart. build_runner é uma ferramenta que automatiza o processo de geração de código, compilando o código fonte Dart, incluindo o código gerado por mobx_codegen. Você o executa a partir da linha de comando para gerar o código necessário para suas anotações MobX, bem como para outras tarefas de geração de código que possam ser necessárias em seu projeto Flutter.

