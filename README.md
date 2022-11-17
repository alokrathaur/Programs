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
    
