# Projeto Clínica

Este projeto implementa um sistema simples de cadastro de pacientes, utilizando PHP e MySQL.
_____________________________________________________________________________________________

## Sobre o projeto

Permite gerenciar cadastros de médicos e consultas com pacientes, fazendo associação entre os médicos e cada consulta.

## Cada módulo apresenta operações CRUD:

- Cadastrar
- Listar
- Editar
- Excluir

## Como executar

1.  Instale XAMPP ou similar.
2.  Inicie Apache e MySQL.
3.  Copie o projeto para htdocs.

O banco de dados está incluído no arquivo, no formato .sql

_____________________________________________________________________________________________

# Pseudocódigo das operações principais

## Cadastrar Médico

INICIO
Ler nome_medico, email_medico, especialidade_medico, telefone_medico
Se nome_medico vazio OU email_medico vazio ENTÃO
Mostrar erro "Nome e email obrigatórios"
PARAR
FIMSE
Conectar ao banco
Inserir registro na tabela medicos (nome, email, especialidade, telefone)
Se inserção OK ENTÃO
Mostrar "Médico cadastrado com sucesso"
SENAO
Mostrar erro com mensagem
FIMSE
FIM

## Listar Médicos

INICIO
 Conectar ao banco
 Executar SELECT * FROM medicos ORDER BY nome_medico
 Para cada registro retornado
 Mostrar linha na tabela com dados do médico e links de ação (editar/
excluir)
 FIMPARA
FIM

## Cadastrar Consulta

INICIO
 Ler nome_consulta, data_consulta, id_medico
 Validar campos obrigatórios
 Se inválido ENTÃO
 Mostrar erro
 PARAR
 
 FIMSE
 Inserir em consultas (nome, data, id_medico)
 Mostrar sucesso ou erro
FIM

________________________________________________________________________________________

## Autor
* Aluno: Luis Filipe Silva Vasconcelos
* Disciplina: Técnicas de Desenvolvimento de Algoritmos
* Curso: Análise e Desenvolvimento de Sistemas
