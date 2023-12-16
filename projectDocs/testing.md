# Testing

## Overview

We are using Jest, a JavaScript testing framework, for testing our JavaScript code. To run the tests, run `npm test` from the root directory. In addition, `npm test` has been included in one of our Github workflows; the tests run every time a pull request is opened against the main branch. The test files can be found in the `lib/__tests__` directory.

## Standards

Here is a list of standards that we try to adhere to when creating tests:

1. Tests should be deterministic. Running a test multiple times should produce the same result.
2. Use the Jest function `describe` to group the tests for a method together.
3. Test names should state what the purpose of the related test is for.
4. Tests should not interfere with the actual code or other tests. Mocking variables and functions is one way of achieving this.
5. Use the test setup and teardown methods that Jest has to reduce the amount of repeated code between tests.

## Manual Testing

### Creating an account

1. Go to https://glitch.com/edit/#!/import/github/CSE-210-Team-6/shuttlecraft.
2. Set the DOMAIN environment variable in `.env` file. It should be `{glitch-project-name}.glitch.me`.
3. Enter your domain in the browser. It should redirect you to `/account/create`, where you can create an account.
4. Add a username and password of your choice. The domain should be the same as the one in the `.env` file.
5. Create the account; you should be logged in and redirected to `/private` to see your account.

### Logging into an account

1. When you go to `/private`, if you are not logged in, you should be redirected to `/account/login`.
2. Enter your username and password.
3. If the credentials are correct, you should be redirected to `/private` to see your account. If the credentials are incorrect, you should be prompted to enter the correct credentials.

### Logging out of an account

1. Go to `/account/logout`.
2. You should be logged out and should be prompted to login again.

### Home page

1. After creating an account/logging in, you should be redirected to the home page. On the left hand side, there should be different sections: `Latest`, `Notifications`, `Messages`, `Compose`, `My Posts`, `Prefs`, and `Bugs & Issues`. The default section that is selected should be `Latest`.

   ![Screenshot 2023-12-14 at 8 08 53 PM](https://github.com/CSE-210-Team-6/shuttlecraft/assets/52771821/f4461699-e8f0-46a2-91fc-880d6eb2c7be)

### Following a person

1. On the left hand side, there is an input box underneath `find a person`. Search for the person you would like to follow by entering their `username@domain`.

   ![Screenshot 2023-12-14 at 8 10 09 PM](https://github.com/CSE-210-Team-6/shuttlecraft/assets/52771821/4f22e2d1-9441-410d-9897-4d63b2b3404a)
2. Click the `Enter` key on your keyboard to execute the search.
3. If the person you are searching for exists, they will show up in the list of results. Click on the person that you would like to follow from the results.
4. Click on the green `Follow` button on the person's profile.
5. Refresh the page.
6. You should see the person you just followed on the left hand side.

### Unfollowing a person

1. On the left hand side, click on the person that you would like to unfollow.
2. Click on the green `Unfollow` button on the person's profile.
3. Refresh the page.
4. You should no longer see the person you unfollowed on the left hand side.

### Sending a message

1. On the left hand side, click on a person that you follow or find a person and click on their profile.
2. Click on the button next to the `Follow` button.
3. You should be redirected to a page that shows your messages with that person.
4. Enter the message that you would like to send in the text box. Click the `Send` button.
5. You should see your message appear on the page.

### Composing a post

1. On the left hand side, click on the `Compose` section. You should be redirected to `/private/post`.
2. Enter what you would like to post in the text box.
3. You may optionally specify a content warning.
4. You may also specify if you would like to allow replies, boosts, or faves. By default, all of them are allowed. To change that, uncheck the checkboxes.
5. Click the `Compose` button to create the post.
6. You should be redirected to the `Latest` section where you should see your post.

### Latest

1. On the left hand side, click on the `Latest` section. You should be redirected to `/private`.
2. You should see a list of the activity from your posts or people that you follow.

### Notifications

1. On the left hand side, click on the `Notifications` section. You should be redirected to `/private/notifications`.
2. You should see a list of the activity from things related to you, e.g., someone following you.

### My Posts

1. On the left hand side, click on the `My Posts` section. You should be redirected to `/private/feeds/{your-username}@{your-domain}`.
2. You should see your profile at the top. Below this, you should see a list of your posts.

### Prefs

1. On the left hand side, click on the `Prefs` section.
2. At the top, you should see links to your public page, your followers, and who you are following.
3. Below that, you can change the emojis and the text of the `Compose` button.
4. Underneath the `Preferences`, you can change your username, set a bio, and choose an avatar for your profile.

### Bugs & Issues

1. On the left hand side, click on the `Bugs & Issues` section. You should be redirected to https://github.com/benbrown/shuttlecraft/issues.

