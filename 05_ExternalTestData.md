# How to use a data file with WebdriverIO

When automating test cases with WebdriverIO you want to make them flexible to having different data used to run the test cases. So, you do not want to hard code data into the test script.  Otherwise, you will have to change the input values of the test cases each time you are provided a new set of test data. Instead, you want to reference an external data file.  So we will cover the different ways you can store data in an external data file and access it from your WebdriverIO test suite.

## Data files for Webdriver
There are different way to store data in a file. You can can [export](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export) a class, use [csv](https://makitweb.com/how-to-read-csv-file-and-display-its-content-using-javascript/) files, and even use [Excel files](https://www.youtube.com/watch?v=JB2jkeyDEQM). We will focus on exporting a class and organizing the test data inputs by conditions. 

Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JavaScript are built on prototypes but also have some syntax and semantics that are unique to classes. When you create a [class](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_classes) you give it the structure you need for your data. Therefore if you want an array with all the values you can do the following:

```
export class testData
{
static testCase1 = [
    "Michael",
    "Myers",
    "mmyers@gmail.com",
    "SuperSecretPassword!",
    "SuperSecretPassword!",
    "Dunbar Ave.",
    "Suite 200",
    "UNITED STATES",
    "San Bernadino",
    "California",
    "92210",
    "858-567-1234"
]
}
```
If you want an an object with key values:

```
export class testData
{
  static testCase1 = {
    firstName: "Michael",
    lastName: "Myers",
    email: "mmyers@gmail.com",
    password: "SuperSecretPassword!",
    confirmpassword: "SuperSecretPassword!",
    streetAddress: "Dunbar Ave.",
    apt: "Suite 200",
    country: "UNITED STATES",
    city: "San Bernadino",
    state: "California",
    zipCode: "92210",
    phone: "858-567-1234",
}

```
How you set up your test data will 
