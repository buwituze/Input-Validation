# validations_app

A Flutter project that includes inputs validation.

# How to Use
## Application Setup

- Clone the repository
- Ensure you have Flutter installed on your system
- Run flutter pub get to install dependencies
- Run the app using flutter run or simply click the run button in android studio

## Application Flow

#### Starting the App

- Launch the app to see the welcome screen
- Click "Go to from" to proceed to the input form

#### Form Input Fields

The form contains four input fields:

- Name
- Address
- Email
- Phone Number

## Input Validation Rules
Name Validation:

dartCopy// Must start with capital letter and contain only letters and spaces
RegExp(r'^[A-Z][a-zA-Z\s]*$')

- Must start with a capital letter
- Can only contain letters and spaces
- No special characters allowed
- Minimum length of 2 characters

Email Validation:

dartCopy// Basic email format validation
RegExp(r'^[a-zA-Z0-9.]+@[a-zA-Z0-9]+\.[a-zA-Z]+')

- Must contain @ symbol
- Must have valid domain format
- Cannot be empty

Phone Number Validation (Follows Rwandan numbers):

dartCopy// Kenyan phone number format
RegExp(r'^07[2389]\d{7}$')

- Must be exactly 10 digits
- Must start with '07'
- Third digit must be 2, 3, 8, or 9



Address Field:

- Optional field with no validation

Form Submission

- All required fields must pass validation
- Form shows error messages for invalid inputs
- Successful submission:
  - Shows green success message
  - Automatically clears all fields
  - Resets form state after successful submission