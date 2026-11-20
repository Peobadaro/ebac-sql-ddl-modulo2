# EBAC – Exercício Módulo 2 (SQL / DDL)

Script de criação das tabelas **customer** (cliente), **product** (produto) e **stock** (estoque) no PostgreSQL, com nomes em inglês.

## Estrutura

| Tabela | O que guarda | Destaques |
|---|---|---|
| `customer` | Cadastro de clientes | `id SERIAL` (auto-increment), `document` e `email` únicos |
| `product` | Cadastro de produtos | `sku` único, preços com `CHECK >= 0` |
| `stock` | Saldo de cada produto por depósito | FK para `product`, quantidade com `CHECK >= 0`, um registro por produto/depósito |

Relação: `product (1) —— (N) stock`.

## Como rodar

```bash
psql -U postgres -d nome_do_banco -f create_tables.sql
```
