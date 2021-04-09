---
description: Quando viene ricevuto un documento firmato, è possibile verificare la validità della firma o delle firme.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Verifica della firma in un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882094"
---
# <a name="verifying-the-signature-on-a-document"></a><span data-ttu-id="c96d8-103">Verifica della firma in un documento</span><span class="sxs-lookup"><span data-stu-id="c96d8-103">Verifying the Signature on a Document</span></span>

<span data-ttu-id="c96d8-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c96d8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c96d8-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c96d8-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="c96d8-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="c96d8-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="c96d8-107">Quando viene ricevuto un documento firmato, è possibile verificare la validità della firma o delle firme.</span><span class="sxs-lookup"><span data-stu-id="c96d8-107">When a signed document is received, the validity of the signature or signatures can be checked.</span></span> <span data-ttu-id="c96d8-108">È possibile verificare una firma:</span><span class="sxs-lookup"><span data-stu-id="c96d8-108">A signature can be checked for:</span></span>

-   <span data-ttu-id="c96d8-109">Validità dell'hash della firma</span><span class="sxs-lookup"><span data-stu-id="c96d8-109">Validity of the signature hash</span></span>
-   <span data-ttu-id="c96d8-110">Validità del certificato del firmatario</span><span class="sxs-lookup"><span data-stu-id="c96d8-110">Validity of the signer's certificate</span></span>

<span data-ttu-id="c96d8-111">L' [*hash*](../secgloss/h-gly.md) della firma viene decrittografato usando la [*chiave pubblica*](../secgloss/p-gly.md) del firmatario trovato nel [*certificato*](../secgloss/c-gly.md)del firmatario, incluso come parte della firma.</span><span class="sxs-lookup"><span data-stu-id="c96d8-111">The signature [*hash*](../secgloss/h-gly.md) is decrypted using the [*public key*](../secgloss/p-gly.md) of the signer found on the signer's [*certificate*](../secgloss/c-gly.md), included as part of the signature.</span></span> <span data-ttu-id="c96d8-112">Se la firma decrittografata corrisponde a un nuovo hash del documento originale, la firma è stata creata dal proprietario della chiave privata associata alla chiave pubblica usata per decrittografare l'hash.</span><span class="sxs-lookup"><span data-stu-id="c96d8-112">If the decrypted signature matches a new hash of the original document, the signature was created by the owner of the private key associated with the public key used to decrypt the hash.</span></span> <span data-ttu-id="c96d8-113">Inoltre, il documento su cui si basa la firma è garantito che non sia stato modificato dopo la creazione della firma.</span><span class="sxs-lookup"><span data-stu-id="c96d8-113">In addition, the document that the signature is based on is guaranteed not to have been changed after the signature was created.</span></span>

<span data-ttu-id="c96d8-114">È anche possibile verificare la validità del certificato che ha fornito la chiave pubblica e l'identità del firmatario, inclusi i problemi che determinano se il certificato è stato revocato, se il certificato è obsoleto o se il certificato è stato emesso da un'autorità di certificazione attendibile.</span><span class="sxs-lookup"><span data-stu-id="c96d8-114">The certificate that provided the public key and the identity of the signer can also be checked for validity including such issues as whether the certificate has been revoked, whether the certificate is out of date, or whether the certificate was issued by a trusted certificate issuer.</span></span>

<span data-ttu-id="c96d8-115">Nell'esempio seguente, il contenuto firmato e l'oggetto **SignedData** vengono letti da un file e la firma e la validità del certificato usato per creare la firma vengono controllati.</span><span class="sxs-lookup"><span data-stu-id="c96d8-115">In the following example, the content signed and the **SignedData** object are read in from a file and the signature and the validity of the certificate used to create the signature are checked.</span></span>

> [!Note]  
> <span data-ttu-id="c96d8-116">Se la firma non è crittograficamente valida o il certificato del firmatario non è valido, viene generata un'eccezione e il programma di verifica deve gestire l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="c96d8-116">If the signature is not cryptographically valid or the certificate of the signer is not valid, an exception is raised and the verifying program must handle the exception.</span></span> <span data-ttu-id="c96d8-117">In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="c96d8-117">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="c96d8-118">Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="c96d8-118">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="c96d8-119">Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="c96d8-119">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
