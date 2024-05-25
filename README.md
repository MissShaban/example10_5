# example10_5
public class Example5_10 { 
public static void main(String[] args) 
{
String str = "Hello ali";   
int width = 15;   
String s = stringFormatter.leftAdjust
(str, width);     
System.out.println("Left justify string is: " + s);
s = stringFormatter.rightAdjust (str, width);     
System.out.println("Right justify string is: " + s);    
s = stringFormatter.center(str, width);
  System.out.println("Middle justify string is: " + s);
}
}

2_stringFormatter.java :

public class stringFormatter 
{ 
   // Pad out s with spaces after it. public static String leftAdjust (String s, int width) 
   {   
  final int stringlength =s.length();    if (stringlength >= width) 
 {    
 // This covers the case when width is negative, too. return s; 
 }    
 else return spaces (width-stringLength).insert (0, s).toString();
 } 
 // Pad out s with spaces before it. public static String rightAdjust (String s, int width)
 { 
 final int stringLength = s.length();  
 if (stringlength >= width) 
 {
 // This covers the case when width is negative, too. return s;
}
else return spaces (width-stringLlength).append(s).toString();
}
//*********************
public static String center(String s, int width) 
{
final int stringlength = s.length();
if(stringLength >= width) 
{ 
  // This covers the case when width is negative, too. return s;
}    
else
{  
final int numSpaces = width-stringLength;    
final int leftSpace = numSpaces / 2,        rightSpace = numSpaces-leftSpace; return spaces (leftSpace).append(s). append(spaces(rightSpace)).toString(); } 
} 
// Return a StringBuffer full of spaces.
private static StringBuffer spaces (int numSpaces) 
{ 
if (numSpaces <= 0)
return new StringBuffer();   
else 
{ 
StringBuffer spaces = new StringBuffer(); 
for (int i = 0;
i < numSpaces; i++) 
spaces.append(' '); 
return spaces;
}
}
}
