---
description: Questa subroutine accetta una stringa password da usare per generare una chiave di crittografia della sessione e il nome di un file da cui verrà letto un messaggio crittografato. Tutti i parametri vengono passati nella subroutine per valori.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Decrittografia di un messaggio in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba984bad7d9289eaf89725e9598a4330f16b49ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311930"
---
# <a name="decrypting-a-message-in-capicom"></a><span data-ttu-id="2a2a7-104">Decrittografia di un messaggio in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="2a2a7-104">Decrypting a Message in CAPICOM</span></span>

<span data-ttu-id="2a2a7-105">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2a2a7-106">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="2a2a7-107">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="2a2a7-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="2a2a7-108">Questa subroutine accetta una stringa password da usare per generare una chiave di crittografia della sessione e il nome di un file da cui verrà letto un messaggio crittografato.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-108">This subroutine take a password string to be used to generate a session encryption key, and the name of a file from which an encrypted message will be read.</span></span> <span data-ttu-id="2a2a7-109">Tutti i parametri vengono passati nella subroutine per valori.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-109">All parameters are passed into the subroutine by values.</span></span>

> [!Note]  
> <span data-ttu-id="2a2a7-110">CAPICOM non supporta il \# tipo di contenuto EncryptedData di PKCS 7, ma usa una struttura ASN non standard per EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-110">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="2a2a7-111">Pertanto, solo CAPICOM è in grado di decrittografare un oggetto capicot EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-111">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="2a2a7-112">Se la decrittografia ha esito negativo, viene verificato il valore **Err. Number** per determinare se l'errore è stato causato dall'utilizzo di una password che non corrisponde alla password utilizzata per crittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-112">If decryption fails, the **Err.Number** value is checked to determine whether the error was caused by the use of a password that did not match the password used to encrypt the message.</span></span> <span data-ttu-id="2a2a7-113">In questo caso, \_ \_ viene restituito l'errore di dati non validi.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-113">In this case, the NTE\_BAD\_DATA error is returned.</span></span>

<span data-ttu-id="2a2a7-114">In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="2a2a7-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="2a2a7-115">Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="2a2a7-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="2a2a7-116">Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="2a2a7-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub DecryptMessage(ByVal hidden As String, ByVal filename As String)
On Error goto ErrorHandler

'Declare an EncryptedData object

Dim message As New EncryptedData

'Declare a string variable to hold the encrypted message.
Dim encrypted As String

' Open an input file and read in the encrypted message
Open filename For Input As #1
Input #1, encrypted
Close #1

' If a message was read in (the length of the input string is 
' greater than 0), set the password and decrypt the message.
If Len(encrypted) > 0 then
    ' Set the password used to generate the key
    ' used to decrypt the message. If the password
    ' not the same as the password used when the message
    ' was encrypted, decryption will fail.
    ' The algorithm name and key length set in the encrypting
    ' process are automatically used to decrypt the message. 
    message.SetSecret hidden
    message.Decrypt encrypted
    ' Display the decrypted message.
    MsgBox message.Content
else
    msgbox "No encrypted message was read in.
endif

' Release the EncryptedData object and exit the subroutine.
Set message = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
'    Check for a bad password error.
    If Err.Number = -2146893819 Then
        MsgBox "Error. The password may not be correct."
    Else
        MsgBox "CAPICOM error found : " & Err.Number
    End If
End If
End Sub
```



 

 



