Download Link: https://assignmentchef.com/product/solved-lab-7-of-7-sequential-files-sovled
<br>
Lab Overview – Scenario/Summary




You will code, build, and execute a program that requires sequential files to create an address database.




Learning Outcomes




<ol>

 <li>Continue using a menu system with console applications</li>

 <li>Be able to write a console application</li>

 <li>Demonstrate entering, appending, storing, and retrieving records</li>

 <li>Be able to write lines of output to a text file in order to create a report</li>

</ol>

<strong> </strong>

<ol>

 <li>Deliverables</li>

</ol>




<table>

 <tbody>

  <tr>

   <td width="85"><strong>Section</strong></td>

   <td width="456"><strong>Deliverable</strong></td>

   <td width="136"><strong>Points</strong></td>

  </tr>

  <tr>

   <td width="85"><strong>Step </strong></td>

   <td width="456">Program Listing and Output</td>

   <td width="136"><strong>45</strong></td>

  </tr>

 </tbody>

</table>







<ol>

 <li>Lab Steps</li>

</ol>

<strong> </strong>

Preparation:




If you are using the Citrix remote lab, follow the login instructions located in the iLab tab in Course Home.




Locate the Visual Studio 2010 icon and launch the application.




Lab:




<table>

 <tbody>

  <tr>

   <td width="677"><strong>Step 1: </strong>Requirements: An Address Database</td>

  </tr>

  <tr>

   <td width="677">Create a C++ console application that will store and retrieve names and addresses in a text file.The program should do the following.

    <ol>

     <li>It should accept a series of names and addresses from the console.</li>

     <li>The user’s input should be written to a text file in the CSV format described in the lecture, but do not include the field names in the first row of the file.</li>

     <li>Read the records from the text file, and display them in a user-friendly format.</li>

     <li>Provide a menu to allow the user to append records to the file, display the records, or exit the application.</li>

    </ol>Build upon the code below to complete the assignment.

    <table width="70%">

     <tbody>

      <tr>

       <td width="100%">//Specification: Append and display records in a address database#include &lt;iostream&gt;#include &lt;fstream&gt;#include &lt;string&gt;using namespace std;void menu(void);void writeData(void);void readData(void);string * split(string, char);const char FileName[] = “TestAddress.txt”;int main () {menu();return 0;} //end mainvoid menu(void) {//allow user to choose to append records, display records or exit the program}//end menuvoid writeData(void){//Write the Address Info to a file}//end write datavoid readData(void){//read data from a file//use the split function to break a//deliminated line of text into fields}//end read datastring * split(string theLine, char theDeliminator){//Break theline into fields and save the fields to an array.//Each field will occupy one element in a character array.//theLine is a string with fields separated with theDeliminator character.//Assumes the last field in the string is terminated with a newline.//Useage: string *theFields = split(lineBuffer, ‘,’);//determine how many splits there will be so we can size our arrayint splitCount = 0;for(int i = 0; i &lt; theLine.size(); i++){if (theLine[i] == theDeliminator)splitCount++;}splitCount++; //add one more to the count because there is not an ending comma//create an array to hold the fieldsstring* theFieldArray;theFieldArray = new string[splitCount];//split the string into seperate fieldsstring theField = “”;int commaCount = 0;for(int i = 0; i &lt; theLine.size(); i++){ //read each character and look for the deliminatorif (theLine[i] != theDeliminator) {theField += theLine[i]; //build the field}else { //the deliminator was hit so save to the field to the arraytheFieldArray[commaCount] = theField; //save the field to the arraytheField = “”;commaCount++;}}theFieldArray[commaCount] = theField; //the last field is not marked with a comma…return theFieldArray;} //end split</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

  <tr>

   <td width="677"><strong>Step 2: </strong>Processing Logic</td>

  </tr>

  <tr>

   <td width="677"> Using the pseudocode below, write the code that will meet the requirements.The pseudocode for the writeData function is shown below.

    <table width="50%">

     <tbody>

      <tr>

       <td width="100%">Startopen the text file to appendstart do while loopAllow user to enter namestore name (using getline method)Allow user to enter citystore city (using getline method)..write name, city, etc. to the fileend loopclose the fileEnd</td>

      </tr>

     </tbody>

    </table>The program input should appear similar to this.

    <table width="40%">

     <tbody>

      <tr>

       <td width="100%">Append RecordsName……….John SmithStreet………902 Union AveCity…………Any TownState………..TXZip Code……78552“Enter another Record? (Y/N) “</td>

      </tr>

     </tbody>

    </table>The file structure should look like this.

    <table width="40%">

     <tbody>

      <tr>

       <td width="100%">John Smith, 902 Union Ave, Any Town, TX, 79552Eric Jones, 345 State Way, Fresno, CA, 93432…</td>

      </tr>

     </tbody>

    </table>The file output should appear similar to the following.

    <table width="40%">

     <tbody>

      <tr>

       <td width="100%">Show Records__________________________________________Record #1Name………..John SmithStreet……….902 Union AveCity………….Any TownState………..TXZip Code……78552__________________________________________Record #2Name………..Eric JonesStreet……….345 State WayCity………….FresnoState………..CAZip Code…….93432__________________________________________(A)ppend Records, (S)how Records, (E)xit</td>

      </tr>

     </tbody>

    </table>  <strong> </strong></td>

  </tr>

  <tr>

   <td width="677"><strong>Step 3: </strong>Create a New Project</td>

  </tr>

  <tr>

   <td width="677">Create a new project and name it LAB7. Write your code using the processing logic in Step 2. Make sure you save your program.</td>

  </tr>

  <tr>

   <td width="677"><strong>Step 4: </strong>Compile and Execute</td>

  </tr>

  <tr>

   <td width="677">a)    Compile your program. Eliminate all the syntax errors. b)    Build your program and verify the results of the program. Make corrections to the program logic, if necessary, until the results of the program execution are what you expect. </td>

  </tr>

  <tr>

   <td width="677"><strong>Step 5: </strong>Print Screenshots and Program</td>

  </tr>

  <tr>

   <td width="677"><em> </em>1.    Capture a screen print of your output. (Do a print screen and paste into an MS Word document.)2.    Copy your code and paste it into the same MS Word document that contains the screen print of your output.3.    Save the Word document as Lab07_LastName_FirstInitial. </td>

  </tr>

  <tr>

   <td width="677"><strong>END OF LAB</strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>