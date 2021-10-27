# Design Patterns

## Falando sobre design patterns

O que é um padrão de projetos?

De forma bem resumida, padrões de projeto são formas de se documentar uma solução para um problema de modelagem. Não precisamos reiventar a roda, devemos saber apenas que ela já existe e como utilizá-la. É preciso prever ao máximo os problemas que podem aparecer durante a modelagem de um sistema e saber quais as soluções implementar para solucionar esses problemas.

Ainda mais que isso, os padrões de projetos não são novas soluções, mas soluções que foram implementadas com sucesso de forma recorrente em diferentes contextos. O livro "Padrões de Projetos: Soluções Reutilizáveis de Software Orientados a Objetos", lançado pela conhecida "A Gangue dos Quatros" em  1994, é prova viva de que a experiência e a prova do tempo consolidaram os padrões de projetos até nossos dias.

Segundo o livro "Padrões de Projetos: Soluções Reutilizáveis de Software Orientados a Objetos" um padrão tem quatro elementos essenciais:


1. O nome do padrão é uma referência que podemos usar para descrever um problema de projeto, suas soluções e conseqüências em uma ou duas palavras.
2. O problema descreve em que situação aplicar o padrão. Ele explica o problema e seu contexto. Pode descrever estruturas de classe ou objeto sintomáticas de um projeto inflexível.
3. A solução descreve os elementos que compõem o padrão de projeto, seus relacionamentos, suas responsabilidades e colaborações.
4. As conseqüências são os resultados e análises das vantagens e desvantagens (trade-offs) da aplicação do padrão. Uma vez que a reutilização é freqüentemente um
fator no projeto orientado a objetos, as conseqüências de um padrão incluem o seu impacto sobre a flexibilidade, a extensibilidade ou a portabilidade de um sistema. 

### Singleton

Garantir que uma classe tenha somente uma instância no programa e fornecer um ponto de acesso global para a mesma.

1. Garantir que uma classe tenha apenas uma única instância.
A razão mais comum para isso é para controlar o acesso a algum recurso compartilhado, por exemplo, uma base de dados, interfaces gráficas, sistemas de arquivos, servidores de impressão, etc.
2. Fornece um ponto de acesso global para aquela instância. Pense num labirinto onde só pode ter um acesso ao premio. isso é Singleton, ele permite apenas um ponto de acesso, sem recorrer a variáveis ou funções globais.

A própria classe é responsável por manter o controle da sua única instância.
```
public class SingletonExemplo() {
  private static Singleton instance;
  
  private Singleton() {}
  
  public static synchronized Singleton getInstance() {
    if(instance == null) {
      instance = new Singleton();
    }
    return instance;
  }

}
```



