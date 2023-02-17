# Analise-Lexica-Sintatica-Compiladores

# Objetivo:

O objetivo deste trabalho é construir um analisador sintático para uma linguagem de programação de alto nível. 
Para isso, utilizamos o Yacc e o Lex.

# Lex

Lex é uma ferramenta que gera um analisador léxico, também conhecido como scanner, que é responsável por analisar a entrada de um programa em busca de padrões de caracteres que representam tokens, tais como palavras-chave, operadores, identificadores, números, símbolos de pontuação, etc. O analisador léxico produz uma sequência de tokens que é passada para o analisador sintático.

# Yacc

Yacc é uma ferramenta que gera um analisador sintático, também conhecido como parser, que é responsável por analisar a estrutura gramatical do programa em busca de padrões de tokens que correspondem a regras gramaticais definidas para a linguagem. O analisador sintático produz uma árvore de análise sintática que é usada pelo compilador ou interpretador para gerar o código executável.

# ARQUIVO DE ENTRADA
    *formato = entrada.txt
    *deve conter palavras que fazem parte do Alfabeto definido
    *caso nao contenha, deve dar erro e apontar a linha onde deu erro
    *foram enviados arquivos de entrada para exemplificar os casos de teste 

# ARQUIVO DE SAIDA
    *formato = resultado.txt
    *contem o token e o lexema de cada elemento do arquivo de entrada
    *estao no formado: TOKEN   LEXEMA\n
    *contém o erro da análise sintática, caso exista algum
    *o erro está no formato: "Erro na linha X: syntax error próximo ao token Y

# COMO EXECUTAR
    *utilizamos o flex e o yacc para a realização deste trabalho.
    *caso queira apenas ir direto ao ponto e executar a "entrada.txt" para testar o programa,
     basta executar o seguinte comando, pelo terminal:

        $ ./meu_programa entrada.txt

    *onde "entrada.txt" deve ser o arquivo contendo os lexemas para teste
    *agora, caso queira ver o processo de geração dos arquivos oriundos do lex e do yacc,
     siga os seguintes comandos, no terminal:

        -> instalação do lex e yacc:
            $ sudo apt-get update
            $ sudo apt-get install flex
            $ sudo apt-get install bison

        -> compilação e execução:
            $ flex -o lex.yy.c --header-file=lex.yy.h lexico.l
            $ yacc -d parser.y
            $ gcc lex.yy.c -lfl -o lexico
            $ gcc lex.yy.c y.tab.c main.c -o meu_programa
            $ ./meu_programa entrada.txt

    *foi compilado utilizando o gcc nas versoes 18.04 e 22.04 do ubuntu
