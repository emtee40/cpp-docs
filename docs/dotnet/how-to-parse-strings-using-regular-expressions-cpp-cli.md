---
title: "How to: Parse Strings Using Regular Expressions (C++/CLI) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-cli"]
ms.topic: "conceptual"
dev_langs: ["C++"]
helpviewer_keywords: ["parsing strings [C++]", "examples [C++], strings", "regular expressions [C++], parsing strings", "strings [C++], parsing"]
ms.assetid: 5b0c7ca3-9bba-4389-a45c-6d373cff91b0
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "dotnet"]
---
# How to: Parse Strings Using Regular Expressions (C++/CLI)
The following code example demonstrates simple string parsing using the <xref:System.Text.RegularExpressions.Regex> class in the <xref:System.Text.RegularExpressions?displayProperty=fullName> namespace. A string containing multiple types of word delineators is constructed. The string is then parsed using the <xref:System.Text.RegularExpressions.Regex> class in conjunction with the <xref:System.Text.RegularExpressions.Match> class. Then, each word in the sentence is displayed separately.  
  
## Example  
  
```  
// regex_parse.cpp  
// compile with: /clr  
#using <system.dll>  
  
using namespace System;  
using namespace System::Text::RegularExpressions;  
  
int main( )  
{  
   int words = 0;  
   String^ pattern = "[a-zA-Z]*";  
   Console::WriteLine( "pattern : '{0}'", pattern );  
   Regex^ regex = gcnew Regex( pattern );  
  
   String^ line = "one\ttwo three:four,five six  seven";     
   Console::WriteLine( "text : '{0}'", line );  
   for( Match^ match = regex->Match( line );   
        match->Success; match = match->NextMatch( ) )   
   {  
      if( match->Value->Length > 0 )  
      {  
         words++;  
         Console::WriteLine( "{0}", match->Value );  
      }  
   }  
   Console::WriteLine( "Number of Words : {0}", words );  
  
   return 0;  
}  
```  
  
## See Also  
 [.NET Framework Regular Expressions](/dotnet/standard/base-types/regular-expressions)   
 [.NET Programming with C++/CLI (Visual C++)](../dotnet/dotnet-programming-with-cpp-cli-visual-cpp.md)