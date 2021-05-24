# Swift-Bases-Platzi
Este es un playground con lo aprendido en el curso de Platzi

import UIKit

// ------------------------
// Operaciones de asignación y aritmeticas
// ------------------------

let name = "Irwing Herrera"
var age = 0

// ------------------------
// Comparaciones
// ------------------------

(1, name) < (2, "Allison Herrera")
(1, name) < (1, "Allison Herrera") // Segundo valor, orden alfabetico

// ------------------------
// Operaciones Ternarias
// ------------------------
var currentYear = 2022
age = age + (currentYear > 2021 ? 26 : 25)

// ------------------------
// Operador Nil Coalescing
// ------------------------

let defaultAge = 18
var userAge: Int?

var ageToBeUsed = userAge ?? defaultAge

// ------------------------
// Rangos
// ------------------------

for idx in 1...5 {
    print(idx)
}

for idx in 1..<5 {
    print(idx)
}

let fruits = ["Naranja", "Mango", "Fresa"]
for index in 0..<fruits.count {
    print("La fruta \(index + 1) se llama \(fruits[index])")
}

for fruit in fruits[1...] {
    print(fruit)
}

// ------------------------
// Strings
// ------------------------

let multiLineaString = """
    Hola
    Mundo
    """
let wiseWords = "\"Hola Mundo\""
let dolarSign = "\u{24}"
let blackHeart = "\u{2665}"
let heart = "\u{1F496}"
print(wiseWords)

let nameChars: [Character] = ["I","r","w","i","n","g"]
let nameString: String = String(nameChars)
var first: Character = nameString[nameString.index(before: nameString.endIndex)]

let collection: [String] = [
"Act 1 Scene 1","Act 1 Scene 2","Act 1 Scene 3","Act 1 Scene 4","Act 1 Scene 5",
"Act 2 Scene 1","Act 2 Scene 2","Act 2 Scene 3",
"Act 3 Scene 1","Act 3 Scene 2"
]

var act1SceneCount = 0
for scene in collection {
    if scene.hasPrefix("Act 1") {
        act1SceneCount += 1
    }
}

print("El numero de escenas del acto 1 es \(act1SceneCount)")

// ------------------------
// Array
// ------------------------

var someInt = [Int]()
someInt.append(25)
someInt.count


var someDoubles = Array(repeating: 3.141592, count: 5)
someDoubles.count

for (index, item) in someDoubles.enumerated() {
    print("Item \(index): \(item)")
}

// ------------------------
// Conjunto (Set) -> No permite tener un elemento mas de una vez y no tiene un orden
// ------------------------

var letters = Set<Character>()
letters.insert("A")
letters.insert("B")
letters.insert("C")
letters.insert("D")
letters.insert("E")
letters.count

if let removedGame = letters.remove("A") {
    print("He eliminado de la lista \(removedGame)")
}
letters

let oddDigits: Set = [1,3,5,7,9]
let evenDigits: Set = [0,2,4,6,8]
let primeNumbers: Set = [2,3,5,7]

// A union B = elementos que son o bien de A, o bien de B o de los dos
oddDigits.union(evenDigits).sorted()

// A interseccion B = elmentos que son a la ve de A y de B
oddDigits.intersection(evenDigits)
evenDigits.intersection(primeNumbers).sorted()
oddDigits.intersection(primeNumbers).sorted()

// A - B = elementos que son de A pero no de B
oddDigits.subtracting(primeNumbers).sorted()

// A + B = (A-B) union (B-A)
oddDigits.symmetricDifference(primeNumbers).sorted()

// ------------------------
// Diccionarios [key:value]
// ------------------------

var namesDictionary: [String: Int] = [
    "Irwing": 25,
    "Allison": 24
]

namesDictionary = [:]
namesDictionary.count
