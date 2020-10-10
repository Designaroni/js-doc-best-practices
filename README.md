# jsdoc-best-practices
Best practices for JSdoc.app annotation standards

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
     * @constant {Object} locationCrumb - jQuery object targeting HTML element .locationCrumb, HTML element is created by 
     */

let

    /**
     * @todo define standard for let
     */

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
