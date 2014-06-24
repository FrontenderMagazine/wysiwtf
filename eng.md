# WYSIWTF

Arguing for “separation of content from presentation” implies a neat division
between the two. The reality, of course, is that content and form, structure and
style, can never be fully separated. Anyone who’s ever written a document and
played around to see the impact of different fonts, heading weights, and
whitespace on the way the writing flows knows this is true. Anyone who’s ever
squinted at HTML code, trying to parse text from tags, knows it too.

On one hand, the division of labor between writing and presentation can be seen
at every point in our history. Ancient scribes chiseling stone tablets, medieval
monks copying illuminated manuscripts, printers placing movable type—we’ve never
assumed that the person who produces the document and the person who comes up
with the ideas must be one and the same.

And yet, we know that medium and message are intertwined so tightly, they can’t
be easily split apart. Graphic designers rail against the notion that “look and
feel” can be painted on at the end of the process, because design influences
meaning. The more skilled we are as communicators, the more we realize that the
separation of content from presentation is an industrial-age feint, an attempt
to standardize and segment tasks that are deeply connected.

Today, we try to enforce the separation of content and form because it’s good
for the web. It’s what makes web standards possible. It enables social sharing
and flexible reuse of content. It supports accessibility. It’s what will keep us
sane as we try to get content onto hundreds of new devices and form factors.

When talking about how best to separate content from presentation, designers and
developers tend to focus on front-end code—which makes sense, because that’s
what we have the most control over. But, as with so many challenges we have with
content on the web, the real issue lies in the tools we give content creators to
help them structure, manage, and publish their content. The form that content
takes depends as much on CMS as it does on CSS.

How should content management tools guide content creators to focus on meaning
and structure? What’s the right amount of control over presentation and styling
in the CMS? And how should these tools evolve as we break out of the web page
metaphor and publish content flexibly to multiple platforms? Let’s look at three
tools that sit at the intersection of content and form.

## Preview button

Even the most die-hard structured content editors still like seeing what their
work is going to look like. Writers print out documents for editing to give them
a different view from what they see on the screen. Bloggers instinctively hit
the preview button to look at their work the way a user will see it.

Whoops. Decades of work refining the emulators between desktop publishing
programs and laser printers means that writers can feel confident that their
document will look virtually identical, regardless of where it’s printed. We’ve
carried that assumption over to the web, where it’s categorically untrue.
Different browsers render content in their own vexingly special way. Users can
change the font size—even add their own custom style sheet. Today, the same
document will render differently on desktops, tablets, and mobile devices. The
preview button is a lie.

Yet we can’t just throw the baby out with the bathwater. In fact, seeing content
in context becomes even more important as our content now lives across devices
and platforms. Instead of throwing up our hands and saying “preview is broken,”
it’s time to invent a better preview button.

One publishing company I know of has built its own custom preview rendering
interface, which shows content producers an example of how each story will
appear on the desktop web, the mobile web, and an app. Is it perfect? Far from
it. Content will appear in many more contexts than just those three. Is it
better than nothing? Absolutely.

## WYSIWYG

The desktop publishing revolution ushered in by the Macintosh allowed the user
to see a document on screen in a form that closely mirrored the printed version.
The toolbar at the top of the screen enabled the user to add formatting—change
the font, insert an image, add typographic effects like headings and bullets,
and much more.

In an effort to carry over this ease of use to the web, we allow content
creators to embed layout and styling information directly into their content.
Unfortunately, the code added by content creators can be at odds with the style
sheet, and it’s difficult for developers to parse what’s style and what’s
substance. When it comes time to put that content on other platforms, we wind up
with a muddled mess.

What is the right amount of formatting control to give content creators? That’s
a difficult question to answer, because it pierces right to the heart of what’s
stylistic and what’s semantic. Even something as simple as adding bold and
italic text forces us to ask if we’re really just styling the text, or adding
semantic meaning (say, a book title or a warning message.)

Better content modeling can solve some of these problems, encouraging content
creators to appropriately “chunk” their text. By banishing blobs of text with
formatting embedded and replacing them with chunks of clean, presentation-
independent content, we’re building in the distinction between content and form
right from the start.

But imagining that each “chunk” of content is a field in the database (with its
own input field) rapidly devolves into the absurd. That way lies madness. The
real solution isn’t necessarily to “banish blobs,” but to replace the WYSIWYG
toolbar with semantic markup. Rather than entering all text into discrete
fields, content authors wrap text that describes what it is. Our book title
doesn’t need to be a separate field if we can wrap it in the proper tags.

Defining what goes in a field and what goes in a tag requires a tighter
collaboration between content authors, CMS architects, and front-end developers.
It’s time we started having these conversations.

## Inline editing

We’re evolving. Not satisfied to rely just on tools that are vestiges of the
desktop publishing era, we’re developing new and innovative ways to mix up
content and formatting that are unique to the way the web works. There’s no
better example of this than inline editing.

Inline editing allows content creators to directly manipulate content in the
interface, with no separation between the editing screen and the display. Medium
offers an editing interface that’s [identical to the desktop display][1] and 
in-place editing is being [added to Drupal 8 core][2].

One of the questions I get asked most frequently is “how can I get my content
creators to understand why it’s so important to add structure and metadata to
their content?” This, I believe, is one of the fundamental challenges we’re
facing on the web, particularly as we adapt to a multi-channel future. Inline
editing encourages content creators to focus on the visual presentation of the
desktop interface. Just at the moment when we need content creators to think
about the underlying structure, we’re investing in tools that obscure the
“connective tissue.”

Jeff Eaton sums up this problem nicely in a post called 
[Inline Editing and the Cost of Leaky Abstractions][3]:

> The editing interfaces we offer to users send them important messages, 
whether we intend it or not. They are affordances, like knobs on doors and 
buttons on telephones. If the primary editing interface we present is also the 
visual design seen by site visitors, we are saying: “This page is what you 
manage! The things you see on it are the true form of your content.”

The best solution isn’t to build tools that hide that complexity from the user,
that make them think that the styling they’re adding to the desktop site is the
“real” version of the content. Instead, our goal should be to communicate the
appropriate complexity of the interface, and help guide users to add the right
structure and styling.

The era of “desktop publishing” is over. Same goes for the era where we
privilege the desktop web interface above all others. The tools we create to
manage our content are vestiges of the desktop publishing revolution, where we
tried to enable as much direct manipulation of content as possible. In a world
where we have infinite possible outputs for our content, it’s time to move
beyond tools that rely on visual styling to convey semantic meaning. If we want
true separation of content from form, it has to start in the CMS.

[1]: https://medium.com/about/df8eac9f4a5e
[2]: http://drupal.org/project/spark
[3]: https://www.lullabot.com/articles/inline-editing-and-cost-leaky-abstractions