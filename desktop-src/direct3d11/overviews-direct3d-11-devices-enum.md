---
title: Come enumerare gli adapter
description: In questo argomento viene illustrato come utilizzare Microsoft DirectX Graphics Infrastructure (DXGI) per enumerare le schede grafiche disponibili in un computer.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af16aba0131d93a5f72732931a68f132126b5d48
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993480"
---
# <a name="how-to-enumerate-adapters"></a><span data-ttu-id="09c8d-103">Procedura: enumerare gli adapter</span><span class="sxs-lookup"><span data-stu-id="09c8d-103">How To: Enumerate Adapters</span></span>

<span data-ttu-id="09c8d-104">In questo argomento viene illustrato come utilizzare Microsoft DirectX Graphics Infrastructure (DXGI) per enumerare le schede grafiche disponibili in un computer.</span><span class="sxs-lookup"><span data-stu-id="09c8d-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to enumerate the available graphics adapters on a computer.</span></span> <span data-ttu-id="09c8d-105">Direct3D 10 e 11 possono utilizzare DXGI per enumerare gli adapter.</span><span class="sxs-lookup"><span data-stu-id="09c8d-105">Direct3D 10 and 11 can use DXGI to enumerate adapters.</span></span>

<span data-ttu-id="09c8d-106">In genere è necessario enumerare gli adapter per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="09c8d-106">You generally need to enumerate adapters for these reasons:</span></span>

-   <span data-ttu-id="09c8d-107">Per determinare il numero di schede grafiche installate in un computer.</span><span class="sxs-lookup"><span data-stu-id="09c8d-107">To determine how many graphics adapters are installed on a computer.</span></span>
-   <span data-ttu-id="09c8d-108">Per facilitare la scelta dell'adattatore da utilizzare per creare un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="09c8d-108">To help you choose which adapter to use to create a Direct3D device.</span></span>
-   <span data-ttu-id="09c8d-109">Per recuperare un oggetto [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) che è possibile usare per recuperare le funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09c8d-109">To retrieve an [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) object that you can use to retrieve device capabilities.</span></span>

<span data-ttu-id="09c8d-110">**Per enumerare gli adapter**</span><span class="sxs-lookup"><span data-stu-id="09c8d-110">**To enumerate adapters**</span></span>

1.  <span data-ttu-id="09c8d-111">Creare un oggetto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) chiamando la funzione [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) .</span><span class="sxs-lookup"><span data-stu-id="09c8d-111">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object by calling the [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) function.</span></span> <span data-ttu-id="09c8d-112">Nell'esempio di codice riportato di seguito viene illustrato come inizializzare un oggetto **IDXGIFactory** .</span><span class="sxs-lookup"><span data-stu-id="09c8d-112">The following code example demonstrates how to initialize an **IDXGIFactory** object.</span></span>
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  <span data-ttu-id="09c8d-113">Enumerare ogni adapter chiamando il metodo [**IDXGIFactory:: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) .</span><span class="sxs-lookup"><span data-stu-id="09c8d-113">Enumerate through each adapter by calling the [**IDXGIFactory::EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) method.</span></span> <span data-ttu-id="09c8d-114">Il parametro *Adapter* consente di specificare un numero di indice in base zero della scheda da enumerare.</span><span class="sxs-lookup"><span data-stu-id="09c8d-114">The *Adapter* parameter allows you to specify a zero-based index number of the adapter to enumerate.</span></span> <span data-ttu-id="09c8d-115">Se non è disponibile alcun adapter in corrispondenza dell'indice specificato, il metodo restituisce l' [**\_ errore DXGI \_ non \_ trovato**](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="09c8d-115">If no adapter is available at the specified index, the method returns [**DXGI\_ERROR\_NOT\_FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>

    <span data-ttu-id="09c8d-116">Nell'esempio di codice riportato di seguito viene illustrato come enumerare le schede in un computer.</span><span class="sxs-lookup"><span data-stu-id="09c8d-116">The following code example demonstrates how to enumerate through the adapters on a computer.</span></span>

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

<span data-ttu-id="09c8d-117">Nell'esempio di codice riportato di seguito viene illustrato come enumerare tutte le schede in un computer.</span><span class="sxs-lookup"><span data-stu-id="09c8d-117">The following code example demonstrates how to enumerate all adapters on a computer.</span></span>

> [!Note]  
> <span data-ttu-id="09c8d-118">Per Direct3D 11,0 e versioni successive, è consigliabile che le app usino sempre [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) e [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) .</span><span class="sxs-lookup"><span data-stu-id="09c8d-118">For Direct3D 11.0 and later, we recommend that apps always use [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) and [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) instead.</span></span>

 


```C++
std::vector <IDXGIAdapter*> EnumerateAdapters(void)
{
    IDXGIAdapter * pAdapter; 
    std::vector <IDXGIAdapter*> vAdapters; 
    IDXGIFactory* pFactory = NULL; 
    

    // Create a DXGIFactory object.
    if(FAILED(CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)))
    {
        return vAdapters;
    }


    for ( UINT i = 0;
          pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND;
          ++i )
    {
        vAdapters.push_back(pAdapter); 
    } 


    if(pFactory)
    {
        pFactory->Release();
    }

    return vAdapters;

}
```



## <a name="related-topics"></a><span data-ttu-id="09c8d-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="09c8d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c8d-120">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="09c8d-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 