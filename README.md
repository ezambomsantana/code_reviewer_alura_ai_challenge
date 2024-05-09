# Code Reviewer

A ideia desse projeto é fazer um revisor de Código automático. A partir de uma lista de regras de boas práticas de uma linguagem de programação validar um código de um arquivo com código fonte.

A motivação para esse projeto é que normalmente muito tempo é gasto para a revisão de código, por isso automatizar partes desse prcesso pode ajudar em reduzir o tempo gasto nessa tarefa, além de reduzir a quantidade de erros humanos, que muitas vezes pode não encontrar um problema no código.

## Como funciona

O primeiro passo é definir uma lista de boas práticas em um dicionário com diferentes linguagens, como por exemplo:

```
languages = {
  "java": [
      'Verificar a identação do código, devem ter 4 espaços.',
      'Verificar se os nomes das classes começam com letra maíscula',
      'Verificar se os nomes de variáveis, classes e métodos usam o camel case'
  ],
  "python": [
      'Verificar se todas as strings usam aspas simples',
      'Verificar se os nomes das classes começam com letra maíscula'
  ]
}
```

Depois, o código vai pedir o link para um arqiuvo de código fonte. A versão atual suporta apenas Python e Java, mas qualquer outra linguagem pode ser usada.

O conteúdo do arquivo será enviado para o Gemini para que ele identifique a linguagem de código.

Por fim, com a linguagem identificada, será enviado a lista de verificações que o Gemini deverá fazer, e será peguntado se o código tem algum problema.

## Conteúdo do repositório

/exemplos -> contém alguns exemplos de código em Java ou em Python com alguns erros que a ferramenta deve detectar



