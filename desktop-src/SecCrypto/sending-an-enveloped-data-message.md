---
description: Nell'esempio seguente viene letto un messaggio in testo non crittografato da un file e viene aperto un archivio certificati contenente i certificati dei destinatari del messaggio previsti.
ms.assetid: 7ae672d3-e11d-453c-b9c0-354d21830ae4
title: Invio di un messaggio di dati in busta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d93c73e22a9ac98e08d12164e78aa585a6b2ba3da6f47bf53675a7320bc206e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900361"
---
# <a name="sending-an-enveloped-data-message"></a>Invio di un messaggio di dati in busta

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Nell'esempio seguente viene letto un messaggio in testo non crittografato da un file e viene aperto un archivio certificati contenente i certificati dei destinatari del messaggio previsti. Tutti i certificati nell'archivio vengono aggiunti come destinatari del messaggio, il messaggio viene in busta e il messaggio in busta viene scritto in un file.

È possibile aggiungere codice aggiuntivo per visualizzare i certificati aggiunti come destinatari del messaggio, per verificare i certificati prima che vengano aggiunti come destinatari previsti o per scegliere in altro modo quelli da aggiungere.

In caso di errore CAPICOM, viene restituito un valore decimale negativo **di Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.


```VB
Sub Envelope(ByVal InFile As String, ByVal OutFile As String, _
             ByVal StoreName As String)

On Error GoTo ErrorHandler

'Open the input file and read the message to be enveloped.

Dim Text As String
Open InFile For Input As #1
Input #1, Text
Close #1
If Len(Text) < 1 Then
    MsgBox "No message to be enveloped."
    Exit Sub
End If

'Open the store containing the certificates of
'the message recipients.

Dim CertStore As New Store
CertStore.Open CAPICOM_CURRENT_USER_STORE, StoreName, _
    CAPICOM_STORE_OPEN_READ_ONLY

' Check for an empty certificate store.

If CertStore.Certificates.Count < 1 Then
    MsgBox "There are no recipient certificates available."
    Set CertStore = Nothing
    Exit Sub
End If

' Declare and initialize an EnvelopedData object

Dim EnvMessage As New EnvelopedData
EnvMessage.Content = Text
Dim I As Integer
For I = 1 To CertStore.Certificates.Count
    EnvMessage.Recipients.Add CertStore.Certificates.Item(I)
    ' The following line can be uncommented to see a prompt
    ' for each certificate in the store.
    ' CertStore.Certificates.Item(I).Display
Next I

'  Set the encryption algorithm and key length. Comment out
'  or remove the following lines to use the default algorithm
'  and key length. The triple DES algorithm and 128 bit key
'  length may not be supported.
Envmessage.Algorithm.Name = ENCRYPTION_ALGORITHM_RC4
Envmessage.Algorithm.KeyLength = KEY_LENGTH_128_BITS

'Declare the string that will hold the enveloped message.

Dim EnvelopedMessage As String

'Encrypt the message into EnvelopedMessage. The enveloped message
'string contains everything that an intended recipient will need to
'decrypt the message, including information on the 
'encryption algorithm key length.
EnvelopedMessage = EnvMessage.Encrypt

' Optionally, check the length of the encrypted string to make sure 
' that the encrypt method worked.

If Len(EnvelopedMessage) < 1 Then
    MsgBox "no message encrypted. "
Else
    MsgBox " Message is " & Len(EnvelopedMessage) & " characters"

    ' Open an output file and write the encrypted message to the 
    ' file. The file is not opened if there is no message to write.
    Open OutFile For Output As #2
    Write #2, EnvelopedMessage
    Close #2
    MsgBox "The message written to file "
End If

' Release the EncryptedData object and the Store object.
Set Envmessage = Nothing
Set CertStore = Nothing

Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found : " & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 



