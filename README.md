## Comandos do MongoDB 🚀
---
### Criando o banco de dados
    use movie
---
### Criando a collection
    db.createCollection('movies')
---
### Inserindo as informações
    db.movies.insertMany([ 
        {movies.json} 
        ])
---
### Atualizando documento //OK FUNCIONANDO
    db.getCollection('movies').update({
        db.getCollection('movies').update({"name" : "The Godfather II"}, {$set: {"name": "The Godfather part II"}})
---
### Exclusão de documento
    db.getCollection('movies').remove({genre: {$ne: "western"}})
---
### Consulta com projeção//OK FUNCIONANDO
    db.getCollection('movies').find({genre: 'action' }).sort({'imdb rating':-1})
---
### Consulta utilizando combinação entre os seletores//OK, TA FUNCIONANDO
    db.getCollection('movies').find({'genre': 'crime', 'imdb rating':{$gte: 9.0}})
---
### Consulta paginada e ordenada (utilizar skip, limit e sort)
    db.getCollection('movies').find({'genre':'crime'}).sort({'imdb rating': 1}).skip(2).limit(1)