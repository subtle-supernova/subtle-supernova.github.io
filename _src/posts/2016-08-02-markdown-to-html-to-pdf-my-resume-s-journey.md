    Title: Markdown to HTML to PDF - My Resume's Journey
    Date: 2016-08-02T00:02:31
    Tags: wkhtmltopdf, html, pdf, markdown

_Replace this with your post text. Add one or more comma-separated
Tags above. The special tag `DRAFT` will prevent the post from being
published._

# How my resume starts out as markdown

## Why would you do this?

Other than my typical reason of "because it's fun?" Document formats are really hard. Not only are they hard, but they're one of the few things in computing we haven't managed to simplify.
Sure, we've made them *featureful* but not *simple*. Have you ever tried to parse an excel file in a meaningful way? It's not fun.

This brings me to my particular problem: I only want to type my resume once, but I wan't it to be as accessable as possible. I love the idea of typing it in markdown. 
I believe markdown to be a sort of mad genius in the same vein as JSON. It only solves about 80% of our problems but it's so easy that it makes it hard to resist. 
Another really great thing about this simplicity is that we can hack on the other 20% it doesn't solve without too much effort. 

## How do I do this?

Well, I've already written about my static content generator. Markdown to HTML isn't exactly exciting. HTML to PDF, however, is barrels of fun. 
To accomplish this I use [wkhtmltopdf](http://wkhtmltopdf.org/). It's a wonderful project that leverages webkit and QT. The coolest part of this tool? You can do it all from CLI.
This has saved my neck a couple of times, because generating PDFs is a pain, but people *love* them. On the flip side, generating HTML is a well explored and decently solved problem. 
That creates a grand solution for us: generate semi-dynamic HTML, and then have some automated process spit out a PDF using wkhtmltopdf. Since it's all in the CLI, you can do this using a simple 
bash script and then leverage arcane things such as the `mail` command for delivery. I love simple things. 

## What's next?

For my resume, I'd like to do some intermediate processing. While wkhtmltopdf supports pulling from a URL directly (which is pretty sweet) we can also use local files. I'll need to remove some 
things like navigation and then add some things like more contact information. I think it'd be a really cool project to let someone enter an email address and recieve the processed resume. 
Well, I've beel looking for a reason to dive into the wide and strange world of OCaml webapps. More on that later, perhaps!

<!-- more -->
