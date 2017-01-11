# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    Image list might have an /images/imageId/picture path on which each picture has an edit button and delete each button could be a componant.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
ember g component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
the component.js is repsonsible for handling actions to bubble up the template renders them. Each piece the action passes on its way to the route is edited in a similar fasction and the routes are edited to hangle the request/whatever the action is doing.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
        {{contacts}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
{{#each model as |contact|}}
{{contacts/my-contact contact="contact"}}
{{/each}}   
```
