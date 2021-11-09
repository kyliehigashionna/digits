<img src="doc/landing.png">

Digits is an application that allows users to:

  * Register an account.
  * Create and manage a set of contacts.
  * Add a set of timestamped notes regarding their interactions with each contact.

## Installation

First, [install Meteor](https://www.meteor.com/install).

Second, [download a copy of Digits](https://github.com/kyliehigashionna/digits). Note that Digits is a private repo and so you will need to request permission from the author to gain access to the repo.

Third, cd into the app directory install the required libraries with:

<img src="doc/meteornpminstall.png">

If you wanted to reset your meteor, you can reset it by invoking:

<img src="doc/meteorreset.png">

Once the libraries are installed and or reset, you can run the application by invoking:

<img src="doc/meteornpmrunstartcommand.png">

The first time you run the app, it will create some default users and data. Here is the output:

<img src="doc/meteornpmrunstart.png">

### Note regarding "bcrypt warning":

You might also get the following message when you run this application:

```
Note: you are using a pure-JavaScript implementation of bcrypt.
While this implementation will work correctly, it is known to be
approximately three times slower than the native implementation.
In order to use the native implementation instead, run

  meteor npm install --save bcrypt

in the root directory of your application.
```

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your site has very high traffic. You can safely ignore this warning without any problems during initial stages of development.

If all goes well, the template application will appear at http://localhost:3000. You can login using the credentials in settings.development.json, or else register a new account.

Lastly, you can run ESLint over the code in the imports/ directory with:

<img src="doc/npmrunlint.png">


## User Interface Walkthrough

#### Landing page

When you first bring up the application, you will see the landing page that provides a brief introduction to the capabilities of Digits:

<img src="doc/landing.png">


#### Register page

If you do not yet have an account on the system, you can register by clicking on “Login”, then “Sign Up”:

<img src="doc/register.png">

#### Sign in page

Click on the Login link, then click on the Signin link to bring up the Sign In page which allows you to login:

<img src="doc/signin.png">

#### User home page

After successfully logging in, the system takes you to your home page. It is just like the landing page, but the NavBar contains links to list contact and add new contacts:

<img src="doc/userhomepage.png">

#### List Contacts

Clicking on the List Contacts link brings up a page that lists all of the contacts associated with the logged in user:

<img src="doc/listcontacts.png">

This page also allows the user to add timestamped “notes” detailing interactions they’ve had with the Contact. For example:

<img src="doc/listcontactsnotes.png">

#### Edit Contacts

From the List Contacts page, the user can click the “Edit” link associated with any Contact to bring up a page that allows that Contact information to be edited:

<img src="doc/editcontacts.png">

#### Add Contacts

From the Add Contacts page, the user can click the “Add Contact” tab to bring up a page that allows the user to fillin the contact information for first name, last name, address, image, and description:

<img src="doc/addcontact.png">

#### Admin mode

It is possible to designate one or more users as “Admins” through the settings file. When a user has the Admin role, they get access to a special NavBar link that retrieves a page listing all Contacts associated with all users:

<img src="doc/adminmode.png">
