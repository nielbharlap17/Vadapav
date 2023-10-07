# Vadapav
Hot vadapav

Palindrome

<html>

    <head>

         <title>JavaScript Palindrome </title>

         </head>

         <body>

            <!-- -->

            <script>

                function validatePalin(str) {

                    const len = str.length;

                    for (let i=0;i<len/2;i++) {

                    if (string[i] !==string[len - 1 -i]) {

                        alert('It is not a palindrome')

                    }

                    }

                alert('It is a palindrome') 

                }

                const string = prompt('Enter a string or number:');

                const value = validatePalin(string);

                console.log(value)

            </script>

        </body>

</html>












#phone book 


html>

<head>

<meta name="viewport" content="width=device-width, initial-scale=1">

<style>

* {

  box-sizing: border-box;

}

#myInput {

  background-image: url('/css/searchicon.png');

  background-position: 10px 12px;

  background-repeat: no-repeat;

  width: 100%;

  font-size: 16px;

  padding: 12px 20px 12px 40px;

  border: 1px solid #d41a1a;

  margin-bottom: 12px;

}



#myUL {

  list-style-type: none;

  padding: 0;

  margin: 0;

}



#myUL li a {

  border: 1px solid #2f1894;

  margin-top: -1px; /* Prevent double borders */

  background-color: #c5c4d3;

  padding: 12px;

  text-decoration: none;

  font-size: 18px;

  color: black;

  display: block

}



#myUL li a:hover:not(.header) {

  background-color: #dd3450;

}

</style>

</head>

<body>



<h2>My Phonebook</h2>

<input type="text" id="myInput" onkeyup="myFunction()" placeholder="Search for names.." title="Type in a name">



<ul id="myUL">

  <li><a href="#">Anna</a></li>

  <li><a href="#">Belly</a></li>



  <li><a href="#">Jerry</a></li>

  <li><a href="#">Bobby</a></li>



  <li><a href="#">Kevin</a></li>

  <li><a href="#">Cherry</a></li>

  <li><a href="#">Lucky</a></li>

</ul>



<script>

function myFunction() {

    var input, filter, ul, li, a, i, txtValue;

    input = document.getElementById("myInput");

    filter = input.value.toUpperCase();

    ul = document.getElementById("myUL");

    li = ul.getElementsByTagName("li");

    for (i = 0; i < li.length; i++) {

        a = li[i].getElementsByTagName("a")[0];

        txtValue = a.textContent || a.innerText;

        if (txtValue.toUpperCase().indexOf(filter) > -1) {

            li[i].style.display = "";

        } else {

            li[i].style.display = "none";

        }

    }

}

</script>



</body>

</html>




#login page

<!DOCTYPE html>
<HTML>
<head>
    <meta name ="viewport" content="width=device-width", initial-scale="1">
    <style>
        body{font-family:Arial,Helvetica,sans-serif;}
        form{border:3px solid #f1f1f1;}
        input[type=text], input[type=password]{
            width:100%;
            padding:12px 20px;
            margin: 8px 0;
            display: inline-block;
            border: 1px solid #ccc;
            box-sizing: border-box;
        }
        button{
            background-color: #2db44f;
            color: white;
            padding: 14PX 20PX;
            margin: 8PX 0;
            border: none;
            cursor: pointer;
            width:100%;
        }
        button:hover{
            opacity:0.8;
        }
        .cancelbtn{
            width: auto;
            padding: 10px 18px;
            background-color: #4152b6;
        }
        .imgcontainer{
            text-align: center;
            margin: 24px 0 12px 0;
        }
        img.avatar{
            width: 40%;
            border-radius: 50%;
        }
        .container{
            padding: 16px;
        }
        span.pws{
            float: right;
            padding-top: 16px;
        }
        @media screen and (max-width:300px ){
            span.pws{
                display: block;
                float:"none";
            }
            .cancelbtn{
                width: 100%;

            }
        }
    </style>
</head>
<body>
    <h2>login form</h2>
    <form action="/action_page.php" method="post">
        <div class="imgcontainer">
            <img src="img_avatar2.png" alt="Avatar" class="avatar">
        </div>
        <div class="container">
            <label for="uname"><b>Username</b></label>
            <input type ="text" placeholder="Enter Username" name="uname" required>
            <label for="psw"><b>Password</b></label>
            <input type ="password" placeholder="Enter Password" name="psw" required>
            <button type="submit">Login</button>
            <label>
                <input type="checkbox" checked="checked" name="remember"> Remember Me </label>
        </div>
        <div class="container" style="background-color: #bbc970">
        <button type="button" class="cancelbtn">Cancel</button>
        <span class="psw">Forgot<a href="#">password?</a></span>
        </div>
     </form>
   </body>
</HTML>

















#calculator

<!DOCTYPE html>
<html lang="en">
<head>
<style>
    *{
   padding: 0;
   margin: 0;
   font-family: 'poppins', sans-serif;
}
body{
   background-color: #495250;
   display: grid;
   height: 100vh;
   place-items: center;
}
.main{
   width: 400px;
   height: 450px;
   background-color: white;
   position: absolute;
   border: 5px solid black;
   border-radius: 6px; 
}
.main input[type='text'] {
   width: 88%;
   position: relative;
   height: 80px;
   top: 5px;
   text-align: right;
   padding: 3px 6px;
   outline: none;
   font-size: 40px;
   border: 5px solid black;
   display: flex;
   margin: auto;
}
.btn input[type='button']{
   width:90px;
   padding: 2px;
   margin: 2px 0px;
   position: relative;
   left: 13px;
   top: 20px;
   height: 60px;
   cursor: pointer;
   font-size: 18px;
   transition: 0.5s;
   background-color: #495250;
   border-radius: 6px;
   color: white;
}
.btn input[type='button']:hover{
   background-color: black;
   color: white;
}

</style>
<script>
    function Solve(val) {
       var v = document.getElementById('res');
       v.value += val;
    }
    function Result() {
       var num1 = document.getElementById('res').value;
       var num2 = eval(num1);
       document.getElementById('res').value = num2;
    }
    function Clear() {
       var inp = document.getElementById('res');
       inp.value = '';
    }
    function Back() {
       var ev = document.getElementById('res');
       ev.value = ev.value.slice(0,-1);
    }
 </script>
 <title>Calulator</title>
</head>
<body>
 <div class="main">
    <input type="text" id = 'res'>
    <div class="btn">
       <input type="button" value = 'C' onclick = "Clear()">
       <input type="button" value = '%' onclick = "Solve('%')">
       <input type="button" value = '←' onclick ="Back('←')">
       <input type="button" value = '/' onclick = "Solve('/')">
       <br>
       <input type="button" value = '7' onclick = "Solve('7')">
       <input type="button" value = '8' onclick = "Solve('8')">
       <input type="button" value = '9' onclick = "Solve('9')">
       <input type="button" value = 'x' onclick = "Solve('*')">
       <br>
       <input type="button" value = '4' onclick = "Solve('4')">
       <input type="button" value = '5' onclick = "Solve('5')">
       <input type="button" value = '6' onclick = "Solve('6')">
       <input type="button" value = '-' onclick = "Solve('-')">
       <br>
       <input type="button" value = '1' onclick = "Solve('1')">
       <input type="button" value = '2' onclick = "Solve('2')">
       <input type="button" value = '3' onclick = "Solve('3')">
       <input type="button" value = '+' onclick = "Solve('+')">
       <br>
       <input type="button" value = '00'onclick = "Solve('00')">
       <input type="button" value = '0' onclick = "Solve('0')">
       <input type="button" value = '.' onclick = "Solve('.')">
       <input type="button" value = '=' onclick = "Result()">
    </div>
 </div>
 <script src = 'Calc.js' ></script>
</body>
</html>









