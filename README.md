
# Tailwind CSS Project

This project is a simple implementation of [Tailwind CSS](https://tailwindcss.com/), a utility-first CSS framework for rapidly building custom designs.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Development](#development)
- [Build for Production](#build-for-production)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Tailwind CSS provides low-level utility classes that let you build completely custom designs without leaving your HTML. This project aims to demonstrate how to integrate and use Tailwind CSS in a web development environment.

## Installation

To get started with Tailwind CSS, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/tailwindcss-project.git
   cd tailwindcss-project
   ```

2. Install the required dependencies:

   ```bash
   npm install
   ```

3. Install Tailwind CSS via npm:

   ```bash
   npm install -D tailwindcss
   ```

4. Create your `tailwind.config.js` file:

   ```bash
   npx tailwindcss init
   ```

## Usage

1. Add the paths to all of your template files in the `tailwind.config.js` file:

   ```js
   module.exports = {
     content: [
       './src/**/*.{html,js}',
       './public/index.html',
     ],
     theme: {
       extend: {},
     },
     plugins: [],
   };
   ```

2. Create a CSS file (e.g., `src/styles.css`) and add the following:

   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

3. Build your CSS:

   ```bash
   npx tailwindcss -i ./src/styles.css -o ./dist/output.css --watch
   ```

4. Include the compiled CSS file in your HTML:

   ```html
   <link href="/dist/output.css" rel="stylesheet">
   ```

## Development

To start developing with Tailwind CSS, run the following command:

```bash
npx tailwindcss -i ./src/styles.css -o ./dist/output.css --watch
```

This will watch your files for changes and automatically rebuild your CSS.

## Build for Production

For production builds, you can optimize the output by purging unused styles. Update the `package.json` scripts:

```json
"scripts": {
  "build": "npx tailwindcss -i ./src/styles.css -o ./dist/output.css --minify"
}
```

Then run:

```bash
npm run build
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
