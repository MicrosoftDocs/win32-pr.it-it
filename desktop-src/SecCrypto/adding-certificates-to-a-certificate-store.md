---
description: I certificati possono essere aggiunti o rimossi dagli archivi certificati se l'archivio viene aperto con autorizzazione di lettura/scrittura.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Aggiunta di certificati a un archivio certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3c4b2fafbcd11bf2d984dfd5b5a575f67dc4f6d3c70337de399ca6076029ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774036"
---
# <a name="adding-certificates-to-a-certificate-store"></a>Aggiunta di certificati a un archivio certificati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

[*I*](../secgloss/c-gly.md) certificati possono essere aggiunti o rimossi dagli archivi [*certificati se*](../secgloss/c-gly.md) l'archivio viene aperto con autorizzazione di lettura/scrittura. L'autorizzazione di lettura/scrittura non viene concessa agli archivi di Active Directory. Anche se i certificati possono essere aggiunti o rimossi dagli archivi di memoria, le modifiche negli archivi di memoria non vengono rese persistenti tra le sessioni.

I certificati possono essere aggiunti a un archivio certificati aperto con autorizzazione di lettura/scrittura tramite il **metodo Add.** Un certificato può essere rimosso da un archivio certificati aperto con autorizzazione di lettura/scrittura tramite il **metodo Remove.** È possibile creare e salvare nuovi archivi nei percorsi CAPICOM \_ CURRENT USER STORE e \_ \_ CAPICOM LOCAL MACHINE \_ \_ \_ STORE. Gli archivi appena creati in uno di questi percorsi possono essere aperti con l'autorizzazione di lettura/scrittura.

Nell'esempio seguente vengono aperti due archivi certificati. I certificati degli oggetti con cognome che iniziano con F vengono recuperati dall'archivio di Active Directory. L'archivio CAPICOM CURRENT USER STORE, CAPICOM CA STORE viene quindi aperto come archivio di lettura/scrittura e il primo certificato dalla raccolta di certificati nell'archivio di Active Directory viene aggiunto ai certificati \_ \_ nell'archivio CA \_ \_ \_ \_ \_ CAPICOM.

A scopo dimostrativo, l'esempio mostra l'apertura di archivi nei percorsi CAPICOM \_ MEMORY \_ STORE, CAPICOM CURRENT USER STORE e \_ \_ \_ CAPICOM \_ LOCAL MACHINE \_ \_ STORE. L'esempio mostra l'esportazione di tutti i certificati da un archivio aperto, la scrittura dei certificati esportati in un file, la lettura e l'importazione in un archivio diverso. I certificati appena importati vengono enumerati e visualizzati.

In caso di errore CAPICOM, viene restituito un valore decimale negativo **Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.

L'esempio seguente illustra l'apertura di archivi certificati usando l'associazione anticipata nella dichiarazione degli oggetti **Store** e nella creazione di un'istanza di tali oggetti.


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
