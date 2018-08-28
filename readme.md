```
var Person = function(firstAndLast) {
  // Complete the method below and implement the others similarly

  //Split the name into an array
  let fullNameArray = firstAndLast.split(/\W+/);

  //Return the first element in the array
  this.getFirstName = function(){
    return fullNameArray[0];
  };

  //Return the second element in the array
  this.getLastName = function(){
    return fullNameArray[1];
  };

  //Rejoin the array to a string and return it
  this.getFullName = function() {
    return fullNameArray.join(" ");
  };

  //Change the first element in array to the new name then join them into a string
  this.setFirstName = function(first){
    fullNameArray.splice(0, 1, first).join(" ");
  };

  //Change the second element in array to the new name then join them into a string
  this.setLastName = function(last){
    fullNameArray.splice(1, 1, last).join(" ");
  };

  //Just like the original param, split this name into an array
  this.setFullName = function(firstAndLast){
    fullNameArray = firstAndLast.split(" ");
  };
};

var bob = new Person('Bob Ross');
bob.getFullName();
```
