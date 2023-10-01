# Web3 Final | Glowforge Pro

<br>

## Overview
The Glowforge Pro checkout flow is a custom site redesigned from [glowforge.com](https://shop.glowforge.com/collections/printers/products/glowforge-pro). The project took place over two terms, designed in Web Graphics 2 (VSCM 221) and coded in Web Graphics 3 (VSCM 222). The goal of the project was to fully develop the checkout flow with HTML and CSS, therefore some page elements like the reviews section are unresponsive to avoid the use of Javascript. 

Three pages are included, a product page, a checkout flow (which is broken up into [two or three steps](#Checkout-Flow)), and a thank you page. The “Buy now” button will start this flow in the live site.

### Organization

HTML files are stored under content. The folder structure is broken up into pages, and then .kit files within to represent sections. I used CodeKit to compile the sections into the checkout, index, and thankyou HTML files that then became the final 3 pages. 

The SCSS files are organized similarly, under `SCSS/sections` the folders are divided into pages, then sections. This is alongside several folders holding universal SCSS for things such as components and navigation. The SCSS is all compiled into one CSS file for the whole site.

<br>

## Branches

Github branches are divided up by page, with one branch to work on each page. Other branches are created for navigation and testing specific features. This was so I could test ideas without having to commit the original branches as it they were still in progress. For info on specific branches, see below.

### [Product-page](https://github.com/evangwhit/Web3-Final-Glowforge/tree/Product-page)

The product page was the most straightforward process to develop. The largest challenges were  using media queries to change the headline “How people use Glowforge” to “Reviews” for mobile, and to add the secondary product photos on larger devices. For the larger displays, I used background images and grid area templates to layout the 4 images to match the Figma file I had designed previously. 

### [Checkout-Flow](https://github.com/evangwhit/Web3-Final-Glowforge/tree/Checkout-Flow)

Checkout posed the largest problems to solve. The mobile flow I had designed included three separate pages for each card while the tablet and desktop displayed one card the entire time and navigated from the “second” to the third. 

In order for the navigation to work for both mobile and desktop, I created three separate stages.

1. The first stage included cards one and two (*receipt* and *shipping*).
2. Second only included stage two (*shipping).*
3. The third included stages one and three (*receipt* and *payment*). 

This allowed me to customize the button destinations with media queries and have the mobile flow got through steps 1-3 while the desktop skipped step two entirely. I then hid the excess cards on mobile and the final product is a seamless checkout flow that takes maximum advantage of screen real estate for each device.

### [Thank-you](https://github.com/evangwhit/Web3-Final-Glowforge/tree/Thank-you)

The thank you page was also simple HTML and CSS layout. I used flexbox to layout the whole section, and then divided the order information into it’s own div at the bottom that then had display:grid applied which made adjustments between the mobile and desktop layouts a simple adjustment to the grid columns.

### [Nav](https://github.com/evangwhit/Web3-Final-Glowforge/tree/Nav)

This was the branch used for the nav bar and footer, I separated these as they were applied universally and I wanted to separate changes here from changes to the individual pages.

### [Nav-testing](https://github.com/evangwhit/Web3-Final-Glowforge/tree/Nav-testing)

The Nav-testing branch was created after I had designed the navigation. It’s purpose was to adjust class names to align with the javascript provided by my professor for a responsive mobile menu. Without an understanding of exactly what the javascript was doing, this took several iterations of tweaking the class names and the HTML structure to make interaction work. Once I solved the problem, I went back to the Nav branch and manually applied my changes. This was the best process for me to avoid the cluttered code I generated when testing the interaction.

### [Shipping-Radio-Testing](https://github.com/evangwhit/Web3-Final-Glowforge/tree/Shipping-Radio-Testing)

This branch was used to customize the radio buttons within the shipping form. The interaction I wanted between the two radio buttons meant I restructured the HTML multiple times as I tested my ability to apply css to the correct classes/tags. After the first iteration, I separated the branch so that I wouldn’t effect the working input fields I had in the form. This allowed me to fix the radio buttons without the fear of damaging the rest of the form.

<br>

# Conclusion

This project consisted of a wide variety of HTML and CSS techniques. I have listed the main components:

- HTML
    - Classes and IDs
    - Unordered lists, divs, sections, forms, links, and images
    - All typography, from H1 to p tags
- CSS
    - SCSS
    - Background image
    - Display: grid, flex, inline
    - mixins
    - media queries
    - variables

If there are any large gaps in my understanding please let me know! I am excited to discover more and have loved the process of problem solving so far.



