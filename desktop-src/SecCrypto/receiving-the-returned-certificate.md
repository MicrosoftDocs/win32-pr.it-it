---
description: Viene illustrato il modo in cui un'applicazione riceve un certificato.
ms.assetid: 7f87dcf5-b434-4f63-abcd-6873831d22bc
title: Ricezione del certificato restituito
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73853250c581e460360f5490defc0c94e76e5be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317702"
---
# <a name="receiving-the-returned-certificate"></a><span data-ttu-id="5a491-103">Ricezione del certificato restituito</span><span class="sxs-lookup"><span data-stu-id="5a491-103">Receiving the Returned Certificate</span></span>

<span data-ttu-id="5a491-104">Quando l'autorità di certificazione (CA) ha verificato le informazioni di identità del richiedente e ha soddisfatto che il richiedente è il proprietario della chiave privata e che i dati sul richiedente sono accurati, la CA costruisce un certificato X. 509, lo firma, lo crea un pacchetto con tutti gli altri certificati necessari, ad esempio il certificato della CA, in un messaggio e invia il messaggio al richiedente.</span><span class="sxs-lookup"><span data-stu-id="5a491-104">When the certification authority (CA) has verified the requester's identity information and is satisfied that the requester is the owner of the private key and that the data about that requester is accurate, the CA constructs an X.509 certificate, signs it, packages it with any other needed certificates (such as the CA's own certificate) in a message, and sends the message to the requester.</span></span> <span data-ttu-id="5a491-105">Il messaggio può essere un \# messaggio PKCS 7 o una risposta CMC (i modelli v2 generano una risposta CMC).</span><span class="sxs-lookup"><span data-stu-id="5a491-105">The message can be a PKCS \#7 message or a CMC response (V2 templates result in a CMC response).</span></span>

<span data-ttu-id="5a491-106">L'applicazione ricevente passa il messaggio al controllo di registrazione certificati.</span><span class="sxs-lookup"><span data-stu-id="5a491-106">The receiving application passes the message to the Certificate Enrollment Control.</span></span> <span data-ttu-id="5a491-107">Il controllo registrazione certificati apre quindi il messaggio ed estrae i certificati.</span><span class="sxs-lookup"><span data-stu-id="5a491-107">The Certificate Enrollment Control then opens the message and extracts the certificates.</span></span> <span data-ttu-id="5a491-108">All'utente viene visualizzata una finestra di dialogo in cui viene chiesto se l'utente accetterà i certificati autofirmati nell'archivio "root".</span><span class="sxs-lookup"><span data-stu-id="5a491-108">The user is prompted with a dialog box asking whether the user will accept self-signed certificates in the "Root" store.</span></span> <span data-ttu-id="5a491-109">Se l'utente accetta il certificato radice, il resto dei certificati (ad eccezione del certificato del richiedente) viene inserito nell'archivio "CA".</span><span class="sxs-lookup"><span data-stu-id="5a491-109">If the user accepts the root certificate, the rest of the certificates (except for the requester's certificate) are placed in the "CA" store.</span></span> <span data-ttu-id="5a491-110">Il certificato del richiedente viene inserito nell'archivio certificati specificato dal richiedente [**nella proprietà.**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename)</span><span class="sxs-lookup"><span data-stu-id="5a491-110">The requester's certificate is placed in the certificate store specified by the requester in the [**MyStoreName**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) property.</span></span>

<span data-ttu-id="5a491-111">Nell'esempio seguente viene illustrato come utilizzare le Visual Basic Scripting Edition (VBScript) e HTML in una pagina Web per ricevere e archiviare i certificati restituiti.</span><span class="sxs-lookup"><span data-stu-id="5a491-111">The following example shows how to use the Visual Basic Scripting Edition (VBScript) and HTML in a webpage to receive and store the returned certificates.</span></span>


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



 

 
