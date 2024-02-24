# EmmaB
I am a student.
<!DOCTYPE html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Make-Up Assignment</title>
<style>
   button
   {
color: rgb(58, 214, 53);
background-color: black;
border-radius: 8px;
   } 
</style>
</head>
<body>
    <h1>Multiple Choice</h1>
    <form id="multipleForm">
        <div class="question">
            <b><p>1. What does HTML stand for ?</p></b>
            <input type="radio" name="qn1" value="hyperl"> Hyperlinks and Text Markup Language<br>
            <input type="radio" name="qn1" value="hpert"> Hyper Text Markup Language<br>
            <input type="radio" name="qn1" value="home_to"> Home Tool Markup Language<br>
        </div>
        <div class="question">
            <b><p>2. Who is making the Web standards?</p></b>
            <input type="radio" name="qn2" value="the_wwc"> The World Wide Web Consortium<br>
            <input type="radio" name="qn2" value="mozilla"> Mozilla<br>
            <input type="radio" name="qn2" value="google"> Google<br>
            <input type="radio" name="qn2" value="microsoft"> Microsoft<br>
        </div>
        <div class="question">
            <b><p>3. Choose the correct HTML element for the largestheading:</p></b>
            <input type="radio" name="qn3" value="heading"> &lt;heading&gt;<br>
            <input type="radio" name="qn3" value="h1"> &lt;h1&gt;<br>
            <input type="radio" name="qn3" value="h6"> &lt;h6&gt;<br>
            <input type="radio" name="qn3" value="head"> &lt;head&gt;<br>
        </div>
        <div class="question">
            <b><p>4. What is the correct HTML element for Inserting a line break?</p></b>
            <input type="radio" name="qn4" value="lb"> &lt;lb&gt;<br>
            <input type="radio" name="qn4" value="br"> &lt;br&gt;<br>
            <input type="radio" name="qn4" value="break"> &lt;break&gt;<br>
        </div>
        <div class="question">
            <b><p>5. What Is the correct HTML for creating a hyperlink?</p></b>
            <input type="radio" name="qn5" value="a_name"> &lt;a name="http://www.w3schools.com"&gt;W3Schools.com&lt;/a&gt;<br>
            <input type="radio" name="qn5" value="a_url">  &lt;a url="http://www.w3schools.com"&gt;W3Schools.com&lt;/a&gt;<br>
            <input type="radio" name="qn5" value="a_href"> &lt;a href="http://www.w3schools.com"&gt;W3Schools.com&lt;/a&gt;<br>
        </div>
        <div class="question">
            <b><p>6. Inline elements are normally displayed without starting a new line.</p></b>
            <input type="radio" name="qn6" value="true"> True<br>
            <input type="radio" name="qn6" value="false"> False<br>
        </div>
        <div class="question">
            <b><p>7. How can you make a bulleted list?</p></b>
            <input type="radio" name="qn7" value="dl"> &lt;dl&gt;<br>
            <input type="radio" name="qn7" value="ul"> &lt;ul&gt;<br>
            <input type="radio" name="qn7" value="ol"> &lt;ol&gt;<br>
            <input type="radio" name="qn7" value="list"> &lt;list&gt;<br>
        </div>
        <div class="question">
            <b><p>8. What is the correct HTML for making a drop-down list?</p></b>
            <input type="radio" name="qn8" value="input_type0"> &lt;input type="dropdown"&gt;<br>
            <input type="radio" name="qn8" value="input_type1">&lt;input type="list"&gt; <br>
            <input type="radio" name="qn8" value="select"> &lt;select&gt;<br>
            <input type="radio" name="qn8" value="list"> &lt;list&gt;<br>
        </div>
        <b><button type="button" id="resultBtn">Result</button></b>
    </form>
    <div id="result"></div>

    <script>
        document.getElementById('resultBtn').addEventListener('click', function() {
            let totalMarks = 0; 
    
            // Calculate marks for each question
            
            const answers = {
                'qn1': 'hpert',
                'qn2': 'the_wwc',
                'qn3': 'h1',
                'qn4': 'br',
                'qn5': 'a_href',
                'qn6': 'true',
                'qn7': 'ul',
                'qn8': 'select'
            };
    
            Object.keys(answers).forEach(question => {
                const selectedAnswer = document.querySelector(`input[name="${question}"]:checked`);
                if (selectedAnswer) {
                    if (selectedAnswer.value === answers[question]) {
                        // If correct, add 5 marks to total
                        totalMarks += 5;
                    } else {
                        // If wrong, do nothing (0 marks)
                    }
                } else {
                    // If no answer selected, do nothing (0 marks)
                }
            });
    
            //Display total marks -->
            document.getElementById('result').innerText = `Total Marks: ${totalMarks}`;
        });
        //This is end of my make-up assignment Thanks Madam!
    </script>
</body>
</html>

