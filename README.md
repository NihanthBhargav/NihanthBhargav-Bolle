# Shopify EcomExperts Test Submission Theme

## Project Overview

This repository contains the custom theme development for the EcomExperts test, focusing on enhancing the product discovery and purchase flow within a Shopify storefront. The core of this project involves a dynamic image grid section integrated with a quick-view product modal, designed to offer a streamlined user experience.

The primary goal was to implement direct "Add to Cart" functionality from the quick-view modal while maintaining a clean, responsive, and aesthetically pleasing interface.

## Key Features Implemented

- **Responsive Image Grid Section:** Displays a collection of product images in a visually engaging, responsive grid layout that adapts to various screen sizes (desktop, tablet, mobile).
- **Product Quick View Modal:**
  - Opens a modal popup when an overlay icon on a grid image is clicked.
  - Displays the main product image (prioritizing the clicked grid image), product price, and description.
  - Includes custom variant selectors for "Color" and "Size" with interactive UI elements (sliding background for colors, dropdown for sizes).
- **Direct "Add to Cart" Functionality:**
  - The "ADD TO CART" button within the quick-view modal is always enabled.
  - Clicking it attempts to add the currently selected product variant directly to the Shopify cart via AJAX.
  - Provides immediate, in-modal success or error feedback using a custom message box (no disruptive browser alerts).
- **Consistent Button Text:** The "ADD TO CART" button always displays "ADD TO CART →", providing a consistent call to action without showing "Sold Out" text. (Note: Shopify's backend still manages actual stock; an error message will display if an unavailable item is attempted to be added).
- **Enhanced User Experience:** Implemented custom, non-blocking message boxes for user feedback, ensuring a smoother interaction compared to native browser alerts.

## Technologies and Tools Used

- **Shopify Liquid** — Templating language used for building the theme structure and dynamically accessing store data.  
- **HTML5** — For structuring the web content.  
- **CSS3** — For styling and ensuring responsiveness across devices.  
- **JavaScript (ES6+)** — For interactive elements, AJAX calls to the Shopify Storefront API (`/cart/add.js`, `/products/*.js`), and dynamic content updates.  
- **Git & GitHub** — For version control and hosting.  
- **Shopify CLI / GitHub Integration** — For local theme development and deployment to the Shopify store.  

## Setup and Deployment

1. **Clone the Repository**
   ```bash
   git clone https://github.com/NihanthBhargav/NihanthBhargav-Bolle.git
   cd NihanthBhargav-Bolle
2. **Local Theme Development**

shopify login --store your-store-name.myshopify.com
shopify theme dev


Runs the theme locally for development (not for production deployment).

3. **Deploy to Shopify Store**

Connect the main branch of this repo to your Shopify store:
Admin → Online Store → Themes → Add theme → Connect from GitHub

Or push manually:

shopify theme push --theme-id <your-theme-id>(id: 179530137967)
