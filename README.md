# Two-git-profiles-setup
Managing multiple Git profiles on a single device can be challenging, especially when you switch between work and personal projects. In this guide, I’ll show you how to set up and manage two different Git profiles by configuring global and local Git settings.

Step 1: Check Your Current Git User Configurations

Before setting up multiple profiles, check your current user configuration to know what’s already in place.

--> git config --get user.name 
--> git config --get user.email

If you’re using Git on your machine for the first time, these may return nothing. If you have a global user profile, it will display the configured username and email.

Step 2: Set a Global Git Profile for work project

Typically, you’ll use your global Git profile for most of your projects, like personal or open-source contributions. However, when you’re working on a project that requires a different github account username and email (e.g., a work project or a client project), you can set a local profile for that specific repository.

To set your global profile for general use, run the following commands:

--> git config --global user.name "your-username"
--> git config --global user.email "your-email"
This sets up a default profile for any repositories you work on unless you override it with a different configuration

Step 4: Handling Credentials with Different Profiles

To ensure that the correct credentials are used when accessing remote repositories, you may want to set up different credentials for each profile. You can store credentials using Git’s credential helper.

For HTTP/HTTPS URLs, run the following command to store the credentials path-specific:

--> git config --global credential.useHttpPath true

This tells Git to store credentials specific to each repository’s remote URL, which is helpful when switching between different accounts (like GitHub work and GitHub personal).

Step 5: Verify Your Setup using following commands

git config --get user.name
git config --get user.email

Conclusion :
With these steps, you can seamlessly manage multiple Git profiles on one device without getting your credentials mixed up. This setup helps when you need to use different usernames and emails for personal and work repositories, ensuring that commits are properly attributed. If you ever need to modify your settings, you can update the global and local configurations at any time using the commands above.
