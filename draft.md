# Understanding Recursion

Recursion. What's that? I dunno, should probably Google it….  
[ google image ]  
Very funny google. (if you don't understand that joke, you'll understand it when you understand recursion jokes.) A [friendlier web service](http://en.wikipedia.org/wiki/Recursion) starts off this way: "Recursion is the process of repeating items in a self-similar way." The simplest example I can think of might be a spiral - it sort of goes around and in a little, and then goes around and in a little and goes around and in a little, etc.  
Here's another real-world example that is a little more procedural and will get our brains warmed-up to go fully into some real code:

## Real-World Recursion

You're in front of a mailbox with these instructions:   
>*if you are not holding an iPhone in your hand, open the next thing you can.  
repeat.*

Since you have a thing (mailbox) that isn't an iPhone, you open it and find a shipping box. It's a thing that isn't an iPhone so you open it and find an iPhone box. It's not an iPhone and it's a thing: you open it and have both an iPhone and a headphones box. You have an iPhone so you stop. Simple enough?

What if i left out the "if you're not holding an iPhone" part? Your instructions would be:  
>*open the next thing you can.  
repeat.*

You'd have gotten to the iPhone and headphones box part and then opened the next thing you could and you'd have a pair of headphones. Since you're a good instruction follower, you'd maybe tear the headphones open and have some sort of little speaker in your hand. You'd rip that open and have some other electronics wizardry and keep going - before you know it you'd be [ripping apart](http://en.wikipedia.org/wiki/Big_Rip) the fabric of space-time\* - and that's what trying to imagine recursion can feel like if you're approaching it the wrong way: Like the fabric of your brain is being shredded by a guy on a wild hunt for an iPhone. Well, not *specifically* like that, maybe.

## Getting closer to the code...

If we were to write the above instructions in psuedocode it might look like this:

```
open_thing(thing)
  if not iphone, open_thing(next_thing)
end
```

Let's notice and remember a few important things about the above code.  

1. The open_thing method is called inside itself
2. When it is called within itself, the argument it takes is *similar* but not *identical* to the argument it takes outside.
3. There's an **if** somewhere

You could say it is **repeated in a self-similar manner.** It doesn't open the same thing again and again - it opens a *next_thing*. So It's recursive! But in a special way because there's also that **if**. The **if** defines our *Base Case*. The thing that tells us to stop recursing. To avoid tearing open the headphones.

## Pause

I forgot to tell you why I'm writing this. Recursion can be a bewildering topic for some. Before this post my understanding of it danced around the periphery of the concept. Yea, I knew what it meant and how it generally worked and about fractals and all that, but I couldn't *intuit* the workings of it - and more importantly, relative to my current endeavor: I didn't get how the heck a computer makes sense of it. I don't want to take such an interesting, complex and pragmatically useful topic on faith. I want to *get* it. If you feel the same way then please read on. I promise your understanding will be different by the end. 

## Back to Learning!

As I see it, the typical confusion when thinking about recursion (in terms of programming) comes from two sources: 

- Poor understanding of how the base case works
- Visualizing how the computer will interpret your code

The idea of repeated iteration is not foreign to a programmer. We `each`, `loop`  all the time ( heh ). The key is to realizing that recursion with a base case is similar to iteration - it'll stop eventually - and that recursive functions get evaluated exactly the same as any other code.  
Visuals help and as always: 
###Understanding is reached by moving methodically in very tiny steps while replacing large complex chunks with smaller, digestible ones 
So let's do that!

## Visuals, Examples, Graphs, Yay!

Here is the code for a real 

















\* - *Ripping Spacetime*, pretty awesome speed metal band name?
 