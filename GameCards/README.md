## Game Cards

First Pass: 

```html
<!DOCTYPE html>
<html>
<head>
	<title>Game Cards</title>
	<style>
		.container {
			display: grid;
			grid-template-columns: repeat(2, 1fr);
			grid-template-rows: repeat(9, 1fr);
			grid-gap: 10px;
		}

		.card {
			border: 1px solid black;
			padding: 20px;
			text-align: center;
		}
		@media print {
			.card {
				page-break-inside: avoid;
			}
		}

		.container {
			display: grid;
			grid-template-columns: repeat(2, 1fr);
			grid-template-rows: repeat(9, 1fr);
			grid-gap: 10px;
		}

		.card {
			border: 1px solid black;
			padding: 20px;
			text-align: center;
		}		
	</style>
</head>
<body>
	<div class="container">
		<div class="card">Card 1</div>
		<div class="card">Card 2</div>
		<div class="card">Card 3</div>
		<div class="card">Card 4</div>
		<div class="card">Card 5</div>
		<div class="card">Card 6</div>
		<div class="card">Card 7</div>
		<div class="card">Card 8</div>
		<div class="card">Card 9</div>
		<div class="card">Card 10</div>
		<div class="card">Card 11</div>
		<div class="card">Card 12</div>
		<div class="card">Card 13</div>
		<div class="card">Card 14</div>
		<div class="card">Card 15</div>
		<div class="card">Card 16</div>
		<div class="card">Card 17</div>
		<div class="card">Card 18</div>
	</div>
</body>
</html>
```

---
> Please change the code above so that dashed lines are used and that there is no space between the cards..

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Game Cards</title>
    <style>
      @page {
        size: A4;
        margin: 0;
      }

      body {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(9, 1fr);
        gap: 0;
        padding: 20px;
        margin: 0;
      }

      .card {
        background-color: white;
        border: 1px dashed black;
        padding: 10px;
        font-size: 18px;
        text-align: center;
      }
    </style>
  </head>
  <body>
    <div class="card">Card 1</div>
    <div class="card">Card 2</div>
    <div class="card">Card 3</div>
    <div class="card">Card 4</div>
    <div class="card">Card 5</div>
    <div class="card">Card 6</div>
    <div class="card">Card 7</div>
    <div class="card">Card 8</div>
    <div class="card">Card 9</div>
    <div class="card">Card 10</div>
    <div class="card">Card 11</div>
    <div class="card">Card 12</div>
    <div class="card">Card 13</div>
    <div class="card">Card 14</div>
    <div class="card">Card 15</div>
    <div class="card">Card 16</div>
    <div class="card">Card 17</div>
    <div class="card">Card 18</div>
  </body>
</html>
```

---
>  What does '@page' mean? How does this compare with '@media print ' ? 

To answer your question, @page is a CSS at-rule that lets you define the styles for the page when it is printed. In this code, it is used to set the page size to A4 and remove the default margins.

On the other hand, @media print is another CSS at-rule that lets you define the styles that should be applied when the page is printed. It is similar to @page, but @media print can be used to define styles for specific parts of the page, such as headers, footers, or other elements that should only appear when the page is printed.

So, while both @page and @media print can be used to style pages for print, @media print gives you more control over the specific elements that should be styled for print, while @page is more focused on defining the overall page layout.







