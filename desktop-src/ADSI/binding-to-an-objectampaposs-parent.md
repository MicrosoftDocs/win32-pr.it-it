---
title: Associazione all'elemento padre di un oggetto
description: In ADSI ogni oggetto directory è rappresentato da un oggetto ADSI COM che espone l'interfaccia IADs.
ms.assetid: 3740e862-4cfe-484c-8c8e-3923c64cdd47
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associazione all'elemento padre di un oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d72f3b3db3af9f13892494d3855dc5dcb2a74d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855349"
---
# <a name="binding-to-an-objects-parent"></a><span data-ttu-id="9dddf-104">Associazione all'elemento padre di un oggetto</span><span class="sxs-lookup"><span data-stu-id="9dddf-104">Binding to an Object's Parent</span></span>

<span data-ttu-id="9dddf-105">In ADSI ogni oggetto directory è rappresentato da un oggetto ADSI COM che espone l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="9dddf-105">In ADSI, every directory object is represented by an ADSI COM object that exposes the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="9dddf-106">Per ottenere il contenitore padre di un oggetto, usare il metodo [**IADs:: Get \_ Parent**](iads-property-methods.md) per ottenere ADsPath dell'oggetto padre, quindi eseguire l'associazione a ADsPath dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="9dddf-106">To obtain the parent container of an object, use the [**IADs::get\_Parent**](iads-property-methods.md) method to obtain the ADsPath of the parent object, then bind to the ADsPath of the parent.</span></span>

<span data-ttu-id="9dddf-107">Nell'esempio di codice C++ riportato di seguito viene illustrato come ottenere l'elemento padre di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="9dddf-107">The following C++ code example shows how to obtain the parent of an object .</span></span>


```C++
HRESULT GetParentObject(IADs *pObject,   // Pointer to the object whose parent to bind to.
                        IADs **ppParent) // Return a pointer to the parent object.
{
    if(NULL == ppParent)
    {
        return E_INVALIDARG;
    }
 
    *ppParent = NULL;

    if(NULL == pObject)
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    BSTR bstr;

    // Get the ADsPath of the parent.
    hr = pObject->get_Parent(&bstr);
    if(SUCCEEDED(hr))
    {
        // Bind to the parent.
        hr = ADsOpenObject(bstr,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)ppParent);

        SysFreeString(bstr);
    }

    return hr;
}
```



 

 




