# star-wars-crawl

link to the online version: https://xandervdh.github.io/star-wars-crawl/

## What is this about?
In this assignment I made the opening crawler from Star Wars with only HTML and CSS.

## How does it work?
### HTML
```html
<div id="starwars">
    <div id="crawl">
        <h1>CSS STRIKES BACK</h1>
        <p>Holding her is dangerous. If word of this gets out, it could generate sympathy for the Rebellion in the senate. I have traced the Rebel spies to her. Now she is my only link to find their secret base! She'll die before she tells you anything. Leave that to me. Send a distress signal and then inform the senate that all aboard were killed! Lord Vader, the battle station plans are not aboard this ship! And no transmissions were made. An escape pod was jettisoned during the fighting, but no life forms were aboard. She must have hidden the plans in the escape pod. Send a detachment down to retrieve them. See to it personally, Commander. There'll be no one to stop us this time. Yes, sir.</p>

        <p>He says he's the property of Obi-Wan Kenobi, a resident of these parts. And it's a private message for him. Quite frankly, sir I don't know what he's talking about. Our last master was Captain Antilles, but with what we've been through, this little R2 unit has become a bit eccentric. Obi-Wan Kenobi? I wonder if he means old Ben Kenobi? I beg your pardon, sir, but do you know what he's talking about? Well, I don't know anyone named Obi-Wan, but old Ben lives out beyond the dune sea. He's kind of a strange old hermit. I wonder who she is. It sounds like she's in trouble. I'd better play back the whole thing.</p>

        <p>It looks like Sandpeople did this, all right. Look, here are Gaffi sticks, Bantha tracks. It's just...I never heard of them hitting anything this big before. They didn't. But we are meant to think they did. These tracks are side by side. Sandpeople always ride single file to hide there numbers. These are the same Jawas that sold us Artoo and Threepio. And these blast points, too accurate for Sandpeople. Only Imperial stormtroopers are so precise. Why would Imperial troops want to slaughter Jawas? If they traced the robots here, they may have learned who they sold them to. And that would lead them home! Wait, Luke! It's too dangerous. Uncle Owen! Aunt Beru! Uncle Owen!</p>

        <p>That malfunctioning little twerp. This is all his fault! He tricked me into going this way, but he'll do no better. Wait, what's that? A transport! I'm saved! Over here! Help! Please, help! Artoo-Detoo! It's you! It's you!</p>

        <p>Did you hear that? They've shut down the main reactor. We'll be destroyed for sure. This is madness! We're doomed! There'll be no escape for the Princess this time. What's that? Artoo! Artoo-Detoo, where are you? At last! Where have you been? They're heading in this direction. What are we going to do? We'll be sent to the spice mine of Kessel or smashed into who knows what! Wait a minute, where are you going?</p>
    </div>
</div>                
```
Here you can see that I made to div's
<br>
one with id "starwars"
<br>
and another one in the previous one with id "crawl"

### CSS
We are going to start with the body

```html
body {
    overflow: hidden;
    height: 100%;
    color: yellow;
    background-image: url("star-wars-backgrounds-25.jpg");
}
```
to make sure that people can't scroll on the page we use "overflow: hidden" and "height:100%"
and we ad the starry background. We also tell it that the font color has to be yellow

Next we will center the text
```html
#crawl {
    margin: auto;
    width: 50%;
    padding: 10px;
    font-family: "Droid Serif";
    font-weight: bold;
    word-spacing: 5px;
    font-size: x-large;
}
```
We call on the crawl id and add a width of 50% and "margin:auto" so it will be centered.
We also add the font and change the wait.

next we will ad a piece of code to this one to start the animation that we will be creating after
```html
animation: animateCrawl 60s ease-in;
```
"animateCrawl" tells the code the name of the animation he needs to use.

"60s" tells it how long the animation schould last.

and the "ease-in" will tell it to go slower in the beginning and then go faster.

Next we are adding the perspectif to the text with the next piece of code
```html
#starwars {
    transform: perspective(100px) rotateX(10deg);
}
```
it tells the code to give perspective to the text and the rotateX is telling it to rotate backwards to make it look as if it is going away from us.

the last thing to do is add the animation itself
```html
@keyframes animateCrawl {
    0% {
        transform: rotateX(30deg) translateY(-1600px);
    }
    100% {
        transform: rotateX(30deg) translateY(-800px);
    }
}
```
we use @keyframes for that.

we name the animation by putting it after @keyframes.

next we define how the animation should look like at 0%
and at 100%

we keep the rotateX the same but change the "translateY"

with translateY you are going to move the dir on the y axis, so vertically.

also make sure to add normalize.css, it's mainly for the background image