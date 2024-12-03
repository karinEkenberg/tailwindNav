```markdown
# Tailwind CSS Navigation with Mobile Toggle

This project demonstrates a responsive navigation menu built with **Tailwind CSS** and **Ionicons**.
The navigation includes a mobile menu toggle functionality that uses simple JavaScript to show and hide the menu on smaller screens.

# Images

![nav-desktop](https://github.com/user-attachments/assets/f61a7bbb-c180-4a8a-8d63-be00064fca54)

![nav-mobile](https://github.com/user-attachments/assets/a9c9d977-a5ab-446c-855d-c9efc0ac3c55)

## Features

- **Responsive Navigation**: The menu adjusts its layout based on screen size.
- **Mobile Toggle**: A hamburger-style toggle button that appears on mobile devices.
- **Smooth Transitions**: The menu slides in and out with a smooth transition effect.
- **Custom Fonts**: The project uses Poppins and Titillium Web fonts from Google Fonts.

## Installation

To use this project, follow the steps below:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/repositoryname.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd repositoryname
   ```

3. **Open the HTML file in your browser**.

## HTML Overview

- **Navigation Bar**: Contains a logo on the left and navigation links on the right.
- **Mobile Toggle**: A hamburger-style icon (`ion-icon`) which toggles the visibility of the menu on small screens.
- **Menu Visibility**: The menu slides in from the top when the toggle is clicked and slides out when clicked again.

## CSS and Styling

The project uses **Tailwind CSS** for styling. The navigation bar is styled with a gradient background and spacing utilities for responsive layouts.

### Key Classes:
- **`bg-[#AB4459]`**: Background color of the navigation bar.
- **`absolute`** and **`top-[-100%]`**: Initially hides the mobile menu off-screen. When toggled, it moves to the top of the screen (`top-[0%]`).
- **`md:hidden`**: Hides the hamburger icon on medium and larger screens.

## JavaScript Functionality

A simple JavaScript function controls the toggling of the mobile menu.

```js
const navLinks = document.querySelector(".nav-links");

function onToggleMenu(e) {
  e.name = e.name === "menu" ? "close" : "menu";

  if (navLinks.classList.contains("top-[-100%]")) {
    navLinks.classList.remove("top-[-100%]");
    navLinks.classList.add("top-[0%]");
  } else {
    navLinks.classList.remove("top-[0%]");
    navLinks.classList.add("top-[-100%]");
  }
}
```

- The `onToggleMenu()` function changes the `name` of the hamburger icon (`menu` to `close`).
- It also toggles the `top` property of the navigation links, either showing or hiding them.

## Demo

You can see the project in action by opening the `index.html` file in your browser. On smaller screens, click the hamburger icon to toggle the visibility of the navigation menu.

## Contributing

If you wish to contribute, follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-name`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature-name`)
6. Open a pull request

