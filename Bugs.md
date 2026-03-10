Bug 1 – Sistema permite cadastro com campos vazios
Severidade: Alta (Impacta a integridade dos dados)

Passos para reproduzir:

Acessei a página de cadastro de cursos.

Tentei salvar o formulário sem preencher os campos obrigatórios.

Cliquei no botão "Salvar".

O que está acontecendo (Resultado atual):
O sistema aceita o envio e cadastra o curso mesmo com as informações em branco, gerando itens vazios na listagem.

O que deveria acontecer (Resultado esperado):
O sistema deve validar os campos obrigatórios, impedir o salvamento e exibir uma mensagem de alerta para o usuário.

Bug 2 – Data final permitida como menor que a data inicial
Severidade: Média (Inconsistência na regra de negócio)

Passos para reproduzir:

Iniciei o cadastro de um novo curso.

No campo de datas, inseri uma "Data Inicial" posterior à "Data Final" (ex: Início em 10/10 e Fim em 01/10).

Tentei finalizar o cadastro.

O que está acontecendo (Resultado atual):
O sistema permite o cadastro normalmente, aceitando um período de curso que não faz sentido cronológico.

O que deveria acontecer (Resultado esperado):
O sistema deve bloquear o cadastro e informar que a data de término não pode ser anterior à data de início.
