# gpass 🔑 

> Graphical Password Authentication System for Security

![Registration/Login Components](https://i.imgur.com/L8i2d3B.png)

### Check Live Version [here](https://vigorous-blackwell-7bfba7.netlify.app)

## Features

- Easy to Use
- Efficient Way to Create New Password
- A lot of Usability Perks
- User Oriented Password Creation

## Install

`npm install @tadynas/gpass`

or 

`yarn add @tadynas/gpass`

then add style sheet to the root of your project

```js 
import '@tadynas/gpass/styles-min.css'
```

## Registration Password

```js
import { RegistrationPass } from '@tadynas/gpass'

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
import { LoginPass } from '@tadynas/gpass'

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

## Example Code

### Login Page

```js
import { useState } from 'react'

import '@tadynas/gpass/styles-min.css'

import { LoginPass } from '@tadynas/gpass'


function App() {
  const [email, setEmail] = useState('test@email.com')
  const [password, setPassword] = useState('')
  const [error, setError] = useState('')

  return (
    <LoginPass 
      images={['https://tinyurl.com/ye9k9847', 
              'https://tinyurl.com/yttpmuyt', 
              'https://tinyurl.com/4nex98t3', 
              'https://tinyurl.com/y6nd8jha']}
      email={email}
      password={password}
      handleChangePassword={(updatedPassword) => setPassword(updatedPassword)}
      handleSignIn={() => console.log('Sign In')}
      error={error}
    />
  )
}

export default App
```

### Registration Page

```js
import { useState } from 'react'

import '@tadynas/gpass/styles-min.css'

import { RegistrationPass } from '@tadynas/gpass'


function App() {
  const [email, setEmail] = useState('test@email.com')
  const [password, setPassword] = useState('')
  const [error, setError] = useState('')

  return (
    <RegistrationPass 
      images={['https://tinyurl.com/ye9k9847', 
              'https://tinyurl.com/yttpmuyt', 
              'https://tinyurl.com/4nex98t3', 
              'https://tinyurl.com/y6nd8jha']}
      email={email}
      password={password}
      handleChangePassword={(updatedPassword) => setPassword(updatedPassword)}
      handleSignUp={() => console.log('Sign Up')}
      error={error}
    />
  )
}

export default App
```
