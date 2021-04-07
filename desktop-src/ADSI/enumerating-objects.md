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
# <a name="enumerating-objects"></a><span data-ttu-id="abd07-104">Enumerazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="abd07-104">Enumerating Objects</span></span>

<span data-ttu-id="abd07-105">Per visualizzare l'oggetto figlio di un contenitore, ad esempio un'unità organizzativa, enumerare l'oggetto contenitore.</span><span class="sxs-lookup"><span data-stu-id="abd07-105">To view the child object of a container, such as an organizational unit (OU), enumerate the container object.</span></span> <span data-ttu-id="abd07-106">Per eseguire un'analogia a una file system, l'oggetto figlio corrisponderebbe ai file nella directory, mentre il contenitore, che è l'oggetto padre, corrisponderebbe alla directory stessa.</span><span class="sxs-lookup"><span data-stu-id="abd07-106">To make an analogy to a file system, the child object would correspond to files in the directory, while the container, which is the parent object, would correspond to the directory itself.</span></span> <span data-ttu-id="abd07-107">È anche possibile usare l'operazione enumerate quando si desidera ottenere l'oggetto padre di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="abd07-107">You may also use the enumerate operation when you want to get the parent object of an object.</span></span>

<span data-ttu-id="abd07-108">Quando si enumera un oggetto, in realtà si esegue l'associazione a un oggetto nella directory e viene restituita un'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="abd07-108">When you enumerate an object, you actually bind to an object in the directory, and an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface is returned on each object.</span></span>

<span data-ttu-id="abd07-109">Nell'esempio di codice riportato di seguito viene illustrato come enumerare gli elementi figlio di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="abd07-109">The following code example shows how to enumerate the children of a container.</span></span>


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



<span data-ttu-id="abd07-110">È possibile filtrare i tipi di oggetti restituiti dall'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="abd07-110">You can filter the types of objects returned from the enumeration.</span></span> <span data-ttu-id="abd07-111">Per visualizzare, ad esempio, solo gli utenti e i gruppi, usare l'esempio di codice seguente prima dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="abd07-111">For example, to display only users and groups, use the following code example before the enumeration.</span></span>


```VB
Ou.Filter = Array("user", "group")
```



<span data-ttu-id="abd07-112">Se si dispone di un riferimento a un oggetto, è possibile ottenere l'elemento padre dell'oggetto utilizzando la proprietà [**padre**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="abd07-112">If you have an object reference, you can get the object's parent using the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent**](iads-property-methods.md) property.</span></span> <span data-ttu-id="abd07-113">Nell'esempio di codice riportato di seguito viene illustrato come eseguire l'associazione all'oggetto padre.</span><span class="sxs-lookup"><span data-stu-id="abd07-113">The following code example shows how to bind to the parent object.</span></span>


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



<span data-ttu-id="abd07-114">Per ulteriori informazioni, vedere [enumerazione di oggetti ADSI](enumerating-adsi-objects.md).</span><span class="sxs-lookup"><span data-stu-id="abd07-114">For more information, see [Enumerating ADSI Objects](enumerating-adsi-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="abd07-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="abd07-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abd07-116">Ricerca di oggetti</span><span class="sxs-lookup"><span data-stu-id="abd07-116">Searching for Objects</span></span>](searching-for-objects.md)
</dt> </dl>

 

 




