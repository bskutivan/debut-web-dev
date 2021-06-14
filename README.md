# debut-web-dev-sklls-test

For this skills test there were 3 main sections to achieve.<br>

Link to Store: https://kicks-collaborative.myshopify.com/ <br>
store password: blueacornFE1

## Section 1 - Create a new Dynamic Shopify Section
### Requirements -
1. Create a brand new dynamic section for the homepage called Feature Products.
2. The section should be able to be moved up and down the page using the theme settings.
3. The user should be able to specify a collection in the theme settings and the first 4 products of the collection should display in a row.
4. The user should be able to specify a title for the section which appears above the product row.
5. For each product, display the following: Main Product Image, Product Title, Product Price.
6. Clicking on the Product Image or Product Title should link the user to the Product Page.
7. On desktop, display the items 4 across. On tablet and below, display them 2 x 2.
8. The inherited styles from the theme are fine for the text elements.

The requirements of this section were achieved using shopify liquid to build out a section with schema that allowed for a dynamic section header and the ability to move the section in the theme editor. Thanks to Shopify Liquid it was easy to use a for loop to go through each product in the section and create dynamic dom elements with that product's information.

## Section 2 - Add to Cart Button Styling

### Requirements -
1. Button should say "Add To Cart."
2. Button should match styling given in skills test doc.
3. Button should match hover styling givin in skills test doc.
4. BEM class naming conventions should be used
5. SCSS should be used over CSS

The requirements of this section were achieved utilizing browser developer tools and sass to ensure the button styling was as close to the given styling as possible. Pseudo elements were utilized to achieve folded corner look. Theme styling did not need to be overwritten for focus state but it looked really awful so I decided to make the hover state the focus state as well for continuity.
## Section 3 - Add to Cart Button Javascript

### Requirements -
1. Clicking "Add to Cart" button should add 1 of the product's selected or first available variants to cart.
2. Page should not reload.
3. The header cart does not need to update at this time.
4. The updated cart response received back from the API should log out to the browser console.

### Technical Approach -
1. Make a REST API call to POST to the Shopify cart/add.js endpoint on the front end.
2. Use liquid to get the product's variant ID which needs to be passed in the API call.
3. Set the quantity to add to 1 directly in the Javascript.

The requirements were achieved by following the technical approach as closely as possible. Thanks to Shopify Liquid I was able to isolate each product variants id and then passing this id into an onClick attribute in the button element itself. This was then passed into the POST API call in the item object as well as the quanitity of said item. Thanks to the JQuery documentation I was able to reframe the request so that it console logs the response object with the item added to the cart.
