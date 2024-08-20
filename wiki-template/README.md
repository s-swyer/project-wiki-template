# README: Creating a GitHub Wiki by Cloning the Wiki Repository

**DELETE THIS README AFTER WIKI SETUP**

This README provides step-by-step instructions for creating a GitHub Wiki by cloning the Wiki repository and copying template Wiki files from the `gs-gs/gs-delivery-assurance/wiki-template` directory. Following these steps will ensure that your Wiki is properly set up and that GitHub's requirements are met, including the necessary `Home` page for Wiki navigation.

## Prerequisites

Before you begin, ensure you have the following:

- **Git**: Installed and configured on your local machine.
- **GitHub Repository**: The repository for which you want to create a Wiki.
- **Access Rights**: Sufficient permissions to push changes to the GitHub repository.

## Steps to Create the Wiki

### 1. Clone the GitHub Wiki Repository

Every GitHub repository has an associated Wiki repository. To begin, you need to clone this Wiki repository to your local machine.

1. Navigate to your GitHub repository.
2. Click on the **Wiki** tab.
3. On the right side, click **Clone this wiki locally**. You will see a URL similar to the following:

   ```
   git clone https://github.com/your-username/your-repo.wiki.git
   ```

4. Clone the Wiki repository using the URL provided:

   ```
   git clone https://github.com/your-username/your-repo.wiki.git
   ```

5. Navigate to the cloned Wiki repository:

   ```
   cd your-repo.wiki
   ```

### 2. Copy the Template Wiki Files

With the Wiki repository cloned, you can now copy the template files from the `gs-gs/gs-delivery-assurance/wiki-template` directory into your Wiki.

1. Assuming you have the `gs-gs/gs-delivery-assurance/wiki-template` directory in your local file system, copy its contents into the cloned Wiki repository:

   ```
   cp -r /path/to/wiki-template/* .
   ```

2. Verify that all files have been copied correctly by listing the contents of your Wiki repository:

   ```
   ls
   ```

   You should see a list of Markdown (`.md`) files and any other resources (such as images) that were in the `wiki-template` directory.

### 3. Ensure the 'Home' Page Exists

GitHub Wikis require a `Home.md` file to be present in the root of the Wiki repository. This file serves as the landing page for your Wiki and provides the navigation to other pages.

1. Confirm that a `Home.md` file is present:

   ```
   ls | grep Home.md
   ```

2. If the `Home.md` file is missing, create it manually:

   ```
   echo "# Welcome to the Wiki" > Home.md
   ```

   Alternatively, ensure your template includes a `Home.md` file.

> **Note:** The `Home.md` file is essential for GitHub to render the Wiki correctly. Without it, the Wiki will not display navigation links properly.

### 4. Push Changes to the GitHub Wiki

Once you have copied the template files and ensured the `Home.md` file is in place, you can push the changes back to GitHub.

1. Stage the changes:

   ```
   git add .
   ```

2. Commit the changes:

   ```
   git commit -m "Initialise Wiki with template files"
   ```

3. Push the changes to the GitHub Wiki repository:

   ```
   git push origin main
   ```

### 5. Verify the Wiki on GitHub

After pushing the changes, navigate to the **Wiki** tab in your GitHub repository to verify that the Wiki pages have been correctly published. The `Home` page should be the default landing page, with other pages accessible through the navigation links.
