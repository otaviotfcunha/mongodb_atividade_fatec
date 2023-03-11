<h1>mongodb_atividade_fatec</h1>

<h3>Banco de Dados Não Relacional<br>
Trabalho Prático<br>
Persistência em Banco de Dados NoSQL</h3>

<h3>Para realização da tarefa foram executadas os seguintes passos:</h3>

**1-** Utilizando o MongoDB Compass, criei um novo database com nome de aula e um collection com nome livros.<br>
**2-** Fiz download da estrutura e dos dados no link: https://fatecspgov-my.sharepoint.com/:u:/g/personal/mateus_fuini_fatec_sp_gov_br/EQFIusmR_o9Mj6ZE0-SDqcsByM7h2gGafTQ4bHgjmGU3Uw?e=aNIiAX<br>
**3-** No MongoDB Compass, importei os dados para a collection livros.<br>
**4-** Executei os comandos de NoSQL utilizando o MONGOSH do MongoDB Compass.<br><br>

<h3>Os resultados informados foram:</h3>


**1-** show dbs: aula 8.00 KiB.<br>
**2-** use aula: 'switched to db aula'.<br>
**3-** show collections: livros.<br>
**4-** db.livros.find().count() = 431.<br>
**5-** db.livros.find({pageCount:{$lte: 100}}).pretty().count() = 166.<br>
**6-** db.livros.find({isbn:{$lte: "1617200000"}}).pretty().count() = 22.<br>
**7-** db.livros.find({isbn:{$lte: "1617200000"}}).pretty().count() = 'Graphics File Formats'.<br>
**8-** {<br>
  acknowledged: true,<br>
  insertedIds: {<br>
    '0': ObjectId("640bc2cfc58364819c83a8d2"),<br>
    '1': ObjectId("640bc2cfc58364819c83a8d3"),<br>
    '2': ObjectId("640bc2cfc58364819c83a8d4"),<br>
    '3': ObjectId("640bc2cfc58364819c83a8d5")<br>
  }<br>
}<br>
**9-** db.livros.find({isbn:{$lte:"10"}}).count() = 4.<br>
**9.1-** db.livros.find({isbn:{$lte:"100"}}).count() = 5.<br>
**10-** db.livros.find({isbn:{$lte:"10"}}, {title:1}).pretty().limit(2) = Comprehensive Networking Glossary and Acronym Guide e Personal Videoconferencing. <br>
**11-** db.livros.find({isbn:{$lte: "100"}}).pretty().skip(2) = Multimedia Computing, Implementing SAP R/3, Second Edition e Saci Pererê.<br>
**12-** db.livros.find({title: /Windows/}).count() = 11.<br>
**13-** db.livros.find({ }, {"pageCount":1, "_id":0}).sort({"pageCount": -1}).limit(2) = 1101 e 1096. <br><br>

<h3>O print da tarefa está neste repositório.</h3>
