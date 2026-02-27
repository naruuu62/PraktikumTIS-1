NIM : 245150700111011
Name : SEPTIAN NURIL ARIFIN
CLASS : TIS - C 

# CRUD MongoDB - Bookstore

## Show Database
show dbs

##Use Database
use bookstore

## Show Collections
show collections

# Insert One
db.books.insertOne({title: "Overlord I", author: "Kugane Maruyama", year: 2012, pages: 548, summary: "Lorem ipsum sir dolor amet", publisher: "Yen Press"})

# Insert Many
db.books.insertMany([{
        title: "The Setting Sun",
        author: "Osamu Dazai",
        year: 1947,
        pages: 175,
        summary: "Kisah tentang kemunduran keluarga bangsawan Jepang",
        publisher: "Yen Press",
        language: "English",
        rating: 4.5,
        tags: ["fiction", "classic", "japanese"]
    }, {
        title: "Hujan",
        author: "Tere Liye",
        year: 2016,
        pages: 320,
        summary: "Kisah cinta di tengah bencana dan kehilangan memori",
        publisher: "Gramedia",
        language: "Indonesian",
        rating: 4.9,
        tags: ["fiction", "romance", "indonesian"]
    },])

# Find Specific
db.books.find({author: "Osamu Dazai"})

# Find All
db.books.find()

# Update One
db.books.updateOne(
    { title: "Hujan" },
    { $set: { summary: "Buku yang bagus (Septian Nuril Arifin, 245150700111011)" } }
)

# Update Many
db.books.updateMany({})

# Delete One
db.books.deleteOne({title: "Overlord I"})

# Delete Many
db.books.deleteMany({author: "Osamu Dazai"})

