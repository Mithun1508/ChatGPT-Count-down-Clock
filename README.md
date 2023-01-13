# build a simple yet useful web app — a countdown clock that a user can interact with. Here's the kicker: we'll only use chatGPT + Replit.

 We’ll be using two tools to build this app. I recommend you follow along.

1) ChatGPT (that’s why you’re here).

2) Replit (no, don’t boot up a code editor and terminal, just use Replit).

There’s an art to how you talk to AI. And there’s some banger notes on how to do this already. Read any of the below if you want to dive deeper:

# Intro to GPT-3 and Promp

But sometimes, the most direct approach works.

I simply asked “Can you generate the html code for a countdown clock?” LOL.
ChatGPT obliged and started spittin’ code.

All I did was copy and paste what it wrote into Replit, hit run, and watch the magic happen. Check out the basic html site it generated. I had to hard code the countdown date.

# ChatGPT is conversational. So converse.
What makes ChatGPT interesting is that it’s like having a conversation with someone. It follows along with what you two have already talked about (context). No need to start afresh each time.

Now a countdown clock isn’t very useful if you have to change the actual html code by hand. So I asked ChatGPT this:

“Can you rewrite the code so that a user could input their own time they want to count down to?"

And surely, it did (still needed work, but we were making progress). I won't paste the code here purely because I want you to go and ask it to make something and ask a follow-up to improve the code. But, here's what our output looks like right now when you take the code and paste it in replit.

Kinda basic, but we'll fix that later.

Next, I asked ChatGPT if it could rewrite the code so that I could set the countdown by using a calendar.

"Please rewrite the code so that a person could set the countdown by using a calendar"

ChatGPT understands you and can iterate!

Check out the next version here. Not bad at all.
Our code now looks like this. Note: I don't want you to copy the above code. Just go to chatGPT and start talking! That's the whole point of this article. 

Time to beautify our site with chatGPT.
Honestly, I have always liked the look of an old school all-text site. But I still wanna see if ChatGPT can do more.

Let’s start with something simple — center the text on the page.

Well…here’s the TLDR. You know how it’s a pain in the ass to center stuff sometimes? Apparently AI has problems with it too.

Look at all of that whitespace.

I decided to change tactics and asked for the css code directly.

"please write the css code for style.css so that everything is centered on the web page"

It fixed the problem immediately and even told me how to reference the styling file in my html code!

# The final touches.
If you’ve been playing along, you will notice that ChatGPT is like your buddy that knows how to code. But it’s not entirely good at figuring out what you want — which is exactly like talking to your friend that does nothing but code.
