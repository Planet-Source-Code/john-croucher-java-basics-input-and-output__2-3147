<div align="center">

## Java Basics \- Input and Output


</div>

### Description

This tutorial provides any beginner with the basic skills required to start programming in Java.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[John Croucher](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/john-croucher.md)
**Level**          |Beginner
**User Rating**    |4.5 (50 globes from 11 users)
**Compatibility**  |Java \(JDK 1\.1\), Java \(JDK 1\.2\)
**Category**       |[Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/input-output__2-84.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/john-croucher-java-basics-input-and-output__2-3147/archive/master.zip)





### Source Code

<font color="#000000" face="Comic Sans MS" size="2">
<BR>At the end of this tutorial you should be able to create a basic Java program that requests input from a user, does something with the information and displays the results.
<BR>
<BR>In this tutorial we will be making a program that requests the user’s name, the year they were born and the current year. It will then display the user’s name and their age.
<BR>
<BR>The basic structure of a Java program is as follows.
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">class ClassName {
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>The class name must be the same as the file name, for example.
<BR>For our program we will call it Tut1. We will make the file name called Tut1.java so the structure will be
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">class Tut1{
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>Within a class you will find methods the structure of these is as follows.
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">methodName( ){
<BR>}
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>You will notice that there are brackets after the method name. You can place variable names within these brackets which will receive the values passed to the method. I will talk more about this at a later stage.
<BR>
<BR>The most common method that you will use is the ‘main’ method. The class that is actually executed must have this in method in the class. However not every class must have a ‘main’ method. The structure of the main method is as followed:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">public static void main(String args[])
<BR>{
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>Note the capital ‘S’ for string. This is important or you will receive an error.
<BR>
<BR>I believe that there are many different ways of outputting text. I will use one method which uses the standard java package.
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">System.out.println("Welcome To My First Java Program ");</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>Again in this example note the capital ‘S’ for system.
<BR>This code basically prints a line of text which is contained within the quotes. The line is ended, like most lines in java, with a semi colon.
<BR>
<BR>If we put all this code together it will look like this:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">class Tut1 {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public static void main(String args[])
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;	{
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Welcome To My First Java Program”);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>This program will output the following on the screen:
<BR>
<BR>Welcome To My First Java Program
<BR>
<BR>This is the most basic program you can make that provides any functionality.
<BR>
<BR>Next we will extend on this program to request data from the user via the keyboard.
<BR>To read input from the keyboard we will use the standard java classes. We will need to use the IOException class which is in the java.io package.
<BR>
<BR>To use this class we must import the java.io package into this class. This is done by the following:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">import java.io.* ;</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>There are many other packages that you can import in a similar manner.
<BR>
<BR>The first step is to create the InputStreamReader. The format is as follows:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">InputStreamReader varName = new InputStreamReader(System.in) ;</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>This will create the reader and assign it to the variable varName. You can change varName to what ever you want providing you follow the naming rules for a variable.
<BR>This code does the actual reading from the keyboard and converts them to Unicode characters. This is not very useful to us as we want the information in a string. This is where the BufferedReader comes in:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">BufferedReader varName = new BufferedReader(varName) ;</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>Again the rules with the variable names apply here. Also note that you can not have the InputStreamReader and BufferedReader with the same name. I have only done this for demonstration purposes. Also the varName within the brackets in the BufferedReader must be the variable name or your InputStreamReader.
<BR>Here is an example of the actual code that we will use for our project:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">InputStreamReader istream = new InputStreamReader(System.in) ;
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">BufferedReader bufRead = new BufferedReader(istream) ;</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>Note the case of the characters and the semicolons.
<BR>
<BR>The for this example we want to read a line in. You can do this by the following:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">String firstName = bufRead.readLine();</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>*Note the capital L.
<BR>
<BR>To read from the keyboard you must also create a try catch block:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">try {
<BR>}
<BR>catch (IOException err) {
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>To use a try catch block you place the code for reading the values in, in the try section and in the catch block you place any error messages, or what to do if there is an error.
<BR>Here is the code for our project:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">try {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;String firstName = bufRead.readLine();
<BR>}
<BR>catch (IOException err) {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Error reading line”);
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>
<BR>This will try to read the input. It will then catch any IOException errors and print out a user friendly error if one occurs. In this case the error is “Error reading line”.
<BR>Within the try block we will also ask the user to enter in their first name or the user wont know what they are supposed to enter:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">try {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Please Enter In Your First Name: ”);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;string firstName = bufRead.readLine();
<BR>}
<BR>catch (IOException err) {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Error reading line”);
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>
<BR>Lets now put what we have so far of our code together.
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">import java.io.* ;
<BR>
<BR>class Tut1 {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public static void main(String args[])
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;InputStreamReader istream = new InputStreamReader(System.in) ;
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;BufferedReader bufRead = new BufferedReader(istream) ;
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Welcome To My First Java Program”);
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;try {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Please Enter In Your First Name: ”);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;String firstName = bufRead.readLine();
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;catch (IOException err) {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Error reading line”);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>
<BR>Congratulations you have now made a fairly useless program. It asks for information and does nothing with it.
<BR>
<BR>We will now expand on this base code.
<BR>We also want to ask for the user’s birth year and the current year:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">System.out.println(“Please Enter In The Year You Were Born: ”);
<BR>String bornYear = bufRead.readLine();
<BR>
<BR>System.out.println(“Please Enter In The Current Year: ”);
<BR>String thisYear = bufRead.readLine();</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>From this information we want to calculate the person’s age. But there is a problem how do you take a string from another string. You can’t so we must change the string value into a numeric value. We will convert the string values into Integer values using the parseInt function:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">int bYear = Integer.parseInt(bornYear);
<BR>int tYear = Integer.parseInt(thisYear);</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>This code must go in a try catch block. You can then catch the conversion error:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">catch(NumberFormatException err) {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Error Converting Number”);
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>The next step is to calculate the age of the person and output all the data:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">int age = tYear – bYear ;
<BR>System.out.println(“Hello “ + firstName + “. You are “ + age + “ years old”);
<BR></Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>The last step is to combine all our code:
<BR>
<BR></FONT><font color="#0000CD" face="Comic Sans MS" size="2">import java.io.* ;
<BR>
<BR>class Tut1 {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public static void main(String args[])
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;InputStreamReader istream = new InputStreamReader(System.in) ;
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;BufferedReader bufRead = new BufferedReader(istream) ;
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println("Welcome To My First Java Program");
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;try {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println("Please Enter In Your First Name: ");
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;String firstName = bufRead.readLine();
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Please Enter In The Year You Were Born: ”);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;String bornYear = bufRead.readLine();
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Please Enter In The Current Year: ”);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;String thisYear = bufRead.readLine();
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;int bYear = Integer.parseInt(bornYear);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;int tYear = Integer.parseInt(thisYear);
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;int age = tYear – bYear ;
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Hello “ + firstName + “. You are “ + age + “ years old”);
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;catch (IOException err) {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println("Error reading line");
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;catch(NumberFormatException err) {
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(“Error Converting Number”);
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>
<BR>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
<BR>}</Font><font color="#000000" face="Comic Sans MS" size="2">
<BR>
<BR>
<BR>Well that’s your first basic Java program and the end of my first tutorial.
<BR>Check out my site for more tutorials and code.
<BR>
</Font>

