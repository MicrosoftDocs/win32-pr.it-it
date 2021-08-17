---
description: Questa subroutine accetta una stringa da crittografare, una stringa di password da usare per generare una chiave di crittografia e il nome di un file in cui verrà scritto il messaggio crittografato.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Crittografia di un messaggio in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3ef531fa75fc4d99a423ffbb6c0edd591caf6b1939f12fea439e7f9fbc80dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766193"
---
# <a name="encrypting-a-message-in-capicom"></a>Crittografia di un messaggio in CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Questa subroutine accetta una stringa da crittografare, una stringa di password da usare per generare una chiave di crittografia e il nome di un file in cui verrà scritto il messaggio crittografato. Tutti i parametri vengono passati nella subroutine in base ai valori. Per decrittografare il messaggio, è necessario usare la stessa stringa di password. Se la password viene persa, il testo non può essere decrittografato. La privacy del messaggio viene persa se un destinatario non intenzionale ottiene l'accesso alla password.

> [!Note]  
> CAPICOM non supporta il tipo di contenuto PKCS 7 EncryptedData, ma usa una struttura ASN non standard \# per EncryptedData. Di conseguenza, solo CAPICOM può decrittografare un oggetto CAPICOM EncryptedData.

 

In caso di errore CAPICOM, viene restituito un valore decimale negativo della **proprietà Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.


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



 

 



