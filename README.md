# Built a simple useful web Application — A countdown clock that a user can interact with. 
# shows how to build a countdown timer in just one minute using ChatGPT!  


#chatgpt #openai #HTML #CSS #JS: 


 Will be using two tools to build this app.

1) ChatGPT 

2) Replit 

There’s an art to how you talk to AI. And there’s some banger notes on how to do this already.

# Intro to GPT-3 and Promp

But sometimes, the most direct approach works.

simply asked “Can you generate the html code for a countdown clock?” LOL.
ChatGPT obliged and started spittin’ code.

All did was copy and paste what it wrote into Replit, hit run, and watch the magic happen. Check out the basic html site it generated. had to hard code the countdown date.

# ChatGPT is conversational
What makes ChatGPT interesting is that it’s like having a conversation with someone. It follows along with what you two have already talked about (context). No need to start afresh each time.

Now a countdown clock isn’t very useful if you have to change the actual html code by hand. So asked ChatGPT this:

“Can you rewrite the code so that a user could input their own time they want to count down to?"

And surely, it did (still needed work, but we were making progress). I won't paste the code here purely because I want you to go and ask it to make something and ask a follow-up to improve the code. But, here's what our output looks like right now when you take the code and paste it in replit.

Kinda basic, but we'll fix that later.

Next, asked ChatGPT if it could rewrite the code so that could set the countdown by using a calendar.

"Please rewrite the code so that a person could set the countdown by using a calendar"

ChatGPT understands you and can iterate!

Check out the next version here. Not bad at all.
Our code now looks like this. Note: I don't want you to copy the above code. Just go to chatGPT and start talking! 

Time to beautify our site with chatGPT.

Let’s start with something simple — center the text on the page.

Well…here’s the TLDR. You know how it’s a pain in the ass to center stuff sometimes? Apparently AI has problems with it too.

Look at all of that whitespace.

Have decided to change tactics and asked for the css code directly.

"please write the css code for style.css so that everything is centered on the web page"

It fixed the problem immediately and even told me how to reference the styling file in my html code!

# I asked ChatGPT that 'Can you generate the html code for a countdown clock'?

![Screenshot (26)](https://user-images.githubusercontent.com/93249038/212460871-71411eb6-f546-4cfc-8d3c-45ee0e263958.png)


# FULL HTML GENERATED CODE


<!DOCTYPE html>
<html>
<head>
  <title>Countdown Clock</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <div id="clockdiv">
    <span id="days"></span> days 
    <span id="hours"></span> hours 
    <span id="minutes"></span> minutes 
    <span id="seconds"></span> seconds
  </div>
  <br>
  <div id="user-input">
  <label for="deadline">Enter a countdown date:</label>
  <input type="date" id="deadline">
  <button onclick="setDeadline()">Set Countdown</button>
  </div>
  <script>
    function getTimeRemaining(endtime) {
      var t = Date.parse(endtime) - Date.parse(new Date());
      var seconds = Math.floor((t / 1000) % 60);
      var minutes = Math.floor((t / 1000 / 60) % 60);
      var hours = Math.floor((t / (1000 * 60 * 60)) % 24);
      var days = Math.floor(t / (1000 * 60 * 60 * 24));
      return {
        'total': t,
        'days': days,
        'hours': hours,
        'minutes': minutes,
        'seconds': seconds
      };
    }
    
    function initializeClock(endtime) {
      var daysSpan = document.getElementById("days");
      var hoursSpan = document.getElementById("hours");
      var minutesSpan = document.getElementById("minutes");
      var secondsSpan = document.getElementById("seconds");

      function updateClock() {
        var t = getTimeRemaining(endtime);

        daysSpan.innerHTML = t.days;
        hoursSpan.innerHTML = ('0' + t.hours).slice(-2);
        minutesSpan.innerHTML = ('0' + t.minutes).slice(-2);
        secondsSpan.innerHTML = ('0' + t.seconds).slice(-2);

        if (t.total <= 0) {
          clearInterval(timeinterval);
        }
      }

      updateClock();
      var timeinterval = setInterval(updateClock, 1000);
    }
    
    function setDeadline() {
    var deadline = document.getElementById("deadline").value;
    document.getElementById("clockdiv").style.display = "block";
    document.getElementById("user-input").style.display = "none";
    initializeClock(deadline);
    }
    
  </script>
</body>
</html>


This code creates a countdown clock that displays the remaining time in days, hours, minutes, and seconds. The user can enter a date as a deadline using an input field and when the user clicks the "Set Countdown" button, the clock is displayed and begins counting down to the deadline that was entered. The code uses JavaScript to calculate the time remaining until the deadline and update the clock display. You can also style the clock using CSS in a separate


# Site is Live Now Do check it out :  

https://spectacular-naiad-f03cbd.netlify.app/ 



![Screenshot (20)](https://user-images.githubusercontent.com/93249038/212231152-e4464d76-f803-4141-bdd5-b006f8903c65.png)

![Screenshot (21)](https://user-images.githubusercontent.com/93249038/212231171-0857abbd-ef67-42b5-b9b0-0d6dc5502f9a.png)

