# Requisitos - Agenda+

## 1. Visão do Produto
O Agenda+ é um sistema web para clínicas que permite aos pacientes consultar horários disponíveis, solicitar agendamentos de consultas e reservar medicamentos sem precisar ligar para a clínica. A equipe da clínica (secretários e médicos) utiliza o sistema para gerenciar a agenda, confirmar ou recusar solicitações, controlar o estoque de medicamentos e se preparar para os atendimentos, enquanto o administrador controla o acesso da equipe e as permissões de cada usuário.

## 2. Papéis de Usuário
| Papel | Descrição |
|-------|-----------|
| Paciente | Pessoa atendida pela clínica. Cadastra-se no sistema, consulta horários, solicita consultas, reserva medicamentos e acompanha suas solicitações. |
| Secretário | Membro da recepção. Gerencia horários e a agenda diária, confirma ou recusa solicitações, atualiza o estoque e valida receitas. |
| Médico | Profissional de saúde. Consulta sua agenda de atendimentos e os dados básicos dos pacientes agendados. |
| Administrador | Responsável pelo sistema. Cadastra a equipe, altera papéis e inativa contas de usuários. |

## 3. Histórias de Usuário

### H01 - Fazer login (Essencial)
**Como** usuário, **eu quero** fazer login **para** acessar as funções do meu perfil.

**Critérios de aceitação:**
- [ ] O usuário acessa o sistema informando credenciais válidas.
- [ ] Após o login, são exibidas apenas as funções correspondentes ao papel do usuário.
- [ ] Credenciais inválidas ou contas inativas exibem uma mensagem de erro e não permitem o acesso.

### H02 - Cadastrar-se no sistema (Essencial)
**Como** paciente, **eu quero** me cadastrar no sistema **para** acessar os serviços da clínica.

**Critérios de aceitação:**
- [ ] O paciente informa seus dados pessoais e cria uma senha para acesso.
- [ ] O sistema não permite cadastro com dados obrigatórios em branco ou com e-mail/CPF já cadastrado.
- [ ] Após o cadastro, o paciente consegue fazer login.

### H03 - Ver horários disponíveis (Essencial)
**Como** paciente, **eu quero** ver os horários disponíveis de atendimento **para** escolher o melhor momento para minha consulta sem precisar ligar para a clínica.

**Critérios de aceitação:**
- [ ] São exibidos apenas os horários liberados e ainda não ocupados.
- [ ] Horários bloqueados ou já reservados não aparecem para o paciente.
- [ ] Caso não haja horários disponíveis, uma mensagem informativa é exibida.

### H04 - Solicitar agendamento de consulta (Essencial)
**Como** paciente, **eu quero** solicitar o agendamento de uma consulta em um horário disponível **para** garantir meu atendimento sem precisar ligar para a clínica.

**Critérios de aceitação:**
- [ ] O paciente seleciona um horário disponível e envia a solicitação.
- [ ] A solicitação é registrada com o status "pendente".
- [ ] Um mesmo horário não pode ser solicitado por dois pacientes ao mesmo tempo.

### H05 - Acompanhar status das solicitações (Importante)
**Como** paciente, **eu quero** acompanhar o status das minhas solicitações (pendente, confirmada, recusada) **para** saber se minha consulta foi aceita.

**Critérios de aceitação:**
- [ ] O paciente visualiza a lista de suas solicitações com o status atual de cada uma.
- [ ] Solicitações recusadas exibem a justificativa informada pelo secretário.

### H06 - Reservar medicamento (Importante)
**Como** paciente, **eu quero** reservar um medicamento anexando a receita quando necessário **para** ter certeza de que ele estará disponível.

**Critérios de aceitação:**
- [ ] O paciente seleciona um medicamento disponível em estoque e solicita a reserva.
- [ ] Para medicamentos que exigem receita, o sistema só permite enviar a reserva com a receita anexada.
- [ ] A reserva fica com status "pendente" até ser avaliada pelo secretário.

### H07 - Receber notificações (Desejável)
**Como** paciente, **eu quero** receber notificações sobre minha consulta ou reserva **para** não depender de abrir o sistema.

**Critérios de aceitação:**
- [ ] O paciente é notificado quando uma solicitação de consulta ou reserva é confirmada ou recusada.
- [ ] O paciente recebe um lembrete antes da data da consulta.

### H08 - Confirmar ou recusar solicitações (Essencial)
**Como** secretário, **eu quero** confirmar ou recusar solicitações com justificativa **para** controlar a agenda.

**Critérios de aceitação:**
- [ ] O secretário visualiza as solicitações pendentes.
- [ ] Ao recusar uma solicitação, o preenchimento da justificativa é obrigatório.
- [ ] Ao confirmar ou recusar, o status da solicitação é atualizado e fica visível para o paciente.

### H09 - Gerenciar horários (Essencial)
**Como** secretário, **eu quero** cadastrar, liberar e bloquear horários **para** que o paciente veja só o que está disponível.

**Critérios de aceitação:**
- [ ] O secretário cadastra novos horários de atendimento vinculados a um médico.
- [ ] O secretário pode liberar ou bloquear um horário existente.
- [ ] Horários bloqueados deixam de ser exibidos para os pacientes.

### H10 - Consultar agenda do dia (Importante)
**Como** secretário, **eu quero** consultar a agenda de atendimentos por dia **para** organizar a recepção.

**Critérios de aceitação:**
- [ ] O secretário seleciona uma data e visualiza os atendimentos confirmados daquele dia.
- [ ] A agenda exibe horário, paciente e médico de cada atendimento.

### H11 - Atualizar estoque e validar receitas (Importante)
**Como** secretário, **eu quero** atualizar o estoque e validar receitas **para** aprovar ou recusar reservas corretamente.

**Critérios de aceitação:**
- [ ] O secretário cadastra medicamentos e atualiza a quantidade em estoque.
- [ ] O secretário visualiza a receita anexada e aprova ou recusa a reserva.
- [ ] Ao aprovar uma reserva, a quantidade em estoque é atualizada.

### H12 - Consultar agenda do médico (Importante)
**Como** médico, **eu quero** consultar minha agenda de atendimentos **para** organizar minha rotina.

**Critérios de aceitação:**
- [ ] O médico visualiza apenas os seus atendimentos confirmados.
- [ ] A agenda pode ser filtrada por dia.

### H13 - Ver dados básicos do paciente (Desejável)
**Como** médico, **eu quero** ver os dados básicos do paciente agendado **para** me preparar para o atendimento.

**Critérios de aceitação:**
- [ ] O médico acessa os dados básicos do paciente a partir de um atendimento da sua agenda.
- [ ] O médico só visualiza dados de pacientes agendados com ele.

### H14 - Cadastrar médicos e secretárias (Essencial)
**Como** administrador, **eu quero** cadastrar médicos e secretárias **para** que a equipe acesse o sistema.

**Critérios de aceitação:**
- [ ] O administrador cadastra um usuário informando seus dados e o papel (médico ou secretário).
- [ ] O usuário cadastrado consegue fazer login com o papel atribuído.

### H15 - Alterar papel de usuário (Importante)
**Como** administrador, **eu quero** alterar o papel de um usuário **para** controlar as permissões de acesso.

**Critérios de aceitação:**
- [ ] O administrador seleciona um usuário e altera o seu papel.
- [ ] As permissões do usuário passam a corresponder ao novo papel.

### H16 - Inativar contas de usuários (Importante)
**Como** administrador, **eu quero** inativar contas de usuários **para** impedir o acesso sem perder o histórico.

**Critérios de aceitação:**
- [ ] Usuários com conta inativa não conseguem fazer login.
- [ ] O histórico de consultas, reservas e ações do usuário inativado é mantido no sistema.

## 4. Priorização de Requisitos
| Prioridade | Histórias |
|------------|-----------|
| Essencial | H01, H02, H03, H04, H08, H09, H14 |
| Importante | H05, H06, H10, H11, H12, H15, H16 |
| Desejável | H07, H13 |
| Fora do escopo | - |

## 5. Requisitos Não Funcionais
| ID | Requisito |
|----|-----------|
| RNF01 | O sistema deve ser acessível por navegador web, em computadores e dispositivos móveis. |
| RNF02 | As senhas dos usuários devem ser armazenadas de forma criptografada. |
| RNF03 | Cada usuário deve acessar somente as funções permitidas pelo seu papel. |
| RNF04 | Os dados pessoais e de saúde dos pacientes devem ser tratados conforme a LGPD. |
| RNF05 | O sistema deve responder às consultas de horários e agendas em menos de 2 segundos. |
