# Agenda+

Projeto da disciplina de Engenharia de Software 2, UFOP.

## Ideia geral

O Agenda+ é um sistema web que apoia o processo de marcação de consultas em clínicas e consultórios. O paciente consulta datas e horários disponíveis e envia solicitações de agendamento, além de poder reservar medicamentos disponíveis no estoque. A secretaria analisa, confirma ou recusa solicitações, organiza a agenda, disponibiliza novos horários e gerencia o estoque de medicamentos.

O objetivo é reduzir a dependência de ligações e mensagens manuais, para que a secretaria possa dar mais atenção a quem já está presente na clínica.

## Descrição geral do sistema

O sistema é dividido em quatro portais:

- **Portal do Paciente:** visualiza horários disponíveis, solicita agendamentos, acompanha o status dos pedidos (pendente, confirmado ou recusado) e reserva medicamentos, anexando receita quando necessário.
- **Portal da Secretária:** gerencia solicitações de agendamento, disponibilidade de horários, estoque de medicamentos e validação de receitas.
- **Portal do Médico:** consulta sua agenda de atendimentos e as informações básicas dos pacientes vinculados.
- **Portal do Administrador:** cadastra e remove usuários internos, associa papéis e controla o acesso ao sistema.

**Serviços:** agendamento, gestão de atendimentos, gestão de medicamentos, autenticação e gestão de usuários.

## Tecnologias e estrutura inicial

- **Front-end:** Next.js com React e JavaScript.
- **Back-end:** Node.js, em uma aplicação separada do front-end.

```text
frontend/   Front-end e seu package.json
backend/    Back-end e seu package.json
docs/       Documentação do projeto
```

O repositório está na etapa de preparação inicial. Os arquivos `package.json` definem a base dos projetos; ainda não há páginas ou servidor implementados. As dependências do front-end estão declaradas, e as bibliotecas do back-end serão escolhidas posteriormente.

Para o desenvolvimento, é necessário ter Node.js e npm instalados.

## Quadro Kanban

(https://github.com/users/LucasOSRodrigues/projects/5)

## Integrantes

- Arthur Mendes Torres
- Felipe Guedes
- Guilherme Nogueira Zanon
- João Lucas Oliveira Silva Rodrigues
- Luiz Fernando
- Pedro Vitor
- Rafael Granato
- Thiago Linhares Lage
