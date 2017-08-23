# IOS-Programming

Swift



variables———————————
var month = “april”
let day = “10”


string concatenation:

let date = month + day

string interpolation:

let interpolatedAddress = “\(country)”


year = 2017 //int

version = 3.0 //float

type safety

let bestPlayer: String = “Micheal Jordan”
let year: Int = 22

let hallOfFame: Bool = true

operators———————————
assignment =

==
!=

arrays—————————————
var todo: [String] = []

//insert
todo += [“array concat”]
or
todo.insert(“watch tv”, at: 2)
	//doesn’t delete

//remove. shift left
todo.remove(at: 2)

//count 
todo.count


dictionary————————————
/*
	this is a hash map in swift 
*/

//init

let airportCodes: [String: String] = [“LGA”: “La Guardia”]

//read
airportCodes[“LGA”] //reading

//insert
airportCodes.updateValue(“SYD”, forKey: “Sydney”) 

//remove

airportCodes.removeValues(forKey: “”)



loops———————————

//for each

for task in todo{
		print(task)
}

//inclusive operator

for number in 1…10{

}

//half open range operator (exclusive)

for number in 1..<10{

}

//while loop

var x = 0
while x <= 20{

}

//do while
repeat {


}while 

if statements———————————

if temperature < 20{
		print(“hi”)
}

if !isRaining{

}

Switch Statements————

switch {
	case value1: do something
	case value1: do something
	default: do something else
}

really good for ranges

Functions————

func area(length: Int, width: Int) -> Int {
	let areaOfRoom = length * width
	return areaOfRoom
}

area(length: 10, width: 12)


or 

void

func someFunction() -> (){}

Function Scope————

func arrayModifier(array: [Int]){
	var arrayOfInts = array //local
	arrayOfInts.append(5)

	var secondArray = arrayOfInts
}

var arrayOfInts = [1,2,3,4]
arrayModifier(array: arrayOfInts)

OOP Structs————
struct Point{
	let x: Int
	let y: Int

	init(x: Int, y: Int){
		self.x = x
		self.y = y
	}

	fun points(inRange range: Int = 1)->[Point]{
		var results = [Point]()
		let lowerBoundOfXRange = x - range

		let upperBoundOfXRange = x+ range

		let lowerBoundOfYRange = y - range

		let upperBoundOfYRange = y + range


		for xCoordinate in lowerboundOfXRange … upperBoundOfXRange{
			for yCoordinate in lowerboundOfYRange … upperBoundOfYRange{
			let coordinatePoint = Point(x: xCoordinate, y: yCoordinate)
			results.append(coordinatePoint)
			}
		}

		return results
	}
}
let p1 = Point(x: 1, y: 2)

OOP Class————

class Enemy {
	var life: Int = 2
	let position: Point
	init(x: Int, y: Int){
		self.position = Point(x: x, y: y)
	}
func decreaseLife(by factor: Int){
	 life -= factor 
}
}
class Tower{
let position: Point
var range: Int = 1
var strength: Int = 1
init(x: Int, y: Int){
		self.position = Point(x: x, y: y)
}
}
