# Redux Filter Etsy Results

Modeling state and filtering data with a reducer

## Model the State  

Within ./src/reducers/reducer.js perform the following tasks:

- Define the initialState object.
  - Make sure the initialState object contains the products array imported in this file.
  - initialState will also require a property for the current state of filterable data.

- Finish writing the reducer for the FILTER_PRODUCTS action.
  - Provide the reducer function declaration with the necessary parameters.
  - Give the state parameter a default value of initialState.
  - When a FILTER_PRODUCTS is provided, return a new state
  - Be sure not to mutate state
  - Use the update operator provided by immutability-helper to update the the state property describing current state of filterable data provided by the action.payload

## Where State Contents are Rendered

Review ./src/components/Product.js and take note of the product property being used to populate the contents.

## Populate a List and Filter the Array

Within ./src/containers/ProductList.js perform the following tasks:

- Create a dynamically populated list of <Product /> components.
  - Each <Product /> component should have a single object from the products state property (array) applied to the component as a product property.

- Using the mapStateToProps function, filter the array stored in the state products property based on 3 criteria:
  - underTwenty
  - overTwenty
  - all or the default

- Complete the if else statement including conditions and products value.

## Call the Action

Within ./src/containers/FilterProducts.js perform the following tasks:

- Within the the createFilterRadio function, return a <button> template which will accept a value and text from arguments passed to createFilterRadio.
  - The button should call filterProducts when clicked, passing in the value from createFilterRadio as it's argument.
  - Use the text argument as the content for the button element.
  - If the current this.props.filter value matches the value passed as an argument to createFilterRadio, apply a class of 'active', otherwise provide a default class of 'inactive'.
  - Don't forget to provide the <button> with a key attribute.

- Review the filterProducts function.
  - Take note of the parameter accepting a filter value from the <button> elements above and passing said value to the reducer function we named filterProducts when we imported it into this file.

## Results  

Once complete, you should see the following functionality in your application:

- All belt product listings are visible when the app loads
- Clicking either "Show under $20" or "Show over $20" will filter the product listings by only those listings whose price is under or over $20.

![](mockup.gif)
