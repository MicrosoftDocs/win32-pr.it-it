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
# <a name="extending-adsi"></a><span data-ttu-id="ce549-103">Estensione di ADSI</span><span class="sxs-lookup"><span data-stu-id="ce549-103">Extending ADSI</span></span>

<span data-ttu-id="ce549-104">Con il modello di estensione ADSI è possibile associare una classe di directory al proprio oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="ce549-104">With the ADSI extension model, you can associate a directory class with your own COM object.</span></span> <span data-ttu-id="ce549-105">Dal punto di vista di un programmatore ADSI o di uno script writer, l'estensione diventa parte integrante di ADSI.</span><span class="sxs-lookup"><span data-stu-id="ce549-105">From an ADSI programmer or script writer's perspective, the extension becomes an integral part of ADSI.</span></span> <span data-ttu-id="ce549-106">Ad esempio, quando un nuovo dipendente viene aggiunto a Fabrikam, l'amministratore di Windows NT creerà un oggetto utente nella directory e l'amministratore delle retribuzioni dovrà configurare alcune voci nei sistemi di risorse umane per questo utente.</span><span class="sxs-lookup"><span data-stu-id="ce549-106">For example, when a new employee joins Fabrikam, the Windows NT administrator will create a user object in the directory and the payroll administrator will need to set up some entries in the human resource systems for this user.</span></span> <span data-ttu-id="ce549-107">Con un'estensione ADSI, questo processo può essere semplificato in un unico script.</span><span class="sxs-lookup"><span data-stu-id="ce549-107">With an ADSI extension, this process can be streamlined into one single script.</span></span>


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



<span data-ttu-id="ce549-108">Per altre informazioni, vedere [estensioni ADSI](adsi-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ce549-108">For more information, see [ADSI Extensions](adsi-extensions.md).</span></span>

 

 




