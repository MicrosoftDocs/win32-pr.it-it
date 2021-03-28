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
# <a name="how-to-enumerate-adapters"></a>Procedura: enumerare gli adapter

In questo argomento viene illustrato come utilizzare Microsoft DirectX Graphics Infrastructure (DXGI) per enumerare le schede grafiche disponibili in un computer. Direct3D 10 e 11 possono utilizzare DXGI per enumerare gli adapter.

In genere è necessario enumerare gli adapter per i motivi seguenti:

-   Per determinare il numero di schede grafiche installate in un computer.
-   Per facilitare la scelta dell'adattatore da utilizzare per creare un dispositivo Direct3D.
-   Per recuperare un oggetto [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) che è possibile usare per recuperare le funzionalità del dispositivo.

**Per enumerare gli adapter**

1.  Creare un oggetto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) chiamando la funzione [**CreateDXGIFactory**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory) . Nell'esempio di codice riportato di seguito viene illustrato come inizializzare un oggetto **IDXGIFactory** .
    ```
    IDXGIFactory * pFactory = NULL;

    CreateDXGIFactory(__uuidof(IDXGIFactory) ,(void**)&pFactory)
    ```

    

2.  Enumerare ogni adapter chiamando il metodo [**IDXGIFactory:: EnumAdapters**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters) . Il parametro *Adapter* consente di specificare un numero di indice in base zero della scheda da enumerare. Se non è disponibile alcun adapter in corrispondenza dell'indice specificato, il metodo restituisce l' [**\_ errore DXGI \_ non \_ trovato**](/windows/desktop/direct3ddxgi/dxgi-error).

    Nell'esempio di codice riportato di seguito viene illustrato come enumerare le schede in un computer.

    ```
    for (UINT i = 0; 
         pFactory->EnumAdapters(i, &pAdapter) != DXGI_ERROR_NOT_FOUND; 
         ++i) 
    { ... }
    ```

    

Nell'esempio di codice riportato di seguito viene illustrato come enumerare tutte le schede in un computer.

> [!Note]  
> Per Direct3D 11,0 e versioni successive, è consigliabile che le app usino sempre [**IDXGIFactory1**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1) e [**CreateDXGIFactory1**](/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1) .

 


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

 

 