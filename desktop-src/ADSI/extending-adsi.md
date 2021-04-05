---
title: Estensione di ADSI
description: Con il modello di estensione ADSI è possibile associare una classe di directory al proprio oggetto COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e597d4b2dd2cf6a3b4a81f1fff3515289418b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707426"
---
# <a name="extending-adsi"></a>Estensione di ADSI

Con il modello di estensione ADSI è possibile associare una classe di directory al proprio oggetto COM. Dal punto di vista di un programmatore ADSI o di uno script writer, l'estensione diventa parte integrante di ADSI. Ad esempio, quando un nuovo dipendente viene aggiunto a Fabrikam, l'amministratore di Windows NT creerà un oggetto utente nella directory e l'amministratore delle retribuzioni dovrà configurare alcune voci nei sistemi di risorse umane per questo utente. Con un'estensione ADSI, questo processo può essere semplificato in un unico script.


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



Per altre informazioni, vedere [estensioni ADSI](adsi-extensions.md).

 

 




