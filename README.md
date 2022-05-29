# Admin Dashboard
This is a design example of an admin dashboard built with responsiveness in mind and making significant use of the CSS Grid features. 

## Features
- A navigation sidebar with links to different pages on the website
- A header with user information, notification button, and profile pictures
- A search bar
- A responsive grid of project cards, each card showing a different project that's easily accessible on screen
- An announcements block on the upper right
- A trending profiles block on the lower right

## Implementation Process
The main goal of this project is to practice my layout skills with CSS Grid, using its many different features to provide a responsive website along with a clean and organized layout.

I started off with designing the overall skeleton of the website, with the fixed-width sidebar to the left, the fixed-height header on top, and the dynamically sized main section. All three sections except the sidebar use CSS Grid to create its entire layout.

Implementing the sidebar and header involved only a few small issues that I was able to solve pretty easily, such as getting the alignments right, figuring out how to import SVG icons, realizing I had to use the line-height property to get paragraph elements to properly align, and figuring out how to get the profile pictures to be contained inside a circle.

Implementing the dynamic layout of the project cards involved a bit more work. I had to use the minmax() function along with the repeat() and auto-fit properties of CSS grid to have the number of columns be dependent on how wide the screen is. In addition, the cards shouldn't shrink down to too small a width in order to prevent overflow or readability issues.

There was also a misunderstanding of the "auto" keyword for grid-template-rows and grid-template-columns. It turns out that "auto" basically acts as "1fr" in that it takes up all remaining available space instead of only the minimum space required to fit the content. The only exception is if it's combined with a "1fr", in that cas the "1fr" takes priority and takes up the remaining space instead of the row or column set to "auto". 

Other smaller issues included figuring out how to get the left blue side border on each card, how to get the gray dividers in between the announcements in the announcements block, and realizing I can use min-content to solve the problem in the previous paragraph.