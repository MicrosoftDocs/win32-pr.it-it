---
title: Come enumerare gli adapter
description: Questo argomento illustra come usare Microsoft DirectX Graphic Infrastructure (DXGI) per enumerare le schede grafiche disponibili in un computer.
ms.assetid: f8ef981c-363e-4ac8-8734-69c68f346950
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa74a41f95095c4de9ad58615c5b860153c72d1fcd706286b295653a8004d187
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098256"
---
# <a name="how-to-enumerate-adapters"></a>Procedura: Enumerare gli adapter

Questo argomento illustra come usare Microsoft DirectX Graphic Infrastructure (DXGI) per enumerare le schede grafiche disponibili in un computer. Direct3D 10 e 11 possono usare DXGI per enumerare le schede.

In genere è necessario enumerare gli adapter per i motivi seguenti:

-   Per determinare il numero di schede grafiche installate in un computer.
-   Per facilitare la scelta dell'adattatore da usare per creare un dispositivo Direct3D.
-   Per recuperare un [**oggetto IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) che è possibile usare per recuperare le funzionalità del dispositivo.

**Per enumerare gli adapter**

1.  Creare un [**oggetto IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) chiamando la [**funzione CreateDXGIFactory.**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) Nell'esempio di codice seguente viene illustrato come inizializzare **un oggetto IDXGIFactory.**
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  Enumerare ogni adattatore chiamando il [**metodo IDXGIFactory::EnumAdapters.**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) Il *parametro Adapter* consente di specificare un numero di indice in base zero dell'adattatore da enumerare. Se non è disponibile alcun adattatore in corrispondenza dell'indice specificato, il metodo restituisce [**DXGI \_ ERROR \_ NOT \_ FOUND**](/windows/desktop/direct3ddxgi/dxgi-error).

    Nell'esempio di codice seguente viene illustrato come enumerare tramite le schede in un computer.

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

Nell'esempio di codice seguente viene illustrato come enumerare tutte le schede in un computer.

> [!Note]  
> Per Direct3D 11.0 e versioni successive, è consigliabile che le app usino sempre [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) e [**CreateDXGIFactory1.**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1)

 


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 