---
title: Codice di esempio per l'eliminazione di utenti in un server membro o Windows 2000 Professional
description: Questo argomento contiene un esempio di codice che illustra come eliminare un utente in un server membro o in una workstation.
ms.assetid: 04469061-f95c-4810-99d0-03d98b70d3d3
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory , eliminazione di utenti in un server membro o Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2da6ad3a0c8bacf10dbf4e0210e35076d4d4bf9c76b082c861428ae3198f14d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118190744"
---
# <a name="example-code-for-deleting-users-on-a-member-server-or-windows-2000-professional"></a>Codice di esempio per l'eliminazione di utenti in un server membro o Windows 2000 Professional

Il codice Visual Basic seguente elimina un utente in un server membro o in una workstation.


```VB
Dim cont As IADsContainer
Dim oGroup As IADsGroup

'Example: Deleting a user on a member server or workstation
 
''''''''''''''''''''
'Parse the arguments
''''''''''''''''''''
On Error Resume Next
sComputer = InputBox("This script deletes a user from a member " _
                     & "server or workstation." _
                     & vbCrLf & vbCrLf _
                     & "Specify the computer name:")
If sComputer = "" Then
    Exit Sub
End If

sUser = InputBox("Specify the user name:")
If sUser = "" Then
    Exit Sub
End If
 
''''''''''''''''''''
'Bind to the computer
''''''''''''''''''''
Set cont = GetObject("WinNT://" & sComputer & ",computer")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
''''''''''''''''''''
'Delete the user
''''''''''''''''''''
cont.Delete "user", sUser

If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADsContainer::Delete method"
End If
 
strText = "The user " & sUser & " was deleted on computer " _
          & sComputer & "."
 
Call show_users(strText, sComputer) 
''''''''''''''''''''
'Display subroutines
''''''''''''''''''''
Sub show_users(strText, strName)
    MsgBox strText, vbInformation, "Delete user on " & strName
End Sub
```



 

 




