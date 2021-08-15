---
title: Estensione di ADSI
description: Con il modello di estensione ADSI è possibile associare una classe di directory al proprio oggetto COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e9f5bd316fc4703cf522e2c5facfd6c32c5236da191668f6ba38ae6a904f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428454"
---
# <a name="extending-adsi"></a>Estensione di ADSI

Con il modello di estensione ADSI è possibile associare una classe di directory al proprio oggetto COM. Dal punto di vista del programmatore o del writer di script ADSI, l'estensione diventa parte integrante di ADSI. Ad esempio, quando un nuovo dipendente si unisce a Fabrikam, l'amministratore di Windows NT creerà un oggetto utente nella directory e l'amministratore delle retribuzioni dovrà configurare alcune voci nei sistemi delle risorse umane per questo utente. Con un'estensione ADSI, questo processo può essere semplificato in un unico script.


```VB
Dim usr
Dim sUserName

On Error Resume Next

sUserName = InputBox ("Enter the name of the user to add:")

Set usr = ou.Create("user", "CN=" & sUserName)

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

// Insert code to set some attributes

usr.SetInfo

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

usr.AddToPayroll  'this is a custom method from an ADSI Extension

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

Debug.Print "User: " & usr.Name & "has been created"
```



Per altre informazioni, vedere [Estensioni ADSI.](adsi-extensions.md)

 

 




