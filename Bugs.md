

Bug Report – Desafio QA Beedoo 2026
Este documento detalha as falhas identificadas durante os testes de regressão e funcionalidade do módulo de Cadastro e Listagem de Cursos.

🔴 BUG-01: Cadastro de curso sem nome
Severidade: Alta (Impede a identificação do item na listagem)

Passos para reproduzir:

Acessar a tela de cadastro de curso.

Deixar o campo "Nome do curso" vazio.

Clicar em Salvar.

O que está acontecendo: O sistema salva o registro sem validar o nome e não exibe alertas.

O que deveria acontecer: O cadastro deve ser bloqueado, exibindo a mensagem: "O campo nome é obrigatório".

🟡 BUG-02: Conflito de lógica nas datas (Data Final < Inicial)
Severidade: Média

Passos para reproduzir:

Acessar a tela de cadastro de curso.

Inserir uma Data Inicial (ex: 10/05) superior à Data Final (ex: 01/05).

Clicar em Salvar.

O que está acontecendo: O sistema aceita o intervalo cronológico impossível.

O que deveria acontecer: O sistema deve validar o período e informar que a data final não pode ser anterior à inicial.

🟡 BUG-03: Caracteres especiais no campo "Número de vagas"
Severidade: Média

Passos para reproduzir:

No cadastro de curso, localizar o campo "Número de vagas".

Tentar inserir símbolos como . ou -.

Clicar em Salvar.

O que está acontecendo: O campo aceita caracteres não numéricos.

O que deveria acontecer: O campo deve ser restrito apenas a números inteiros positivos.

🔴 BUG-04: Falta de atualização reativa na exclusão
Severidade: Alta (Gera confusão de dados para o usuário)

Passos para reproduzir:

Cadastrar um curso e localizá-lo na lista.

Clicar no botão Excluir.

Observar a listagem.

O que está acontecendo: O item permanece visível na tela até que o usuário force um F5 (Refresh).

O que deveria acontecer: A interface deve remover o item da lista imediatamente após a confirmação da exclusão.

🔴 BUG-05: Cadastro de curso sem descrição
Severidade: Alta

Passos para reproduzir:

Preencher todos os campos obrigatórios.

Deixar o campo Descrição vazio.

Clicar em Salvar.

O que está acontecendo: O sistema ignora a ausência de descrição.

O que deveria acontecer: O campo descrição deve ser obrigatório para garantir a qualidade da informação do curso.

🔴 BUG-06: Cadastro "Fantasma" (Todos os campos vazios)
Severidade: Alta (Risco de poluição do banco de dados)

Passos para reproduzir:

Acessar a tela de cadastro.

Clicar em Salvar sem interagir com nenhum campo.

O que está acontecendo: O sistema cria um registro vazio no banco.

O que deveria acontecer: Bloqueio total do envio e destaque visual dos campos obrigatórios.

🟡 BUG-07: Falha de máscara/validação em URL (Modalidade Online)
Severidade: Média

Passos para reproduzir:

Selecionar a modalidade "Online".

No campo de link, digitar um texto aleatório (ex: teste_sem_link).

Clicar em Salvar.

O que está acontecendo: O sistema não valida se o texto inserido é uma URL válida.

O que deveria acontecer: O campo deve exigir um formato de link válido (ex: https://...).
