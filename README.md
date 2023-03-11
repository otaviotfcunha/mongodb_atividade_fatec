# mongodb_atividade_fatec

##Banco de Dados Não Relacional
##Trabalho Prático
##Persistência em Banco de Dados NoSQL

###Para realização da tarefa foram executadas os seguintes passos:

**1-** Utilizando o MongoDB Compass, criei um novo database com nome de aula e um collection com nome livros.
**2-** Fiz download da estrutura e dos dados no link: https://fatecspgov-my.sharepoint.com/:u:/g/personal/mateus_fuini_fatec_sp_gov_br/EQFIusmR_o9Mj6ZE0-SDqcsByM7h2gGafTQ4bHgjmGU3Uw?e=aNIiAX
**3-** No MongoDB Compass, importei os dados para a collection livros.
**4-** Executei os comandos de NoSQL utilizando o MONGOSH do MongoDB Compass.

###Os resultados informados foram:


**1-** show dbs: aula 8.00 KiB.
**2-** use aula: 'switched to db aula'.
**3-** show collections: livros.
**4-** db.livros.find().count() = 431.
**5-** db.livros.find({pageCount:{$lte: 100}}).pretty().count() = 166.
**6-** db.livros.find({isbn:{$lte: "1617200000"}}).pretty().count() = 22.
**7-** db.livros.find({isbn:{$lte: "1617200000"}}).pretty().count() = 'Graphics File Formats'.
**8-** {
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("640bc2cfc58364819c83a8d2"),
    '1': ObjectId("640bc2cfc58364819c83a8d3"),
    '2': ObjectId("640bc2cfc58364819c83a8d4"),
    '3': ObjectId("640bc2cfc58364819c83a8d5")
  }
}
**9-** db.livros.find({isbn:{$lte:"10"}}).count() = 4.
**9.1-** db.livros.find({isbn:{$lte:"100"}}).count() = 5.
**10-** db.livros.find({isbn:{$lte:"10"}}, {title:1}).pretty().limit(2) = Comprehensive Networking Glossary and Acronym Guide e Personal Videoconferencing
**11-** db.livros.find({isbn:{$lte: "100"}}).pretty().skip(2) = Multimedia Computing, Implementing SAP R/3, Second Edition e Saci Pererê.
**12-** db.livros.find({title: /Windows/}).count() = 11.
**13-** db.livros.find({ }, {"pageCount":1, "_id":0}).sort({"pageCount": -1}).limit(2) = 1101 e 1096

###O print da tarefa está neste repositório.
