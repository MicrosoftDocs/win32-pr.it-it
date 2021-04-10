---
description: Esempio di Visual Basic Scripting Edition (VBScript) che usa il tag OBJECT per creare un'istanza dell'oggetto controllo di registrazione certificati.
ms.assetid: 6e2a230e-81c1-4b63-9ad5-3edfc239ad7c
title: Controllo di registrazione del certificato di cui è stata creata un'istanza in VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da14c55a3c9005f820be8f8d60026bc31ac4920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966747"
---
# <a name="the-certificate-enrollment-control-instantiated-in-vbscript"></a>Controllo di registrazione del certificato di cui è stata creata un'istanza in VBScript

Nell'esempio seguente Visual Basic Scripting Edition (VBScript) viene utilizzato il tag OBJECT per creare un'istanza dell'oggetto controllo di registrazione certificati. L'oggetto viene liberato dalla memoria quando esce dall'ambito.


```VB
<HTML>
<HEAD>
<TITLE>VBScript Certificate Enrollment Control Sample
</TITLE>
<OBJECT classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    codebase="xenroll.dll"
    id=Enroll >
</OBJECT>
<BR>
Certificate Enrollment Control Instantiation Sample
<BR>
<BR>

<SCRIPT language="VBScript">
<!--
' Declare a local variable.
Dim varName
' Enable error handling.
On Error Resume Next
' Attempt to use the control, in this case to retrieve a property.
varName = Enroll.MyStoreName
' If above line failed, Err.Number will not be 0.
if ( Err.Number <> 0 ) then
    MsgBox("Error!")
    Err.clear
else
    ' The control property was successfully retrieved,
    ' display the property value.
    varName = "MyStoreName is " & varName
    MsgBox( varName )
end if
-->
</SCRIPT>
<BR>
</HEAD>
</HTML>
```



 

 



