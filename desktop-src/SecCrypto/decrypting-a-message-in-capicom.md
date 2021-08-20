---
description: Questa subroutine accetta una stringa di password da usare per generare una chiave di crittografia della sessione e il nome di un file da cui verrà letto un messaggio crittografato. Tutti i parametri vengono passati nella subroutine in base ai valori.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Decrittografia di un messaggio in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744878378fbe2791e66151e451029be8adde2435b451d540196a1082c4e005f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767759"
---
# <a name="decrypting-a-message-in-capicom"></a>Decrittografia di un messaggio in CAPICOM

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Questa subroutine accetta una stringa di password da usare per generare una chiave di crittografia della sessione e il nome di un file da cui verrà letto un messaggio crittografato. Tutti i parametri vengono passati nella subroutine in base ai valori.

> [!Note]  
> CAPICOM non supporta il tipo di contenuto PKCS 7 EncryptedData, ma usa una struttura ASN non standard \# per EncryptedData. Pertanto, solo CAPICOM può decrittografare un oggetto CAPICOM EncryptedData.

 

Se la decrittografia non riesce, viene controllato il valore **Err.Number** per determinare se l'errore è stato causato dall'uso di una password che non corrisponde alla password usata per crittografare il messaggio. In questo caso, viene restituito l'errore NTE \_ BAD \_ DATA.

In caso di errore CAPICOM, viene restituito un valore decimale negativo **di Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.


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



 

 



