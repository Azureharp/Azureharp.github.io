## html parsing preamble

# The Beginnings

there was a time where I knew even less about html

then one day I wanted to read text from some web pages on my phone 

When I took a look at the html I said "golly there's the stuff I want, but there's a bunch of junk inbetween it!"

I was far less inexperienced with rust and so to model that I went with an enum that went something like

```
enum CurrentPosition {
  BeforeContent,
  DoCopy,
  ArrrYeBeInJunkMeLad,
  AfterContent,
}
```

Not a bad idea in itself...

Except it wasn't nearly this clean, and couldn't be
I had to deal with html formatting tags and content, scripts & css showing up at any time

How did I deal? Add more states...

if it was an image, skip it. found a cool script script? Ignore that


I must've some other stuff to make it hard to work with.
All in all it took a few hours to make but it did it's job (didn't get all the text)


still a long way out from beating github.com/y21/tl or github.com/cloudflare/lol-html

