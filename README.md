# ios-senior

## Desenvolvimento nativo para iOS

Para o desenvolvimento nativo de apps para iOS, nós temos duas opções: Objective-C e Swift.

## Objective-C

Objective-C é uma linguagem de longa data, criada no inicio da década de 1980 e baseada em linguagens como [C](https://www.gnu.org/software/libc/manual/pdf/libc.pdf) e [Smalltalk](http://smalltalk.gnu.org/documentation).

Objective-c utiliza-se dos conceitos de [Dynamic typing](https://developer.apple.com/library/archive/documentation/General/Conceptual/DevPedia-CocoaCore/DynamicTyping.html) e [Message passing](https://en.wikipedia.org/wiki/Message_passing).

## Swift 

É uma linguagem relativamente nova, atualmente na versão 4.2. A Apple iniciou em 2010 e a lançou em 2014. Em 2015 Swift se tornou Open Source. Com abordagens modernas, sua principais caracteristicas são: 
[generics](https://docs.swift.org/swift-book/LanguageGuide/Generics.html), [optionals](https://developer.apple.com/documentation/swift/optional), [type inference](https://en.wikipedia.org/wiki/Type_inference) e [higher-order functions](https://en.wikipedia.org/wiki/Message_passing).

## Struct ou Classe

Classes são do tipo "Reference Type" e Struct "Value Type". O que significa isso? Basicamente: 
Struct (Value Type)
cada instância mantém uma cópia exclusiva de seus dados. Um tipo que cria uma nova instância (cópia) quando atribuído a uma variável ou constante, ou quando passado para uma função.

Classe (Reference Type)
Cada instância compartilha uma única cópia dos dados. Um tipo que, uma vez inicializado, quando atribuído a uma variável ou constante, ou quando passado para uma função, retorna uma referência à mesma instância existente.

## Comparações

Estruturas e classes em Swift tem várias coisas em comum. São elas:

- Definir propriedades para armazenar valores
- Definir métodos para fornecer funcionalidades
- Definir "subscripts" para fornecer acesso aos seus valores usando a sintaxe de subscript
- Definir inicializadores para configurar um estado inicial
- Estender para expandir funcionalidades

### Generics

"Generics" permite criar um código flexivel, reutilizável, permitindo trabalhar com qualquer tipo, de acordo com os requisitos que você define. Muito da biblioteca do Swift é construido com Generics, como por exemplo Arrays e Dictionary que são coleções de genéricos.

Ex:
Uma simples função que exibe o valor do objeto passado por parâmetro.

```swift
func exibeInt(_ a: Int) {
    print("O int é: \(a)")
}

func exibeString(_ a: String) {
    print("A string é: \(a)")
}

func exibeDouble(_ a: Double) {
    print("O double é: \(a)")
}

exibeInt(17)
exibeString("Apple :)")
exibeDouble(3.50)
```
Podemos substitui-la por apenas uma, utilizando Generic Type.

```swift
func exibeValor<T>(_ a: T) {
    print("O valor é: \(a)")
}

exibeValor(17)
exibeValor("Apple :)")
exibeValor(3.50)
```

## Design Patterns

Podemos descrever basicamente como um modelo genérico para resolver uma situação. O padrão da arquitetura tem grande impacto 
sobre toda a base de código. O que deve se ter em mente é que: não há uma arquitetura ruim. A escolha depende da situação, conhecimento, etc.

### MVC

Esse é o modelo básico utilizado nos projetos de iOS. Utiliza-se uma grande quantidade de UIViewController para controlar todas as views e trabalhar com os modelos necessários para apresentar ao usuário final. Podemos chamar um API Endpoint usando URLSession ou Alamofire, validar os dados de resposta e formatá-los para apresentá-los na tela.

### MVVM

Model-View-ViewModel é uma arquitetura que nos deixa mais perto de uma arquitetura limpa, mas não tão perto assim.

### MVP

Model View Presenter...

### Viper


![Modelo](https://i.imgur.com/EAsRo3h.png)

Baseado no principio [S.O.L.I.D](https://en.wikipedia.org/wiki/SOLID)







# Referências

Design Patterns / Viper: [ref](https://theswiftdev.com/2018/03/12/the-ultimate-viper-architecture-tutorial/)

