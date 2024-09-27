
# Tailwind CSS Project

This project is a simple implementation of [Tailwind CSS](https://tailwindcss.com/), a utility-first CSS framework for rapidly building custom designs.

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Development](#development)

## Introduction

Tailwind CSS provides low-level utility classes that let you build completely custom designs without leaving your HTML. This project aims to demonstrate how to integrate and use Tailwind CSS in a web development environment.


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


4. Include the compiled CSS file in your HTML:

   ```html
   <link href="/dist/output.css" rel="stylesheet">
   ```
