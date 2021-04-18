---
description: Un uso standard di una firma consiste nel firmare un testo e salvare il testo firmato in un file. Il testo firmato potrebbe anche essere inviato tramite Internet. Il messaggio firmato è in \# formato PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Firma di un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305589"
---
# <a name="signing-a-document"></a><span data-ttu-id="893df-105">Firma di un documento</span><span class="sxs-lookup"><span data-stu-id="893df-105">Signing a Document</span></span>

<span data-ttu-id="893df-106">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="893df-106">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="893df-107">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="893df-107">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="893df-108">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="893df-108">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="893df-109">Un uso standard di una firma consiste nel firmare un testo e salvare il testo firmato in un file.</span><span class="sxs-lookup"><span data-stu-id="893df-109">A standard use of a signature is to sign a text and save that signed text to a file.</span></span> <span data-ttu-id="893df-110">Il testo firmato potrebbe anche essere inviato tramite Internet.</span><span class="sxs-lookup"><span data-stu-id="893df-110">The signed text could also be sent over the Internet.</span></span> <span data-ttu-id="893df-111">Il messaggio firmato è in \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="893df-111">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="893df-112">In questo esempio, la firma viene creata per il contenuto scollegato (quando il contenuto non è incluso nella firma).</span><span class="sxs-lookup"><span data-stu-id="893df-112">In this example, the signature is created for detached content (when the content is not included with the signature).</span></span> <span data-ttu-id="893df-113">Una firma scollegata verrebbe spesso utilizzata se il destinatario della firma ha una copia del testo firmato esatto.</span><span class="sxs-lookup"><span data-stu-id="893df-113">A detached signature would most often be used if the recipient of the signature has a copy of the exact signed text.</span></span> <span data-ttu-id="893df-114">Nell'esempio seguente il messaggio originale e la firma scollegata vengono scritti in file distinti.</span><span class="sxs-lookup"><span data-stu-id="893df-114">In the example below, the original message and the detached signature are written to separate files.</span></span>

<span data-ttu-id="893df-115">In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="893df-115">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="893df-116">Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="893df-116">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="893df-117">Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="893df-117">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="893df-118">La creazione di una firma usa la [*chiave privata*](../secgloss/p-gly.md)del firmatario.</span><span class="sxs-lookup"><span data-stu-id="893df-118">Creating a signature uses the signer's [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="893df-119">È possibile creare una firma solo se è disponibile il certificato del firmatario con una chiave privata associata.</span><span class="sxs-lookup"><span data-stu-id="893df-119">A signature can only be created if the signer's certificate with an associated private key is available.</span></span> <span data-ttu-id="893df-120">Questo esempio di metodo **Sign** non specifica un firmatario.</span><span class="sxs-lookup"><span data-stu-id="893df-120">This example of the **Sign** method does not specify a signer.</span></span> <span data-ttu-id="893df-121">Se non si specifica un firmatario e nessun certificato nell' **\_ \_ archivio personale** ha una chiave privata associata, il metodo **Sign** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="893df-121">If a signer is not specified and no certificate in **CAPICOM\_MY\_STORE** has an associated private key, the **Sign** method fails.</span></span> <span data-ttu-id="893df-122">Se un solo certificato in **CApicol \_ My \_ Store** ha una chiave privata associata, il certificato e la relativa chiave privata vengono usati per creare la firma.</span><span class="sxs-lookup"><span data-stu-id="893df-122">If one and only one certificate in **CAPICOM\_MY\_STORE** has an associated private key, that certificate and its private key is used to create the signature.</span></span> <span data-ttu-id="893df-123">Se a più di un certificato nell'archivio del **\_ \_ negozio personale** è associata una chiave privata, viene visualizzata una finestra di dialogo in cui l'utente può scegliere il certificato da usare per creare la firma.</span><span class="sxs-lookup"><span data-stu-id="893df-123">If more than one certificate in the **CAPICOM\_MY\_STORE** store has an associated private key, a dialog box appears and the user can choose the certificate to be used to create the signature.</span></span>

<span data-ttu-id="893df-124">Quando un'applicazione basata sul Web usa il metodo **Sign** , viene sempre visualizzata una richiesta e l'autorizzazione dell'utente è richiesta prima che venga creata una firma che usa la chiave privata del firmatario.</span><span class="sxs-lookup"><span data-stu-id="893df-124">When a web-based application uses the **Sign** method, a prompt is always displayed and the user's permission is required before a signature that uses that signer's private key is created.</span></span>


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="893df-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="893df-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="893df-126">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="893df-126">**Store.Open**</span></span>](store-open.md)
</dt> <dt>

[<span data-ttu-id="893df-127">**Firmatario. Certificate**</span><span class="sxs-lookup"><span data-stu-id="893df-127">**Signer.Certificate**</span></span>](signer-certificate.md)
</dt> <dt>

[<span data-ttu-id="893df-128">**Attributo**</span><span class="sxs-lookup"><span data-stu-id="893df-128">**Attribute**</span></span>](attribute.md)
</dt> <dt>

[<span data-ttu-id="893df-129">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="893df-129">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
