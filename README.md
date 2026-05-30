# Paradise Nursery Shopping Cart

This project is a React-based plant shopping application for Paradise Nursery. The product page displays different plant categories and allows users to view plant details, including the plant name, image, description, and cost.

## Product List Component

The `ProductList.jsx` component displays the available plants using a `plantsArray`. The array contains plant categories, and each category contains multiple plant objects.

Each plant object includes:

* `name`
* `image`
* `description`
* `cost`

The product page uses the JavaScript `map()` method to loop through the plant categories and display each plant card inside the `product-grid` section.

## Features Completed

* Displayed all plant categories on the product page.
* Rendered each plant inside a product card.
* Displayed each plant’s image, name, description, and cost.
* Added an **Add to Cart** button for every plant.
* Created local state using `useState` to track which plants were added to the cart.
* Added `handleAddToCart()` functionality.
* Dispatched selected plant data to the Redux cart using the `addItem` action from `CartSlice.jsx`.
* Updated the button text after a plant is added to the cart.
* Disabled the button after the item has been added.

## Add to Cart Functionality

When the user clicks the **Add to Cart** button, the selected plant object is passed into the `handleAddToCart()` function.

The function dispatches the selected plant to the Redux cart state and updates local component state to show that the item has been added.

```jsx
const handleAddToCart = (product) => {
    dispatch(addItem(product));

    setAddedToCart((prevState) => ({
        ...prevState,
        [product.name]: true,
    }));
};
```

## Technologies Used

* React
* JavaScript
* JSX
* CSS
* Redux Toolkit
* React Redux
* GitHub

## How to Run the Project

Install the project dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

## GitHub Update

The completed changes were saved and pushed to the GitHub repository.

```bash
git add .
git commit -m "Complete ProductList layout and add cart functionality"
git push origin main
```
