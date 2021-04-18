---
description: Questa subroutine accetta una stringa da crittografare, una stringa password da usare per generare una chiave di crittografia e il nome di un file in cui verrà scritto il messaggio crittografato.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Crittografia di un messaggio in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8039586736c09673644cacc90759e8d5f25b6e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316181"
---
# <a name="encrypting-a-message-in-capicom"></a><span data-ttu-id="c3bf9-103">Crittografia di un messaggio in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="c3bf9-103">Encrypting a Message in CAPICOM</span></span>

<span data-ttu-id="c3bf9-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c3bf9-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="c3bf9-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="c3bf9-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="c3bf9-107">Questa subroutine accetta una stringa da crittografare, una stringa password da usare per generare una chiave di crittografia e il nome di un file in cui verrà scritto il messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-107">This subroutine takes a string to be encrypted, a password string to be used to generate an encryption key, and the name of a file where the encrypted message will be written.</span></span> <span data-ttu-id="c3bf9-108">Tutti i parametri vengono passati nella subroutine per valori.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-108">All parameters are passed into the subroutine by values.</span></span> <span data-ttu-id="c3bf9-109">Per decrittografare il messaggio, è necessario usare la stessa stringa di password.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-109">To decrypt the message, the same password string must be used.</span></span> <span data-ttu-id="c3bf9-110">Se la password viene persa, il testo non può essere decrittografato.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-110">If the password is lost, the text cannot be decrypted.</span></span> <span data-ttu-id="c3bf9-111">La privacy del messaggio viene persa se un destinatario indesiderato Ottiene l'accesso alla password.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-111">The privacy of the message is lost if an unintended recipient gains access to the password.</span></span>

> [!Note]  
> <span data-ttu-id="c3bf9-112">CAPICOM non supporta il \# tipo di contenuto EncryptedData di PKCS 7, ma usa una struttura ASN non standard per EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-112">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="c3bf9-113">Di conseguenza, solo CAPICOM è in grado di decrittografare un oggetto capicot EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-113">As a result, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="c3bf9-114">In caso di errore di CAPICOM, viene restituito un valore decimale negativo della proprietà **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="c3bf9-114">On any CAPICOM error, a negative decimal value of the **Err.Number** property is returned.</span></span> <span data-ttu-id="c3bf9-115">Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="c3bf9-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="c3bf9-116">Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="c3bf9-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub EncryptMessage(ByVal TobeEncrypted As String, ByVal hidden _
    As String, ByVal filename As String)

    On Error GoTo ErrorHandler

    ' Declare and initialize an EncryptedData object.
    ' Algorithm.Name and KeyLength do not need to be set.

    Dim message As New EncryptedData
    message.Content = Tobeencrypted
    message.SetSecret(hidden)
    ' Optionally, the encryption algorithm and key length can be set.
    ' If these properties are not set, the default algorithm and key 
    ' length are used.
    ' Information about the algorithm and key length is saved with 
    ' the encrypted string and the individual decrypting the message
    ' does not need to set these properties.

    message.Algorithm.Name = CAPICOM_ENCRYPTION_ALGORITHM_DES

    ' Declare the string that will hold the encrypted message.

    Dim encryptedmessage As String

    ' Encrypt the message storing the result in the encryptedmessage
    ' string.
    encryptedmessage = message.Encrypt

    ' Optionally, check the length of the encrypted string to 
    ' make sure that the encrypt method worked. 

    If Len(encryptedmessage) < 1 Then
        MsgBox("no message encrypted. ")
    Else
        MsgBox(" Message is " & Len(encryptedmessage) & " characters")

        ' Open an output file and write the encrypted message to the
        ' file. The file is not opened if there is no message
        ' to write.
    Open filename For Output As #1
    Write #1, encryptedmessage
    Close #1
        MsgBox("Encrypted message written to file ")
    End If

    ' Release the EncryptedData object.
    message = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 



