---
description: Per decrittografare un messaggio in busta digitale, il destinatario corrisponde a un certificato dell'archivio My con una chiave privata disponibile con un certificato nel messaggio in busta digitale.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Ricezione di un messaggio di dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884846"
---
# <a name="receiving-an-enveloped-data-message"></a><span data-ttu-id="95cf7-103">Ricezione di un messaggio di dati in busta</span><span class="sxs-lookup"><span data-stu-id="95cf7-103">Receiving an Enveloped Data Message</span></span>

<span data-ttu-id="95cf7-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="95cf7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="95cf7-105">Usare invece il .NET Framework per implementare le funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="95cf7-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="95cf7-106">Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="95cf7-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="95cf7-107">Per decrittografare un messaggio in busta digitale, il destinatario corrisponde a un [*certificato*](../secgloss/c-gly.md) dell'archivio My con una chiave privata disponibile con un certificato nel messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="95cf7-107">To decrypt an enveloped message, the recipient matches a [*certificate*](../secgloss/c-gly.md) from the My store that has an available private key with a certificate in the enveloped message.</span></span> <span data-ttu-id="95cf7-108">Se viene trovata una corrispondenza, la chiave crittografata associata a tale certificato viene decrittografata e la chiave decrittografata viene utilizzata per decrittografare il messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="95cf7-108">If a match is found, the encrypted key associated with that certificate is decrypted and that decrypted key is used to decrypt the enveloped message.</span></span> <span data-ttu-id="95cf7-109">Un destinatario del messaggio che non dispone di un certificato corrispondente con una chiave privata disponibile non può decrittografare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="95cf7-109">A message recipient that does not have a matching certificate with an available private key cannot decrypt the message.</span></span>

<span data-ttu-id="95cf7-110">Nell'esempio seguente viene passato un nome file alla subroutine, il file viene aperto e viene letto un messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="95cf7-110">In the example that follows, a file name is passed into the subroutine, that file is opened and an enveloped message is read in.</span></span> <span data-ttu-id="95cf7-111">Il messaggio in busta viene quindi decrittografato.</span><span class="sxs-lookup"><span data-stu-id="95cf7-111">The enveloped message is then decrypted.</span></span> <span data-ttu-id="95cf7-112">I passaggi per la corrispondenza di un certificato utente con un certificato nel messaggio in busta, della decrittografia della chiave di crittografia e infine della decrittografia del messaggio vengono tutti eseguiti dietro le quinte.</span><span class="sxs-lookup"><span data-stu-id="95cf7-112">The steps of matching a user certificate with a certificate in the enveloped message, of decrypting the encryption key, and finally of decrypting the message are all done behind the scenes.</span></span> <span data-ttu-id="95cf7-113">Viene generato un errore se non viene trovata una corrispondenza del certificato o se la decrittografia ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="95cf7-113">An error is raised if a certificate match is not found or if the decryption fails.</span></span>

<span data-ttu-id="95cf7-114">In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="95cf7-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="95cf7-115">Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="95cf7-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="95cf7-116">Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="95cf7-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub ReceiveMessage(ByVal InFile As String)
On Error GoTo ErrorHandler

'Declare an EnvelopedData object

Dim Envmessage As New EnvelopedData

'Declare a string variable to hold the encrypted message.

Dim Encrypted As String

' Open an input file and read in the encrypted message
Open InFile For Input As #1
Input #1, Encrypted
Close #1

' If the length of the input string is greater than 0, 
' an encrypted message string is available. Decrypt the message.
' Note: to decrypt the message, a certificate with access to
' a user's private key must be available, and that certificate must
' match one of the certificates in the Recipients collection of 
' certificates.
If Len(Encrypted) > 0 Then
    ' Receive and decrypt the message
    Envmessage.Decrypt encrypted
    
    ' Display the decrypted message.
    MsgBox Envmessage.Content
Else
    MsgBox "No enveloped message was read in."
End If
' Release the EncryptedData object.
Set Envmessage = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 
