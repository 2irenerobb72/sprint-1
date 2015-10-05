# Review

Nice work.

Your biggest issues have to do with the HTML, and are hard to diagnose because the code is messy.

It's very important to have *readable* code, and to do that, we need to indent carefully and properly. Do you see how carefully the `roles.html` file is indented. Compare that side-by-side with your `index.html`. Do you see the difference? (Some people don't. If you've never been trained to see detail, you may not. Please let me know if this is difficult for you.)

If you can see the difference, your next task is to clean up your `index.html` file to make it readable.

Consider that each HTML element is like a box. We put other HTML elements or content into the box. So HTML is a set of boxes inside boxes inside boxes.

We mark the start of a box with a tag, and the end of the box with a slightly different tag. Everything between those tags is "inside the box", that is, inside the HTML element.

**Please indent the contents of each HTML element two spaces.**

So, for example, you have this:

```html
<aritcle>
  <header>
    <h2>Dogs</h2>
    <img src="http://i.imgur.com/oikbZjW.jpg?1">
    <p>This is a dog, he can smile. He is a mix, a terrier and a chihuahua. His favorite thing to do is chase cats, even though he is small. </p>
  </header>
</article>
```

This isn't too bad, except that you have a typo in the first tag (look closely) that will break all your code. (You have "aritcle".) Also, the lines should be limited to 80 characters or fewer, so the paragraph line is too long. Indent the content on it's own line(s):

```html
<article>
  <header>
    <h2>Dogs</h2>
  </header>

  <img src="http://i.imgur.com/oikbZjW.jpg?1">

  <p>
    This is a dog, he can smile. He is a mix, a terrier and a chihuahua. His
    favorite thing to do is chase cats, even though he is small.
  </p>
</article>
```

Note also that you have placed the image and the paragraph inside the header, but they're not part of the header, are they? They're part of the body of the article, so they go outside of the header. Look at the above code and compare yours with ours until you're clear on the differences. Slack us if you're still stuck.

Here's another example:

```html
<footer>
  <p>Copyright:IreneWins</p>
  <a href="I win"</a>
  <a href="I really do"</a>
</footer>
```

What's wrong with this? Well, there are a couple of minor things. For example, copyright is normally with a date and a space, not with a colon and no space, but hey, we'll put that down to your "style". And hrefs *must be* URLs, so you, uh, haven't won yet. But you will. :-) But there's one more error here.

I think that you actually intended for the "I win" and "I really do" to be the *labels* of the `<a>` tags, which would mean that they would go between the opening and closing tags. But do you see what has happened here? The opening `<a>` tag never closes. It looks like this: `<a`. So the text is not a label.

What you want is this:

```html
<footer>
  <p>Copyright 2015 by IreneWins</p>
  <a href="http://irenewins.com/">I win</a>
  <a href="http://irenewins.com/noreally">I really do</a>
</footer>
```

Do you see the difference? Study them until you do. Then go back and clean up your code and commit the changes.

When you indent your code properly, it will be easy to see that you've got your tags all mixed up.

For example, on line 30, you open a `<nav>` element (think box). On line 31, you open a `<div>` element. But then you close the `<nav>` element on line 37. How is this possible? The `<div>` element (box) is *inside* the `<nav>` element, *but you have not closed it yet*.

If you open an element *inside* another element, then you must close the latter element *before* you close the former. Does this make sense? Please ask questions on Slack if not.

Let's try another pass at the `index.html` file (just repairing the one you have, don't make a new one). Use the `roles.html` file as an example. And we'll keep making passes over this file until we get it perfect.

Nice work. Let's get it cleaned up so you can have it as a reference for future weeks.
