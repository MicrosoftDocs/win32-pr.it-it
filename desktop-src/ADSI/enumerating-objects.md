---
title: Enumerazione di oggetti
description: Per visualizzare l'oggetto figlio di un contenitore, ad esempio un'unità organizzativa, enumerare l'oggetto contenitore.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855321"
---
# <a name="enumerating-objects"></a>Enumerazione di oggetti

Per visualizzare l'oggetto figlio di un contenitore, ad esempio un'unità organizzativa, enumerare l'oggetto contenitore. Per eseguire un'analogia a una file system, l'oggetto figlio corrisponderebbe ai file nella directory, mentre il contenitore, che è l'oggetto padre, corrisponderebbe alla directory stessa. È anche possibile usare l'operazione enumerate quando si desidera ottenere l'oggetto padre di un oggetto.

Quando si enumera un oggetto, in realtà si esegue l'associazione a un oggetto nella directory e viene restituita un'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) per ogni oggetto.

Nell'esempio di codice riportato di seguito viene illustrato come enumerare gli elementi figlio di un contenitore.


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



È possibile filtrare i tipi di oggetti restituiti dall'enumerazione. Per visualizzare, ad esempio, solo gli utenti e i gruppi, usare l'esempio di codice seguente prima dell'enumerazione.


```VB
Ou.Filter = Array("user", "group")
```



Se si dispone di un riferimento a un oggetto, è possibile ottenere l'elemento padre dell'oggetto utilizzando la proprietà [**padre**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Nell'esempio di codice riportato di seguito viene illustrato come eseguire l'associazione all'oggetto padre.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Per ulteriori informazioni, vedere [enumerazione di oggetti ADSI](enumerating-adsi-objects.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca di oggetti](searching-for-objects.md)
</dt> </dl>

 

 




