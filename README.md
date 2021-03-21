# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Josh Fitzgerald**

Time spent: **~5** hours spent in total

Link to project: (insert your link here, should start with https://glitch.com...)

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [X] Playback speeds up on each turn
* [ ] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](your-link-here)


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

N/A



2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

I had relatively little trouble until it came time for the computer to initiate the first tone and visual cue upon the user pressing the start button. I could not figure out what exactly what the problem was but through debugging and seeing the feedback in the console, I realized there was some sort of error in the playSingleClue function, particularly when it called the lightButton function. 
I tried tracing where the logic error was in my implementation, and when I compared my code and how it differed from the tutorial code, I realized I had changed my button names to "firstButton, secondButton, etc." from the tutorial version of "button1, button2, etc." and changed them back to match the tutorial. This removed the error and successfully showed the first button with its corresponding tone when the user pressed start.
Another area of trouble I encountered was the incrementation of the clueHoldTime variable. When I had originally incremented the variable in the for loop, I chose a relatively small incrementation of -25 each iteration. It appeared to be working smoothly each round, but would suddenly speed up an incredible amount at a later round without a corresponding tone. To get around this, I simply incremented less and would test each new value until the problem stopped occurring.



3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

Because Glitch saves progress as you go, I assume to the cloud or to the web server, why is web development not widely regarded as superior to local development on one's personal device that requires frequent saving and memory? Perhaps it is more popular than I think it is, but from my academic experience in coding, nearly everything has been done on my personal computer. 
An additional question I have is if different languages are better-suited to web-based development. I know the walkthrough said that javascript was originally made for web development, but I am not quite sure what features or characteristics make such a claim true. Is Python or Java a good language to use for web development? Why or why not?



4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

A feature I would be interested in adding would be to have a theoretically unlimited pattern instead of capping out at 8. In addition to this feature, I would want to have a highscore tally that the user would be able to see to track what score they should be striving to surpass. A problem that I can see arising in my logic towards the problem would be if I would decide to have an incredibly large array, say, 100 turns, instead of having an array that will randomly add a new element to the pattern after each successful round from the user. Although there is no guarentee that the user gets to 100, if they do somehow reach that mark, then the pattern realistically is not unlimited, so I would have to think which would be a better route to go down in my implementation.



## License

    Copyright [YOUR NAME]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.