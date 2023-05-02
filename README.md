Download Link: https://assignmentchef.com/product/solved-comp2396b-assignment-4-interface-in-java
<br>
This assignment tests your understanding of <strong>interface</strong> in Java.

You are required to implement an authentication module for a system that manages users’ login information. The authentication module allows the user to create and modify their information. It also provides the function to authenticate the user by password.

You need to design the program structure. Please make good use of object-oriented programming for this assignment. You must make use of <strong>interface</strong>, <strong>and all instant variables must be private</strong>. The marking criteria are included at the end of this assignment description.

You are also required to write <strong>JavaDoc</strong> for all non-private classes and non-private class members.

<h1>Tasks</h1>

When the program is executed, the following menu should be displayed:

Welcome to the COMP2396 Authentication system!

<ol>

 <li>Authenticate user</li>

 <li>Add user record</li>

 <li>Edit user record</li>

</ol>

What would you like to perform?

Please enter your command (1-3, or 0 to terminate the system):




In the sample outputs below, texts in <strong>bold</strong> are user inputs.

<ol>

 <li>Hashing interface

  <ul>

   <li>Create an Interface class Hash to perform hashing (MD5, SHA1, SHA256 etc…) o Implement a hash function for the program to use.

    <ul>

     <li>To use the Java hash utility, please refer to:</li>

    </ul></li>

  </ul></li>

</ol>

https://docs.oracle.com/javase/8/docs/api/java/security/MessageDige st.html

<ul>

 <li>To allow the system to change the hashing algorithm without modifying the program logic.</li>

 <li>The hashing interface should be used in the following:

  <ul>

   <li>Hash the user input password when adding a user. o Hash the user input password for the authentication.</li>

   <li>Hash the user input password when the user change or reset the password.</li>

  </ul></li>

</ul>

<ol start="2">

 <li>Add user record</li>

</ol>

Welcome to the COMP2396 Authentication system!

<ol>

 <li>Authenticate user</li>

 <li>Add user record</li>

 <li>Edit user record</li>

</ol>

What would you like to perform?

Please enter your command (1-3, or 0 to terminate the system):

<strong>2 </strong>

Please enter your username:

<strong>Raymond </strong>

Please enter your password:

<h2>123456</h2>

Your password has to fulfil: at least 1 small letter, 1 capital letter,

1 digit!

Please enter your password:

<strong>123456Abc </strong>

Please re-enter your password:

<strong>123456Abc </strong>

Please enter your full name:

<strong>Raymond Chan </strong>

Please enter your email address:

<strong><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="fc9f9e9f949d92bc9f8fd2949789d29497">[email protected]</a> </strong>

Please enter your phone number:

<h2>12345678</h2>

Record added successfully!

Please enter your command (1-3, or 0 to terminate the system):

<ul>

 <li>Define a User class to store the following:

  <ul>

   <li>Username o Hashed password o Full Name o Email address o Phone number</li>

   <li>Failed login count o Account locked</li>

  </ul></li>

 <li>Add a user record in the authentication system.</li>

 <li>If the username is used by another, print out “The username is already taken!” right after the user inputted the desired username and exit the add user process.</li>

 <li>Use the hashing function to hash the user input password. <strong>The system should store the hashed password instead of the plain text password</strong>.</li>

 <li>The program should check if the password fulfils the following requirements:

  <ul>

   <li>The password should contain at least 6 characters, with at least 1 small letter, 1 capital letter, 1 digit.</li>

  </ul></li>

 <li>The program should check if the two passwords entered are identical. If not identical, print out “Passwords do not match, no user added!” and exit the add user process.</li>

</ul>




<ol start="3">

 <li>Authentication with error handlings and error count</li>

</ol>

Please enter your command (1-3, or 0 to terminate the system):

<strong>1 </strong>

Please enter your username:

<strong>Raymond </strong>

Please enter your password:

<h2>123456Abc</h2>

Login success! Hello Raymond!

Please enter your command (1-3, or 0 to terminate the system):

<ul>

 <li>The authentication module should validate if the user can provide a correct username and password.</li>

</ul>

<table width="0">

 <tbody>

  <tr>

   <td width="569">Please enter your command (1-3, or 0 to terminate the system):<strong>1 </strong>Please enter your username: <strong>Ray </strong>Please enter your password:<strong>123456Abc </strong>User not found!Please enter your command (1-3, or 0 to terminate the system):</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>If the user tries to login with a username that does not exist, print out “User not found!”.</li>

</ul>

<table width="0">

 <tbody>

  <tr>

   <td width="621">Please enter your command (1-3, or 0 to terminate the system):<strong>1 </strong>Please enter your username:<strong>Raymond </strong>Please enter your password: <strong>147852369 </strong>Login failed!Please enter your command (1-3, or 0 to terminate the system):<strong>1 </strong>Please enter your username:<strong>Raymond </strong>Please enter your password: <strong>147852369 </strong>Login failed!Please enter your command (1-3, or 0 to terminate the system):<strong>1 </strong>Please enter your username: <strong>Raymond </strong>Please enter your password: <strong>147852369 </strong>Login failed!Please enter your command (1-3, or 0 to terminate the system):<strong>1 </strong>Please enter your username:<strong>Raymond </strong>Please enter your password:<strong>147852369 </strong>Login failed! Your account has been locked!Please enter your command (1-3, or 0 to terminate the system):</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>If the user enters a wrong password, print out “Login failed!”.</li>

 <li>If the failed count is less than 3 and the user can login successfully, the failed count will reset to 0.</li>

 <li>If the failed count is greater than or equal to 3, the user account is locked, and the user will not be allowed to login again. In this case, no matter the user has inputted a correct password not, print out “Login failed! Your account has been locked!”.</li>

</ul>




<ol start="4">

 <li>Modify user record</li>

</ol>

<table width="0">

 <tbody>

  <tr>

   <td width="570">Please enter your command (1-3, or 0 to terminate the system):<strong>3 </strong>Please enter your username:<strong>Raymond </strong>Please enter your password:<strong>123456Abc </strong>Login success! Hello Raymond!Please enter your new password:<strong>123456Acb </strong>Please re-enter your new password:<strong>123456Acb </strong>Please enter your new full name:<strong>Raymond Chan </strong>Please enter your new email address: <strong><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="8be8e9e8e3eae5cbe8f8a5e3e0fea5e3e0">[email protected]</a> </strong>Record update successfully!Please enter your command (1-3, or 0 to terminate the system):</td>

  </tr>

 </tbody>

</table>

<ul>

 <li>To modify the user record, the user has to provide the username and password before he can edit the record.</li>

 <li>The program should handle incorrect username or password input in the same way as stated in part 3. In those cases, the user will not be prompted to edit the user record. (Refer to part 3 for sample output)</li>

 <li>When the user successfully login, allow the user to change the password, full name, and email address.</li>

 <li>The program should check if the two new passwords entered are identical. If not identical, print out “New passwords do not match, user record not edited!” and exit the edit user process.</li>

</ul>




<ol start="5">

 <li>Exit the program

  <ul>

   <li>When “0” is inputted to the system, your program should terminate.</li>

  </ul></li>

</ol>




<ol start="6">

 <li>Reading user input

  <ul>

   <li>You must use BufferedReader to read user inputs.</li>

   <li>Declare the BufferedReader once in your program.</li>

   <li>Call readLine() once to read one line of user input.</li>

   <li>If you fail to do so, your program may not be able to read the user input from the Moodle evaluation system.</li>

  </ul></li>

</ol>

<table width="0">

 <tbody>

  <tr>

   <td width="635">// Declare BufferedReader to read from System.inBufferedReader input = <strong>new</strong> BufferedReader(<strong>new</strong> InputStreamReader(System.<strong><em>in</em></strong>));// Use readLine() wherever reading user input is needed to read one line of inputString inputLine; <strong>try</strong> {inputLine = input.readLine();} <strong>catch</strong> (IOException e) {System.<strong><em>out</em></strong>.print(“Input Error.”); }</td>

  </tr>

 </tbody>

</table>