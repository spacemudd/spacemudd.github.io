---
layout: post
title:  "Converting legacy code"
date:   2018-06-28 06:00:11 +0300
categories: code refactoring
---
This short post deals with what I'm experiencing now: writing a legacy code in modern technology.

Truth to be told, many developers (and even I) might wince at the idea of re-writing because it is expensive and draining.

The main problem is while the developers might find the benefit and ease of maintainability, the clients or the users 
will notice little to nothing improvement.

Right now I have legacy accounting software using double-entry bookkeeping concept. It is a based desktop application.

The issues I've encountered so far attempting to manage it were:

- Bugs are difficult to fix because it is propriety language with limited support online.

- When it comes to marketing/sales, desktop applications are seen too difficult to install.

- Generating analytics on users' is very limited. (I can't imagine doing an A/P test)

So I decided to bite the bullet and rebuild the entire application. Here's what I needed:

1. An automated way to test the new application.

2. A working-condition emulator or virtual machine running the legacy application.

3. Patience.

Now here's the interesting thing, when I tried diagnosing a specific feature from A to Z, it was very difficult to
 follow or to write a case test for.

I suppose what I discovered is it _might_ save you time is to commit an action in the legacy code, record the end 
result, and finally do a case test based on the end result, not having to focus solely on every single step being done 
in the old code. 

Now onto the benefits of the new code:

1. Features are automatically tested from the ground up. (Confidence 50/100 - yes, I rarely trust code)

2. Design a better sales pipeline around our product.

3. Quickly update our product without the users noticing. (When we don't want them to know 😉)

But you know what's rather endearing? The way developers of that time did things. In some certain things, you can 
imagine nothing has changed but with other things like database schemas and other concept-like, there has been _a lot_
of improvement and ease.

We must owe it to them because in their time they didn't have `yarn add whateverpackagetheyneed` to end up
with an 8mb app.js.
