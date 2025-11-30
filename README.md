🐾 Sistema de Gerenciamento de Clínica Veterinária – Doctor Pet
Experiência Prática IV – Implementação e Manipulação de Dados (SQL)

Este repositório contém todos os scripts SQL desenvolvidos para a Experiência Prática IV do projeto Doctor Pet, incluindo criação das tabelas, inserção de dados, consultas, e comandos de atualização e remoção.
O objetivo é implementar completamente o modelo lógico do banco de dados e manipular informações reais.

📘 Descrição do Projeto

A clínica veterinária Doctor Pet realiza consultas, exames, vacinações e atendimentos para animais domésticos.
O sistema registra e gerencia:

Tutores (clientes)

Animais

Veterinários

Serviços

Agendamentos

Atendimentos

Exames

Os scripts deste repositório implementam o banco de dados desse projeto em MySQL, com manipulação completa das entidades.

📁 Estrutura do Repositório
📦 doctorpet-sql
 ┣ 📄 ddl_doctorpet.sql              # Script completo de criação do banco e tabelas
 ┣ 📄 inserts_doctorpet.sql          # Script de povoamento das tabelas
 ┣ 📄 selects_doctorpet.sql          # Consultas SQL solicitadas
 ┣ 📄 updates_deletes_doctorpet.sql  # Comandos UPDATE e DELETE
 ┣ 📄 README.md                      # Documentação do projeto
 ┗ 📄 modelagem.pdf                  # (Opcional) DER e documentação anterior

🛠 Tecnologias Utilizadas

MySQL 8.0

MySQL Workbench

SQL (DDL e DML)

🧱 1. Criação do Banco e Tabelas (DDL)

O script completo está no arquivo:

➡️ ddl_doctorpet.sql

Ele contém:

Criação do banco doctorpet

Todas as tabelas

Chaves primárias e estrangeiras

Cascades de update e delete

🟢 2. Inserção de Dados (INSERT)

Arquivo:
➡️ inserts_doctorpet.sql

Inclui dados reais e coerentes para:

cliente

veterinario

servico

animal

agendamento

atendimento

exame

Pronto para rodar sem conflitos de FK.

🔍 3. Consultas SQL (SELECT)

Arquivo:
➡️ selects_doctorpet.sql

Inclui:

✔ JOIN entre tabelas
✔ ORDER BY
✔ WHERE
✔ LIMIT (opcional)
✔ Consultas detalhadas de atendimentos, agendamentos e exames

Exemplo:

SELECT a.nome AS animal, a.especie, c.nome AS tutor
FROM animal a
JOIN cliente c ON a.id_cliente = c.id_cliente
ORDER BY tutor;

✏ 4. Atualizações e Exclusões (UPDATE e DELETE)

Arquivo:
➡️ updates_deletes_doctorpet.sql

Inclui:

3 comandos de UPDATE

3 comandos de DELETE

Todos com condições (WHERE) para evitar remoção acidental

Exemplo:

UPDATE servico
SET preco = 160.00
WHERE id_servico = 3;

🚀 Como Executar o Projeto
1️⃣ Importar os arquivos no MySQL Workbench

Abra o Workbench

Vá em File > Open SQL Script

Execute os scripts na seguinte ordem:

1. ddl_doctorpet.sql
2. inserts_doctorpet.sql
3. selects_doctorpet.sql
4. updates_deletes_doctorpet.sql

2️⃣ Verificar relacionamento e consistência

As constraints com ON UPDATE CASCADE e ON DELETE CASCADE garantem integridade referencial.
