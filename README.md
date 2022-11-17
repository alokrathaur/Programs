# Programs with Login in Swift

Find 2nd larget number in an integer array in swift .

    func largestNum(intArray : [Int]){
        var array = intArray //[78,-1,7,1,34,18,36];
        var max1 = array[0];
        var max2 = array[1];
        for i in 2...array.count-1 {
            if(array[i] > max2){
                
                max2 = array[i];
            }
            if(max2 > max1){
                var temp = max1;
                max1 = max2;
                max2 = temp;
            }
            
        }
        print(max1);
        print(max2);
        
    }
    
____________________________________________________________________________

Remove elements using indexes array:

Array of Strings and indexes

let animals = ["cats", "dogs", "chimps", "moose", "squarrel", "cow"]
let indexAnimals = [0, 3, 4]
let arrayRemainingAnimals = animals
    .enumerated()
    .filter { !indexAnimals.contains($0.offset) }
    .map { $0.element }

print(arrayRemainingAnimals)

//result - ["dogs", "chimps", "cow"]
Array of Integers and indexes

var numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12]
let indexesToRemove = [3, 5, 8, 12]

numbers = numbers
    .enumerated()
    .filter { !indexesToRemove.contains($0.offset) }
    .map { $0.element }

print(numbers)

//result - [0, 1, 2, 4, 6, 7, 9, 10, 11]
____________________________________________________________________________

Remove elements using element value of another array

Arrays of integers

let arrayResult = numbers.filter { element in
    return !indexesToRemove.contains(element)
}
print(arrayResult)

//result - [0, 1, 2, 4, 6, 7, 9, 10, 11]
____________________________________________________________________________

Arrays of strings

let arrayLetters = ["a", "b", "c", "d", "e", "f", "g", "h", "i"]
let arrayRemoveLetters = ["a", "e", "g", "h"]
let arrayRemainingLetters = arrayLetters.filter {
    !arrayRemoveLetters.contains($0)
}

print(arrayRemainingLetters)

//result - ["b", "c", "d", "f", "i"]
