+++
date = '2026-07-28T21:15:16+02:00'
draft = true
title = 'Digital desire paths, or the joy of userscripts'
+++

## Desire Paths

The first thing that comes up in my image search for 'desire path' is this.

[[https://allwork.space/2026/01/what-are-desire-paths-and-what-do-they-have-to-do-with-coworking/]]

I think of this concept often. It comes to my mind every time I try to find 'X' or 'leave me alone' or 'fuck off' on a privacy policy banner, but find only 'I accept' and 'your privacy choices'. Or when a paywall jumps at me just as I move past the first paragraph of an article. It's easy to spot and utilise a desire path when walking through your neigbourhood. On the internet, however, things are different. Adblock helps the browsing experience from becoming completely unbearable, but It's more of a city worker siphoning sewage from inbetween the cobblestones of the road, and not a new alternate path for shaping our experience along a more natural path.

The analogy between walking in the park and browsing the internet breaks down quickly, as desire paths in real life are formed by the fact that many people choose them over the planned paths; What I'll be arguing for is more of a personal solution. 


My answer to this problem (at least in the browsing experience on a computer) is a personal userscript library.


> A userscript (or user script) is a program, usually written in JavaScript, for modifying web pages to augment browsing. Uses include adding shortcut buttons and keyboard shortcuts, controlling playback speeds, adding features to sites, and enhancing the browsing history
Wikipedia

It sounds quite simple, and it is! One often forgets that for all their complexity, web browsers ultimately wrangle quite simple files in the end, and the result is often a bland html document. At the same time, browsers embedd an entire UI stack for us, and both a programmatic and terse way of interacting with it. Javascript, for all it's folly, is quite a good language for a quick and dirty script meant to bend a stubborn website to our will: it can achieve a lot in very few lines, especially if one knows how to search through browser APIs.


The process of accumulating the scripts took me by suprise. I'd scribble a couple lines here and there, just to save myself jumping through a hoop or two on the next wisit to some site, and soon enough colleagues started to say in bewilderment when looking at my screen: "Since when does springer link to scihub on their articles?", or "How'd you get the search bar to actually work?". 
Of course, whenever a thought of automating anything is banging around in my head a [https://xkcd.com/1205/](certain xkcd) is trying hard to act in opposition. And yes, while being technically correct about the timeframes, I'd argue that the time shaved off is one thing, but the mental fatigue and a subjective experimence is another (though they do correlate, especially if the time shaved would have been spent waiting or clicking through bullshit).

So, here's a couple of my own use-cases:
### Paywall-avoider
Resources like [Read something wonderfull](https://readsomethingwonderful.com/) bring me enormous joy. One irk I have, however, is that every now and again I stumble into an article that turns out to be paywalled. With ~5 lines of javascript you can generate a link to paywall-skipped version that clicks itself.

### Podcast player 
I recently revisited a podcast I've listened through some years ago. It's hosted online, with simple html masterpage linking all the chapter's `.mp3` files. I soon grew tired of clicking back and forth between chapters. A `querySelector`, `map` and `filter` on the masterpage later, having ordered list of all the chapters and their URLs, I could embedd simple controls for next/prev chapter on the browser's mp3 player page. Just click next chapter straight from playing previous one.

### Brainrot spiral mitigator 
With some manager-dependent fuckery, you can talk to your localhost (or even external servers) from the script. This means you can have persistent state that is independent of the website itself. 
This technique is a bit more involved, since it requires that you make and run additonal server, but it is also more powerful.
I figured that I could use this to track the time I spent on social media, and after reaching some threshold, act on my higher self's behalf and firewall the dopamine-filled tarpit away.
Can I rewrite the rules back? Sure. But in practice the effort exerted to do that is high enough that I usually don't, and so the desired outcome is reached.
Here I want to make another point: I bet I could do the same with some standard, polished browser extension. But the act of having to think about the problem, and the quick orchestraction of a solution places me into the role of an active participant in problemsolving. 
Imagine my solution stops working, let's say I have a convenient rules-rewriter in my shell history, or in the case of some standard extension I have developed muscle-memory of the exact sequence of clicks to disable it. In the case of the extension, nothing I can do now, but for my script? Hmmm, let's think. I can make it password-protect the unlock mechanism, and give me a password when I solve a sudoku. Or do a n-back puzzle. Or review my flashcards. Or the unlock code is sent to someone I know to pass it back to me. I can actively participate in solving the problem. Could the social pressure make me less likely to ask for the code? Could reviewing my flashcards change my mood to abandon the doomscroll urge? Isn't it wonderful to be able to check and play around?


All those examples are not single-handedly curing brainrot, fixing the internet, or doing anything high and mighty -- but they serve as a tool and a reminder.A reminder that I can shape my own experience however I please. And a tool to allow doing so with minimal effort.


PS. This niche could also serve pretty well for teaching people how to program. I'm of the opinion that the only way to learn is by doing and the best thing to do is something practical and useful. However, there is a certain level of knowledge, where building a useful program from scratch feels overwhelming, but yet no existing useful program is simple enough to modify and tinker with. Modifying websites is great for this - we already visit them for their content, that's where the usefulness comes from, and we can improve some pain points with our scripts!


PS 2: If this post convinced you, make sure to familiarise yourself with security implications that usescripts exist in. My simple setup: I have a separate vanilla browser for the 'logged-in' experience (financial transactions, personal information, etc), and a daily driver browser -- enhanced  with multitude of tiny scripts.
