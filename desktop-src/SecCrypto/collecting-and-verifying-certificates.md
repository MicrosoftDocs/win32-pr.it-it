---
description: Nell'esempio seguente i certificati in un archivio locale vengono enumerati e verificati per verifica della validità.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Raccolta e verifica dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60b793cf4aeca7d05d166a4b205b924db53faee09683cefcef7b0244a9eb0289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769532"
---
# <a name="collecting-and-verifying-certificates"></a>Raccolta e verifica dei certificati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

Spesso è necessario [*raccogliere e*](../secgloss/c-gly.md) verificare un gruppo di certificati. Questa operazione viene spesso eseguita per preparare un gruppo di destinatari per un messaggio in busta. Nell'esempio seguente i certificati in un archivio locale vengono enumerati e verificati per verifica della validità. Viene quindi aperto un archivio di Active Directory per recuperare e aggiungere nuovi certificati all'archivio locale. I certificati recuperati dall'archivio di Active Directory vengono verificati per verifica della validità e, se validi, vengono aggiunti all'archivio locale. Entrambi i negozi vengono quindi chiusi.

In caso di errore CAPICOM, viene restituito un valore decimale negativo **di Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.

In questo esempio il nome dell'archivio locale viene passato come parametro di stringa. Come parametro viene passata anche una stringa che indica i criteri di ricerca per i certificati nell'archivio di Active Directory.


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
