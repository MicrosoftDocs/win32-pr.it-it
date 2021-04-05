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
# <a name="receiving-an-enveloped-data-message"></a>Ricezione di un messaggio di dati in busta

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Per decrittografare un messaggio in busta digitale, il destinatario corrisponde a un [*certificato*](../secgloss/c-gly.md) dell'archivio My con una chiave privata disponibile con un certificato nel messaggio in busta digitale. Se viene trovata una corrispondenza, la chiave crittografata associata a tale certificato viene decrittografata e la chiave decrittografata viene utilizzata per decrittografare il messaggio in busta digitale. Un destinatario del messaggio che non dispone di un certificato corrispondente con una chiave privata disponibile non può decrittografare il messaggio.

Nell'esempio seguente viene passato un nome file alla subroutine, il file viene aperto e viene letto un messaggio in busta digitale. Il messaggio in busta viene quindi decrittografato. I passaggi per la corrispondenza di un certificato utente con un certificato nel messaggio in busta, della decrittografia della chiave di crittografia e infine della decrittografia del messaggio vengono tutti eseguiti dietro le quinte. Viene generato un errore se non viene trovata una corrispondenza del certificato o se la decrittografia ha esito negativo.

In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** . Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md). Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.


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



 

 
