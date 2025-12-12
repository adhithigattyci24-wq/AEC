function calculateFactorial()
{
  let number=parseInt(document.getElementById("number").value);
  if (isNaN(number)||number<0)
  {
    alert("Please enter a valid non-negetive number");
    return;
  }
  
  let factorial = 1;
  for (let i = 1; i <=number; i++)
  {
    factorial *=i;
  }
  
  document.getElementById("result").innerText=`Factorial of ${number} is ${factorial}`;
}

function checkPalindrome()
{
  let number = document.getElementById("number").value;
  if(number === "")
  {
    alert("Please enter a valid number");
    return;
  } 

  let reversed = number.split("").reverse().join("");
  let isPalindrome = (number === reversed);
  document.getElementById("result").innerText=`${number} is ${isPalindrome ? "" :"not "} a palindrome`;
}

