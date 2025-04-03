# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


HTML Part

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav class="navbar">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="grid-layout">
            <div class="sidebar">Sidebar content</div>
            <div class="content">
                <h1>Main Content</h1>
                <p>This is the main content section. Here you can add articles, text, or images.</p>
            </div>
            <div class="extra">Additional Content</div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 My Website</p>
    </footer>
</body>
</html>

CSS Part
/* Basic Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Body Styling */
body {
    font-family: Arial, sans-serif;
}

/* Navigation Bar */
.navbar {
    background-color: #333;
    padding: 1rem;
}

.navbar ul {
    display: flex;
    justify-content: space-around;
    list-style-type: none;
}

.navbar ul li {
    padding: 0.5rem;
}

.navbar ul li a {
    color: white;
    text-decoration: none;
    font-size: 1rem;
}

/* Main Layout */
main {
    padding: 2rem;
}

.grid-layout {
    display: grid;
    grid-template-columns: 1fr 3fr 1fr;
    gap: 20px;
}

.sidebar, .extra {
    background-color: #f4f4f4;
    padding: 1rem;
    border: 1px solid #ddd;
}

.content {
    background-color: #fff;
    padding: 1rem;
    border: 1px solid #ddd;
}

/* Footer */
footer {
    background-color: #333;
    color: white;
    padding: 1rem;
    text-align: center;
}

/* Media Queries for Responsiveness */

/* Mobile: Stacking Layout */
@media (max-width: 600px) {
    .navbar ul {
        flex-direction: column;
        text-align: center;
    }

    .grid-layout {
        grid-template-columns: 1fr;
    }

    .sidebar, .extra {
        display: none;
    }
}

/* Tablet: Adjust Layout */
@media (max-width: 768px) {
    .grid-layout {
        grid-template-columns: 1fr 2fr;
    }

    .sidebar {
        display: block;
    }

    .extra {
        display: none;
    }
}

/* Desktop: Default Grid Layout */
@media (min-width: 1024px) {
    .grid-layout {
        grid-template-columns: 1fr 3fr 1fr;
    }
}

