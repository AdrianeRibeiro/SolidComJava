# Revisão Conceitos POO

<br>

<b> Coesão </b>
- Uma classe que executa bem uma única tarefa, de forma concisa. 
- Cada classe deve ser responsável por apenas uma coisa, e deve executar esta tarefa muito bem.

<br>

<b> Encapsulamento </b>
- É uma forma de manter os objetos das classes protegidos, fornecendo apenas o que é estritamente necessário para o mundo exterior. 
- Ao encapsular o acesso a determinados dados, liberando acesso apenas ao necessário, os objetos da classe se tornam mais fáceis de serem utilizados.
- Getters e setters por si só não fornecem nenhum tipo de encapsulamento. Na verdade, quebra o encapsulamento da classe. Métodos set permitem manipular o atributo, mesmo que ele seja privado, podendo dessa forma ter uma violação de regras de negócio.

<br>

<b> Acoplamento </b>
- É a dependência entre classes. É comum que classes dependam de outras para executar determinadas tarefas. O problema é uma classe saber demais da outra.
- Quando uma classe A chama uma classe B. Dependência demais da classe A com relação a classe B. Qualquer alteração na classe B impacta A.

<br>

# SOLID com Java: Princípios da programação orientada a objetos

<br>

<b> Single Responsibily Principle: princípio da responsabilidade única </b>
- Uma classe (ou módulo, função, etc) deve ter um e apenas um motivo para mudar.
- Relacionado a coesão.
- Facilita a manutenção.

<br>

<b> Open Closed Principle: princípio Aberto/Fechado </b>
- Um sistema deve ser aberto para a extensão, mas fechado para a modificação. Ou seja, devemos poder criar novas funcionalidades e estender o sistema sem precisar modificar muitas classes já existentes.
- Ao usar esse princípio acaba-se implementando também os princípios S e D.

<br>

<b> Liskov Substitution Principle: princípio de substituição de Liskov </b>
- Embora a herança favoreça o reaproveitamento de código, ela pode trazer efeitos colaterais quando não utilizada da maneira correta, fazendo com que se herde comportamentos indevidos.
- Por exemplo: O sistema de rh da empresa A possui a classe Funcionário, com o métodos de reajuste salarial e promoção de cargo. Recentemente, a empresa A passou a atulizar o serviço de terceirização da empresa B.  Ao utilizar a herança, fazendo a classe Terceirização herdar de Funcionario, teria-se a herança desses métodos. Contudo, a empresa B deve ser responsável pelo ajuste e promoção do funcionário terceirizado e não a empresa A.  

<br>

<b> Dependency Inversion Principle: princípio da inversão de dependências  </b>
- Abstrações não devem depender de implementações. A implementação sim é que deveria depender de uma abstração.
- Ao depender de interfaces e não de implementações, caso uma determinada implementação mude, não seremos afetados, pois dependemos apenas de sua interface. Se um método muda a forma como realiza sua tarefa, desde que a interface se mantenha, não vamos precisar nos preocupar nem em editar o nosso código.

<br>

<b> Interface Segregation Principle: princípio de segregação de interface </b>
- Uma classe não deveria ser forçada a depender de métodos que não utilizará.
- Uma classe não deve ser obrigada a implementar um método de determinada interface, se ele não será útil. Para isso, uma interface deverá ser extraída apenas com os métodos necessários.

<br>

<hr>

Referência:
https://cursos.alura.com.br/course/solid-orientacao-objetos-java
