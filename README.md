<div id="bemu-validator-documentation" class="container">

<div class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

# Documentation for Bemu Validator

</div>

</div>

<div class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

<div class="panel panel-default">

<div class="panel-heading">

<div class="panel-title">[Page contents (click here)](#)</div>

</div>

<div class="panel-collapse collapse in" style="">

<div class="list-group">[isString](#isString)[isNumber](#isNumber)[isBoolean](#isBoolean)[isUrl](#isUrl)[isEmail](#isEmail)[isArray](#isArray)[bundleWithConfig](#bundleWithConfig)[stringValidator](#stringValidator)[numberValidator](#numberValidator)[booleanValidator](#booleanValidator)[urlValidator](#urlValidator)[emailValidator](#emailValidator)[arrayValidator](#arrayValidator)[customValidator](#customValidator)[objectValidator](#objectValidator)</div>

</div>

</div>

</div>

</div>

<div id="isString" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## isString(object [, config])

This method check if the given object is a valid string and checks if it satisfies given config fields

### Config fields

<div class="table-responsive">

<table class="table table-striped table-bordered table-hover">

<thead>

<tr>

<th>Property</th>

<th>Value</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>minLength</td>

<td>number</td>

<td>Checks if the string is longer than the given number.</td>

</tr>

<tr>

<td>maxLength</td>

<td>number</td>

<td>Checks if the string is shorter than the given number.</td>

</tr>

<tr>

<td>reduceSpaces</td>

<td>boolean</td>

<td>Trims the string and reduces multiple space to only one before checking for minLength and maxLength.</td>

</tr>

<tr>

<td>alphaOnly</td>

<td>boolean</td>

<td>Checks if the string is letters only.</td>

</tr>

<tr>

<td>alphanumericOnly</td>

<td>boolean</td>

<td>Checks if the string is letters and numbers only.</td>

</tr>

<tr>

<td>allowedCharacters</td>

<td>object</td>

<td>Object containing the definitions for allowedCharacters.</td>

</tr>

<tr>

<td>allowedCharacters.allowLetters</td>

<td>boolean</td>

<td>If true, letters will be allowed in string. Required in allowedCharacters.</td>

</tr>

<tr>

<td>allowedCharacters.allowNumbers</td>

<td>boolean</td>

<td>If true, numbers will be allowed in string. Required in allowedCharacters.</td>

</tr>

<tr>

<td>allowedCharacters.specialCharacters</td>

<td>array</td>

<td>characters from array will be allowed in the string. NOTE: The array can only contain strings of length 1(single character). Required in allowedCharacters.</td>

</tr>

</tbody>

</table>

</div>

### Example usage

<iframe width="100%" frameborder="0" id="gist-85b6f0836348baf46585e19de39ce35d" style="height: 529px;"></iframe>[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="isNumber" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## isNumber(object [, config])

This method check if the given object is a valid number and checks if it satisfies given config fields

### Config fields

<div class="table-responsive">

<table class="table table-striped table-bordered table-hover">

<thead>

<tr>

<th>Property</th>

<th>Value</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>min</td>

<td>number</td>

<td>Checks if the number is bigger than the given number.</td>

</tr>

<tr>

<td>max</td>

<td>number</td>

<td>Checks if the number is smaller than the given number.</td>

</tr>

<tr>

<td>integer</td>

<td>boolean</td>

<td>Checks if the number is an integer.</td>

</tr>

</tbody>

</table>

</div>

### Example usage

<iframe width="100%" frameborder="0" id="gist-d8046443e0090e0baf0b51720c5b0476" style="height: 294px;"></iframe>[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="isBoolean" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## isBoolean(object)

This method check if the given object is a valid boolean

### Example usage

<iframe width="100%" frameborder="0" id="gist-658363c5744d67b1ab85991d9f8d3d5a" style="height: 150px;"></iframe>[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="isUrl" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## isUrl(object [, config])

This method check if the given object is a valid url and checks if it satisfies given config fields

NOTE: This method may have give some false positives, if you find any please report them at the [GitHub repo](https://github.com/Mustajbasic/bemu-validator/issues) so I can investigate them and fix them asap.

### Config fields

<div class="table-responsive">

<table class="table table-striped table-bordered table-hover">

<thead>

<tr>

<th>Property</th>

<th>Value</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>httpsOnly</td>

<td>boolean</td>

<td>Allows only https urls</td>

</tr>

</tbody>

</table>

</div>

### Example usage

<iframe width="100%" frameborder="0" id="gist-c18f8e5741a3b7e256374ceaab7dc7c1" style="height: 337px;"></iframe>[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="isEmail" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## isEmail(object [, config])

This method check if the given object is a valid email and checks if it satisfies given config fields

### Config fields

<div class="table-responsive">

<table class="table table-striped table-bordered table-hover">

<thead>

<tr>

<th>Property</th>

<th>Value</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>minNameLength</td>

<td>number</td>

<td>Defines the minimum length of the email name (everything before @, not really sure what is the propper name for this)</td>

</tr>

<tr>

<td>maxNameLength</td>

<td>number</td>

<td>Defines the maximum length of the email name (everything before @, not really sure what is the propper name for this)</td>

</tr>

<tr>

<td>domains</td>

<td>array</td>

<td>Defines the allowed domains, eg. ['gmail.com', 'yahoo.com']</td>

</tr>

<tr>

<td>domainNames</td>

<td>array</td>

<td>Defines the allowed domain names but does not care about extension, eg. ['gmail', 'yahoo']</td>

</tr>

<tr>

<td>domainExtensions</td>

<td>array</td>

<td>Defines the allowed domain extensions but does not care about names, eg. ['com', 'io']</td>

</tr>

</tbody>

</table>

</div>

NOTE: Some email domains like 'email.co.uk' may be problematic to use with domainNames and domainExtensions so please for that matter use domains while I work on the fix

### Example usage

<iframe width="100%" frameborder="0" id="gist-eda76ba574c81e345ce408ea0f3c8f58" style="height: 379px;"></iframe>[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="isArray" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## isArray(object [, config])

This method check if the given object is a valid array and checks if it satisfies given config fields

### Config fields

<div class="table-responsive">

<table class="table table-striped table-bordered table-hover">

<thead>

<tr>

<th>Property</th>

<th>Value</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>minLength</td>

<td>number</td>

<td>Defines the minimum amount of elements that the array has to have.</td>

</tr>

<tr>

<td>maxLength</td>

<td>number</td>

<td>Defines the maximum amount of elements that the array can have.</td>

</tr>

<tr>

<td>elementType</td>

<td>function</td>

<td>Function that every element of the array is tested against. The prototype of the function is (object) => boolean. For this you can use any of the built in validation functions like 'isString', 'isNumber' ..., but if you want to add config to the function you have to bundle it with [bundleWithConfig](#bundleWithConfig) function.</td>

</tr>

</tbody>

</table>

</div>

### Example usage

<iframe width="100%" frameborder="0" id="gist-9590c73cfb0b823c4749b6726f8a1c1a" style="height: 358px;"></iframe>[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="bundleWithConfig" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## bundleWithConfig(validator, config)

This method bundles the validation function with config fo enable easy custom validation functions. Also this method is used for passing config to to the 'elementType' config property of [isArray](#isArray) method.

### Example usage

<iframe width="100%" frameborder="0" id="gist-0b863803327ad19474b9bddcd30c4360" style="height: 443px;"></iframe>[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="stringValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## stringValidator(isRequired [, config])

Creates a string validator object which is used in [objectValidator](#objectValidator)

The 'isRequired' argument is a boolean and indicates if the field is required. The config object is the same as the from [isString](#isString) method

### Example usage

The example uage is provided in the [Example usage](#objectValidatorExample) of objectValidator

[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="numberValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## numberValidator(isRequired [, config])

Creates a number validator object which is used in [objectValidator](#objectValidator)

The 'isRequired' argument is a boolean and indicates if the field is required. The config object is the same as the from [isNumber](#isNumber) method

### Example usage

The example uage is provided in the [Example usage](#objectValidatorExample) of objectValidator

[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="booleanValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## booleanValidator(isRequired [, config])

Creates a boolean validator object which is used in [objectValidator](#objectValidator)

The 'isRequired' argument is a boolean and indicates if the field is required. The config object is the same as the from [isBoolean](#isBoolean) method

### Example usage

The example uage is provided in the [Example usage](#objectValidatorExample) of objectValidator

[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="urlValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## urlValidator(isRequired [, config])

Creates a url validator object which is used in [objectValidator](#objectValidator)

¸

The 'isRequired' argument is a boolean and indicates if the field is required. The config object is the same as the from [isUrl](#isUrl) method

### Example usage

The example uage is provided in the [Example usage](#objectValidatorExample) of objectValidator

[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="emailValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## emailValidator(isRequired [, config])

Creates a email validator object which is used in [objectValidator](#objectValidator)

The 'isRequired' argument is a boolean and indicates if the field is required. The config object is the same as the from [isEmail](#isEmail) method

### Example usage

The example uage is provided in the [Example usage](#objectValidatorExample) of objectValidator

[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="arrayValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## arrayValidator(isRequired [, config])

Creates a array validator object which is used in [objectValidator](#objectValidator)

The 'isRequired' argument is a boolean and indicates if the field is required. The config object is the same as the from [isArray](#isArray) method

### Example usage

The example uage is provided in the [Example usage](#objectValidatorExample) of objectValidator

[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="customValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## customValidator(isRequired, isValid [, config])

The 'isRequired' argument is a boolean and indicates if the field is required.

In case you need a custom validator, create a function that takes one object (and config if you desire), and returns true or false. Pass the function as the 'isValid' argument and add any aditional config.

### Example usage

The example uage is provided in the [Example usage](#objectValidatorExample) of objectValidator

[Return to top](#bemu-validator-documentation)</div>

</div>

<div id="objectValidator" class="row">

<div class="col-lg-8 col-lg-offset-2 col-md-8 col-md-offset-2 col-sm-10 col-sm-offset-1">

## objectValidator(properties)

This method allows you to crreate a validation function for any kind of object. The 'properties' argument is an object which is a reflection of the object we want to test. This means that propery names of the object are the same as in the object we want to test but the values are validators (stringValidator, numberValidator, booleanValidator, urlValidator, emailValidator, arrayValidator and customValidator).

### Example usage

In this first example we create an object validator and test an object against it

<iframe width="100%" frameborder="0" id="gist-f7bc36e4cac7bdbee3068479cc2d127e" style="height: 827px;"></iframe>

If a fied is not required we simply set the isRequired flag to false as seen in this simple example

<iframe width="100%" frameborder="0" id="gist-baf04173743233da9f4a966e3d72984f" style="height: 379px;"></iframe>

We can create more complex validators like in the following example. Lets combine isBook and isPerson from the last two examples.

<iframe width="100%" frameborder="0" id="gist-1c33f16e45bfa0a2cf23224beb6e1758" style="height: 955px;"></iframe></div>

</div>

</div>
