---
description: I certificati possono essere recuperati da un archivio di Active Directory in cui sono archiviati i certificati degli utenti di un dominio.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Apertura dell'archivio di Active Directory e recupero dei certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2dc5810e97669e40b27bc374bee09f16c0a7c9a3b2bd4a1fa2951e1249a737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979122"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a>Apertura dell'archivio di Active Directory e recupero dei certificati

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece il .NET Framework per implementare le funzionalità di sicurezza. Per altre informazioni, vedere [Alternative all'uso di CAPICOM.](alternatives-to-using-capicom.md)\]

[*I*](../secgloss/c-gly.md) certificati possono essere recuperati da un archivio di Active Directory in cui sono archiviati i certificati degli utenti di un dominio. Un archivio di Active Directory può essere aperto solo in modalità di sola lettura e le applicazioni non possono aggiungere o rimuovere certificati da un archivio di Active Directory tramite CAPICOM.

In caso di errore CAPICOM, viene restituito un valore decimale negativo **Err.Number.** Per altre informazioni, vedere [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Per informazioni sui valori decimali positivi **di Err.Number,** vedere Winerror.h.

L'esempio seguente illustra l'apertura di un archivio di Active Directory e il recupero di certificati da tale archivio.


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



 

 
