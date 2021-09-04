# Frontend Mentor - 3-column preview card component

![Design preview for the 3-column preview card component coding challenge](./design/desktop-preview.jpg)

## Welcome! 👋

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

**To do this challenge, you need a basic understanding of HTML, CSS and JavaScript.**

## The challenge

The challenge was for me to build out this 3-column preview card component and get it looking as close to the design as possible.

There were no constraints on which tools could be used to complete the challenge so I used Bootstrap v5.0 alongside a custom CSS style sheet for custom styling.

Users of this project should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

Want some support on the challenge? [Join our Slack community](https://www.frontendmentor.io/slack) and ask questions in the **#help** channel.

## Where to find everything

Our task is to build out the project to the designs inside the `/design` folder. You will find both a mobile and a desktop version of the design.

The designs are in JPG static format. Using JPGs will mean that you'll need to use your best judgment for styles such as `font-size`, `padding` and `margin`.

We will be completing the free version of this challenge but frontend mentor does offer a paid version whereas if you want all of the design files (we provide Sketch & Figma versions) to inspect the design in more detail, you can get access to those files by [subscribing as a PRO member](https://www.frontendmentor.io/pro).

All required assets can be found in the `/images` folder and the assets are already optimized.

A `style-guide.md` file containing the information you'll need, such as color palette and fonts is also included.

## Building your project

Feel free to use any workflow that you feel comfortable with. Below is a suggested process, but do not feel like you need to follow these steps:

1. Initialize your project as a public repository on [GitHub](https://github.com/). Creating a repo will make it easier to share your code with the community if you need help. If you're not sure how to do this, [have a read-through of this Try Git resource](https://try.github.io/).
2. Configure your repository to publish your code to a web address. This will also be useful if you need some help during a challenge as you can share the URL for your project with your repo URL. There are a number of ways to do this, and we provide some recommendations below.

### The Game Plan

Since I haven't had much (really any) experience w/ Figma or any other wireframing tools, I begin my design plan by creating a "hand-drawn" copy of the wireframe and its included elements. This allows me to better visualize how the elements will be placed on the page and takes out alot of the guesswork as it relates to the layout of that section or page and also helps you to think about how CSS classes will be used to create reusable styles as well as how id's will be used to style elements independently.

As a general rule of thumb (for me at least), its ALWAYS as good idea to start by creating the HTML markup. This first step is critical in creating logically structured content.

Now onward to the CSS. We will begin by developing the base/ global styles for the project such as `font-family` and `font-size`. I find that creating a design system and implementing it using CSS variables gets me alot closer to a finished product as opposed to adding the same properties and values to multiple elements. Design systems and CSS variables allow for fast and easy changes to multiple elements and works wonders to "DRY" up your code.

Now that the design system is in place I begin working from left-to-right and top-to-bottom.
Every project is different and will not be approached in the same fashion. Some projects have more complex layout requirements than others. I like to start working on the item that I think might take the most time to design. I do this because I have found truth to the old addage "90% of your time will be spent on 10% of a project" (Paraphrasing).
I Start by adding styles to the top of the page and working downward. I move on to the next section once I'm comfortable with the area I've been working on.

## Deploying the project

As mentioned above, there are many ways to host your project for free. I used github pages to deploy this project and it can be viewed at

- [GitHub Pages](https://pages.github.com/) <-- Add link to live site here?

## What Did I Learn?

As with every project there is almost always something new to learn.

### What to do with the SVG?

I used an <img> tag to link to the external file containing the SVG as it proved to be a simpler solution. Setting the SVG as a background image via CSS would have required me to margin-top or to the paragraph content to prevent it from sitting atop the background image. Whereas linking to the external SVG file using the <img> tag, I was able to set `display: block` which forced the <p> element to the next line and prevented the text content from stting on top of the image.

### Bootstrap & .gitignore

Bootstrap is the only frontend library with which I've had experience and it is an invaluable tool for being able to design layouts faster as opposed to using standalone CSS. This project was built using Bootstrap 5.0.2 locally w/ the project (no CDN) along with a custom CSS stylesheet to allow me to have greater control of styling the elements as needed. I'm also using a `.gitignore` file to ignore certain elements of the project that don't need to be made public. If you include Bootstrap locally in your project and add the Bootstrap directory to `.gitignore` the all of the Bootstrap files and stylings will be ignored.
When I first made the project live I saw that my styling was not the same as it was on my development server. My development environment had all of the correct breakpoints/ containers etc... whereas the live deployment did not. The reason for this is because I added the directory in which the Bootstrap files are located to the `.gitignore` file.

You can resolve the issue of the missing Bootstrap styles at live deployment by removing the Bootstrap directory from the `.gitignore` file and committing the changes. Live deployment should now contain Bootstrap styles alongside styles from your custom CSS stylesheet if you have one.

### Bootstrap and Column Classes

To prevent columns from breaking/wrapping in unexpected fashion use class .col{breakpoint}_ to create a simple grid system that starts off vertically stacked then goes horizontally unstacked at the specified breakpoint.
**NOTE: Remember the number of columns on a row should total 12!** For example, since this is a 3-column preview card the columns will unstack horizontally and each card column will have a class "col-md-4". The total number of columns in a view port is 12 therfore: 3 sections with each section taking up 4 of the available 12 columns.
Think: 3 sections _ 4 columns = 12 total columns.

#Google Fonts

Google Fonts are a very cool way to add custom fonts to a project! When the `font-family` is selected on the site Google lists a set of instructions for using the selected fonts that involve adding some addiitonal <link> tags to the <head> section of the HTML document

We need the api link and gstatic link ONCE to allow access to the entire google fonts library. (In other words, if you are using more than one `font-family` in a project, include the "https://fonts.googleapis.com" and "https://fonts.gstatic.com" links only once. )

    ### fonts.googleapis.com link (include only once)
    <link rel="preconnect" href="https://fonts.googleapis.com">

    ### fonts.gstatic.com link
    (include only once)
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    ### link containing the font-family
    (include as needed to get selected font families)
    <link href="https://fonts.googleapis.com/css2?family=Lexend+Deca:wght@100&display=swap" rel="stylesheet">

Links to other font families can be added w/o having to add the above mentioned links again.
