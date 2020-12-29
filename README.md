# js-doc-best-practices
Best Practices for JavaScript (ES5,ES6), JSdoc.app annotation standards, and general/personal best practices.

---
JavaScript ES5 & ES6+ commenting best practices & personal preferences
---

When possible follow JSdoc standards set here: https://jsdoc.app/about-getting-started.html#getting-started

---

Common tags to be used code:
---

@todo - optional, as applicable

@summary - required

@description - optional

@public or @private - required

@param {*} paramName - required if applicable

@returns - required for function documentation blocks

@yeilds - optional

@exports - optional

@example - required for function documentation blocks

Annotating Variables  
---

@summary - optional

@var or @constant or @lexical? - required as applicable

@example - optional

---

var

    /**
     * @summary Define an HTML element to use when toggleing CSS class '.classname'
     * @var {Object} variablename - jQuery object targeting .classname div elements
     * @example
     * variablename = $('.classname')
     */

const

    /**
     * @constant {Object} breadcrumbTwo - jQuery object targeting HTML element .breadcrumbs .two
     */

let

    /**
     * @todo define standard for let
     */
     
Annotating with single quotes, back ticks (aka back quotes) & double quotes
---

When describing DOM elements, CSS classes or Id's in comment strings use single quotes

    /**
     * Site Logo Image Adjustments Component
     * @description Removes _small on 'css-class' DOM element
     * @requires {*} Runs on all CMS pages with the CSS body class of 'specialPage'
     * @see [_site_logo_image_adjustments.scss]
     */
     
When declaring strings in JavaScript use back ticks whenever possible, this follows ES6 improvements and sets a standard to allow for separate purposes for single and double quotes.

    /**
     * Check for CSS class '.specialPage', applied to page element
     */
    if ( $(`.specialPage`).exists() ) {
    
    ...
    
    }
    
When defining HTML attributes on DOM element strings use double quotes.
    
    /**
     * Create element '.a-link'
     */
    let markup += `<a class="a-link" href="${href}"></a>"`

Annotating Functions
---

General Function annotation

    /**
      * @summary Builds initial exoskeleton of the search form 
      * @function
      * @private
      *
      * @returns undefined
      *
      * @example
      * buildExoskeleton();
      * > Manipulates DOM, injects new elements
      */

Function Definitions

    /**
     * @todo define standard for function definitions
     */

Function Expressions
    
    /**
     * @todo define standard for function expressions
     */

Comments in ES6 Template Strings
---

Give the comment a short one line summary, cover purpose, description & related code as applicable & reasonable

    ${/** …Comment… */''}

Commenting out code in JavaScript ES6 Template Strings

    ${/* <p class='breadcrumb'></p> */''}

All together now, example:

    `<div class='breadcrumbs'>
      ${/** Comment out breadcrumb one temporarily */''}
      ${/* <p class='breadcrumb one'></p> */''}
      <p class='breadcrumb two'></p>
      <p class='breadcrumb three'></p>
      <p class='breadcrumb four'></p>
    </div>`
