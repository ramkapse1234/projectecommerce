In this project, let's build a Nxt Trendz - Specific Product Details app by applying the concepts we have learned till now.

Refer to the image below:

product details output

Design Files
Click to view
Extra Small (Size < 576px) and Small (Size >= 576px) - Success
Extra Small (Size < 576px) and Small (Size >= 576px) - Failure
Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Success
Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Failure
Set Up Instructions
Click to view
Download dependencies by running npm install
Start up the app using npm start
Completion Instructions
Functionality to be added

The app must have the following functionalities

When an unauthenticated user, tries to access the Product Item Details Route, then the page should be navigated to Login Route
When an authenticated user clicks on a product in the Products Route, then the page should be navigated to Product Item Details route
When an authenticated user opens the Product Item Details Route,
An HTTP GET request should be made to productDetailsApiUrl with jwt_token in the Cookies and product id as path parameter
loader should be displayed while fetching the data
After the data is fetched successfully, display the product details and similar products received in the response
Initially, the quantity of the product should be 1
The quantity of the product should be incremented by one when the plus icon is clicked
The quantity of the product should be decremented by one when the minus icon is clicked
If the HTTP GET request made is unsuccessful, then the Failure view should be displayed
When the Continue Shopping button in the Failure view is clicked, then the page should be navigated to Products Route
API Requests & Responses

productDetailsApiUrl

API: https://apis.ccbp.in/products/:id
Example: http://localhost:3000/products/16
Method: GET
Description:
Returns a response containing the Product details

Sample Success Response
{
  "id":16,
  "image_url":"https://assets.ccbp.in/frontend/react-js/ecommerce/cloths-long-fork.png",
  "title":"Embroidered Net Gown","price":62990,"description":"An Embroidered Net Gown is the clothing worn by a bride during a wedding ceremony. It enhances your beauty wearing this vibrant, gorgeous, and beautiful Wedding Gown. Find your dream wedding dress today. It features foldable, one hoop steel, two layers of tulles, and is elastic in the waist part. ",
  "brand":"Manyavar",
  "total_reviews":879,
  "rating":3,
  "availability":"In Stock",
  "similar_products":[
    {
      "id":1,
      "image_url":"https://assets.ccbp.in/frontend/react-js/ecommerce/clothes-cap.png",
      "title":"Wide Bowknot Hat",
      "style":"Wide Bowknot Hat for Women and Girls (Multicolor)",
      "price":288,
      "description":"This Summer's perfect White Wide Brim Straw Beach hat is perfect for a hot day. It has the Floppy Style which gives you good coverage from the sun's hot rays and is sure to make the right style statement. It is made of high-quality & skin-friendly paper straw material and lightweight. ",
      "brand":"MAJIK",
      "total_reviews":245,
      "rating":3.6,
      "availability":"In Stock"
    },
      ...
  ]
}
Sample Failure Response
{
  "status_code": 404,
  "error_msg": "Product Not Found"
}
Components Structure

component breakdown structure

Implementation Files

Use these files to complete the implementation:

src/components/ProductCard/index.js
src/components/ProductCard/index.css
src/components/ProductItemDetails/index.js
src/components/ProductItemDetails/index.css
src/components/SimilarProductItem/index.js
src/components/SimilarProductItem/index.css
Quick Tips
Click to view

The line-height CSS property sets the height of a line box. It's commonly used to set the distance between lines of text.

line-height: 1.5;

cursor pointer
Important Note
Click to view

The following instructions are required for the tests to pass

Home Route should consist of / in the URL path

Login Route should consist of /login in the URL path

Products Route should consist of /products in the URL path

Product Item Details Route should consist of /products/:id in the URL path

Cart Route should consist of /cart in the URL path

No need to use the BrowserRouter in App.js as we have already included in index.js

Prime User credentials

 username: rahul
 password: rahul@2021
Non-Prime User credentials

 username: raja
 password: raja@2021
Wrap the Loader component with an HTML container element and add the data-testid attribute value as loader to it

<div data-testid="loader">
  <Loader type="ThreeDots" color="#0b69ff" height={80} width={80} />
</div>
The product image in Product Item Details Route should have the alt as product

The similar product image in Product Item Details Route should have the alt as similar product {product title}

similar product Wide Bowknot Hat
BsPlusSquare, BsDashSquare icons from react-icons should be used for plus and minus buttons in ProductItemDetails Route

The Product Item Details Route should consist of two HTML button elements with data-testid attribute values as plus and minus respectively

Resources
Image URLs
https://assets.ccbp.in/frontend/react-js/star-img.png alt should be star
https://assets.ccbp.in/frontend/react-js/nxt-trendz-error-view-img.png alt should be error view
Colors

Hex: #12022f
Hex: #616e7c
Hex: #171f46
Hex: #cbced2
Hex: #ffffff
Hex: #3b82f6
Hex: #1e293b
Hex: #475569
Font-families
Roboto
