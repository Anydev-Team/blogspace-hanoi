# Architecture of Blogspace Lite

In this document, we will discuss the architecture of Blogspace Lite, a blog platform develop for open-source projects. The platform is designed to be simple, lightweight, and easy to use, with a focus on content creation, documentation and sharing.

## Overview

Blogspace Lite is a static website using git and GitHub Pages for hosting. In order to create an easy to develop and maintain, we do have to define file structure and rules for writing content, furthermore, we also have also define some of collaboration rules for contributors and members.

## File Structure

The file structure of Blogspace Lite is as follows:

```
blogspace-lite/
├── blogs/
│   ├── 1/
│   │   ├── content.md
│   │   │ ── description.json
│   │   │ ── index.html
│   │   └── images/
│   │       └── image1.jpg
│   ├── 2/
│   │   ├── content.md
│   │   │ ── description.json
│   │   │ ── index.html
│   │   └── images/
│   │       └── image2.jpg
│   └── ...
│ ── assets/
│ ── index.html

```

The `blogs` directory contains all the blog posts written by students. Each blog post is stored in a separate directory with a unique ID (e.g., `1`, `2`, `3`, etc.). Each blog post directory contains the following files:

- `content.md`: the main content of the blog post written in Markdown format.
- `description.json`: a JSON file containing metadata about the blog post, such as the title, author, date, etc.
- `index.html`: the HTML file generated from the Markdown content.
- `images/`: a directory containing any images used in the blog post.

The `assets` directory contains all the assets for the website, such as images, CSS, JavaScript, etc.
The `index.html` file is the main landing page of the website, which lists all the blog posts in reverse chronological order. Each blog post is displayed as a card with a title, author, date, and excerpt of the content.

## Rules for Writing Content

In order to maintain consistency and quality across all blog posts, we have defined the following rules for developing content:

- All blog posts must first be written in Markdown format. This makes it easy to write and format content without having to worry about HTML or CSS. It also allows for easy version control and collaboration using git.
- Blog post must include a `description.json` file with metadata about the blog post, such as the title, author, date, etc. This file is used to generate the index page and display information about the blog post.
- All images used in blog posts must be stored in the `images/` directory within the blog post directory. This makes it easy to manage and reference images in the content.
- Blog post must be reviewed and approved by a moderator before being published. This ensures that the content is accurate, relevant, and appropriate for the platform.

NOTE: The `index.html` file is generated automatically from the `content.md` file using a static site generator. This allows for easy deployment and maintenance of the website without having to manually update HTML files. HOWEVER, the `index.html` file can be manually updated if necessary if you are member of Blogspace Lite.

## Collaboration Rules

As for members in Blogspace Lite, we have defined the following rules for collaboration:

- Members should use git and GitHub to contribute to the platform. This allows for easy version control, collaboration, and deployment of the website.
- Members should follow the file structure and rules for writing content as outlined above. This ensures that the platform remains consistent and easy to maintain.
- Members should respect the contributions of others and provide constructive feedback when reviewing blog posts. This helps to maintain a positive and supportive community within Blogspace Lite.

Git and GitHub guidelines: (in example of changing button color on homepage) 

- Fork the repository to your account.
- Create a new branch for your changes. (e.g., `feature/homepage-ui-update`)
```bash
git checkout -b feature/homepage-ui-update`)
```

- Make your changes and commit them to your branch. (e.g., `change button color`)
```bash
git add .
git commit -m "dev: change button color"
```

- Push your changes to the branch on your forked repository or remote repository.
```bash
git push origin feature/homepage-ui-update
```

- Create a pull request to the main repository.
- Wait for the pull request to be reviewed and merged by a moderator.