##UI
**Modal**  
A modal view prevents interaction with any other UI until it is dismissed.
A modal view controller is simply a UIViewController class that is presented modally. When the view controller is presented modally it covers whatever the existing view was (using an animation if specified) and the user most somehow dismiss this view before they can return to what they were doing.
To present a view controller in a modal fashion, you can use the method:
```Objective-C
- (void)presentModalViewController:(UIViewController *)modalViewController animated:(BOOL)animated;
```


##Other

**Numbers, Formatting, Conversions**  
http://stackoverflow.com/questions/2573611/converting-nsdecimalnumber-to-nsstring  
http://stackoverflow.com/questions/2985170/format-string-integer-with-leading-zeros  
http://stackoverflow.com/questions/4793181/how-to-increment-a-nsnumber  
http://stackoverflow.com/questions/4358987/objective-c-convert-number-to-nsnumber  

**Strings**  
http://stackoverflow.com/questions/1612337/objective-c-best-way-to-extract-substring-from-nsstring

**Checking if a string is numeric or not**  
http://stackoverflow.com/questions/11588571/ios-how-do-i-check-if-a-string-is-numeric-or-not  
http://stackoverflow.com/questions/1320295/check-that-a-input-to-uitextfield-is-numeric-only  
http://stackoverflow.com/questions/6091414/finding-out-whether-a-string-is-numeric-or-not  
```Objective-c
NSScanner *scanner = [NSScanner scannerWithString:testString];
BOOL isNumeric = [scanner scanInteger:NULL] && [scanner isAtEnd];
```
```Objective-c
NSCharacterSet* notDigits = [[NSCharacterSet decimalDigitCharacterSet] invertedSet];
if ([newString rangeOfCharacterFromSet:notDigits].location == NSNotFound)
{
    // newString consists only of the digits 0 through 9
}
```
```Objective-c
BOOL valid;
NSCharacterSet *alphaNums = [NSCharacterSet decimalDigitCharacterSet];
NSCharacterSet *inStringSet = [NSCharacterSet characterSetWithCharactersInString:myInputField.text];
valid = [alphaNums isSupersetOfSet:inStringSet];    
if (!valid) // Not numeric
```


**Declaring constants**  
Integer? Just add like this -  
```objective-c
#define var_name 2
```
String? Declare as static constants -
```objective-c
static NSString* const var_name @"String";
```
http://stackoverflow.com/questions/1937685/static-nsstring-usage-vs-inline-nsstring-constants  
http://stackoverflow.com/questions/2092005/when-to-use-static-string-vs-define  
http://stackoverflow.com/questions/18283988/ios-define-or-static-const-for-global-strings  

