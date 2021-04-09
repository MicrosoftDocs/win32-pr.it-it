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
# <a name="verifying-the-signature-on-a-document"></a>Verifica della firma in un documento

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Quando viene ricevuto un documento firmato, è possibile verificare la validità della firma o delle firme. È possibile verificare una firma:

-   Validità dell'hash della firma
-   Validità del certificato del firmatario

L' [*hash*](../secgloss/h-gly.md) della firma viene decrittografato usando la [*chiave pubblica*](../secgloss/p-gly.md) del firmatario trovato nel [*certificato*](../secgloss/c-gly.md)del firmatario, incluso come parte della firma. Se la firma decrittografata corrisponde a un nuovo hash del documento originale, la firma è stata creata dal proprietario della chiave privata associata alla chiave pubblica usata per decrittografare l'hash. Inoltre, il documento su cui si basa la firma è garantito che non sia stato modificato dopo la creazione della firma.

È anche possibile verificare la validità del certificato che ha fornito la chiave pubblica e l'identità del firmatario, inclusi i problemi che determinano se il certificato è stato revocato, se il certificato è obsoleto o se il certificato è stato emesso da un'autorità di certificazione attendibile.

Nell'esempio seguente, il contenuto firmato e l'oggetto **SignedData** vengono letti da un file e la firma e la validità del certificato usato per creare la firma vengono controllati.

> [!Note]  
> Se la firma non è crittograficamente valida o il certificato del firmatario non è valido, viene generata un'eccezione e il programma di verifica deve gestire l'eccezione. In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** . Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md). Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.

 


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



 

 
