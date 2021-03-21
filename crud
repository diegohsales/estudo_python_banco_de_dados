import sqlite3
def conexao():
    connection = sqlite3.connect("db_cliente.db")
    return connection

def create_table():
    sql = ''' CREATE TABLE cliente (id_cliente integer primary key,
                           nome varchar(50),
                           comentario varchar(100)) '''
    # abrindo ou criando o banco de dados
    connection =  conexao()
    # crio o curso, para poder executar as operação de BD
    cursor = connection.cursor()
    cursor.execute(sql) 
    connection.commit() # efetivo a criação do BD
    cursor.close()
    connection.close() 

create_table()

def insert():
    id_cliente = int(input("Informe o ID: "))
    nome = input("Informe o nome: ")
    comentario = input("Faça seu comentario: ")
    sql = ''' INSERT INTO cliente (id_cliente, nome, comentario)
              VALUES (?, ?, ?)''' #prepare stantement
    
    # abrindo ou criando o banco de dados
    connection =  conexao()
    # crio o curso, para poder executar as operação de BD
    cursor = connection.cursor()
    cursor.execute(sql, [id_cliente, nome, comentario])
    print("Concluido com sucesso!!!")
    connection.commit() # efetivo a criação do BD
    cursor.close()
    connection.close()

insert()

def update():
    id_cliente = int(input("Informe o ID: "))
    nome = input("Informe o nome: ")
    comentario = input("Faça seu comentario: ")
    sql = ''' UPDATE cliente SET nome = ?, comentario = ?
              WHERE id_cliente = ? '''
    
        # abrindo ou criando o banco de dados
    connection =  conexao()
    # crio o curso, para poder executar as operação de BD
    cursor = connection.cursor()
    cursor.execute(sql, [nome, comentario, id_cliente])
    print("Alterado com sucesso!!!")
    connection.commit() # efetivo a criação do BD
    cursor.close()
    connection.close()

update()

def delete():
    try:
        id_cliente = int(input("Informe o ID "))
        sql = '''DELETE FROM cliente WHERE id_cliente = ?'''
        # abrindo ou criando o banco de dados
        connection =  conexao()
        # crio o curso, para poder executar as operação de BD
        cursor = connection.cursor()
        cursor.execute(sql,[id_cliente]) 
        print("Excluido com sucesso!!!")
        connection.commit() # efetivo a criação do BD
    except:
        print("Erro ao excluir")
    finally:    
        cursor.close()
        connection.close()

def read_all():
    try:
        sql = ' SELECT * FROM cliente '
        connection =  conexao () # abri o BD
        cursor = connection.cursor() # criei o cursor
        cursor.execute(sql) # executei o script SQL
        rows = cursor.fetchall() # peguei todos os dados da tabela
        for row in rows:
            print("Valores...: ", row[0], row[1], row[2])
    except:
         print("Erro ao consultar")
    finally:
        cursor.close()
        connection.close()

read_all()

def read_one():
    try:
        id_cliente = int(input("Informe o ID "))
        sql = '''SELECT * from cliente WHERE id_cliente = ?'''
        connection =  conexao() # abri o BD
        cursor = connection.cursor() # criei o cursor
        cursor.execute(sql, [id_cliente]) # executei o  SQL
        row = cursor.fetchone() # peguei todos os dados da tabela
        print ("Valor...: ", row[0], row[1], row[2])
    except:
        print ("Erro ao consultar")
    finally:    
        cursor.close()
        connection.close()
