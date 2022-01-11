# Expressoes regulares Regex

> . o "ponto" que significa qualquer char

> \* o asterisco que serve para definir uma quantidade de chars, zero ou mais vezes

> \{ e } as chaves que servem para definir uma quantidade de caracteres específicas que é desejado encontrar

<strong>Por exemplo:</strong>

- a{3} letra a 3 vezes.

- \d* um digito zero ou mais vezes

- \d\d\d\.\d\d\d\.\d\d\d\-\d\d <- retorna um CPF valido

> <h2>Lista de conhecimento</h2>

- \d     <- vai retornar um numero decimal - 1

- \d\d\d <- vai retornar 3 numeros seguidos - 111

- .      <- vai apresentar qualquer caracteres

- \.     <- vai apresentar somente o ponto

- \?     <- Corresponde a expressão que o precede repetido 0 ou 1 vez. Equivalente à {0,1}.

> <h2>Quantifier</h2>
>Uma forma de mostrar quantos caracteres deveraão ser apresentados de forma mais eficiente

>> \d\d\d\.\d\d\d\.\d\d\d\-\d\d <- retorna um CPF valido sem usar o Quantifier <br/>
\d{3}\.\d{3}\.\d{3}-\d{2}    <- nota como reduzimos e deixamos mais legivel, {3} vai retornar a quantidade de caracteres<br/>
>> \d{2}\.\d{3}\.\d{3}\/\d{4}-\d{2} <- retorna um CNPJ valido usando Quatifier 

>Na frase<br/>
João Fulano,123.456.789-00,21 de Maio de 1993,(21) 3079-9987,Rua do Ouvidor,50,20040-030,Rio de Janeiro<br/>
Como o Regex para identificar o CEP?
>>\d{5}-\d{3}<br/>

>Qual padrão podemos utilizar para encontrar o número telefônico? Por exemplo: (21) 3216-2345<br/>
>>\(\d{2}\) \d{4}-\d{4}

>Na frase agora nosso CPF não esta formatado com ponto, como resolvemos? usando o Quantifier ? ele mostra se tiver ou não
>>João Fulano,12345678900,21 de Maio de 1993,(21) 3079-9987,Rua do Ouvidor,50,20040-030,Rio de Janeiro<br/>
Como o Regex para identificar o CEP?
>>\d{3}\.?\d{3}\.?\d{3}-?\d{2}

# Classes de Caracteres
> <h2>Posso definir um conjunto de caracteres que deveram aparecer na posição definida</h2>
> Se quisermos definir um conjunto que caracteres que possivelmente podem aparecer em um campo de CPF usamos as Classes<br/>
> 123.123.123-12 <br />
> \d{3}\.?\d{3}\.?\d{3}[@\.-]\d{2} <- repare no conjunto que caracteres entre [ ], todos os definidos poderam aparecer


