---
description: L'esempio seguente illustra gli aspetti dell'uso dell'oggetto Store. Mostra l'apertura di archivi nei percorsi CAPICOM \_ MEMORY \_ STORE, CAPICOM CURRENT USER STORE e \_ \_ \_ CAPICOM \_ LOCAL MACHINE \_ \_ STORE.
ms.assetid: bfb7ff48-1d6b-404f-9dd4-6de1898354b7
title: Uso di archivi in posizioni diverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e57e1c1584754f0b02b61438a7a6a83694c36cd77c633c52f6bec216721d7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971407"
---
# <a name="using-stores-in-different-locations"></a>Uso di archivi in posizioni diverse

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

L'esempio seguente illustra gli aspetti dell'uso [**dell'oggetto**](store.md) Store. Mostra l'apertura di archivi nei percorsi CAPICOM \_ MEMORY \_ STORE, CAPICOM CURRENT USER STORE e \_ \_ \_ CAPICOM \_ LOCAL MACHINE \_ \_ STORE.

L'esempio illustra [*l'esportazione*](../secgloss/c-gly.md) di certificati da un archivio [*aperto,*](../secgloss/c-gly.md)la scrittura dei certificati esportati in un file, la lettura e l'importazione dei certificati in un archivio diverso. I certificati appena importati vengono quindi enumerati e visualizzati.

In caso di errore CAPICOM, viene restituito un valore decimale negativo **di Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.


```VB
Sub OpenStores()

    On Error GoTo ErrorHandler

    'Open Memory, current user, and local machine stores
    Dim MemoryStore As New Store
    Dim CurrentUserStore As New Store
    Dim LocalMachineStore As New Store
    Dim NumCerts As Integer

    MemoryStore.Open(CAPICOM_MEMORY_STORE, "MemStore", _
        CAPICOM_STORE_OPEN_READ_WRITE)
    CurrentUserStore.Open(CAPICOM_CURRENT_USER_STORE, _
        CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_ONLY)
    LocalMachineStore.Open(CAPICOM_LOCAL_MACHINE_STORE, _
        CAPICOM_CA_STORE, CAPICOM_STORE_OPEN_READ_ONLY)

    ' Check the number of certificates in the stores.
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the memory store. ")
    NumCerts = CurrentUserStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the current user store. ")
    NumCerts = LocalMachineStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the local machine store. ")


    '  Export the certificates in the current user MY store
    '  to a file.
    Dim ExportString As String
    ExportString = CurrentUserStore.Export
Open "Exportcerts.txt" For Output As #1
Write #1, ExportString
Close #1

    ' Read the store the file.
    Dim importString As String
Open "exportcerts.txt" For Input As #2
Input #2, importString
Close #2
    MemoryStore.Import(importString)

    ' Check the number of certificates in the memory store after 
    ' import()
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates now in the memory store. ")

    ' Enumerate the certificates in the memory store and display each
    ' certificate
    Dim i As Long
    For i = 1 To NumCerts
        MemoryStore.Certificates.Item(i).Display()
    Next i

    ' Release the store objects
    MemoryStore = Nothing
    CurrentUserStore = Nothing
    LocalMachineStore = Nothing
    Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found: " & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
