Prompt 1:

I asked ChatGPT the following prompt: What are 2 things I should accept from this plan and one thing I should reject. (and why)

Two things I accepted

I accepted the suggestion to use Flexbox for the header and hero section. This made sense because both sections only needed alignment in one direction (row or column), and Flexbox is good for that.

I also accepted the recommendation to use CSS Grid for the card layout. Grid made it easier to control how many columns appear at different screen sizes.

One Thing I Rejected (and Why)

The AI suggested creating multiple small media queries for different layout changes. I decided not to do that because it would make the CSS file longer and harder to read. Instead, I grouped my changes into two main breakpoints (900px and 600px) to keep things more organized.
__________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

Prompt 2:

While testing the site, I noticed that when I resized the browser to mobile size (under 600px), the hero section was not stacking vertically. The hero card stayed next to the text instead of moving below it.

CSS Snippet 

.hero {
  display: flex;
  padding: 20px;
}

Most Important part of the AI response

The AI explained that Flexbox automatically uses flex-direction: row by default. That means the items stay side-by-side unless you change the direction. It told me that I needed to set flex-direction: column inside a mobile media query to make the hero stack vertically.

What I changed afterwards

What I Changed Afterward

I added a mobile media query and changed the flex direction:

@media (max-width: 600px) {
  .hero {
    flex-direction: column;
  }
}
