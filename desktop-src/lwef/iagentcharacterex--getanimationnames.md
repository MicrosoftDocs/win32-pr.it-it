---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/14/2021
ms.locfileid: "106320062"
---
# <a name="iagentcharacterexgetanimationnames"></a><span data-ttu-id="6df2f-103">IAgentCharacterEx::GetAnimationNames</span><span class="sxs-lookup"><span data-stu-id="6df2f-103">IAgentCharacterEx::GetAnimationNames</span></span>

<span data-ttu-id="6df2f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6df2f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

<span data-ttu-id="6df2f-105">Recupera i nomi di animazione per un carattere.</span><span class="sxs-lookup"><span data-stu-id="6df2f-105">Retrieves the animation names for a character.</span></span>

-   <span data-ttu-id="6df2f-106">Restituisce **\_ OK** per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6df2f-106">Returns **S\_OK** to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6df2f-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="6df2f-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="6df2f-108">Indirizzo dell'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per la raccolta di animazioni del carattere.</span><span class="sxs-lookup"><span data-stu-id="6df2f-108">The address of the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the character's animation collection.</span></span>

</dd> </dl>

<span data-ttu-id="6df2f-109">Questa funzione consente di enumerare i nomi delle animazioni per un carattere.</span><span class="sxs-lookup"><span data-stu-id="6df2f-109">This function enables you to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="6df2f-110">Gli elementi della raccolta non hanno proprietà, quindi non è possibile accedere direttamente a singoli elementi.</span><span class="sxs-lookup"><span data-stu-id="6df2f-110">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span> <span data-ttu-id="6df2f-111">Per accedere alla raccolta, eseguire una query su punkEnum per l'interfaccia IEnumVARIANT:</span><span class="sxs-lookup"><span data-stu-id="6df2f-111">To access the collection, query punkEnum for the IEnumVARIANT interface:</span></span>


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> <span data-ttu-id="6df2f-112">Per i caratteri ACF, la raccolta restituisce tutte le animazioni definite per il carattere, aggiungendo quelle che sono state recuperate con il metodo [**Get**](https://www.bing.com/search?q=**Get**) .</span><span class="sxs-lookup"><span data-stu-id="6df2f-112">For ACF characters, the collection returns all the animations that have been defined for the character, adding to the ones that have been retrieved with the [**Get**](https://www.bing.com/search?q=**Get**) method.</span></span>
