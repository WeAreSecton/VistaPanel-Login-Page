# VistaPanel Login Page
![GitHub](https://img.shields.io/github/license/wearesecton/vistapanel-login-page?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/wearesecton/vistapanel-login-page?color=red&style=for-the-badge)

This is a simple login page for VistaPanel, designed with the Tabler interface. It includes a form with username and password fields, and a password reset link.

## Usage
For the page to function properly, you might need to modify the code. Here are the main things you should change:

- **pattern**: Change the pattern attribute in the username input tag to match your username format. *(required)*
- **prefix**: Change the "prefix_" in the placeholder attribute of the username input tag to your desired username prefix. *(optional)*
- **maxlength**: Change the maxlength attribute in the username input tag to match your maximum username length. *(optional)*

## Code breakdown

The code for this login form is written in HTML and uses the Tabler CSS framework for styling. Here is a breakdown of the different parts of the code:

### Form tag

The form tag specifies the URL of the login script to which the form data will be submitted, as well as the HTTP method (in this case, POST).

```html
<form action="https://cpanel.byethost.com/login.php" method="post" name="login" class="mb-3">
```

### Username input
The username input field has an ID of "mod_login_username". The "pattern" attribute specifies a regular expression that the username must match, and the "placeholder" attribute specifies the default text that will appear in the input field. The "minlength" and "maxlength" attributes specify the minimum and maximum lengths of the username.

```html
<label for="mod_login_username" class="form-label">Username<input name="uname" id="mod_login_username" type="text" class="form-control ps-1" alt="username" pattern="^prefix_.*" minlength="10" placeholder="prefix_" maxlength="14"/></label>
```

### Password input
The password input field has an ID of "mod_login_password".

```html
<label for="mod_login_password" class="form-label">Password<input type="password" id="mod_login_password" name="passwd" class="form-control ps-1" alt="password"/></label>
```

### Reset password link and login button
The reset password link and login button are wrapped in a div. The reset password link has an href attribute that points to the URL of your password reset page.

```html
<a href="https://cpanel.byethost.com/lostpassword.php" class="btn btn-link link-secondary">Reset your password</a>
<input type="submit" name="Submit" class="btn btn-primary" value="Login" />
```

## License
The code is licensed under the MIT License. See the LICENSE file for more information.
