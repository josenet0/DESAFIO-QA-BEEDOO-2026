# DESAFIO QA - BEEDOO 2026

## Aplicação analisada
https://creative-sherbet-a51eac.netlify.app/

---

# Objetivo da aplicação

A aplicação tem como objetivo permitir o gerenciamento de cursos, possibilitando que usuários cadastrem, visualizem e excluam cursos dentro do sistema.

Por meio do sistema é possível registrar cursos com informações como nome, descrição, datas, número de vagas, modalidade e link (quando aplicável).

---

# Fluxos principais identificados

Durante a exploração da aplicação foram identificados os seguintes fluxos principais:

### Cadastro de cursos
Permite registrar novos cursos informando dados como:

- Nome do curso
- Descrição
- Datas
- Número de vagas
- Modalidade (presencial ou online)
- Link do curso (quando modalidade online)

### Listagem de cursos
Após o cadastro, os cursos são exibidos em uma lista onde o usuário pode visualizar os cursos existentes.

### Exclusão de cursos
A aplicação permite excluir cursos previamente cadastrados da listagem.

---

# Análise inicial da aplicação

Durante a exploração inicial, foram identificados alguns pontos críticos que merecem maior atenção durante os testes:

- Validação de **campos obrigatórios**
- Consistência entre **datas inicial e final**
- Validação do **campo número de vagas**
- Comportamento da **exclusão de cursos**
- Validação do **campo link para cursos online**
- Comportamento do sistema quando **dados inválidos são inseridos**

Esses pontos foram utilizados como base para a criação dos cenários de teste.

---

# Estratégia de testes

Para avaliar o comportamento da aplicação, foram considerados diferentes tipos de cenários:

### Fluxos positivos (Happy Path)
Testes para validar se o sistema funciona corretamente quando o usuário segue o fluxo esperado.

Exemplo:
- Cadastro de curso com todos os dados válidos.

### Fluxos negativos
Testes com dados inválidos ou incompletos para verificar como o sistema se comporta.

Exemplos:
- Campo nome vazio
- Cadastro com todos os campos em branco
- Inserção de caracteres inválidos

### Validação de campos
Testes focados em garantir que os campos aceitam apenas dados válidos.

Exemplos:
- Campo de vagas aceitando apenas números
- Validação de URL para cursos online

### Testes exploratórios
Exploração livre da aplicação para identificar comportamentos inesperados ou inconsistências.

---

# Cenários de teste executados

Foram criados e executados **8 cenários de teste**:

| ID | Cenário |
|----|--------|
| CT01 | Cadastro de curso com dados válidos |
| CT02 | Cadastro de curso com campo nome vazio |
| CT03 | Cadastro com data final menor que data inicial |
| CT04 | Validação de caracteres especiais no campo número de vagas |
| CT05 | Exclusão de curso cadastrado |
| CT06 | Cadastro de curso sem preencher descrição |
| CT07 | Cadastro de curso com todos os campos em branco |
| CT08 | Cadastro de curso modalidade online com link inválido |

---

# Casos de teste detalhados

Os casos de teste completos com:

- passos de execução
- resultado esperado
- resultado obtido
- status
- severidade

estão documentados na planilha abaixo:

➡️ **Planilha de Casos de Teste**  
https://docs.google.com/spreadsheets/d/1V9LGeF2nwWGW8TiUH-0rsVKNB_t6MTf0I_wsxjBASCA/edit?usp=sharing

---

# Evidências de execução

As evidências da execução dos testes (prints e gravações de tela) estão organizadas por caso de teste no link abaixo:

➡️ **Evidências dos Testes**  
https://drive.google.com/drive/folders/1T1NUWuYRhEJPHQHKN2PCp42qnoNczNcj?usp=sharing

---

# Resultados da execução

Dos **8 cenários executados**:

- **1 cenário passou**
- **7 cenários falharam**

Os principais problemas encontrados estão relacionados a:

- Falta de validação de campos obrigatórios
- Falta de validação de dados
- Problemas na exclusão de cursos
- Ausência de validação de URL para cursos online

---

# Bugs encontrados

Todos os bugs identificados durante a execução dos testes foram documentados no arquivo abaixo:

➡️ **bugs.md**
