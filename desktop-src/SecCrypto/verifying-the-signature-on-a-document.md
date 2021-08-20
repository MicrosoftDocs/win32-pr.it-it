---
description: Quando viene ricevuto un documento firmato, è possibile verificare la validità della firma o delle firme.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Verifica della firma in un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb1e6bbec678f74c9761c7f4c0712249c8b557a68b5e9f80aeeb3306faede36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970937"
---
# <a name="verifying-the-signature-on-a-document"></a>Verifica della firma in un documento

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Quando viene ricevuto un documento firmato, è possibile verificare la validità della firma o delle firme. Una firma può essere verificata per:

-   Validità dell'hash della firma
-   Validità del certificato del firmatario

[*L'hash*](../secgloss/h-gly.md) della firma [](../secgloss/p-gly.md) viene decrittografato usando la chiave pubblica del firmatario presente nel certificato del firmatario, [](../secgloss/c-gly.md)incluso come parte della firma. Se la firma decrittografata corrisponde a un nuovo hash del documento originale, la firma è stata creata dal proprietario della chiave privata associata alla chiave pubblica usata per decrittografare l'hash. Inoltre, è garantito che il documento su cui si basa la firma non sia stato modificato dopo la creazione della firma.

È anche possibile verificare la validità del certificato che ha fornito la chiave pubblica e l'identità del firmatario, inclusi problemi come la revoca del certificato, la non validità del certificato o l'emissione del certificato da parte di un'autorità di certificazione attendibile.

Nell'esempio seguente il contenuto firmato e l'oggetto **SignedData** vengono letti da un file e vengono controllate la firma e la validità del certificato usato per creare la firma.

> [!Note]  
> Se la firma non è valida dal punto di vista crittografico o il certificato del firmatario non è valido, viene generata un'eccezione e il programma di verifica deve gestire l'eccezione. In caso di errore CAPICOM, viene restituito un valore decimale negativo **di Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.

 


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



 

 
