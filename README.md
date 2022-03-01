# java
## introdução ao java
em java, todo aplicativo começa com um nome de classe que deve ser o mesmo do nome do arquivo 
 criaremos um arquivo chamado Main.java
```` java
public class Main {
  public static void main(String[] args) {
    System.out.println("ola me chamo igor");
  }
}

````  
para execultar o codigo acima devemos ir ate o arquivo no terminal e colocar:
```` sh
javac nomedoarquivo.java
```` 
apos isso ele falare se existe algum erro agora é so colocar:
```` sh
java Nomedoarquivo
````  
nos iremos mostrar em detalhes o codigo abaixo mais a frente o resulatado deve ser `ola me chamo igor`
## sintaxe no java
 toda lina execultada no java deve SEMPRE estar dentro de um arquivo `class` no exemplo da outra aula nomeamos de **Main** uma classe deve sempre começar com a primeira letra maiuscula
 o nome do arquivo java deve ser igual ao da classe 
### o metodo principal 
o `main()` método é necessário e você vera em todos os programas java
```` java
public static void main(String[] args)
```` 
qualquer codigo dentro do `main()` sera executado. agora voce nao precisa saber as palavras-chaves depois de main.conhecera pouco a pouco  
 Por enquanto, apenas lembre-se de que todo programa Java tem um `classnome` que deve corresponder ao nome do arquivo e que todo programa deve conter o método `main()`.
### System.out.println()
Dentro do método `main()`, podemos usar o método `println()` para imprimir uma linha de texto na tela:
```` java 
public static void main(String[] args) {
  System.out.println("Hello World");
}
````

## comentarios no java
Comentários de linha única começam com duas barras (`//`).  
 Comentários de várias linhas começam `/*` e terminam com `*/`.
## variaveis no java
Variáveis ​​são contêineres para armazenar valores de dados.

Em Java, existem diferentes **tipos** de variáveis, por exemplo:

* `String` - armazena texto, como "Olá". Os valores de string são cercados por aspas duplas
* `int` - armazena inteiros (números inteiros), sem decimais, como 123 ou -123
* `float` - armazena números com pontos, com decimais, como 19,99 ou -19,99
* `char` - armazena caracteres únicos, como 'a' ou 'B'. Os valores de caractere são cercados por aspas simples
* `boolean` - armazena valores com dois estados: verdadeiro(`true`) ou falso(`false`)
## criando variáveis 
Para criar uma variável, você deve especificar o tipo e atribuir um valor a ela:
```` java
type variableName = value;
```` 
 Onde type é um dos tipos de Java (como `int` ou `String), e variableName é o nome da variável (como **x** ou **name** ). O sinal de igual é usado para atribuir valores à variável.  
 Para criar uma variável que deve armazenar texto, veja a seguir: 
 Crie uma variável chamada **name** do tipo `String` e atribua a ela o valor " igor ":
```` java
String name = "igor";
System.out.println(name);
````

 Para criar uma variável que deve armazenar numero inteiro, veja a seguir: 
 Crie uma variável chamada **myNum** do tipo `int` e atribua a ela o valor **15**:
```` java
int myNum = 15;
System.out.println(myNum);
```` 
 para declarar uma variável sem atribuir o valor e atribuir o valor posteriormente:
```` java
int myNum;
myNum = 15;
System.out.println(myNum);
```` 
Altere o valor de `myNum` de `15` para `20`:
```` java 
int myNum = 15;
myNum = 20;  // myNum agora é 20
System.out.println(myNum);
```` 
#### variaveis finais
No entanto, você pode adicionar a palavra-chave `fiunal` se não quiser que outros (ou você mesmo) substituam os valores existentes (isso declarará a variável como "final" ou "constante", o que significa imutável e somente leitura):
```` java
final int myNum = 15;
myNum = 20;  // irá gerar um erro: não é possível atribuir um valor a uma variável final
````

#### outros tipos de variaveis
Uma demonstração de como declarar variáveis ​​de outros tipos:
```` java
int myNum = 5;
float myFloatNum = 5.99f;
char myLetter = 'D';
boolean myBool = true;
String myText = "Hello";
```` 
#### variaveis de exibição
 O metodo `println()` é frequentemente usado para exibir variáveis.  
 Para combinar texto e uma variável, use o `+` caractere:
```` java
String name = "John";
System.out.println("Hello " + name);
```` 
também podemos usar o ` + ` para adicionar uma variável a outra variável:
```` java
String firstName = " Igor ";
String lastName = "Silva";
String fullName = firstName + lastName;
System.out.println(fullName);
```` 
Para valores numéricos, o ` + ` caractere funciona como um operador matemático (observe que usamos `int` variáveis ​​(inteiro) aqui):
```` java
int x = 5;
int y = 6;
System.out.println(x + y); // mostra o resultado da soma de x + y
```` 
A partir do exemplo acima, você pode esperar:

* x armazena o valor 5
* y armazena o valor 6
Em seguida, usamos o método `println()` para exibir o valor de x + y, que é 11
#### declarar muitas variáveis
para declarar mais de uma variavel do **mesmo tipo** use uma lista separada por virgulas:
```` java 
int x = 5, y = 6, z = 50;
System.out.println(x + y + z);
```` 
#### identificadores java
 Todas as variáveis ​​Java devem ser identificadas com nomes exclusivos .  

 Esses nomes exclusivos são chamados de identificadores .  

 Os identificadores podem ser nomes curtos (como x e y) ou nomes mais descritivos (idade, soma, volume total).  

 Nota: Recomenda-se usar nomes descritivos para criar um código compreensível e sustentável:  
```` java
int minutesPerHour = 60;

// OK, mas não é tão fácil entender o que m realmente é
int m = 60;
```` 
* Os nomes podem conter letras, dígitos, sublinhados e cifrões
* Os nomes devem começar com uma letra
* Os nomes devem começar com uma letra minúscula e não podem conter espaços em branco
* Os nomes também podem começar com $ e _ (mas não o usaremos neste tutorial)
* Os nomes diferenciam maiúsculas de minúsculas ("myVar" e "myvar" são variáveis ​​diferentes)
* Palavras reservadas (como palavras-chave Java, como `int` ou `boolean`) não podem ser usadas como nomes
## tipos de dados
Conforme explicado no capítulo anterior, uma variável em Java deve ser um tipo de dado especificado:
```` java
int myNum = 5;               // inteiro
float myFloatNum = 5.99f;    // decimal
char myLetter = 'D';         // caractere
boolean myBool = true;       // Boolean
String myText = "Hello";     // String
```` 
os tipos de dados primitivos são divididos em dois grupos
* Tipos de dados primitivos - inclui `byte`, `short`, `int`, `long`, `float`, `double` e `boolean` `char`
*Tipos de dados não primitivos - como String , Arrays e Classes

| tipos de dados|tamanho|descrição|
|---|---|---|
|byte |1 byte|Armazena números inteiros de -128 a 127|
|short |2 bytes|Armazena números inteiros de -32.768 a 32.767|
|int |4 bytes|Armazena números inteiros de -2.147.483.648 a 2.147.483.647|
|long |8 bytes|Armazena números inteiros de -9.223.372.036.854.775.808 a 9.223.372.036.854.775.807|
|float |4 bytes|Armazena números fracionários. Suficiente para armazenar 6 a 7 dígitos decimais|
|double |8 bytes|Armazena números fracionários. Suficiente para armazenar 15 dígitos decimais|
|boolean |1 bit|Armazena valores verdadeiros ou falsos|
|char|2 bytes|Armazena um único caractere/letra ou valores ASCII|
### tipos inteiros
#### byte 
O tipo de dados `byte` pode armazenar números inteiros de -128 a 127. Isso pode ser usado em vez de `int` ou outros tipos inteiros para economizar memória quando você tiver certeza de que o valor estará entre -128 e 127:
```` java
byte myNum = 100;
System.out.println(myNum);
```` 
#### short
o tipo de dado `short` pode armazenar números inteiros de -32768 a 32767:
```` java
short myNum = 5000;
System.out.println(myNum);
```` 
#### inteiro
O tipo de dados `int` pode armazenar números inteiros de -2147483648 a 2147483647. Em geral, e em nosso tutorial, o tipo de dados `int` é o tipo de dados preferido quando criamos variáveis ​​com valor numérico.
```` java
int myNum = 100000;
System.out.println(myNum);
```` 
#### long
o tipo de dados `long` pode armazenar números inteiros de -9223372036854775808 a 9223372036854775807. Isso é usado quando int não é grande o suficiente para armazenar o valor. Observe que você deve terminar o valor com um "L":
```` java
long myNum = 15000000000L;
System.out.println(myNum);
```` 
### tipo decimais
Você deve usar um tipo de ponto flutuante sempre que precisar de um número com decimal, como 9,99 ou 3,14515.
#### float
o tipo de dados `float` pode armazenar números fracionários de 3.4e−038 a 3.4e+038. Observe que você deve terminar o valor com um "f":
```` java
float myNum = 5.75f;
System.out.println(myNum);
```` 
#### double 
o tipo de dados `double` pode armazenar números fracionários de 1.7e−308 a 1.7e+308. Observe que você deve terminar o valor com um "d":
```` java
double myNum = 19.99d;
System.out.println(myNum);
```` 
#### Usar `float` ou `double`?
A **precisão** de um valor com virgula indica quantos dígitos o valor pode ter após o ponto decimal. A precisão de `float` é de apenas seis ou sete dígitos decimais, enquanto `double` as variáveis ​​têm uma precisão de cerca de 15 dígitos. Portanto, é mais seguro usar `double` para a maioria dos cálculos.
#### numeros cientificos
Um número de com virgula também pode ser um número científico com um "e" para indicar a potência de 10:
```` java
float f1 = 35e3f;
double d1 = 12E4d;
System.out.println(f1);
System.out.println(d1);
````

#### boolean
o tipo de dados booleano é declarado com a palavra-chave `boolean` e só pode receber os valores `true` ou `false`:
```` java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // retorna true
System.out.println(isFishTasty);   // retorna false
```` 
#### caracter
O tipo de dados `char` é usado para armazenar um único caractere. O caractere deve estar entre aspas simples, como 'A' ou 'c':
````java
char myGrade = 'B';
System.out.println(myGrade);
```` 
#### string
O tipo de dados `String` é usado para armazenar uma sequência de caracteres (texto). Os valores de string devem estar entre aspas duplas:
```` java
String greeting = "Hello World";
System.out.println(greeting);
```` 
### tipos de dados nao primitivos
 Tipos de dados não primitivos são chamados de tipos de referência porque se referem a objetos.

 A principal diferença entre tipos de dados primitivos e não primitivos são:
* Tipos primitivos são predefinidos (já definidos) em Java. Tipos não primitivos são criados pelo programador e não são definidos por Java (exceto para `String`).
* Tipos não primitivos podem ser usados ​​para chamar métodos para realizar certas operações, enquanto tipos primitivos não podem.
* Um tipo primitivo sempre tem um valor, enquanto tipos não primitivos podem ser `null`.
* Um tipo primitivo começa com uma letra minúscula, enquanto os tipos não primitivos começam com uma letra maiúscula.
* O tamanho de um tipo primitivo depende do tipo de dados, enquanto os tipos não primitivos têm todos o mesmo tamanho.

 Exemplos de tipos não primitivos são Strings , Arrays , Classes, Interface , etc. 
