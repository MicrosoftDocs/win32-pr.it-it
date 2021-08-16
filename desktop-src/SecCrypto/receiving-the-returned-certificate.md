---
description: Viene illustrato come un'applicazione riceve un certificato.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Ricezione del certificato restituito
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb2efe504e2d09b3fae2b6d6293772bf67a3f038a5f9c43330707f541e2ba8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900967"
---
# <a name="receiving-the-returned-certificate"></a>Ricezione del certificato restituito

Quando l'autorità di certificazione (CA) ha verificato le informazioni di identità del richiedente ed è soddisfatto che il richiedente sia il proprietario della chiave privata e che i dati relativi a tale richiedente siano accurati, l'autorità di certificazione costruisce un certificato X.509, lo firma, lo include in un messaggio con qualsiasi altro certificato necessario, ad esempio il certificato della CA,  e invia il messaggio al richiedente. Il messaggio può essere un messaggio PKCS 7 o una risposta \# CMC (i modelli V2 comportano una risposta CMC).

L'applicazione ricevente passa il messaggio al controllo di registrazione certificati. Il controllo registrazione certificati apre quindi il messaggio ed estrae i certificati. All'utente viene visualizzata una finestra di dialogo in cui viene chiesto se l'utente accetterà i certificati autofirmati nell'archivio "Radice". Se l'utente accetta il certificato radice, il resto dei certificati (ad eccezione del certificato del richiedente) viene inserito nell'archivio "CA". Il certificato del richiedente viene inserito nell'archivio certificati specificato dal richiedente nella [**proprietà MyStoreName.**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename)

Nell'esempio seguente viene illustrato come usare Visual Basic Scripting Edition (VBScript) e HTML in una pagina Web per ricevere e archiviare i certificati restituiti.


```VB
<HTML>
<TITLE>Certificate Enrollment Acceptance HTML Page
</TITLE>

<OBJECT  classid="clsid:127698E4-E730-4E5C-A2b1-21490A70C8A1"
    CODEBASE="xenroll.dll"
    id=IControl >
</OBJECT>

<SCRIPT language="VBScript">

<!--

Option Explicit 

'Accept the certificate subroutine.

Sub AcceptCertSub

On Error Resume Next

' Get the issued certificate.
' The following value, "PKCS7", represents the received message. 
' Actually, this value must be supplied through the design of
' the receiving application.
' A possible implementation is as follows: after using 
' ICertRequest.Submit to submit the PKCS #10, call 
' ICertRequest.GetLastStatus to confirm successful certificate 
' creation, and then call ICertRequest.GetCertificate to retrieve 
' the certificate.

document.result.result.value = "PKCS7"

    Call IControl.AcceptPKCS7(document.result.result.value)

    If err.Number = 0 Then
        navigate "..\done.htm"
    Else
        Alert "Error: " & Hex(err)
    End If

    End sub

    ' Decline the certificate sub-routine.
    Sub NoAcceptCertSub
    navigate "..\notdone.htm"
    End sub
-->
</SCRIPT>
</BODY>
</HTML>
```



 

 
