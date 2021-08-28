---
description: Uso di Filter Mapper
ms.assetid: 3f774350-4508-437f-98d1-cca91220f339
title: Uso di Filter Mapper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48758c40b97477200b4fab1215eaccac53823771add86d6a8b915370776495a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049612"
---
# <a name="using-the-filter-mapper"></a>Uso di Filter Mapper

Filter [Mapper è](filter-mapper.md) un oggetto COM che enumera DirectShow filtri in base a vari criteri di ricerca. Il filtro mapper può essere meno efficiente rispetto all'enumeratore dispositivo di sistema, quindi se sono necessari filtri da una determinata categoria, è consigliabile usare l'enumeratore dispositivo di sistema. Tuttavia, se è necessario individuare un filtro che supporta una determinata combinazione di tipi di supporti, ma non rientra in una categoria chiara, potrebbe essere necessario usare Il mapper filtri. Un esempio è un filtro renderer o un filtro decodificatore.

Filter Mapper espone [**l'interfaccia IFilterMapper2.**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) Per cercare un filtro, chiamare il [**metodo IFilterMapper2::EnumMatchingFilters.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) Questo metodo accetta diversi parametri che definiscono i criteri di ricerca e restituisce un enumeratore per i filtri corrispondenti. L'enumeratore supporta [**l'interfaccia IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) e fornisce un moniker univoco per ogni filtro corrispondente.

Nell'esempio seguente vengono enumerati i filtri che accettano l'input video digitale (DV) e hanno almeno un pin di output di qualsiasi tipo di supporto. Il filtro [decodificatore video DV](dv-video-decoder-filter.md) corrisponde a questi criteri.


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



Il [**metodo EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) ha un numero piuttosto elevato di parametri, commentati nell'esempio. I valori significativi per questo esempio includono:

-   Valore minimo di merito: il filtro deve avere un valore di merito superiore a MERIT \_ DO \_ NOT \_ USE.
-   Tipi di input: il chiamante passa una matrice contenente coppie di tipi principali e sottotipi. Solo i filtri che supportano almeno una di queste coppie corrisponderanno.
-   Corrispondenza esatta: un filtro può registrare **valori NULL** per il tipo principale, il sottotipo, la categoria pin o il supporto. A meno che non si specifica una corrispondenza esatta, un **valore NULL** funge da carattere jolly, corrispondente a qualsiasi valore specificato. Con la corrispondenza esatta, il filtro deve corrispondere esattamente ai criteri. Tuttavia, se si assegna un **parametro NULL** nei criteri di ricerca, questo funge sempre da carattere jolly o da valore "don't care", corrispondente a qualsiasi filtro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md)
</dt> <dt>

[Gestione Connessione](intelligent-connect.md)
</dt> </dl>

 

 
