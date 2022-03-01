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

