# Temp
Javascript Logics

1.Object Equality(_.isEqual(ob1,obj2))
    function Card(rank, suit) {
      this.rank = rank;
      this.suit = suit;
      this.equals = function(other) {
         return other.rank == this.rank && other.suit == this.suit;
      };
    }

    var queenOfClubs = new Card(12, "C");
    var kingOfSpades = new Card(13, "S");

    queenOfClubs.equals(kingOfSpades); // => false
    kingOfSpades.equals(new Card(13, "S")); // => true
    
2. Sum Nested Array
    function arraySum(i) {
    var sum=0; // missing var added
    for(var a=0;a<i.length;a++){ // missing var added
        if(typeof i[a]=="number"){
            sum+=i[a];
        }else if(i[a] instanceof Array){
            sum+=arraySum(i[a]);
        }
    }
    return sum;
}
arraySum([2,1,3,[4,5],['h',1]]);

3. Check fo String palindrom
    function isPalindrome(s) {
    return s == s.split("").reverse().join("") ? true : false;
}
console.log(isPalindrome("noon"));

4.Check for Prime Number
    #AS simple as possible:
    function isPrime(num) {
      for(var i = 2; i < num; i++)
        if(num % i === 0) return false;
      return num !== 1;
    }
    
    #With the ES6 syntax
    const isPrime = num => {
        for(let i = 2, s = Math.sqrt(num); i <= s; i++)
            if(num % i === 0) return false; 
        return num !== 1;
    }
    
 5.Sum of Numbers using arguments
    function sum() {
        var s = 0;
        for (var i=0; i < arguments.length; i++) {
            s += arguments[i];
        }
        return s;
    }
    console.log(sum(2, 3));         // 5
    console.log(sum(-10, 1));       // -9
    console.log(sum(1, 1, 1, 1));   // 4

6.Sort Array of String AND Number
    function strDes(a, b) {
       if (a>b) return 1;
       else if (a<b) return -1;
       else return 0;
     }
     var a2=["1", "a", "A", "b","3"];
     a2.sort(strDes);
