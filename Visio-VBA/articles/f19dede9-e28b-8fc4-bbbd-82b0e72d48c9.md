
# Document.HeaderLeft Property (Visio)

Gets or sets the text string that appears in the left portion of a document's header. Read/write.


## Syntax

 _expression_ . **HeaderLeft**

 _expression_ A variable that represents a **Document** object.


### Return Value

String


## Remarks

You can also set this value in the  **Left** box under **Header** in the **Header and Footer** dialog box (click the **File** tab, click **Print**, click  **Print Preview**, and then in the  **Preview** group, click **Header &amp; Footer**).

Both the string that  **HeaderLeft** returns and the string to which you set it can contain escape codes that represent data. These escape codes can be concatenated with other text. For a list of valid escape codes you can use with the **HeaderLeft** property, see the **[FooterLeft](e832c09d-3ddb-4351-43ad-e1c5633b7bc9.md)** property


## Example

The following macro shows how to place a string containing the current date into the left portion of a document's header. After you run this macro, if the date is October 1, 2009, the left portion of the header contains "The date is Thursday, October 1, 2009".


```vb
 
Sub HeaderLeft_Example() 
  
    Dim strHeader as String 
 
    'Build header string. 
    strHeader = "The date is " &amp; "&amp;D"  
 
    'Set header of the current document. 
    ThisDocument.HeaderLeft = strHeader  
 
End Sub 

```

