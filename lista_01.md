# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

X Imprime os números pares de 1 a 10.

b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10.

d) Imprime os números ímpares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

X let carro = new Carro("Toyota");

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

X 18

B) 16

C) 14

D) 12

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?
X ![Uma imagem](assets/ex04_1.PNG)

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

X ![Uma imagem](assets/ex05_1.PNG)

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

X "Olá, meu nome é João. Olá, meu nome é Maria."

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

Criando e manipulando Animais:
- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!

resposta:

```
class Animal {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    descrever() {
        console.log(`Esse é o ${this.nome}` + `, ele tem ${this.idade} anos`);
    }
}

let cachorro = new Animal ("Toby", 5);
cachorro.descrever();

let gato = new Animal ("Miguel", 2);
gato.descrever();
```

______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método descrever() que exiba no console uma descrição do animal com seu nome e idade.

Classe Gato (Herda de Animal):
- Crie uma classe chamada Gato que herda da classe Animal.
- Adicione um atributo extra cor específico para gatos.
- Adicione um método miar() que exiba no console o som que um gato faz.

Criando Animais:
- Crie dois objetos da classe Animal: um chamado cachorro e outro gato, com idades distintas.
- Para o gato, também defina a cor.

Chamando os Métodos:
- Para cada animal, chame o método descrever() para ver a descrição no console.
- Para o gato, chame o método miar() para "ouvir" o som que ele faz (é também para ver o som no console).

Dica: Utilize console.log() para exibir as informações!

```
class Animal {
    constructor(nome, idade) {
        this.nome = nome;
        this.idade = idade;
    }

    descrever() {
        console.log(`Esse é o ${this.nome}` + `, ele tem ${this.idade} anos`);
    }
}

class Gato extends Animal {
    constructor(nome, idade, cor) {
    super (nome, idade);
    this.cor = cor;
    }

    miar() {
        console.log(`Miau`);
    }

    descrever() {
        console.log(`Esse é o ${this.nome}` + `, ele tem ${this.idade} anos e é da cor ${this.cor}`);
    }
}

let gato = new Gato ("Miguel", 2, "preta");
gato.miar();
gato.descrever();

let cachorro = new Animal ("Toby", 5);
cachorro.descrever();
```
______


**9)** Vamos criar um programa em JavaScript para somar notas!

Classe SomadorDeNotas:
- Crie uma classe chamada SomadorDeNotas.
- Adicione um atributo total inicializado com 0 para armazenar a soma das notas.

Método adicionarNota:
- Adicione um método chamado adicionarNota(nota) na classe SomadorDeNotas.
- Este método deve receber um parâmetro nota e somá-lo ao atributo total.

Criando o Somador e Adicionando Notas:
- Crie um objeto da classe SomadorDeNotas, chamado somador.
- Utilize o método adicionarNota(nota) para adicionar algumas notas ao somador.

Chamando o Método para Ver o Total:
- Após adicionar todas as notas, chame um método verTotal() para exibir o total das notas adicionadas.

Dica: Utilize console.log() para exibir as informações!

```
class SomadorDeNotas {
    constructor(total){
        this.total = 0
    }

    adicionarNota(nota){
        return this.total += nota;
    }

    verTotal(){
        console.log(`A soma das notas é igual a ${this.total}`);
    }
}

let somador = new SomadorDeNotas;
somador.adicionarNota(5);
somador.adicionarNota(7);
somador.adicionarNota(9);
somador.adicionarNota(8.9);

somador.verTotal();
```

______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

Funcionário:
- atributo: Nome
- atributo: Idade
- atributo: Salário base
- método: calcularSalario() - Este método calcula o salário total do funcionário. Para cada tipo de funcionário, o cálculo será diferente.

Professor (herança de Funcionário):
- atributo: Disciplina
- atributo: Horas de aula por semana
- método: calcularSalario() - Para calcular o salário do professor, multiplicamos suas horas de aula pelo valor da hora/aula.

Agora, sua tarefa é escrever um código em JavaScript que crie as classes Funcionário e Professor, com suas características e métodos descritos acima. Depois de criar as classes, crie:
- Dois objetos do tipo Professor com informações fictícias.
- Para cada objeto, chame o método calcularSalario() e mostre o salário calculado no console.

Certifique-se de explicar cada parte do código utilizando comentários, explicando para que serve cada atributo e método, bem como a lógica por trás do cálculo de salário para o tipo de funcionário Professor.

```
// é criada a classe funcionário com seus atributos

class Funcionario {
    constructor(nome, idade, salarioBase){
    this.nome = nome;
    this.idade = idade;
    this.salarioBase = salarioBase;
    }
    
// o método calcular salario genérico é igualado ao salário base, já que não existem mais informações sobre o cálculo
    calcularSalario() {
       return salario = salarioBase;
    }
}

// é criada a classe professor que pega os atributos de funcionário
class Professor extends Funcionario {
    constructor(nome, idade, salarioBase, disciplina, horas) {
    super (nome, idade, salarioBase) 
// são adicionados dois novos atributos a classe professor além dos já existentes em funcionário
    this.disciplina = disciplina;
    this.horas = horas;
    }

// o cálculo do salário é feito multiplicando o número de horas por 14 (valor por cada hora)
    calcularSalario(){
// o console.log só leva em consideração os atributos nome e horas
        console.log (`Salário do ${this.nome} é igual a ` + 14 * this.horas + ` reais`);
    }
    
}

// é criada a variável professor 1, com todos seus atributos e cálculo de salário
let professor1 = new Professor ("Cris", 40, 2000, "matemática", 50);
professor1.calcularSalario();

// é criada a variável professor 2, com todos seus atributos e cálculo de salário
let professor2 = new Professor ("Filipe", 30, 2500, "história", 60);
professor2.calcularSalario();
```
