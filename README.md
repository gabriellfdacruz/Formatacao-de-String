# Formatação de Strings e Text Blocks em Java

Este repositório demonstra diferentes formas de trabalhar com **Strings**, **formatação de texto** e **saída formatada** em Java.

O projeto apresenta recursos modernos da linguagem, incluindo:

* escape sequences
* unicode
* text blocks
* `printf`
* `String.format()`
* `.formatted()`

Tudo isso utilizando exemplos simples e práticos no console.

---

# 📂 Estrutura do Projeto

## `Main.java`

Classe principal responsável por demonstrar diferentes técnicas de formatação e exibição de texto em Java.

O código explora:

* listas formatadas
* alinhamento de números
* interpolação de valores
* blocos de texto multilinha

---

# 🧠 Conceitos Demonstrados

## 🔹 Escape Sequences

Utilização de caracteres especiais para formatação de texto.

### Exemplos:

* `\n` → quebra de linha
* `\t` → tabulação
* `\u2022` → símbolo de bullet point (•)

```java id="f8k1mv"
String bulletIt = "Print a Bulleted List:\n" +
        "\t\u2022 First Point\n" +
        "\t\t\u2022 Sub Point";
```

---

## 🔹 Text Blocks (Java 15+)

Uso de blocos de texto multilinha com `"""`.

Torna o código mais legível e reduz a necessidade de caracteres de escape.

```java id="n4q7pt"
String textBlock = """

        Print a Bulleted List:
            \u2022 First Point
                \u2022 Sub Point""";
```

---

## 🔹 `printf()` e Formatação de Saída

Permite imprimir valores formatados diretamente no console.

### Exemplos:

* `%d` → inteiro
* `%.2f` → número decimal com 2 casas
* `%n` → quebra de linha

```java id="w6r2jc"
System.out.printf("Your age is %d%n", age);
```

---

## 🔹 Alinhamento de Texto

O código utiliza especificadores para alinhar números no console.

```java id="z9m5ax"
System.out.printf("Printing %6d %n", i);
```

O número `6` define o espaço mínimo utilizado na impressão.

---

## 🔹 `String.format()`

Cria uma string formatada sem imprimir diretamente.

```java id="s2v8lb"
String formattedString =
        String.format("Your age is %d", age);
```

---

## 🔹 Método `.formatted()`

Forma moderna e mais limpa de formatar strings em Java.

```java id="j1x4ke"
formattedString =
        "Your age is %d".formatted(age);
```

---

# 🚀 Exemplo de Execução

```java id="u5n7pd"
public static void main(String[] args) {

    String bulletIt = "Print a Bulleted List:\n" +
            "\t\u2022 First Point\n" +
            "\t\t\u2022 Sub Point";

    System.out.println(bulletIt);

    String textBlock = """

            Print a Bulleted List:
                \u2022 First Point
                    \u2022 Sub Point""";

    System.out.println(textBlock);

    int age = 35;

    System.out.printf("Your age is %d%n", age);

    int yearOfBirth = 2023 - age;

    System.out.printf(
            "Age = %d, Birth year = %d%n",
            age,
            yearOfBirth);

    System.out.printf(
            "Your age is %.2f%n",
            (float) age);

    for (int i = 1; i <= 100000; i *= 10) {
        System.out.printf("Printing %6d %n", i);
    }

    String formattedString =
            String.format("Your age is %d", age);

    System.out.println(formattedString);

    formattedString =
            "Your age is %d".formatted(age);

    System.out.println(formattedString);
}
```

---

# 💻 Saída Esperada

```txt id="g7r3nf"
Print a Bulleted List:
    • First Point
        • Sub Point

Your age is 35
Age = 35, Birth year = 1988
Your age is 35.00

Printing      1
Printing     10
Printing    100
Printing   1000
Printing  10000
Printing 100000

Your age is 35
Your age is 35
```

---

# ⚙️ Como Executar

## 1️⃣ Clone o repositório

```bash id="p4m2yt"
git clone https://github.com/seu-usuario/java-string-formatting.git
```

---

## 2️⃣ Compile o arquivo

```bash id="v6n8qx"
javac Main.java
```

---

## 3️⃣ Execute o programa

```bash id="r3w9jb"
java Main
```

---

# 📚 Objetivo do Projeto

Este projeto foi criado para praticar recursos de manipulação e formatação de texto em Java.

Ideal para:

* iniciantes em Java
* prática com Strings
* aprendizado de `printf`
* estudo de text blocks
* exercícios de formatação de saída
* portfólio e GitHub

---

# 🛠️ Tecnologias Utilizadas

* Java
* Strings
* Console Output
* Formatação de Texto

---

# 🤝 Contribuição

Contribuições são bem-vindas!

Sugestões de melhorias, exemplos adicionais ou otimizações podem ser enviadas via Pull Request 🚀
