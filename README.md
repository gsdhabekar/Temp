# Temp
Javascript Logics

1.Object Equality
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
    
  
