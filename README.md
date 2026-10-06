# Personal Coaching Website

Source of [francoruiz.net](https://francoruiz.net), the website of my personal development coaching practice. A static single-page site hosted on GitHub Pages, with a multi-step application form.

## Overview

The page is built to do one thing: turn a qualified visitor into an application. It opens with a question the visitor can answer on the spot, and that answer becomes the first step of a three-step application form.

I defined the positioning, content, page structure and every design decision, and implemented the site through AI-assisted development with Claude, iterating on live previews until each section was approved.

## From WordPress to static

The site first ran as a custom WordPress theme on paid hosting, with a PHP backend that stored each application and sent an email notification. For a single page with low traffic, that was more infrastructure than the job needed.

I migrated it to plain HTML, CSS and JavaScript on GitHub Pages and replaced the PHP backend with a form service. The design and behavior are identical, there is no server or database to maintain, and the hosting cost went to zero. The switch was made with no downtime: the new version was published and tested on a temporary address before the domain was pointed to it.

## Features

- Hero with an inline question whose answer is carried into the application form
- Three-step application form with client-side validation and a progress indicator
- Applications delivered by email through Formspree, with a honeypot field against spam
- Fallback to a standard form submission if the background request fails, so no application is lost
- Responsive layout, keyboard focus styles and reduced-motion support
- No frameworks, build step or dependencies

## Tech Stack

- HTML and CSS with custom properties
- Vanilla JavaScript
- GitHub Pages with a custom domain
- Formspree for form handling

## Structure

```
index.html   Page markup and metadata
estilo.css   All styles
main.js      Multi-step form logic and submission
assets/      Images
```

## Live Site

[francoruiz.net](https://francoruiz.net)

## Preview

![Home](screenshots/home.png)

![About](screenshots/about.png)

![Who it is for](screenshots/audience.png)

![How I work](screenshots/process.png)

![Application form](screenshots/form.png)
