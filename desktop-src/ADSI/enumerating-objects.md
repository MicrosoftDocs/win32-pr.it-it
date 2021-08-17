---
title: Enumerazione di oggetti
description: Per visualizzare l'oggetto figlio di un contenitore, ad esempio un'unità organizzativa, enumerare l'oggetto contenitore.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerazione di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e4bcead2d3fc8f98daeada89cdd10b3ad30bed855563efd89b3eebce8995f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961950"
---
# <a name="enumerating-objects"></a>Enumerazione di oggetti

Per visualizzare l'oggetto figlio di un contenitore, ad esempio un'unità organizzativa, enumerare l'oggetto contenitore. Per fare un'analogia con un file system, l'oggetto figlio corrisponderebbe ai file nella directory, mentre il contenitore, che è l'oggetto padre, corrisponderebbe alla directory stessa. È anche possibile usare l'operazione di enumerazione quando si desidera ottenere l'oggetto padre di un oggetto .

Quando si enumera un oggetto, si esegue effettivamente l'associazione a un oggetto nella directory e viene restituita [**un'interfaccia IAD**](/windows/desktop/api/Iads/nn-iads-iads) per ogni oggetto.

Nell'esempio di codice seguente viene illustrato come enumerare gli elementi figlio di un contenitore.


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



È possibile filtrare i tipi di oggetti restituiti dall'enumerazione . Ad esempio, per visualizzare solo utenti e gruppi, usare l'esempio di codice seguente prima dell'enumerazione .


```VB
Ou.Filter = Array("user", "group")
```



Se si dispone di un riferimento a un oggetto, è possibile ottenere l'elemento padre dell'oggetto usando la [**proprietà padre IADs.**](/windows/desktop/api/Iads/nn-iads-iads) [](iads-property-methods.md) Nell'esempio di codice seguente viene illustrato come eseguire l'associazione all'oggetto padre.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Per altre informazioni, vedere [Enumerazione di oggetti ADSI.](enumerating-adsi-objects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca di oggetti](searching-for-objects.md)
</dt> </dl>

 

 




