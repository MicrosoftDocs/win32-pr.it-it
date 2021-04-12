---
description: Fornire un allocatore personalizzato
ms.assetid: 4ce2db4b-c901-43a5-b905-7d6d923c940b
title: Fornire un allocatore personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e85a8d133ee5b686e25bc0d7d4a3e2444cb2791
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401159"
---
# <a name="providing-a-custom-allocator"></a>Fornire un allocatore personalizzato

In questa sezione viene descritto come fornire un allocatore personalizzato per un filtro. Sono descritte solo le connessioni [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , ma i passaggi per una connessione [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) sono simili.

Definire innanzitutto una classe C++ per l'allocatore. L'allocatore può derivare da una delle classi di allocatore standard, [**CBaseAllocator**](cbaseallocator.md) o [**CMemAllocator**](cmemallocator.md), oppure è possibile creare una classe allocator completamente nuova. Se si crea una nuova classe, deve esporre l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

I passaggi rimanenti variano a seconda che l'allocatore appartenga a un pin di input o a un pin di output sul filtro. I pin di input svolgono un ruolo diverso rispetto ai pin di output durante la fase di negoziazione dell'allocatore, perché il pin di output seleziona infine l'allocatore.

**Fornire un allocatore personalizzato per un pin di input**

Per fornire un allocatore per un pin di input, eseguire l'override del metodo [**CBaseInputPin:: Getallocator**](cbaseinputpin-getallocator.md) del PIN di input. All'interno di questo metodo, controllare la variabile membro **\_ pAllocator m** . Se questa variabile è non **null**, significa che l'allocatore è già stato selezionato per questa connessione, quindi il metodo **getallocator** deve restituire un puntatore a tale allocatore. Se **m \_ PAllocator** è **null**, significa che l'allocatore non è stato selezionato, quindi il metodo **getallocator** deve restituire un puntatore all'allocatore preferito del PIN di input. In tal caso, creare un'istanza dell'allocatore personalizzato e restituire il relativo puntatore [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Il codice seguente illustra come implementare il metodo **Getallocator** :


```C++
STDMETHODIMP CMyInputPin::GetAllocator(IMemAllocator **ppAllocator)
{
    CheckPointer(ppAllocator, E_POINTER);
    if (m_pAllocator)  
    {
        // We already have an allocator, so return that one.
        *ppAllocator = m_pAllocator;
        (*ppAllocator)->AddRef();
        return S_OK;
    }

    // No allocator yet, so propose our custom allocator. The exact code
    // here will depend on your custom allocator class definition.
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface to the caller.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Quando il filtro upstream seleziona un allocatore, chiama il metodo [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) del PIN di input. Eseguire l'override del metodo [**CBaseInputPin:: NotifyAllocator**](cbaseinputpin-notifyallocator.md) per verificare le proprietà dell'allocatore. In alcuni casi, il pin di input potrebbe rifiutare l'allocatore se non è l'allocatore personalizzato, sebbene ciò possa causare un errore dell'intera connessione del PIN.

**Fornire un allocatore personalizzato per un pin di output**

Per fornire un allocatore per un pin di output, eseguire l'override del metodo [**CBaseOutputPin:: InitAllocator**](cbaseoutputpin-initallocator.md) per creare un'istanza dell'allocatore:


```C++
HRESULT MyOutputPin::InitAllocator(IMemAllocator **ppAllocator)
{
    HRESULT hr = S_OK;
    CMyAllocator *pAlloc = new CMyAllocator(&hr);
    if (!pAlloc)
    {
        return E_OUTOFMEMORY;
    }

    if (FAILED(hr))
    {
        delete pAlloc;
        return hr;
    }

    // Return the IMemAllocator interface.
    return pAlloc->QueryInterface(IID_IMemAllocator, (void**)ppAllocator);
}
```



Per impostazione predefinita, la classe [**CBaseOutputPin**](cbaseoutputpin.md) richiede innanzitutto un allocatore dal pin di input. Se l'allocatore non è adatto, il pin di output crea il proprio allocatore. Per forzare la connessione a usare l'allocatore personalizzato, eseguire l'override del metodo [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) . Tuttavia, tenere presente che questo può impedire la connessione del PIN di output con determinati filtri, perché l'altro filtro potrebbe richiedere anche un allocatore personalizzato. Una terza opzione consiste nel modificare l'ordine: provare prima l'allocatore personalizzato e quindi eseguire il fallback all'allocatore dell'altro filtro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Negozi di allocatori](negotiating-allocators.md)
</dt> </dl>

 

 



