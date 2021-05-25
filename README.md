# gpass 🔑

> Graphical Password Authentication Security for Systems

![Registration/Login Components](https://i.imgur.com/L8i2d3B.png)

## Features

- Easy to Use
- Efficient Way to Create New Password
- A lot of Usability Perks
- User Oriented Password Creation

## Install

`npm install @tadynas/gpass --registry=https://npm.pkg.github.com/`

or 

`yarn add @tadynas/gpass --registry=https://npm.pkg.github.com/`

then add style sheet to the root of your project

```js 
import '@tadynas/gpass/styles-min.css'
```

## Registration Password

```js
<RegistrationPass 
   images={images}
   email={email}
   password={password}
   disableButton={false}
   handleChangePassword={(updatedPassword) => setPassword(updatedPassword)}
   handleSignUp={() => console.log('Sign Up')}
   error={error}
/>
```

1. **images** - array of 4 images links that will be displayed for the user
2. **email** - user provided email
3. **password** - password that user will provide
4. **disableButton** - disable button when waiting response from server
5. **handleChangePassword** - updated password
6. **handleSignUp** - user pressed 'Sign Up' button when available
7. **error** - provide a message when server is not working or user password is incorrect

## Login Password

```js
<LoginPass 
   images={images}
   email={email}
   password={password}
   disableButton={false}
   handleChangePassword={(updatedPassword) => setPassword(updatedPassword)}
   handleSignIn={() => console.log('Sign In')}
   error={error}
/>
```

1. **images** - array of 4 images links that will be displayed for the user
2. **email** - user provided email
3. **password** - password that user will provide
4. **disableButton** - disable button when waiting response from server
5. **handleChangePassword** - updated password
6. **handleSignIn** - user pressed 'Sign In' button when available
7. **error** - provide a message when server is not working or user password is incorrect

