### Step 1: Create a GitHub Account

If you haven't already, go to [GitHub](https://github.com/) and sign up for a free account.

### Step 2: Install Git

If you haven't already, install Git on your computer. You can download it from the [official Git website](https://git-scm.com/).

### Step 3: Set Up Git

Once Git is installed, open a terminal (Command Prompt on Windows, Terminal on macOS and Linux) and configure Git with your username and email address:

```bash
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

### Step 4: Create a New Repository

1. Go to your GitHub profile and click on the "+" icon in the top right corner, then select "New repository".
2. Give your repository a name, for example, "my-first-repo".
3. Optionally, add a description.
4. Choose whether the repository should be public or private.
5. Check the box to initialize the repository with a README file.
6. Click on "Create repository".

### Step 5: Clone the Repository

Now, back in your terminal, navigate to the directory where you want to store your code, and clone the repository:

```bash
git clone https://github.com/your-username/my-first-repo.git
```

Replace `your-username` with your GitHub username.

### Step 6: Create a Simple README File

Inside the cloned repository directory, create a new file named `README.md`:

```bash
touch README.md
```

Open the `README.md` file with a text editor of your choice and add some content. For example:

```markdown
# My First Repository

This is my first repository on GitHub. It's just a simple example.
```

Save the file.

### Step 7: Add, Commit, and Push Your Changes

Add the `README.md` file to the staging area, commit the changes, and push them to GitHub:

```bash
git add README.md
git commit -m "Add README file"
git push origin master
```

### Step 8: Verify

Go back to your GitHub repository page and refresh. You should see the `README.md` file with the content you added.

That's it! You've successfully created a version-controlled repository on GitHub and pushed your code with a simple README file using Git commands.