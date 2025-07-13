# Max’s Seafood Café Website

## Project Overview

**Max’s Seafood Café Website** is a static marketing site for the Max’s Seafood Café restaurant, built with Jekyll and optimized for deployment on **GitHub Pages**. The site provides an online presence for the restaurant, featuring a visually engaging **menu page built from a Canva design**, and standard sections such as **Home**, **About**, **Menu**, **Contact**, and **Hours**. Social media integration is included to connect visitors with the restaurant’s Facebook and Instagram profiles. As a Jekyll-powered static site, it uses Markdown for content and generates only static files (HTML, CSS, JS), making it fast, secure, and easy to host on GitHub Pages.

## Features

* **Home Page:** Welcomes visitors with a banner or hero image, the restaurant’s tagline, and a brief introduction. It provides immediate links to key information (like menu highlights or reservation contact info) and showcases the ambiance of Max’s Seafood Café.
* **About Page:** Tells the story of Max’s Seafood Café – history, mission, and what makes it unique. This section may include photos of the interior, staff, or signature dishes, along with text describing the restaurant’s heritage and atmosphere.
* **Menu Page:** Displays the restaurant’s food and drink offerings. The menu page is crafted using assets from **Canva** for a polished look – for example, an embedded PDF or high-quality image of the menu designed in Canva. Visitors can view all menu items (with prices and descriptions) in an easy-to-read format. (To update the menu, you can replace the Canva-generated image/PDF in the repository with an updated version.)
* **Contact Page:** Provides contact details and location information. This includes the restaurant’s address (with a link or embedded Google Map for directions), phone number, email, and possibly a simple contact form (or a mailto link) for inquiries. The Contact section also clearly lists the **Hours of Operation** so customers know when the café is open.
* **Social Media Integration:** Throughout the site (for instance, in the header, footer, or contact page), there are icons linking to Max’s Seafood Café’s social media profiles (e.g. Facebook and Instagram). This encourages visitors to connect on those platforms. The site may display social media icons that open the restaurant’s pages in new tabs. *(Note: No live social media feed is embedded, to keep the site simple and fast; only external links.)*
* **Responsive Design:** The website’s layout is mobile-friendly. The navigation menu, images, and text content are styled with CSS to ensure the site looks good on desktops, tablets, and smartphones. Visitors get a consistent experience across devices, which is crucial for a restaurant site (many customers will check the menu or hours from their phones).
* **Navigation & Layout:** A consistent navigation bar is present on all pages, allowing easy switching between Home, About, Menu, Contact, etc. There’s also a footer that might contain the address, hours, and social media links. The site’s look-and-feel is clean and focused on the restaurant’s branding (using the provided logo and color scheme).

## Tech Stack

This project utilizes the following technologies and tools:

* **Jekyll:** Jekyll is a static site generator used to build the website. Content is written in Markdown and Jekyll transforms it into a static site using layouts and includes. Jekyll has built-in support for GitHub Pages, which provides a simplified build process. (Jekyll uses the Liquid templating language to insert dynamic content like menus, headers, and footers into pages.)
* **GitHub Pages:** The site is hosted on GitHub Pages, GitHub’s static hosting service. The repository is configured so that GitHub Pages will automatically build the Jekyll site and serve it. GitHub Pages takes the static files (HTML, CSS, JS) from the repository, runs Jekyll to generate the site, and publishes a website. This eliminates the need for separate hosting or manual deployment – any changes pushed to the repository will trigger a rebuild and update the live site.
* **Markdown:** Most content pages (like About, Menu, etc.) are written in Markdown (`.md` files) for ease of editing. Jekyll converts these Markdown files into HTML during the build. This allows non-developers to update content by editing simple text files without needing to write HTML.
* **HTML & CSS:** Custom HTML templates and CSS styles define the structure and design of the site. The Jekyll theme or layout is written in HTML (with Liquid placeholders for dynamic content), and styling is done with CSS (possibly including a **CSS framework** or just vanilla CSS). The design is tailored to reflect Max’s Seafood Café’s branding (colors, typography, etc.). Modern HTML5 semantic elements are used for accessibility and SEO, and CSS3 is used for layout (including responsive behaviors like a mobile nav).
* **Canva (Design Assets):** Canva was used to design graphical assets for the site, in particular the menu. The menu page uses an image or PDF exported from Canva to present the restaurant’s menu in an attractive format. Additionally, logos or other graphics may have been created or edited in Canva. These assets are included in the repository (for example, in an `assets/images` folder) and integrated into the site’s pages.
* **JavaScript:** Since this is a simple static site, heavy JavaScript frameworks are not used. However, a little JavaScript might be present for interactive elements – for example, a mobile menu toggle, form validation, or embedding a Google Map. Any JS used is lightweight and is included in the repository (or via CDN) to enhance user experience without affecting the site’s speed.
* **Other Tools:** The development was likely done using Git for version control. Bundler (Ruby’s dependency manager) is used to manage the Ruby gems (Jekyll and any plugins). For testing locally, developers use the built-in Jekyll server. If any Jekyll plugins are used (for example, for SEO tags or sitemap generation), they would be listed in the `Gemfile` and `_config.yml`.

## Setup Instructions (Installation and Local Development)

Follow these steps to set up the project on your local machine for development or testing:

1. **Prerequisites – Install Ruby and Bundler:** Ensure you have **Ruby** installed on your system (Jekyll is a Ruby-based tool). Jekyll requires Ruby (version 2.7 or higher is recommended). You can check by running `ruby --version`.

   * If Ruby is not installed, download it from the official site or use a version manager (like `rbenv` or `rvm` for Mac/Linux, or RubyInstaller for Windows).
   * After Ruby is set up, install Bundler (the Ruby gem manager) by running:

     ```bash
     gem install bundler
     ```

     *(You may need administrator privileges for this.)*

2. **Clone the Repository:** Clone the GitHub repository to your local machine. In a terminal, run:

   ```bash
   git clone https://github.com/<YourUsername>/maxs-seafood-cafe-website.git
   ```

   Replace `<YourUsername>/maxs-seafood-cafe-website.git` with the actual GitHub path of the repository (for example, the owner’s username and repo name). This will download the project files into a new folder.

3. **Install Jekyll and Dependencies:** Navigate into the project directory and use Bundler to install the required gems (Jekyll and any plugins/themes specified):

   ```bash
   cd maxs-seafood-cafe-website
   bundle install
   ```

   This will install all dependencies as defined in the `Gemfile`. It includes **Jekyll** and possibly the GitHub Pages gem (which pins the Jekyll version to the one supported by GitHub Pages). If the install succeeds, you should have Jekyll and any plugins ready to use.

4. **Configure (Optional):** The site’s main configuration is in the `_config.yml` file. In most cases you won’t need to change anything to run locally. However, if the site uses a `baseurl` (for project sites) or other custom config that affects local serving, you might adjust or note it. By default, you can leave it as is. (For example, if `baseurl: "/maxs-seafood-cafe"` is set for GitHub Pages, you might run Jekyll with `--baseurl` flag locally. But if not sure, just run the next step and see.)

5. **Run the site locally:** Use Jekyll via Bundler to serve the website on a local development server. Run:

   ```bash
   bundle exec jekyll serve
   ```

   Jekyll will build the site and start a local web server. In the console output, you should see a message indicating the site is running, for example: `Server address: http://127.0.0.1:4000` (and by default, it’s accessible at `http://localhost:4000`). Leave this command running.

6. **Preview the site:** Open your web browser and navigate to `http://localhost:4000/` (or the address Jekyll provided). You should see the Max’s Seafood Café website running locally, exactly as it would appear on GitHub Pages. Navigate through the pages (Home, About, Menu, etc.) to verify everything is working. Jekyll will watch for file changes – if you edit a page or layout, it will regenerate the site and you can refresh the browser to see updates.

7. **Troubleshooting:** If you encounter errors:

   * Make sure all gems installed without errors (you might need to update Bundler or fix any Ruby version issues if any gem failed to install).
   * If Jekyll won’t start, check for messages. Common issues involve invalid YAML in `_config.yml` or front matter. The error log will usually indicate the file and line number.
   * For Windows users: Jekyll is not officially supported on Windows. You can still use it via Windows Subsystem for Linux (WSL) or by using a Docker image. If developing on Windows without WSL, ensure all dependencies (including a DevKit for native gem compilation) are properly installed. See Jekyll’s documentation for Windows if needed.
   * Consult the [Jekyll documentation](https://jekyllrb.com/docs/) if you need more help on setting up or running the site locally.

By completing the above steps, you can run and modify the website locally. Once you are satisfied with changes, you can commit them and push to GitHub to update the live site.

## Deployment (GitHub Pages)

Deploying the site is straightforward since it is designed to work with **GitHub Pages**:

* **GitHub Pages Configuration:** Ensure that GitHub Pages is enabled for the repository. In the repository’s settings on GitHub, under **Pages**, set the publishing source to the appropriate branch. Common setups are:

  * **User/Organization Site:** If this is a user/organization website repository (named `<user>.github.io`), you typically use the `main` branch as the publishing source. GitHub Pages will treat the root of the repository as the site.
  * **Project Site:** If this is a project site (e.g., repository is not named `<user>.github.io`), you can either use the `main` branch `/docs` folder or a dedicated `gh-pages` branch as the publishing source. This project likely uses a branch (for example, the `gh-pages` branch or simply the `main` branch) to publish the site.
* **Automatic Jekyll Build:** When you push changes to the repository’s publishing branch, GitHub Pages will automatically run Jekyll to rebuild the site and deploy the updated version. You don’t need to manually run Jekyll and upload files – GitHub Pages takes care of it during the publishing process. Typically within a minute or so of pushing a commit, the changes go live.
* **Accessing the Live Site:**

  * If using a **GitHub Pages domain**, the site will be available at `https://<username>.github.io/<repository>` for project sites, or `https://<username>.github.io` for user sites. For example, if the repository is `github.com/MaxOwner/maxs-seafood-site` (project site), the default Pages URL would be `https://MaxOwner.github.io/maxs-seafood-site/`.
  * If using a **custom domain** (like **maxsseafoodcafe.com**), make sure a `CNAME` file is present in the repository with the custom domain, and that the domain’s DNS records are pointed to GitHub’s servers. In this project, if deploying to the restaurant’s actual domain, we would add `www.maxsseafoodcafe.com` (and/or the root domain) in a CNAME file. GitHub Pages will serve the site at that domain once DNS is configured. Remember to enforce **HTTPS** in settings for security.
* **Branch Strategy:** Developers should work on a separate branch or fork (especially if multiple people are collaborating), then merge changes into the publishing branch (often `main` or `gh-pages`). This can be done via pull requests to ensure code review and avoid breaking the live site.
* **Continuous Deployment:** Every push to the configured branch triggers a new deployment. There is no additional CI/CD configuration needed for basic usage. (Under the hood, GitHub uses an Actions workflow or their Pages build service to run Jekyll.) If a more complex build process or unsupported plugins are needed in the future, one could set up a custom GitHub Actions workflow to build and deploy the site – but for now, the native Pages deployment is sufficient.
* **Verification:** After deployment, visit the site URL and verify all pages load correctly. It’s wise to test things like navigation, images, links, and forms on the live site. Because Jekyll builds relative links according to the base URL, having the correct `baseurl` and `url` in `_config.yml` (especially for project sites) is important for links to work on GitHub Pages.

In summary, **to deploy**: commit and push your changes to GitHub. As long as the repository’s Pages settings are correctly configured, the live website will update automatically. For major changes or new pages, double-check the live site after a few minutes to ensure everything looks as expected.

## Contributing

Contributions to improve the site are welcome! If you’d like to suggest changes, add features, or fix issues, please follow these steps:

1. **Fork the repository** on GitHub to your own account. This creates your own copy of the project.
2. **Clone your fork** to your local development environment:

   ```bash
   git clone https://github.com/<YourUsername>/maxs-seafood-cafe-website.git
   ```

   (Replace `<YourUsername>` with your GitHub username.)
3. **Create a new branch** for your changes:

   ```bash
   git checkout -b my-improvements
   ```

   Use a descriptive branch name for your feature or fix.
4. **Make your changes** to the code, content, or documentation. This might involve editing Markdown files, HTML layouts, CSS styles, or adding images. For significant changes, try to test the site locally (see **Setup Instructions** above) to ensure your changes work as intended.
5. **Commit and push** your changes to your branch:

   ```bash
   git add .
   git commit -m "Add feature X (or Fix issue Y)"
   git push origin my-improvements
   ```
6. **Open a Pull Request** on the original repository: Go to your fork on GitHub and click “Compare & pull request”. Provide a clear description of your changes and why they’re beneficial. If there is an open issue related to your change, mention “Closes #ISSUE\_NUMBER” in the PR description.
7. **Code Review:** The project maintainer(s) will review your pull request. They may ask questions or request adjustments. Respond to any feedback by making additional commits to your branch. Once the changes are approved, they will be merged.
8. **Ensure consistency:** Follow the coding style and conventions used in the project. For example, keep Markdown formatting consistent, use similar HTML structure as existing pages, and optimize images. This keeps the project maintainable.
9. After your contribution is merged, GitHub Pages will redeploy the updated site. You can see your changes live on the website.

Even if you’re not a developer, you can contribute by opening an **Issue** on the repo to report bugs, request new features, or suggest improvements (like corrections to information, accessibility enhancements, etc.). All contributions are appreciated!

*(Note: If this is primarily a client project repository rather than a community open-source project, the workflow might be limited to the site owner. However, the above process applies if the code is open source and accepting contributions.)*

##
