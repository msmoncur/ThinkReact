# React + Vite

How is state and props are working in the application?

State and Props work in tandem to manage and pass data between the components

For example in this app state is used to keep track of the filterText and if the user wants to see only in-stock products. These values are stored in the FilterableProductTable component using the useState hook. When the user types in the search box or checks the "Only show products in stock" option, the state updates using the setFilterText and setInStockOnly functions. State updates cause the component to re-render, the product list automatically changes based on the user’s input. Keeping state in FilterableProductTable ensures that the filtering logic is consistent and controlled from one place.

On the other hand props are being used to send data and functions from FilterableProductTable to its child components. The SearchBar component receives filterText and inStockOnly as props so it can display the filter settings. It gets two functions, onFilterTextChange and onInStockOnlyChange, which allow it to send user input back to the parent component to update the state. The ProductTable component gets the product list, filter text, and stock filter as props, so it can decide which products to show. Aftr that it passes the relevant product details to ProductCategoryRow and ProductRow, which display the data.