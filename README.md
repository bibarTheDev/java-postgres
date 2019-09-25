# java-postgres
## Simples classe criada para facilitar o acesso à um banco de dados postgres por meio do Java

### Overview
Esta classe disponibiliza dois métodos principais, um para comandos sql que nao retornam valores (`INSERT`, `UPDATE` e `DELETE`) e um para que retornam (`SELECT`), além de conexão seguindo 5 parametros simples (e um adicional, caso necessário).

Caso este arquivo nao esteja descritivo o suficiente, o código também está documentao.

Para funcionar, é necessária a instalação de um driver disponivel [aqui](https://jdbc.postgresql.org/download.html).

### Instalacao do driver
1. Baixe a versão do driver adequada
2. Mova o arquivo `.jar` baixado para os seqgunte caminho: `<diretorio de instalacao do java>/jdk<versao>/jre/lib/ext`

### Uso
Para instanciar o a classe
```java
//sem schema
Banco db = new Banco("<host>", "<porta>", "<usuario>", "<senha>", "<database>");

//ou

//com schema
Banco db = new Banco("<host>", "<porta>", "<usuario>", "<senha>", "<database>", "<schema>");

```

Para executar querys sem retorno
```java
String sql = "INSERT INTO usuario VALUES ('bibar', 'SenhaSecretaNaoContaSHHHHHHH')";
Boolean resultado = noReturnQuery(sql);
```

Para executar querys com retorno
```java
String sql = "SELECT * FROM usuario";
ArrayList< ArrayList<String> > resposta;
respsota = selectQuery(sql);  
```

### ye
Feito por um aluno cansado de fazer métodos específicos pra cada query
twitter: @bibaromito (eu praticamente so reclamo e retweeto meme aqui, mas eventualmente tem coisa que vale a pena juro)
