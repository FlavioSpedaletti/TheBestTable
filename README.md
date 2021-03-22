# TheBestTable

## Código fonte do artigo: https://khalidabuhakmeh.com/remove-rows-from-razor-html-tables

![The best table](https://res.cloudinary.com/abuhakmeh/image/fetch/c_limit,f_auto,q_auto,w_1200/https://khalidabuhakmeh.com/assets/images/posts/html-table-razor/html-razor-table.png)

> My previous understanding was that each row would require its own unique form tag, along with the necessary attributes and values needed to satisfy the endpoint handler.
> Imagining a page with *100 rows, we can start to understand the overhead the requirement could add to our pages. 

```html
<form id="remove" method="post" asp-page-handler="Remove">
  <button type="submit" name="id" value="@person.id">Remove</button>
</form>
```

> HTML button tags can submit any form found on the page using the form attribute.

```html
...

<!-- The form that remove buttons will use -->
<form id="remove" method="post"></form>

...

<button
  type="submit"
  name="id"
  value="@person.Id"
  form="remove"
  asp-page-handler="Remove"
  class="btn btn-danger btn-rounded btn-sm my-0"
>
  Remove
</button>
```
