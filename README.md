## **1. Getting Started with jQuery**
To use jQuery, include the jQuery library in your HTML file.

### **CDN (Recommended)**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>jQuery Example</title>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>
    <h1>Hello, jQuery!</h1>
    <button id="btn">Click Me</button>

    <script>
        $(document).ready(function() {
            $("#btn").click(function() {
                alert("Button Clicked!");
            });
        });
    </script>
</body>
</html>
```

## **2. jQuery Selectors**
| Selector | Description | Example |
|----------|------------|---------|
| `$("p")` | Selects all `<p>` elements | `$("p").hide();` |
| `$("#id")` | Selects element by `id` | `$("#btn").hide();` |
| `$(".class")` | Selects elements by `class` | `$(".box").hide();` |
| `$("*")` | Selects all elements | `$("*").hide();` |
| `$("[name='username']")` | Selects elements by attribute | `$("input[name='username']").val("John");` |

## **3. jQuery Events**
| Event | Description |
|-------|------------|
| `click()` | Fires when an element is clicked |
| `dblclick()` | Fires on double-click |
| `hover()` | Triggers on mouse over/out |
| `keydown()` | Fires when a key is pressed |
| `keyup()` | Fires when a key is released |
| `change()` | Fires when input value changes |

### **Example:**
```js
$("#btn").click(function() {
    $(this).text("Clicked!");
});
```

## **4. jQuery Effects**
| Method | Description |
|--------|------------|
| `hide(speed)` | Hides an element |
| `show(speed)` | Shows an element |
| `toggle(speed)` | Toggles visibility |
| `fadeIn(speed)` | Fades in an element |
| `fadeOut(speed)` | Fades out an element |
| `slideDown(speed)` | Slides down an element |
| `slideUp(speed)` | Slides up an element |

### **Example:**
```js
$("#btn").click(function() {
    $("h1").fadeOut(1000);
});
```

## **5. jQuery DOM Manipulation**
### **Change Content:**
```js
$("#btn").click(function() {
    $("h1").text("New Heading");
});
```

### **Change HTML:**
```js
$("#btn").click(function() {
    $("h1").html("<i>Italic Text</i>");
});
```

### **Change Attribute:**
```js
$("img").attr("src", "new-image.jpg");
```

## **6. jQuery AJAX**
jQuery simplifies AJAX requests for fetching data without reloading the page.

### **Example: Fetch Data from API**
```js
$.get("https://jsonplaceholder.typicode.com/todos/1", function(data) {
    console.log(data);
});
```

## **7. jQuery Traversing**
| Method | Description |
|--------|------------|
| `parent()` | Selects the parent element |
| `children()` | Selects all direct children |
| `next()` | Selects the next sibling |
| `prev()` | Selects the previous sibling |

### **Example:**
```js
$("p").parent().css("border", "1px solid red");
```

## **8. jQuery Form Handling**
### **Example:**
```js
$("#submit").click(function() {
    var name = $("#name").val();
    alert("Hello, " + name);
});
