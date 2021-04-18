---
description: È possibile recuperare i certificati da un archivio Active Directory in cui sono archiviati i certificati degli utenti di un dominio.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Apertura dell'archivio Active Directory e recupero dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd60c7414aaec8b069817b47fbd2493bb11d98c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315378"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a>Apertura dell'archivio Active Directory e recupero dei certificati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [alternative all'uso di CAPICOM](alternatives-to-using-capicom.md).\]

È possibile recuperare i [*certificati*](../secgloss/c-gly.md) da un archivio Active Directory in cui sono archiviati i certificati degli utenti di un dominio. Un archivio Active Directory può essere aperto solo in modalità di sola lettura e le applicazioni non possono aggiungere o rimuovere certificati da un archivio Active Directory con CAPICOM.

In caso di errore di CAPICOM, viene restituito un valore decimale negativo di **Err. Number** . Per altre informazioni, vedere [**\_ \_ codice di errore di CAPICOM**](capicom-error-code.md). Per informazioni sui valori decimali positivi di **Err. Number**, vedere Winerror. h.

Nell'esempio seguente viene illustrata l'apertura di un archivio Active Directory e il recupero di certificati dall'archivio.


```VB
Sub OpenADStore()
        On Error GoTo ErrorHandler
        Dim mystore As Store
        Set mystore = New Store
        
        ' Put a string that represents the name of a certificate 
        ' subject in SubjectNameCn. In the following example, 
        ' the * wildcard character is used in the string so that
        ' the Active Directory store will be searched for all 
        ' certificates with a subject name beginning with 'S.'
       
        Dim SubjectNameCn As String
        ' The following uses 'cn=' and the * wildcard character.
        ' Using this string, all certificates in the Active Directory
        ' store with a subject name beginning with an 'S' would
        ' be returned.

        SubjectNameCn = "CN=S*"
        
        ' Active Directory stores can only be opened with read-only
        ' access.
        
         mystore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE, _
              SubjectNameCn, CAPICOM_STORE_OPEN_READ_ONLY
        
        If mystore.Certificates.Count < 1 Then
               MsgBox "A certificate for " & SubjectNameCn & _
                      " was not found "
        Else
               MsgBox "The certificate has been retrieved."
        End If
        
        Set mystore = Nothing
        Exit Sub

ErrorHandler:
         
         If Err.Number > 0 Then
               MsgBox "Visual Basic error found:" & Err.Description
         Else
               MsgBox "CAPICOM error found : " & Err.Number
         End If
End Sub
```



 

 
