---
description: Un documento può essere firmato da più di un firmatario.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cofirma di un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb384ef47001f1df85810ac37595988da96a356ff3b36b1b140d1a6f54d0d698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769386"
---
# <a name="cosigning-a-document"></a>Cofirma di un documento

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Un documento può essere firmato da più di un firmatario. Ciò si verifica quando, ad esempio, due o più parti firmano un contratto o una nota spese. Nell'esempio seguente un documento già firmato viene ricevuto da un secondo firmatario. Questo firmatario usa il [**metodo CoSign**](signeddata-cosign.md) per allegare una firma aggiuntiva al documento.

Se si verifica un errore CAPICOM, viene restituito un valore negativo nella **proprietà Err.Number.** Per altre informazioni sui codici di errore CAPICOM, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Se il codice di errore **nella proprietà Err.Number** è un valore positivo, l'errore è un errore Windows errore. Per informazioni sui Windows di errore, vedere Winerror.h.

> [!Note]
> La firma di un documento richiede anche che il cofirmatore abbia un certificato disponibile [*con*](../secgloss/c-gly.md) una [*chiave privata*](../secgloss/p-gly.md) per creare la firma. Se non viene specificato un firmatario nella chiamata del metodo [**Sign**](signeddata-sign.md) e non è presente alcun certificato in CAPICOM MY STORE con una chiave privata associata, il \_ metodo ha esito \_ negativo. Se in CAPICOM MY STORE è presente un solo certificato con una chiave privata associata, vengono usati la chiave \_ \_ e il certificato. Se sono presenti più certificati utilizzabili, viene visualizzata una richiesta per consentire all'utente di scegliere il certificato desiderato.
> 
> Se il [**metodo CoSign**](signeddata-cosign.md) viene usato in un'applicazione basata sul Web, viene sempre visualizzato un prompt per ottenere l'autorizzazione dell'utente prima che venga creata una firma usando la chiave privata del firmatario.

 

Nell'esempio seguente vengono letti i file che contengono il documento da firmare e le firme correnti in tale documento, la firma viene firmata e la nuova firma viene scritta in un file. Nell'esempio viene utilizzata una firma scollegata con i dati firmati e la firma in file separati.


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



 

 
