---
description: Uso del mapper dei filtri
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Uso del mapper dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d7acf85a7b415fc161cd21e17d069b46c3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883097"
---
# <a name="using-the-filter-mapper"></a>Uso del mapper dei filtri

Il [mapper del filtro](filter-mapper.md) è un oggetto com che enumera i filtri DirectShow in base a diversi criteri di ricerca. Il mapper del filtro può essere meno efficiente rispetto all'enumeratore di dispositivi di sistema, pertanto se sono necessari filtri da una determinata categoria, è necessario usare l'enumeratore di dispositivo di sistema. Tuttavia, se è necessario individuare un filtro che supporti una determinata combinazione di tipi di supporto, ma non rientra in una categoria non crittografata, potrebbe essere necessario utilizzare il mapper dei filtri. Un esempio potrebbe essere un filtro Renderer o un filtro decodificatore.

Il mapper del filtro espone l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) . Per cercare un filtro, chiamare il metodo [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Questo metodo accetta diversi parametri che definiscono i criteri di ricerca e restituisce un enumeratore per i filtri corrispondenti. L'enumeratore supporta l'interfaccia [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) e fornisce un moniker univoco per ogni filtro corrispondente.

Nell'esempio seguente vengono enumerati i filtri che accettano input video digitale (DV) e hanno almeno un pin di output di qualsiasi tipo di supporto. Il filtro del [decodificatore video DV](dv-video-decoder-filter.md) corrisponde a questi criteri.


```C++
IFilterMapper2 *pMapper = NULL;
IEnumMoniker *pEnum = NULL;

hr = CoCreateInstance(CLSID_FilterMapper2, 
    NULL, CLSCTX_INPROC, IID_IFilterMapper2, 
    (void **) &pMapper);

if (FAILED(hr))
{
    // Error handling omitted for clarity.
}

GUID arrayInTypes[2];
arrayInTypes[0] = MEDIATYPE_Video;
arrayInTypes[1] = MEDIASUBTYPE_dvsd;

hr = pMapper->EnumMatchingFilters(
        &pEnum,
        0,                  // Reserved.
        TRUE,               // Use exact match?
        MERIT_DO_NOT_USE+1, // Minimum merit.
        TRUE,               // At least one input pin?
        1,                  // Number of major type/subtype pairs for input.
        arrayInTypes,       // Array of major type/subtype pairs for input.
        NULL,               // Input medium.
        NULL,               // Input pin category.
        FALSE,              // Must be a renderer?
        TRUE,               // At least one output pin?
        0,                  // Number of major type/subtype pairs for output.
        NULL,               // Array of major type/subtype pairs for output.
        NULL,               // Output medium.
        NULL);              // Output pin category.

// Enumerate the monikers.
IMoniker *pMoniker;
ULONG cFetched;
while (pEnum->Next(1, &pMoniker, &cFetched) == S_OK)
{
    IPropertyBag *pPropBag = NULL;
    hr = pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
       (void **)&pPropBag);

    if (SUCCEEDED(hr))
    {
        // To retrieve the friendly name of the filter, do the following:
        VARIANT varName;
        VariantInit(&varName);
        hr = pPropBag->Read(L"FriendlyName", &varName, 0);
        if (SUCCEEDED(hr))
        {
            // Display the name in your UI somehow.
        }
        VariantClear(&varName);

        // To create an instance of the filter, do the following:
        IBaseFilter *pFilter;
        hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, (void**)&pFilter);
        // Now add the filter to the graph. Remember to release pFilter later.
    
        // Clean up.
        pPropBag->Release();
    }
    pMoniker->Release();
}

// Clean up.
pMapper->Release();
pEnum->Release();
```



Il metodo [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) ha un numero di parametri piuttosto elevato, commentati nell'esempio. I valori significativi per questo esempio includono:

-   Valore minimo di Merit: il filtro deve avere un valore Merit superiore a MERIT non \_ \_ \_ usare.
-   Tipi di input: il chiamante passa una matrice contenente coppie di tipi e sottotipi principali. Solo i filtri che supportano almeno una di queste coppie corrisponderanno.
-   Corrispondenza esatta: un filtro può registrare i valori **null** per il tipo principale, il sottotipo, la categoria del PIN o il supporto. A meno che non si specifichi la corrispondenza esatta, un valore **null** funge da carattere jolly e corrisponde a qualsiasi valore specificato dall'utente. Con la corrispondenza esatta, il filtro deve corrispondere esattamente ai criteri specificati. Tuttavia, se si assegna un parametro **null** nei criteri di ricerca, viene sempre usato come carattere jolly o come valore "Don ' t Care", che corrisponde a qualsiasi filtro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione dei dispositivi e dei filtri](enumerating-devices-and-filters.md)
</dt> <dt>

[Connessione intelligente](intelligent-connect.md)
</dt> </dl>

 

 
