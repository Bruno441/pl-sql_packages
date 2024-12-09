# Sistema de Gerenciamento Acadêmico - PL/SQL

Este projeto contém pacotes PL/SQL para gerenciar alunos, disciplinas e professores em um sistema acadêmico, utilizando o Oracle Database.

## Sumário
- [Descrição dos Pacotes](#descrição-dos-pacotes)
- [Requisitos](#requisitos)
- [Configuração do Ambiente](#configuração-do-ambiente)
- [Execução dos Scripts](#execução-dos-scripts)
- [Testes e Validações](#testes-e-validações)

---

## Descrição dos Pacotes

### **PKG_ALUNO**
Gerencia operações relacionadas aos alunos.
- **EXCLUIR_ALUNO(P_ID_ALUNO)**: Exclui o registro de um aluno e suas matrículas associadas.
- **CURSOR_ALUNOS_MAIORES**: Cursor que retorna todos os alunos com idade superior a 18 anos.
- **CURSOR_ALUNOS_POR_CURSO(P_ID_CURSO)**: Cursor que retorna os alunos matriculados em um curso específico.

### **PKG_DISCIPLINA**
Gerencia operações relacionadas às disciplinas.
- **CADASTRAR_DISCIPLINA(P_NOME, P_DESCRICAO, P_CARGA_HORARIA)**: Cadastra uma nova disciplina.
- **CURSOR_TOTAL_ALUNOS_DISCIPLINAS**: Cursor que retorna as disciplinas com mais de 10 alunos matriculados.
- **CURSOR_MEDIA_IDADE_DISCIPLINA(P_ID_DISCIPLINA)**: Cursor que calcula a média de idade dos alunos matriculados em uma disciplina específica.
- **LISTAR_ALUNOS_DISCIPLINA(P_ID_DISCIPLINA)**: Lista os alunos matriculados em uma disciplina específica.

### **PKG_PROFESSOR**
Gerencia operações relacionadas aos professores.
- **CURSOR_TOTAL_TURMAS_PROFESSOR**: Cursor que retorna os professores responsáveis por mais de uma turma.
- **TOTAL_TURMAS_PROFESSOR(P_ID_PROFESSOR)**: Function que retorna o número total de turmas em que um professor atua.
- **PROFESSOR_DA_DISCIPLINA(P_ID_DISCIPLINA)**: Function que retorna o nome do professor responsável por uma disciplina específica.

---

## Requisitos

1. **Banco de Dados Oracle**: Certifique-se de que o Oracle Database está instalado e configurado.
2. **Tabelas Necessárias**:
   - `ALUNOS`
   - `DISCIPLINAS`
   - `MATRICULAS`
   - `PROFESSORES`
   - `TURMAS`
3. Ferramenta de acesso ao banco (como SQL*Plus ou Oracle SQL Developer).