---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309013"
---
# <a name="saferelease"></a><span data-ttu-id="a7b70-103">SafeRelease</span><span class="sxs-lookup"><span data-stu-id="a7b70-103">SafeRelease</span></span>


<span data-ttu-id="a7b70-104">Molti degli esempi di codice di questa documentazione usano la funzione seguente per rilasciare i puntatori di interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="a7b70-104">Many of the code examples in this documentation use the following function to release COM interface pointers.</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> <span data-ttu-id="a7b70-105">Questa funzione non è definita in un'intestazione SDK.</span><span class="sxs-lookup"><span data-stu-id="a7b70-105">This function is not defined in an SDK header.</span></span> <span data-ttu-id="a7b70-106">Per usare questa funzione, è necessario definirla nel proprio codice.</span><span class="sxs-lookup"><span data-stu-id="a7b70-106">To use this function, you must define it in your own code.</span></span>

 

<span data-ttu-id="a7b70-107">Questa funzione rilascia il puntatore *PPT* e lo imposta su **null**.</span><span class="sxs-lookup"><span data-stu-id="a7b70-107">This function releases the pointer *ppT* and sets it equal to **NULL**.</span></span>

<span data-ttu-id="a7b70-108">Un'altra opzione consiste nell'usare una classe di puntatore intelligente, ad esempio **CComPtr**, definita nella Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="a7b70-108">Another option is to use a smart pointer class, such as **CComPtr**, which is defined in the Active Template Library (ATL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7b70-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a7b70-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7b70-110">Informazioni su Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7b70-110">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="a7b70-111">**IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="a7b70-111">**IUnknown::Release**</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
