---
description: Un uso standard di una firma consiste nel firmare un testo e salvare il testo firmato in un file. Il testo firmato potrebbe anche essere inviato tramite Internet. Il messaggio firmato è in \# formato PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Firma di un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305589"
---
# <a name="signing-a-document"></a>Firma di un documento

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Un uso standard di una firma consiste nel firmare un testo e salvare il testo firmato in un file. Il testo firmato potrebbe anche essere inviato tramite Internet. Il messaggio firmato è in \# formato PKCS 7.

In questo esempio, la firma viene creata per il contenuto scollegato (quando il contenuto non è incluso nella firma). Una firma scollegata verrebbe spesso utilizzata se il destinatario della firma ha una copia del testo firmato esatto. Nell'esempio seguente il messaggio originale e la firma scollegata vengono scritti in file distinti.

In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** . Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md). Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.

La creazione di una firma usa la [*chiave privata*](../secgloss/p-gly.md)del firmatario. È possibile creare una firma solo se è disponibile il certificato del firmatario con una chiave privata associata. Questo esempio di metodo **Sign** non specifica un firmatario. Se non si specifica un firmatario e nessun certificato nell' **\_ \_ archivio personale** ha una chiave privata associata, il metodo **Sign** ha esito negativo. Se un solo certificato in **CApicol \_ My \_ Store** ha una chiave privata associata, il certificato e la relativa chiave privata vengono usati per creare la firma. Se a più di un certificato nell'archivio del **\_ \_ negozio personale** è associata una chiave privata, viene visualizzata una finestra di dialogo in cui l'utente può scegliere il certificato da usare per creare la firma.

Quando un'applicazione basata sul Web usa il metodo **Sign** , viene sempre visualizzata una richiesta e l'autorizzazione dell'utente è richiesta prima che venga creata una firma che usa la chiave privata del firmatario.


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> <dt>

[**Firmatario. Certificate**](signer-certificate.md)
</dt> <dt>

[**Attributo**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
