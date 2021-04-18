---
description: Un documento può essere firmato da più di un firmatario.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cofirma di un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321031"
---
# <a name="cosigning-a-document"></a>Cofirma di un documento

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Un documento può essere firmato da più di un firmatario. Questo errore si verifica quando, ad esempio, due o più entità firmano un contratto o una nota spese. Nell'esempio seguente un documento già firmato viene ricevuto da un secondo firmatario. Questo firmatario usa il metodo [**cosign**](signeddata-cosign.md) per alleghi una firma aggiuntiva al documento.

Se si verifica un errore di capicol, nella proprietà **Err. Number** viene restituito un valore negativo. Per ulteriori informazioni sui codici di errore di capicol, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md). Se il codice di errore nella proprietà **Err. Number** è un valore positivo, l'errore è un errore di Windows. Per informazioni sui codici di errore di Windows, vedere Winerror. h.

> [!Note]
> La firma di un documento richiede anche che il cofirmatario disponga di un [*certificato*](../secgloss/c-gly.md) disponibile con una [*chiave privata*](../secgloss/p-gly.md) per creare la firma. Se un firmatario non viene specificato nella chiamata al metodo [**Sign**](signeddata-sign.md) e non è presente alcun certificato in CAPICOM \_ My \_ Store con una chiave privata associata, il metodo ha esito negativo. Se è presente un solo certificato in CAPICOM \_ My \_ Store con una chiave privata associata, vengono usati la chiave e il certificato. Se è presente più di un certificato utilizzabile, viene visualizzato un messaggio di richiesta per consentire all'utente di scegliere il certificato desiderato.
> 
> Se il metodo [**cosign**](signeddata-cosign.md) viene usato in un'applicazione basata sul Web, viene sempre visualizzata una richiesta per ottenere l'autorizzazione dell'utente prima che venga creata una firma usando la chiave privata del firmatario.

 

Nell'esempio seguente vengono letti i file che contengono il documento da firmare e le firme correnti del documento, la firma è cofirmata e la nuova firma viene scritta in un file. Nell'esempio viene utilizzata una firma scollegata con i dati firmati e la firma in file distinti.


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
