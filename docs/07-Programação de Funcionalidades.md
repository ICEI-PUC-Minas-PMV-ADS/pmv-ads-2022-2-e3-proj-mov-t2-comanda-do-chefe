# Programação de Funcionalidades



|ID    | Descrição do Requisito  | Artefato(s) produzido(s) |
|------|-----------------------------------------|----|
|RF-001| A aplicação deverá apresentar uma tela onde o usuário poderá fazer login como "Funcionário" e "Cliente". | Index.cshtml / LoginController.cs | 
|RF-002| A aplicação deverá apresentar uma tela onde o cliente poderá fazer a solicitação de pedidos. Com campos para informar o escopo da requisição tais como: descrição, pratos, preços e quantidade desejada para realização do pedido. | Create.cshtml / ClienteController.cs | 
|RF-003| A aplicação deverá exibir uma tela de controle dos pedidos feitos, a fim de poder alterar, editar, e criar fazer pagamento.  | Index.cshtml / gerenciadorpedidosController.cs |

# Arquitetura do banco de dados

import * as SQLite from "expo-sqlite";

export const Database = {
  getConnection: () => {
    const db = SQLite.openDatabase("comanda.db");

    db.transaction((tx) => {
      tx.executeSql(
        "create table if not exists cliente (id integer primary key not null, numeroMesa integer not null ,nome text not null, telefone text not null);"
      );
      tx.executeSql(
        "create table if not exists produto (id integer primary key not null, nome text not null, preco text not null, codigo integer not null);"
      );
    });

    const ExecuteQuery = (sql, params = []) =>
      new Promise((resolve, reject) => {
        db.transaction((trans) => {
          trans.executeSql(
            sql,
            params,
            (trans, results) => {
              resolve(results);
            },
            (error) => {
              reject(error);
            }
          );
        });
      });

    return ExecuteQuery;
  },
};

export default Database;




## Gerador de Produtos

//PRATOS
import pratoDoDia from "../Assets/produtos/prato_do_dia.jpg";
import pratoStrogonoff from "../Assets/produtos/strogonoff.png";
import pratoFrango from "../Assets/produtos/frango.png";

// PORÇÕES
import porcaoFritas from "../Assets/produtos/fritas.png";
import porcaoCebola from "../Assets/produtos/cebola.png";
import porcaoNugget from "../Assets/produtos/nuggets.png";

// Bebidas
import bebidaAgua from "../Assets/produtos/agua.png";
import bebidaCoca from "../Assets/produtos/coca.png";
import bebidaFanta from "../Assets/produtos/fanta.png";

import produtos from "../Assets/data/produtos.json";
import { contantes } from "../Utilitarios/Contantes";

import { Image } from "react-native";

const obj = {
  teste: pratoFrango,
};

const images = {
  [contantes.PRATOS.DO_DIA]: pratoDoDia,
  [contantes.PRATOS.STROGONOFF]: pratoStrogonoff,
  [contantes.PRATOS.FRANGO]: pratoFrango,
  [contantes.PRATOS.FRITAS]: porcaoFritas,
  [contantes.PRATOS.ANEIS]: porcaoCebola,
  [contantes.PRATOS.NUGGETS]: porcaoNugget,
  [contantes.PRATOS.AGUA]: bebidaAgua,
  [contantes.PRATOS.COCA]: bebidaCoca,
  [contantes.PRATOS.FANTA]: bebidaFanta,
};

export function GeradorDePratos() {
  return produtos[contantes.CATEGORIA.PRATO_DO_DIA];
}

export function GeradorDePorcao() {
  return produtos[contantes.CATEGORIA.PORCOES];
}

export function GeradorDeBebidas() {}

export function GeradorDeImagem(name, width, height, borderRadius) {
  return (
    <Image
      source={images[name]}
      style={{ width: width || 100, height: height || 100, borderRadius: borderRadius || 20 }}
    />
  );
}

## Serviços do banco

import Database from "./DbServices";

const DB_EXEC = Database.getConnection();

export const criaCliente = async (param) => {
  let results = await DB_EXEC(
    "insert into cliente(numeroMesa, nome, telefone) values (?,?,?)",
    [param.numeroMesa, param.nome, param.telefone]
  );
  return results.rowsAffected;
};

export const criaProduto = async (param) => {
  let results = await DB_EXEC(
    "insert into produto(nome, preco, codigo) values (?,?,?)",
    [param.nome, param.preco, param.codigo]
  );
  return results.rowsAffected;
};

export const consultaClientes = async () => {
  let results = await DB_EXEC("select * from cliente");
  return results.rows._array;
};

export const consultaProdutos = async () => {
  let results = await DB_EXEC("select * from produto");
  return results.rows._array;
};



# Instruções de acesso

Para ter acesso a aplicação interativa, <a href="https://www.figma.com/proto/Ldgh6dhVdV0199YAUMj8vU/Comanda-do-chefe?node-id=8%3A130&scaling=scale-down&page-id=0%3A1&starting-point-node-id=8%3A16&show-proto-sidebar=1/">clique aqui</a>.

Para fazer o login no sistema, utilize os dados abaixo:

Click na opção: 
## Cliente
