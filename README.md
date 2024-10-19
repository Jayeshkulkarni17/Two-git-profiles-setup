## Managing Multiple Git Profiles

Follow these steps to set up and manage multiple Git profiles on your machine.

### Step 1: Check Your Current Git User Configurations

Before setting up multiple profiles, check your current user configuration to see what’s already in place.

git config --get user.name
git config --get user.email

If you’re using Git for the first time, these may return nothing. If you have a global user profile, it will display the configured username and email.

Step 2: Set a Global Git Profile for General Use
To set your global profile for most of your projects (personal or open-source contributions), run the following commands:

git config --global user.name "your-username"
git config --global user.email "your-email"

This sets up a default profile for any repositories unless you override it with a different local configuration.

Step 3: Set a Local Git Profile for a Specific Repository
When working on a project that requires a different GitHub account (e.g., work or client projects), you can set a local profile for that repository:

git config --local user.name "your-work-username"
git config --local user.email "your-work-email"

This configures Git to use the specified username and email for this particular repository.

Step 4: Handling Credentials with Different Profiles
To ensure the correct credentials are used for different repositories, you can store credentials using Git’s credential helper. For HTTP/HTTPS URLs, run the following command:

git config --global credential.useHttpPath true

This tells Git to store credentials specific to each repository’s remote URL, making it easier when switching between personal and work GitHub accounts.

Step 5: Verify Your Setup

You can verify the configuration for each repository using the following commands:

git config --get user.name
git config --get user.email

Conclusion
With these steps, you can seamlessly manage multiple Git profiles on one device without mixing up your credentials. This setup is particularly useful when you need to use different usernames and emails for personal and work repositories.
You can update your global and local configurations at any time using the commands above.
