# Analise-Lexica-Sintatica-Compiladores


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
