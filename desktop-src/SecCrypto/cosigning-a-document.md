---
description: Un documento può essere firmato da più di un firmatario.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cofirma di un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321031"
---
# <a name="cosigning-a-document"></a><span data-ttu-id="74de2-103">Cofirma di un documento</span><span class="sxs-lookup"><span data-stu-id="74de2-103">Cosigning a Document</span></span>

<span data-ttu-id="74de2-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="74de2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="74de2-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="74de2-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="74de2-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="74de2-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="74de2-107">Un documento può essere firmato da più di un firmatario.</span><span class="sxs-lookup"><span data-stu-id="74de2-107">A document can be signed by more than one signer.</span></span> <span data-ttu-id="74de2-108">Questo errore si verifica quando, ad esempio, due o più entità firmano un contratto o una nota spese.</span><span class="sxs-lookup"><span data-stu-id="74de2-108">This happens when, for instance, two or more parties sign a contract or an expense report.</span></span> <span data-ttu-id="74de2-109">Nell'esempio seguente un documento già firmato viene ricevuto da un secondo firmatario.</span><span class="sxs-lookup"><span data-stu-id="74de2-109">In the following example, a document already signed is received by a second signer.</span></span> <span data-ttu-id="74de2-110">Questo firmatario usa il metodo [**cosign**](signeddata-cosign.md) per alleghi una firma aggiuntiva al documento.</span><span class="sxs-lookup"><span data-stu-id="74de2-110">This signer uses the [**CoSign**](signeddata-cosign.md) method to attach an additional signature to the document.</span></span>

<span data-ttu-id="74de2-111">Se si verifica un errore di capicol, nella proprietà **Err. Number** viene restituito un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="74de2-111">If any CAPICOM error occurs, a negative value is returned in the **Err.Number** property.</span></span> <span data-ttu-id="74de2-112">Per ulteriori informazioni sui codici di errore di capicol, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="74de2-112">For more information about CAPICOM error codes, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="74de2-113">Se il codice di errore nella proprietà **Err. Number** è un valore positivo, l'errore è un errore di Windows.</span><span class="sxs-lookup"><span data-stu-id="74de2-113">If the error code in the **Err.Number** property is a positive value, then the error is a Windows error.</span></span> <span data-ttu-id="74de2-114">Per informazioni sui codici di errore di Windows, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="74de2-114">For information about Windows error codes, see Winerror.h.</span></span>

> [!Note]
> <span data-ttu-id="74de2-115">La firma di un documento richiede anche che il cofirmatario disponga di un [*certificato*](../secgloss/c-gly.md) disponibile con una [*chiave privata*](../secgloss/p-gly.md) per creare la firma.</span><span class="sxs-lookup"><span data-stu-id="74de2-115">Cosigning a document also requires that the cosigner have an available [*certificate*](../secgloss/c-gly.md) with a [*private key*](../secgloss/p-gly.md) to create the signature.</span></span> <span data-ttu-id="74de2-116">Se un firmatario non viene specificato nella chiamata al metodo [**Sign**](signeddata-sign.md) e non è presente alcun certificato in CAPICOM \_ My \_ Store con una chiave privata associata, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="74de2-116">If a signer is not specified in the call of the [**Sign**](signeddata-sign.md) method and there is no certificate in CAPICOM\_MY\_STORE with an associated private key, the method fails.</span></span> <span data-ttu-id="74de2-117">Se è presente un solo certificato in CAPICOM \_ My \_ Store con una chiave privata associata, vengono usati la chiave e il certificato.</span><span class="sxs-lookup"><span data-stu-id="74de2-117">If there is one and only one certificate in CAPICOM\_MY\_STORE with an associated private key, that key and certificate are used.</span></span> <span data-ttu-id="74de2-118">Se è presente più di un certificato utilizzabile, viene visualizzato un messaggio di richiesta per consentire all'utente di scegliere il certificato desiderato.</span><span class="sxs-lookup"><span data-stu-id="74de2-118">If there is more than one usable certificate, a prompt is displayed to allow the user to choose the desired certificate.</span></span>
> 
> <span data-ttu-id="74de2-119">Se il metodo [**cosign**](signeddata-cosign.md) viene usato in un'applicazione basata sul Web, viene sempre visualizzata una richiesta per ottenere l'autorizzazione dell'utente prima che venga creata una firma usando la chiave privata del firmatario.</span><span class="sxs-lookup"><span data-stu-id="74de2-119">If the [**CoSign**](signeddata-cosign.md) method is used in a web-based application, a prompt is always displayed to get the user's permission before a signature is created by using that signer's private key.</span></span>

 

<span data-ttu-id="74de2-120">Nell'esempio seguente vengono letti i file che contengono il documento da firmare e le firme correnti del documento, la firma è cofirmata e la nuova firma viene scritta in un file.</span><span class="sxs-lookup"><span data-stu-id="74de2-120">In the following example, files that contain the document to be signed and the current signatures on that document are read, the signature is cosigned, and the new signature is written to a file.</span></span> <span data-ttu-id="74de2-121">Nell'esempio viene utilizzata una firma scollegata con i dati firmati e la firma in file distinti.</span><span class="sxs-lookup"><span data-stu-id="74de2-121">The example uses a detached signature with the data signed and the signature in separate files.</span></span>


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
