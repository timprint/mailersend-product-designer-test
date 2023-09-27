# mailersend-product-designer-test

Built using HTML and CSS only.

No frameworks or pre-processors.

## HTML

Semanticly structured HTML making use of header, main, footer.

## SVG Icons

SVG icons are inline at the start of the body and used via the use tag.

`<svg><use xlink:href="#icon-cart"></use></svg>`.

This technique makes them very easy to style via CSS.

## Accessibility

Skip to main content link is included.

SVG icons are never used as links without supporting text for screen readers.

Where appropriate, text is included in the document which is only available for screen readers and is hidden by CSS for sighted users. For example the **'Star Rating'** for each book is included as text but shown visually via icons.

Focus styles are included for all clickable items

Tabbing order is logical and follows the flow of the document.

Book items include the title and description first and the add to basket last in the document order. This makes more sense for screen reader users. The layout uses `flex-direction: row-reverse;` to switch this visually.

`button` and `a` tags are used appropriately for actions and links.

Alt text is included for content images.

## Layout

Responsive, mobile first design.

Minimum media queries used (only for the main grid layout and one layout change in the footer). I find extensive use of media queries in a layout makes it much more time consuming to maintain and update.

1,2,3,4 and 6 column grid for the page title and ten books means we are never left with any orphaned books on the last line. The grid is always full.

Flexbox is used on the book items to get a good balance between the image and the text.

I have used flexible spacing in some places. For instance the page margins on the header, main and footer.
`clamp(1rem, 0.082rem + 3.918vw, 4rem)`
This gives us a minimum of 16px at 375px viewport width or below and a maximum of 64px at 1600px viewport width or above. The spacing will scale automatically between those two values.

## Typography

Type sizes set up as CSS variables in a similar way to Tailwind

I have also used the `clamp` technique to give us flexible font sizes where appropriate (page title, header links).

## Colours

All colors are set up as CSS variables.

Grey 'zinc' colors borrowed from Tailwind.

## Animation

I have only used some very light animation on page load. Anything more didn't feel appropriate for this page.