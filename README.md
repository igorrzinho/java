# java
# introdução ao java
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
# sintaxe no java
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

# comentarios no java
Comentários de linha única começam com duas barras (`//`).  
 Comentários de várias linhas começam `/*` e terminam com `*/`.
# variaveis no java
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
 Onde type é um dos tipos de Java (como `int` ou `String`), e variableName é o nome da variável (como **x** ou **name** ). O sinal de igual é usado para atribuir valores à variável.  
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
# tipos de dados
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
## conversão de tipo
 A conversão de tipo é quando você atribui um valor de um tipo de dados primitivo a outro tipo.
* **Ampliação** da transmissão (feito automaticamente) - convertendo um tipo menor em um tamanho de tipo maior
`byte`-> `short`-> `char`-> `int`-> `long`-> `float`->`double`
* **Estreitando** (feito manualmente) - convertendo um tipo maior para um tipo de tamanho menor
`double`-> `float`-> `long`-> `int`-> `char`-> `short`->`byte`

## conversão de ampliação
 A conversão de ampliação é feita automaticamente ao passar um tipo de tamanho menor para um tipo de tamanho maior:
 ```` java
 public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // automaticamente converte: int para double

    System.out.println(myInt);      // retorna 9
    System.out.println(myDouble);   // retorna 9.0
  }
}
 ````
 ## conversão de redução
 A redução da conversão deve ser feita manualmente, colocando o tipo entre parênteses na frente do valor:
 ```` java
 public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78d;
    int myInt = (int) myDouble; //: conversão manual double para int

    System.out.println(myDouble);   // mostra 9.78
    System.out.println(myInt);      // mostra 9
  }
}
 ````
 # operadores java
## Operadores aritméticos
 Operadores aritméticos são usados ​​para realizar operações matemáticas comuns.
|operador|nome|descrição|exemplo|
|---|---|---|---|
|` + `|adição|Soma dois valores|x+y|
|` - `|subtração|Subtrai um valor de outro|x-y|
|` * `|multiplicação|Multiplica dois valores|x*y|
|` / `|divisão|Divide um valor por outro|x/y|
|` % `|modulo|Retorna o resto da divisão|x%y|
|` -- `|incremento|aumenta o valor de uma variável em 1|++x|
|` -- `|diminuir|Diminui o valor de uma variável em 1|--x|

## operadores de atribuição
 Os operadores de atribuição são usados ​​para atribuir valores a variáveis.

|operador|exemplo|igual|
|---|---|---|
|`=`|x = 5|x = 5|
|`+=`|x += 3|x = x + 3|
|`-=`|x -= 3|x = x - 3|
|`*=`|x *= 3|x = x * 3|
|`/=`|x /= 3|x = x / 3|
|`%=`|x %= 3|x = x % 3|
|`&=`|x &= 3|x = x & 3|
|`|=`|x |= 3|x = x | 3|
|`^=`|x ^= 3|x = x ^ 3|
|`>>=`|x >>= 3|x = x >> 3|
|`<<=`|x <<= 3|x = x << 3|
## operadores de comparação
 Os operadores de comparação são usados ​​para comparar dois valores:
|operador|nome|igual|
|---|---|---|
|`==`|igual a|x == y|
|`!=`|diferente de|x != y|
|`>`|maior que|x > y|
|`<`|menor que|x < y|
|`>=`|maior ou igual a|x >= y|
|`<=`|menor ou igual a|x <= y|
## operadores logicos
 Os operadores lógicos são usados ​​para determinar a lógica entre variáveis ​​ou valores:
|operador|nome|descrição|exemplo|
|---|---|---|---|
|` && `|and, e|Retorna verdadeiro se ambas as declarações forem verdadeiras|x < 5 &&  x < 10|
|` || `|or, ou|Retorna verdadeiro se uma das afirmações for verdadeira|x < 5 || x < 4|
|` ! `|not, negação|Reverse the result, returns false if the result is true|!(x < 5 && x < 10)|
# strings em java
 Uma `String` variável contém uma coleção de caracteres entre aspas duplas:
```` java
String greeting = "Hello";
````
## comprimento de uma string
 Uma String em Java é na verdade um objeto, que contém métodos que podem realizar certas operações em strings. Por exemplo, o comprimento de uma string pode ser encontrado com o método `length()`:
```` java
String txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
System.out.println("The length of the txt string is: " + txt.length());
````
## mais metodos de string
 Existem muitos métodos de string disponíveis, por exemplo `toUpperCase()` e `toLowerCase()`:
```` java
String txt = "Hello World";
System.out.println(txt.toUpperCase());   // mostra "HELLO WORLD"
System.out.println(txt.toLowerCase());   // mostra "hello world"
````
## encontrando um caractere em uma string
 O método `indexOf()` retorna o índice (a posição) da primeira ocorrência de um texto especificado em uma string (incluindo espaços em branco):
```` java
String txt = "Please locate where 'locate' occurs!";
System.out.println(txt.indexOf("locate")); // Outputs 7
````
## concatenação de string
O operador `+` pode ser usado entre as strings para combiná-las. Isso é chamado de concatenação :

```` java
String firstName = "John";
String lastName = "Doe";
System.out.println(firstName + " " + lastName);
````
 Você também pode usar o método `concat()` para concatenar duas strings:

```` java
String firstName = "John ";
String lastName = "Doe";
System.out.println(firstName.concat(lastName));
````
## caracteres especiais
 Como as strings devem ser escritas entre aspas, o Java interpretará mal essa string e gerará um erro:
```` java
String txt = "We are the so-called "Vikings" from the north.";
````
 A solução para evitar esse problema é usar o **caractere de escape de barra invertida .**  
 O caractere de escape de barra invertida (`\`) transforma caracteres especiais em caracteres de string:

|caractere ultilizado|resultado|descrição|
|---|---|---|
|`\'`|'|aspa unica|
|`\"`|"|aspas dupla|
|`\\`|\|barra invertida|
```` java
// A sequência \"  insere aspas duplas em uma string:
String txt = "We are the so-called \"Vikings\" from the north.";
// A sequência \'  insere uma aspa simples em uma string:
String txt = "It\'s alright.";
// A sequência \\  insere uma única barra invertida em uma string:
String txt = "The character \\ is called backslash.";
````
# java math
 A classe Java Math tem muitos métodos que permitem realizar tarefas matemáticas em números.
## Math.max(x,y)
 O método pode ser usado para encontrar o maior valor de x e y :`Math.max(x,y)`
```` java
Math.max(5,10);// retorna 10
````
## Math.min(x,y)
 esse metodo é usado para encontrar o menor valor de x e y:`Math.min(x,y)`
```` java
Math.min(5, 10);//retorna 5
````
## Math.sqrt(x)
 esse metodo retorna a raiz quadrada de x: `Math.sqrt(x)`
```` java
Math.sqrt(64);//retorna *8
````
## Math.abs(x)
 O método retorna o valor absoluto (positivo) de x :`Math.abs(x)
```` java
Math.abs(-4.7);//retorna 4.7
````
## Math.random()
 `Math.random()` retorna um número aleatório entre 0,0 (inclusive) e 1,0 (exclusivo):
```` java
Math.random();
````
 Para obter mais controle sobre o número aleatório, por exemplo, você deseja apenas um número aleatório entre 0 e 100, você pode usar a seguinte fórmula:
```` java
int randomNum = (int)(Math.random() * 101);  // 0 ate 100
````
# valores booleanos
 os valores booleno são declarados com a palavra-chave `boolean`e so podem receber os valores `true` ou `false`
```` java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // mostra true
System.out.println(isFishTasty);   // mostra false
````
No entanto, é mais comum retornar valores booleanos de expressões booleanas para testes condicionais (veja abaixo).
## expressão booleana
 Uma expressão booleana é uma expressão Java que retorna um valor booleano: `true` ou `false`.
 Você pode usar um operador de comparação, como o operador maior que (`>`) para descobrir se uma expressão (ou uma variável) é verdadeira:
```` java
int x = 10;
int y = 9;
System.out.println(x > y); //retorna true, pois 10 é maior que 9
````
 ou ainda mais facil
```` java
System.out.println(10 > 9); // retorna true, pois 10 é maior que 9
````
 usamos o operador igual a (`==) para avaliar uma expressão:
```` java
int x = 10;
System.out.println(x == 10); // retorna true, pois o valor de x é igual 10
````

```` java
System.out.println(10 == 15); // retorna false, pois 10 não é igual a 15
````
# if else
 Java suporta as condições lógicas usuais da matemática:
* Menor que: `a < b`
* Menor ou igual a: `a <= b`
* Maior que: `a > b`
* Maior ou igual a: `a >= b`
* igual a `a == b`
* Diferente de:` a != b`
Java tem as seguintes declarações condicionais:
* Use `if` para especificar um bloco de código a ser executado, se uma condição especificada for verdadeira
* Use `else` para especificar um bloco de código a ser executado, se a mesma condição for falsa
* Use `else if` para especificar uma nova condição a ser testada, se a primeira condição for falsa
* Use `switch` para especificar muitos blocos alternativos de código a serem executados
 ## declaração if
   Use a `if` instrução para especificar um bloco de código Java a ser executado se uma condição for `true.
```` java
if (condition) {
  // sera executado se a condition for true
}
````
 No exemplo abaixo, testamos dois valores para descobrir se 20 é maior que 18. Se a condição for `true, imprima algum texto:
```` java
if (20 > 18) {
  System.out.println("20 é maior que 18");
}
````
 tambem podemos usar variaveis:
```` java
int x = 20;
int y = 18;
if (x > y) {
  System.out.println("x é maior que y");
}
````
 No exemplo acima usamos duas variáveis, x e y , para testar se x é maior que y (usando o operador `>`). Como x é 20 e y é 18, e sabemos que 20 é maior que 18, imprimimos na tela que "x é maior que y".
 ## declaração else
 Use a instrução `else` para especificar um bloco de código a ser executado se a condição for `false.
```` java
if (condition) {
  // sera executado se a condição for true
} else {
  // sera executado se a condição for false
}
````

```` java
int time = 20;
if (time < 18) {
  System.out.println("bom dia.");
} else {
  System.out.println("boa noite.");
}
// retorna "boa noite."
````
No exemplo acima, o tempo (20) é maior que 18, então a condição é `false`. Por conta disso, passamos para a `else` condição e imprimimos na tela "Boa noite". Se a hora fosse menor que 18, o programa imprimiria "Bom dia".
## else if
```` java
if (condition1) {
  // sera executado se  condition1 é true
} else if (condition2) {
  //sera executado se condition1 for false e a  condition2 for true
} else {
  // sera executado se condition1 for false e condition2 for false
}
````

```` java
int time = 22;
if (time < 10) {
  System.out.println("bom dia.");
} else if (time < 20) {
  System.out.println("boa tarde.");
} else {
  System.out.println("boa noite.");
}
// retorna "boa noite."
````
No exemplo acima, o tempo (22) é maior que 10, então a primeira condição é `false`. A próxima condição, na instrução `else if`, também é `false`, então passamos para a `else` condição já que a condição1 e a condição2 são `false` e imprimimos na tela "Boa noite".

No entanto, se a hora fosse 14, nosso programa imprimiria "boa tarde".
# operador ternário
 Há também uma abreviação if else, que é conhecida como **operador ternário** porque consiste em três operandos. Ele pode ser usado para substituir várias linhas de código por uma única linha. É frequentemente usado para substituir instruções if else simples:
```` java
variable = (condition) ? se for true : se for false;
````
 em vez de escrevermos :
```` java
int time = 20;
if (time < 18) {
  System.out.println("bom dia.");
} else {
  System.out.println("boa noite.");
}
````
 podemos escrever apenas
```` java
int time = 20;
String result = (time < 18) ? "bom dia." : "boa noite.";
System.out.println(result);
````
# case java
 Use a instrução `switch` para selecionar um dos muitos blocos de código a serem executados.
```` java
switch(expression) {
  case x:
    // codigor a ser execultado
    break;
  case y:
  // codigor a ser execultado
    break;
  default:
  // codigor a ser execultado
}
````
 o case funciona assim:
* a expressão `switch` é avaliada uma vez
* O valor da expressão é comparado com os valores de cada case
* Se houver uma correspondência, o bloco de código associado será executado.
* As palavras-chave `break` e `default`são opcionais e serão descritas posteriormente

 O exemplo abaixo usa o número do dia da semana para calcular o nome do dia da semana:
```` java
int day = 4;
switch (day) {
  case 1:
    System.out.println("segunda");
    break;
  case 2:
    System.out.println("terça");
    break;
  case 3:
    System.out.println("quarta");
    break;
  case 4:
    System.out.println("quinta");
    break;
  case 5:
    System.out.println("sexta");
    break;
  case 6:
    System.out.println("sabado");
    break;
  case 7:
    System.out.println("domingo");
    break;
}
// mostra "quinta" (dia 4)
````
## palavra chave `break`

 Quando o Java atinge uma palavra-chave `break`, ele sai do bloco `switch`.

 Isso interromperá a execução de mais código e teste de caso dentro do bloco.

 Quando uma correspondência é encontrada e o trabalho está concluído, é hora de uma pausa. Não há necessidade de mais testes.
## palavra chave `default`
 A palavra-chave `default` especifica algum código a ser executado se não houver correspondência entre maiúsculas e minúsculas:
```` java
int day = 4;
switch (day) {
  case 6:
    System.out.println("hoje é sabado");
    break;
  case 7:
    System.out.println("hoje é domingo");
    break;
  default:
    System.out.println("hoje é outro dia da semana");
}
// mostra "hoje é outro dia da semana"
````
# loops em java
 Os loops podem executar um bloco de código desde que uma condição especificada seja alcançada.

 Os loops são úteis porque economizam tempo, reduzem erros e tornam o código mais legível.

## while
 O loop `while` percorre um bloco de código desde que uma condição especificada seja `true`.
```` java
while (condition) {
  // codigo para ser execultado
}
````
 No exemplo abaixo, o código no loop será executado repetidamente, desde que uma variável (i) seja menor que 5:

```` java
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
````
## do/while
O loop `do/while`é uma variante do loop`while`. Este loop executará o bloco de código uma vez, antes de verificar se a condição é verdadeira, então repetirá o loop enquanto a condição for verdadeira.

```` java
do {
  // codigo para ser execultado
}
while (condition);
````
O exemplo abaixo usa um loop `do/while`. O loop sempre será executado pelo menos uma vez, mesmo que a condição seja falsa, pois o bloco de código é executado antes que a condição seja testada:
```` java
int i = 0;
do {
  System.out.println(i);
  i++;
}
while (i < 5);
````
## loop for
 Quando você souber exatamente quantas vezes deseja percorrer um bloco de código, use o loop `for` em vez de um loop `while`:
```` java
for (statement 1; statement 2; statement 3) {
  // codigo para ser execultado
}
````
 **A instrução 1** é executada (uma vez) antes da execução do bloco de código.
 **A instrução 2** define a condição para executar o bloco de código.

 **A instrução 3** é executada (todas as vezes) após a execução do bloco de código.

 O exemplo abaixo imprimirá os números de 0 a 4:

```` java
or (int i = 0; i < 5; i++) {
  System.out.println(i);
}
````
### Exemplo explicado
 A instrução 1 define uma variável antes do início do loop (int i = 0).

 A instrução 2 define a condição para a execução do loop (i deve ser menor que 5). Se a condição for verdadeira, o loop começará novamente, se for falso, o loop terminará.

 A instrução 3 aumenta um valor (i++) cada vez que o bloco de código no loop é executado.
### exemplo 2
 Este exemplo imprimirá apenas valores pares entre 0 e 10:
```` java
for (int i = 0; i <= 10; i = i + 2) {
  System.out.println(i);
}
````
## loop for-Each
 Há também um loop **" for-each ", que é usado exclusivamente para percorrer elementos em um array**:
```` java
for (type variableName : arrayName) {
  // codigo de bloco a ser execultado
}
````
O exemplo a seguir gera todos os elementos no array cars , usando um loop " for-each ":

```` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
````

# Java Break and Continue
## java Break
 Você já viu a instrução `break` usada em um capítulo anterior deste tutorial. Foi usado para "saltar" de uma declaração `switch`.

 a instrução `break` também pode ser usada para sair de um **loop**.

 Este exemplo interrompe o loop quando i é igual a 4:
```` java
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    break;
  }
  System.out.println(i);
}
````
## Java Continue
 A instrução `continue` interrompe uma iteração (no loop), se ocorrer uma condição especificada, e continua com a próxima iteração no loop.

 Este exemplo não mostra o valor de 4:
```` java
for (int i = 0; i < 10; i++) {
  if (i == 4) {
    continue;
  }
  System.out.println(i);
}
````
## Interromper e continuar no loop while

Você também pode usar `break`e `continue` em loops while:

 continue Break
```` java
int i = 0;
while (i < 10) {
  System.out.println(i);
  i++;
  if (i == 4) {
    break;
  }
}
````

 continue exemplo
```` java
int i = 0;
while (i < 10) {
  if (i == 4) {
    i++;
    continue;
  }
  System.out.println(i);
  i++;
}
````
# java arrays
Arrays são usados ​​para armazenar vários valores em uma única variável, em vez de declarar variáveis ​​separadas para cada valor.

Para declarar um array, defina o tipo de variável com **colchetes** :
```` java
String[] cars;
````

 Agora declaramos uma variável que contém um array de strings. Para inserir valores nele, podemos usar um literal de array - coloque os valores em uma lista separada por vírgulas, entre chaves:
```` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
````
 Para criar um array de inteiros, você poderia escrever:
```` java
int[] myNum = {10, 20, 30, 40};
````
## Acesse os elementos de um array
 Você acessa um elemento da matriz referindo-se ao número do índice.
 Esta instrução acessa o valor do primeiro elemento em cars:
```` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars[0]);
// mostra Volvo
````
## Alterar um elemento de matriz
Para alterar o valor de um elemento específico, consulte o número do índice:

```` java
cars[0] = "Opel";
````

```` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
System.out.println(cars[0]);
// agora mostra Opel no lugar de  Volvo
````
## comprimento de uma matriz
Para descobrir quantos elementos um array possui, use a propriedade `length`:
```` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
System.out.println(cars.length);
// mostra 4
````
## Loop através de uma matriz
 Você pode percorrer os elementos da matriz com o loop `for` e usar a propriedade `length` para especificar quantas vezes o loop deve ser executado.

 O exemplo a seguir gera todos os elementos na matriz cars :
```` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (int i = 0; i < cars.length; i++) {
  System.out.println(cars[i]);
}
````

## Loop através de uma matriz com For-Each
 Há também um loop "**for-each ", que é usado exclusivamente para percorrer elementos em arrays**:

  sintaxe
```` java
for (type variable : arrayname) {
  ...
}
````
 O exemplo a seguir gera todos os elementos no array cars , usando um loop " for-each ":

```` java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
````
  O exemplo acima pode ser lido assim: para cada elemento `String` (chamado i - como em index ) em cars , imprima o valor de i .

 Se você comparar o loop `for` com o loop `for-each` , verá que o método `for-each` é mais fácil de escrever, não requer um contador (usando a propriedade length) e é mais legível.

# objetos em java
 Um array multidimensional é um array de arrays.
Para criar um array bidimensional, adicione cada array dentro de seu próprio conjunto de chaves :
```` java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
````
 myNumbers agora é um array com dois arrays como seus elementos.

 Para acessar os elementos da matriz **myNumbers** , especifique dois índices: um para a matriz e outro para o elemento dentro dessa matriz. Este exemplo acessa o terceiro elemento (2) no segundo array (1) de myNumbers:

```` java
int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
int x = myNumbers[1][2];
System.out.println(x); // mostra 7
````
 Também podemos usar um for loopdentro de outro for looppara obter os elementos de um array bidimensional (ainda temos que apontar para os dois índices):

```` java
public class Main {
  public static void main(String[] args) {
    int[][] myNumbers = { {1, 2, 3, 4}, {5, 6, 7} };
    for (int i = 0; i < myNumbers.length; ++i) {
      for(int j = 0; j < myNumbers[i].length; ++j) {
        System.out.println(myNumbers[i][j]);
      }
    }
  }
}
````

## metodos em java
```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

```` java
````

# java
