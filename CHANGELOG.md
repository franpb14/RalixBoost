# Changelog

## [1.0.0] - 2024-01-16

### Added:
- Readme completed
- Snippets added:

| name       | Prefixes                                  | Body                                         | Description                                                               |
|---------------|-----------------------------------------|----------------------------------------------|---------------------------------------------------------------------------|
| find          | `querySelector`, `find`                | `find(${1:selector})`                        | Finds one element                                                        |
| findAll       | `querySelectorAll`, `findAll`          | `findAll(${1:selector})`                     | Finds multiple elements                                                  |
| findParent     | `closest`, `findParent`                 | `findParent(${1:selector}, ${2:queryParent})`| Finds the first parent element matching queryParent.                    |
| findParents    | `closest`, `findParent`                 | `findParent(${1:selector}, ${2:queryParent})`| Finds multiple elements matching queryParent among parents.              |
| addClass      | `classList`, `addClass`                 | `addClass(${1:query}, ${2:classList})`       | Adds specified classes using classList.                                   |
| removeClass   | `classList`, `removeClass`              | `removeClass(${1:query}, ${2:classList})`    | Removes specified classes using classList.                                |
| toggleClass   | `classList`, `toggleClass`              | `toggleClass(${1:query}, ${2:classList}, ${4:optionalClassValue})` | Toggles specified classes using classList.               |
| hasClass      | `classList`, `hasClass`                 | `hasClass(${1:query}, '${2:className}')`    | Checks if the element has a specified class.                             |
| attr          | `getAttribute`, `setAttribute`, `attr` | `attr(${1:query}, '${2:attribute}', ${3:optionalValue})` | Gets/sets the element attribute.                                |
| removeAttr    | `removeAttribute`, `removeAttr`         | `removeAttr(${1:query}, '${2:attribute}')` | Removes specified element attribute(s).                                  |
| data          | `dataset`, `data`                       | `data(${1:query}, '${2:attribute}', ${3:optionalValue})` | Similar to attr(), but for dataset.                         |
| removeData    | `dataset`, `removeData`                 | `removeData(${1:query}, '${2:attribute}')` | Similar to removeAttr(), but for dataset. If no attribute or attributes are passed, all dataset attributes will be deleted. |
| insertHTML    | `innerHTML`, `appendChild`, `insertHTML` | `insertHTML(${1:query}, ${2:html}, '${3\|inner,prepend,append,begin,end\|}')` | Inserts passed HTML to the query element, based on position.              |
| elem          | `createElement`, `elem`                 | `elem(${1:type}, ${2:attributes})`           | Creates and returns an HTML element and assigns given attributes.       |
| render        | `render`                                | `render('${1:template}', ${2:data})`        | Renders the template, passing the given data.                             |
| serialize     | `URLSearchParams`, `serialize`          | `serialize(${1:query})`                      | Serializes the given form. It could also be used for hash elements.      |
| submit        | `fire`, `requestSubmit`, `submit`        | `submit(${1:query})`                         | If rails_ujs is provided in new RalixApp(), submits the form via Rails.fire, otherwise uses requestSubmit (if available) or submit. |
| reload        | `reload`                                | `reload()`                                  | Reloads the current page.                                                |
| visit         | `location`, `visit`                     | `visit(${1:url})`                           | Navigates to the given URL, uses Turbo.visit (or Turbolinks.visit) if possible. |
| back          | `referrer`, `back`                       | `back(${1:fallbackUrl})`                    | Returns the user to the previous page (via history.back()). If there is no previous page or the referrer has a different hostname than the current one, it will navigate to the fallback URL visit(fallbackUrl). |
| currentUrl    | `location`, `currentUrl`                | `currentUrl()`                             | Returns the current location.                                             |
| getParam      | `searchParams`, `getParam`              | `getParam(${1:optionalParam})`              | Gets the param value from the current location. If you don't pass any argument, it will return all current parameters in JSON format. |
| on            | `addEventListener`, `on`                | `on(${1:query}, '${2:events}', (${3:event}) => { ${4:callback} })` | Wraps addEventListener. on performs preventDefault() on click events for interactive elements (links, buttons, and inputs). |
| ajax          | `fetch`, `ajax`                         | `ajax(${1:path}, { params: ${2:params}, options: ${3:options} })` | Wraps fetch. Adds the object params to path or options.body depending on options.method. |
| get           | `fetch`, `get`                          | `get(${1:path}, { params: ${2:params}, options: ${3:options} })` | Alias for ajax method with options.method as GET.                         |
| post          | `fetch`, `get`                          | `get(${1:path}, { params: ${2:params}, options: ${3:options} })` | Alias for ajax method with options.method as POST.                        |
