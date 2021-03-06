---
title: "Accelerator Modifier Property | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-windows"]
ms.topic: "conceptual"
dev_langs: ["C++"]
helpviewer_keywords: ["Modifier property"]
ms.assetid: f05a9379-e037-4cfb-b6ef-d2c655bcfa7f
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "uwp"]
---
# Accelerator Modifier Property
The following are legal entries for the Modifier property in the accelerator table.  
  
|Value|Description|  
|-----------|-----------------|  
|**None**|User presses only the Key value. This is most effectively used with the ASCII/ANSI values 001 through 026, which is interpreted as ^A through ^Z (CTRL-A through CTRL-Z).|  
|**Alt**|User must press the ALT key before the Key value.|  
|**Ctrl**|User must press the CTRL key before the Key value. Not valid with ASCII Type.|  
|**Shift**|User must press the SHIFT key before the Key value.|  
|**Ctrl+Alt**|User must press the CTRL key and the ALT key before the Key value. Not valid with ASCII Type.|  
|**Ctrl+Shift**|User must press the CTRL key and the SHIFT key before the Key value. Not valid with ASCII Type.|  
|**Alt+Shift**|User must press the ALT key and the SHIFT key before the Key value. Not valid with ASCII Type.|  
|**Ctrl+Alt+Shift**|User must press CTRL, ALT, and SHIFT before the Key value. Not valid with ASCII Type.|  
  
## Requirements  
 Win32  
  
## See Also  
 [Setting Accelerator Properties](../windows/setting-accelerator-properties.md)   
 [Accelerator Editor](../windows/accelerator-editor.md)