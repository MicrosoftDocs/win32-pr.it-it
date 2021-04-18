---
description: Utilizzo delle categorie pin
ms.assetid: 1ee648b3-8370-4e4d-b513-d998131512ee
title: Utilizzo delle categorie pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac58fff91821477cca51e0613772e3e5763d4d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308936"
---
# <a name="working-with-pin-categories"></a>Utilizzo delle categorie pin

Per eseguire la ricerca in un filtro per un pin con una categoria di pin specificata, è possibile usare il metodo [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) . L'esempio seguente cerca un pin di anteprima video:


```C++
int i = 0;
hr = pBuild->FindPin(
    pFilter,               // Pointer to a filter to search.
    PINDIR_OUTPUT,         // Which pin direction?
    &PIN_CATEGORY_PREVIEW, // Which category? (NULL means "any category")
    &MEDIATYPE_Video,      // What media type? (NULL means "any type")
    FALSE,                 // Must be connected?
    i,                     // Get the i'th matching pin (0 = first match)
    &pPin                  // Receives a pointer to the pin.
);
```



Il primo parametro è un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro. I tre parametri successivi specificano la direzione, la categoria del PIN e il tipo di supporto. Il valore **false** nel quinto parametro indica che il pin può essere connesso o non connesso. Per le definizioni esatte di questi parametri, fare riferimento alla documentazione relativa al metodo. Se il metodo trova un pin corrispondente, restituisce un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) nel parametro *pPin* .

Sebbene il metodo [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) sia pratico, è anche possibile scrivere funzioni helper personalizzate, se si preferisce. Per determinare la categoria di un PIN, chiamare il metodo [**IKsPropertySet:: Get**](ikspropertyset-get.md) come descritto nell'argomento [set di proprietà pin](pin-property-set.md).

Il codice seguente illustra una funzione helper che controlla se un PIN corrisponde a una categoria specificata:


```C++
// Returns TRUE if a pin matches the specified pin category.

BOOL PinMatchesCategory(IPin *pPin, REFGUID Category)
{
    BOOL bFound = FALSE;

    IKsPropertySet *pKs = NULL;
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (SUCCEEDED(hr))
    {
        GUID PinCategory;
        DWORD cbReturned;
        hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
            &PinCategory, sizeof(GUID), &cbReturned);
        if (SUCCEEDED(hr) && (cbReturned == sizeof(GUID)))
        {
            bFound = (PinCategory == Category);
        }
        pKs->Release();
    }
    return bFound;
}
```



L'esempio seguente è una funzione che cerca un PIN per categoria, simile al metodo [**FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) :


```C++
// Finds the first pin that matches a specified pin category and direction.

HRESULT FindPinByCategory(
    IBaseFilter *pFilter, // Pointer to the filter to search.
    PIN_DIRECTION PinDir, // Direction of the pin.
    REFGUID Category,     // Pin category.
    IPin **ppPin)         // Receives a pointer to the pin.
{
    *ppPin = 0;

    HRESULT hr = S_OK;
    BOOL bFound = FALSE;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;

    hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (hr = pEnum->Next(1, &pPin, 0), hr == S_OK)
    {
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            goto done;
        }
        if ((ThisPinDir == PinDir) && 
            PinMatchesCategory(pPin, Category))
        {
            *ppPin = pPin;
            (*ppPin)->AddRef();   // The caller must release the interface.
            bFound = TRUE;
            break;
        }
        SafeRelease(&pPin);
    }

done:
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    if (SUCCEEDED(hr) && !bFound)
    {
        hr = E_FAIL;
    }
    return hr;
}
```



Il codice seguente usa la funzione Previous per cercare un PIN della porta video in un filtro:


```C++
IPin *pVP; 
hr = FindPinByCategory(pFilter, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT, &pVP);
if (SUCCEEDED(hr))
{
    // Use pVP ... 
    // Release when you are done.
    pVP->Release();
}
```



Per ulteriori informazioni sui set di proprietà, consultare la documentazione di [Windows Driver Kit (WDK)](/windows-hardware/drivers/gettingstarted/) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[Imposta la proprietà pin](pin-property-set.md)
</dt> <dt>

[Filtri di acquisizione video DirectShow](directshow-video-capture-filters.md)
</dt> </dl>

 

 
