### Bootstrap Grid System: Rows and Columns

Bootstrap's grid system is a powerful tool for building responsive, mobile-first layouts using a combination of **rows** and **columns**. Here’s a concise guide to understanding how it works:

#### 1. **Container**
Everything in Bootstrap's grid system is wrapped inside a container element. Bootstrap provides two types of containers:
   - **`.container`**: Fixed-width container (responsive based on screen size).
   - **`.container-fluid`**: Full-width container that spans the entire width of the viewport.

```html
<div class="container">
  <!-- Grid content goes here -->
</div>
```

#### 2. **Rows**
Rows are the horizontal groupings of columns. They must be placed inside a container and serve as wrappers for columns.
- **Usage**: Always wrap columns inside a row.
- **Gutters**: Rows have negative margins that add space (gutters) between columns.

```html
<div class="row">
  <!-- Columns go here -->
</div>
```

#### 3. **Columns**
Bootstrap's grid system is based on 12 columns, and you can use this system to create layouts by specifying how many of the 12 columns each block (element) will span.

Each row can contain columns of different sizes by using classes like `col-`, `col-sm-`, `col-md-`, `col-lg-`, and `col-xl-` for different breakpoints.

##### Column Syntax:
```html
<div class="col-md-6"> <!-- 50% width on medium (≥768px) screens --> 
  Content
</div>
<div class="col-md-6"> <!-- 50% width on medium (≥768px) screens -->
  Content
</div>
```

#### 4. **Breakpoints**
Breakpoints allow columns to change their width depending on the screen size. You can use specific classes to target different devices:
- **Extra small** (`col-` or `col-xs-` for screens <576px)
- **Small** (`col-sm-` for screens ≥576px)
- **Medium** (`col-md-` for screens ≥768px)
- **Large** (`col-lg-` for screens ≥992px)
- **Extra large** (`col-xl-` for screens ≥1200px)

#### 5. **Equal-Width Columns**
Without specifying a number, columns will divide the available space equally.
```html
<div class="col">Column 1</div>
<div class="col">Column 2</div>
<div class="col">Column 3</div>
```

#### 6. **Offsetting Columns**
You can offset columns to create space on one side using the `offset` classes:
```html
<div class="col-md-4 offset-md-4"> <!-- Centered column on medium screens -->
  Centered content
</div>
```

#### 7. **Nesting Columns**
You can nest columns inside other columns to create more complex layouts.
```html
<div class="row">
  <div class="col-md-8">
    <div class="row">
      <div class="col-md-6">Nested Column</div>
      <div class="col-md-6">Nested Column</div>
    </div>
  </div>
</div>
```

### Example Layout:
```html
<div class="container">
  <div class="row">
    <div class="col-sm-4">Column 1</div>
    <div class="col-sm-4">Column 2</div>
    <div class="col-sm-4">Column 3</div>
  </div>
</div>
```

This layout has three equal-width columns that take up one-third of the available space each on small (≥576px) and larger devices.

### Key Concepts Recap:
- **Rows** are wrappers for **columns**.
- A row contains **12 columns** by default.
- Columns can be of equal width or span specific numbers of columns.
- You can use different breakpoints for responsive design.
- You can **nest columns** for more complex layouts.

The Bootstrap grid is designed to make layouts flexible and responsive, allowing content to adapt across different screen sizes efficiently.