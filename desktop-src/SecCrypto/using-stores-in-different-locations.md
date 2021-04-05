---
description: Nell'esempio seguente vengono illustrati gli aspetti dell'utilizzo dell'oggetto Store. Mostra gli archivi di apertura nell'archivio di \_ memoria CAPICOM \_ , l' \_ archivio utente corrente di CAPICOM \_ e i \_ percorsi di \_ \_ archiviazione del computer locale \_ di CAPICOM.
ms.assetid: bfb7ff48-1d6b-404f-9dd4-6de1898354b7
title: Uso di archivi in posizioni diverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e22fa4d4eca4748d6c4652a8b33d22a1db492a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753439"
---
# <a name="using-stores-in-different-locations"></a>Uso di archivi in posizioni diverse

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

Nell'esempio seguente vengono illustrati gli aspetti dell'utilizzo dell'oggetto [**Store**](store.md) . Mostra gli archivi di apertura nell'archivio di \_ memoria CAPICOM \_ , l' \_ archivio utente corrente di CAPICOM \_ e i \_ percorsi di \_ \_ archiviazione del computer locale \_ di CAPICOM.

Nell'esempio viene illustrata l'esportazione di [*certificati*](../secgloss/c-gly.md) da un [*Archivio*](../secgloss/c-gly.md)aperto, la scrittura dei certificati esportati in un file, la loro lettura e l'importazione in un altro archivio. I certificati appena importati vengono quindi enumerati e visualizzati.

In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** . Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md). Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.


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



 

 
