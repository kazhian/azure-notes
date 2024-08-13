# azure-notes

When you create a GitHub Pages site, the default behavior is to serve HTML files. Markdown (`.md`) files are not automatically rendered as web pages unless they are processed into HTML. Here’s how you can ensure that your Markdown file is displayed correctly on your GitHub Pages site:

### Steps to Display Markdown Files on GitHub Pages

1. **Convert Markdown to HTML**:
   - GitHub Pages can render Markdown files if you use a static site generator like Jekyll. Jekyll automatically converts Markdown files to HTML when you push them to your GitHub Pages repository.

2. **Ensure Jekyll is Enabled**:
   - By default, GitHub Pages uses Jekyll to process your site. Make sure you have a `_config.yml` file in the root of your repository. This file can be empty or contain configuration settings for Jekyll.

3. **Create a Jekyll-Compatible Structure**:
   - If you want to display your Markdown file, you should place it in a location where Jekyll can process it. For example, you can create a folder called `_posts` for blog posts or simply place it in the root directory or a subdirectory.

4. **Naming Your Markdown File**:
   - If you are using the `_posts` directory, your Markdown files should follow a specific naming convention: `YYYY-MM-DD-title.md`. For example, `2023-10-01-my-post.md`.

5. **Linking to Your Markdown File**:
   - If your Markdown file is not in the `_posts` directory, you can create an HTML file that links to it or use a layout that includes it. For example, you can create an `index.html` file that links to your Markdown file:
     ```html
     <html>
     <head>
         <title>My GitHub Pages Site</title>
     </head>
     <body>
         <h1>Welcome to My Site</h1>
         <a href="subfolder/myfile.md">View My Markdown File</a>
     </body>
     </html>
     ```

6. **Using Jekyll Front Matter**:
   - If you want to create a standalone page from your Markdown file, you can add Jekyll front matter at the top of your Markdown file. For example:
     ```markdown
     ---
     layout: default
     title: My Markdown Page
     ---
     
     # My Markdown Content
     This is the content of my Markdown file.
     ```

7. **Check Your GitHub Pages Settings**:
   - Ensure that your GitHub Pages settings are correctly configured to point to the right branch and folder.

### Example Structure

Here’s an example of how your repository might look:

```
my-repo/
│
├── index.html
├── _config.yml
├── _posts/
│   ├── 2023-10-01-my-post.md
│
└── subfolder/
    ├── myfile.md
```

### Accessing Your Markdown File

- If you have set everything up correctly, you should be able to access your Markdown file as a rendered HTML page. For example, if your file is named `myfile.md` and is located in a subfolder, you can access it via:
  ```
  https://username.github.io/repository-name/subfolder/myfile.html
  ```

### Conclusion

By following these steps, you should be able to display your Markdown files on your GitHub Pages site. If you continue to have issues, double-check your file structure, naming conventions, and ensure that Jekyll is processing your files correctly.
