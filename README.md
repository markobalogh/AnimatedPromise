# AnimatedPromise
Angular 7 attribute directive allowing a css animation to play while a promise is pending and finish when the promise is resolved.

**Be sure to check browser compatibility:** https://developer.mozilla.org/en-US/docs/Web/API/Animation

# Usage

There are two basic usage modes:
1) Building a basic animation with directive inputs in angular template syntax
2) Using a custom animation object defined in your component typescript

#1 is easiest but less powerful - you are limited to a small subset of all possible animations - but this will often be satisfactory because typically only one animated property is necessary to communicate the pending state to the user.

#2 is more powerful but less convenient due to the need to set up an animation in your component typescript.

## Animation defined by multiple directive inputs

`<button (click)="apiDataPromise = getApiData()" [animatedPromise]="apiDataPromise" [animateProperty]="'background-color'" [startValue]="rgba(0,0,0,0)" [finishValue]="rgba(0,0,0,1)" [duration]="1000">Click me!</button>`
