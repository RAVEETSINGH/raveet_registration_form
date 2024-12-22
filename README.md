# Raveet_Registration_Form

This is a simple **Registration Form** that collects user details such as Full Name, Username, E-mail, Phone Number, Password, and Confirm Password. The form also includes gender selection and uses JavaScript for basic validation, such as ensuring the password and confirm password fields match and allowing the user to toggle password visibility.

## Features

- **Form Fields**: Collects essential information from the user:
  - Full Name
  - Username
  - E-mail
  - Phone Number
  - Password
  - Confirm Password
  - Gender (Male, Female, Prefer not to say)
  
- **Password Validation**: Ensures that the password and confirm password fields match before submission.

- **Password Visibility Toggle**: Allows the user to toggle the visibility of both password fields.

- **Google Script Integration**: The form is set up to integrate with Google Apps Script to send form data to a Google Sheet upon submission.

- **Responsive Design**: The form layout is responsive and looks great on all devices, thanks to the use of flexible and fluid CSS.

## Technologies Used

- **HTML5**: Structure of the form
- **CSS3**: Styling the form and providing a visually appealing layout
- **JavaScript**: 
  - Form validation
  - Password visibility toggle functionality
- **Google Apps Script**: Used to handle form submissions and send the data to a Google Sheet.

  ## Live Demo

You can try out the live demo of the registration form below:

[**Live Demo Link**](https://your-demo-link.com)

## Installation

To use this form, you can clone the repository and open the `index.html` file in your browser:
Customizing for Your Own Google Sheet
To link the form to your own Google Sheet:

## Replace the scriptURL in the JavaScript:

In your index.html file, update the scriptURL variable with the new URL from your Google Apps Script:
 ```const scriptURL = 'YOUR_GOOGLE_APPS_SCRIPT_URL';


## Create a Google Sheet.

## Create a Google Apps Script:

1. Go to Google Apps Script and create a new project.
2. Use the following code in your script editor:
 ```javascript
   function doPost(e) {
     var ss = SpreadsheetApp.openById('YOUR_SHEET_ID');
     var sheet = ss.getSheets()[0];
     var data = JSON.parse(e.postData.contents);
     sheet.appendRow([data.fullName, data.username, data.email, data.phone, data.password, data.confirmPassword, data.gender]);
     return ContentService.createTextOutput("Success");
   }
Replace 'YOUR_SHEET_ID' with your actual Google Sheet ID.
Deploy the script as a web app and set it to allow anyone to access it.
3. Replace the scriptURL in the JavaScript:


In the scriptURL variable, replace the URL with your own Google Apps Script URL.
```bash
git clone https://github.com/your-username/registration-form.git
cd registration-form
open index.html
