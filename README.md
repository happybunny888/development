# Development

### Link to Deployed Website
Link to deployed website is https://happybunny888.github.io/development/. 

### Goal and Value of the Application
The app is for purchasing tickets to see movies at a drive in theater (since this is mandated to be single page, removed/did not consider time or scheduling for this app). Users can see what films are offered, their descriptions, prices, ratings, see the poster. Users can sort by ticket price for the film or by the ratings. Users can also filter by Movie Type/Genre: (currently for this demo only three categories) Anime, Action, or Romance. 

### Usability Principles Considered
Status of system is clearly present: sort and filters cause the movies to show up in different order or their presence is immediate after selecting sort/filters. Increasing or decreasing amount of tickets per movie will be indicated in the aggregator: film x number is made immediately clear with the price.

All elements, options, and options are visible in the app. No short forms are used, headings/labels are present, the reset and clear cart buttons are clear and in their respective areas. 

### Organization of Components

TicketItem Component: which is responsible for displaying each of the movie/ticket items (title of move, description of movie, price per ticket for the movie, Rotten Tomato rating, and the poster). It also contains buttons for adding (+) and subtracting (-) tickets to the cart for each movie.

Aggregator Component: which is responsible for accessing the state of the cart, displaying the shopping cart (items, quantity of tickets for each, price, and total price) and having a button to clear the shopping cart.

Filter Component: which is responsible for having the code for the function HandleChanged (which selects the option of filtering fromthe filter options, and changing the checked states of the filter). The code for displaying or the styling of the checkbox items for filtering type of movie is present. 

Sort Component: which is responsible for having the code for the function HandleChanged (which selects the sorting type from the sort options, and changing the checked states of the sort). The code for displaying or the styling of the selection items for sorting movie is present. 

### How Data is Passed Down Through Components

In App.js: There is a map through all the sortedData of movies which produce a TicketItem Component for each movie, in the order of sorting type. For each movie Item mapped through, the item, and the addToCart and removeFromCart functions are passed through the components. There are two calls to state in App.js, one to retrieve the filter types and one to retrieve the sort. The functions selectFilterType and selectSort, and resetFilter and resetSort, matchesFilterType and matchesSortType are defined in App.js to help generate the sortedData and filterData for the mapping of movies on the tiles. In the side bar area of the app in App.js, the components for Filter and Sort are present.

### How the User Triggers State Changes
The user triggers state changes when:the user increases or decreases the tickets to the cart (or clear cart button), the changes in filtering, the changes in sorting types, the reset filters+sorting button. There are two calls to state in App.js, one to retrieve the filter types and one to retrieve the sort. There is a call to state in Aggregator.js for retrieving the cart state, which will change depending on what the user adds and removes from the cart.
