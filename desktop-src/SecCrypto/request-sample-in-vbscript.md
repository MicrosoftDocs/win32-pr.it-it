---
description: Il codice di esempio VBScript seguente mostra come è possibile usare il controllo di registrazione certificati con l'oggetto CCertRequest per creare e inviare una richiesta di certificato.
ms.assetid: be1bc66a-7bc5-4369-9344-168af53fdfb9
title: Esempio di richiesta in VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 12e14507f0bb27e7bc8caba605158a70f5e08ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318232"
---
# <a name="request-sample-in-vbscript"></a>Esempio di richiesta in VBScript

Il codice di esempio VBScript seguente mostra come è possibile usare il controllo di registrazione certificati con l'oggetto CCertRequest per creare e inviare una [*richiesta di certificato*](../secgloss/c-gly.md).


```VB
<HTML>
<HEAD>
<TITLE>VBScript Certificate Enrollment Control Sample
</TITLE>
<OBJECT classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    codebase="xenroll.dll"
    id=Enroll >
</OBJECT>
<OBJECT classid="clsid:98AFF3F0-5524-11D0-8812-00A0C903B83C"
    codebase="certcli.dll"
    id=Request >
</OBJECT>
<BR>
Certificate Enrollment Control Request Sample
<BR>
<BR>

<SCRIPT language="VBScript">
<!--
' Declare the distinguished name variable.
Dim strDN

' Declare the request variable.
Dim strReq

' Declare a local variable for request disposition.
Dim nDisp

' Enable error handling.
On Error Resume Next

' Declare constants used by CertRequest object.
const CR_IN_BASE64 = &H1
const CR_IN_PKCS10 = &H100

' Build the DN.
strDN =  "CN=UserName" _
      & ",OU=UserUnit" _
      & ",O=UserOrg" _
      & ",L=UserCity" _
      & ",S=WA" _
      & ",C=US"

' Attempt to use the control, in this case, to create a PKCS #10.
MsgBox("Creating PKCS #10 " & strDN)
strReq = Enroll.createPKCS10( strDN, "1.3.6.1.4.1.311.2.1.21")
' If above line failed, Err.Number will not be 0.
if ( Err.Number <> 0 ) then
    MsgBox("Error in call to createPKCS10 " & Err.Number)
    err.clear
else
    MsgBox("Submitting request " & strReq)
    nDisp = Request.Submit( CR_IN_BASE64 OR CR_IN_PKCS10, _
                            strReq, _
                            "", _
                            "Machine\CertAuth")
    ' If the preceding line failed, Err.Number will not be 0.
    if ( Err.Number <> 0 ) then
        MsgBox("Error in Request Submit " & Err.Number)
        err.clear
    else
        MsgBox("Submitted certificate; disposition = " & nDisp)
    end if

end if
-->
</SCRIPT>
<BR>
</HEAD>
</HTML>
```



 

 
