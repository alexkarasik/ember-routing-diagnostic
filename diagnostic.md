# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    The Ember router maps the current URL to one or more route handlers. The route handlers can...
    render a template,
    load a model available to the template,
    redirect to a new route,
    handle actions involving change or transitions

    The main task of an Ember Route is to pass model data down to components, along with route actions.
    The main actions are URL transitions, data-related operations and other route related concerns.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
  ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
      {{#link-to '/campus/boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
  I believe the first one sets up products as the base route already and the path just goes straight to the product_id while the second one gives the full path name.

    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    <!-- your response here -->
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    export default Ember.Route.extend({
        setupController() {
            this.controllerFor('application').set('navigation', ["nav1", "nav2"]);
        }
    });
    ```
