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
# <a name="using-the-filter-mapper"></a><span data-ttu-id="9c9b3-103">Uso del mapper dei filtri</span><span class="sxs-lookup"><span data-stu-id="9c9b3-103">Using the Filter Mapper</span></span>

<span data-ttu-id="9c9b3-104">Il [mapper del filtro](filter-mapper.md) è un oggetto com che enumera i filtri DirectShow in base a diversi criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-104">The [Filter Mapper](filter-mapper.md) is a COM object that enumerates DirectShow filters based on various search criteria.</span></span> <span data-ttu-id="9c9b3-105">Il mapper del filtro può essere meno efficiente rispetto all'enumeratore di dispositivi di sistema, pertanto se sono necessari filtri da una determinata categoria, è necessario usare l'enumeratore di dispositivo di sistema.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-105">The Filter Mapper can be less efficient than the System Device Enumerator, so if you need filters from a particular category, you should use the System Device Enumerator.</span></span> <span data-ttu-id="9c9b3-106">Tuttavia, se è necessario individuare un filtro che supporti una determinata combinazione di tipi di supporto, ma non rientra in una categoria non crittografata, potrebbe essere necessario utilizzare il mapper dei filtri.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-106">But if you need to locate a filter that supports a certain combination of media types, but does not fall into a clear-cut category, you might need to use the Filter Mapper.</span></span> <span data-ttu-id="9c9b3-107">Un esempio potrebbe essere un filtro Renderer o un filtro decodificatore.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-107">(An example would be a renderer filter or a decoder filter.)</span></span>

<span data-ttu-id="9c9b3-108">Il mapper del filtro espone l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="9c9b3-108">The Filter Mapper exposes the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span> <span data-ttu-id="9c9b3-109">Per cercare un filtro, chiamare il metodo [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) .</span><span class="sxs-lookup"><span data-stu-id="9c9b3-109">To search for a filter, call the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method.</span></span> <span data-ttu-id="9c9b3-110">Questo metodo accetta diversi parametri che definiscono i criteri di ricerca e restituisce un enumeratore per i filtri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-110">This method takes several parameters that define the search criteria, and returns an enumerator for the matching filters.</span></span> <span data-ttu-id="9c9b3-111">L'enumeratore supporta l'interfaccia [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) e fornisce un moniker univoco per ogni filtro corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-111">The enumerator supports the [**IEnumMoniker**](/windows/win32/api/objidl/nn-objidl-ienummoniker) interface, and supplies a unique moniker for each matching filter.</span></span>

<span data-ttu-id="9c9b3-112">Nell'esempio seguente vengono enumerati i filtri che accettano input video digitale (DV) e hanno almeno un pin di output di qualsiasi tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-112">The following example enumerates filters that accept digital video (DV) input and have at least one output pin, of any media type.</span></span> <span data-ttu-id="9c9b3-113">Il filtro del [decodificatore video DV](dv-video-decoder-filter.md) corrisponde a questi criteri.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-113">(The [DV Video Decoder](dv-video-decoder-filter.md) filter matches these criteria.)</span></span>


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



<span data-ttu-id="9c9b3-114">Il metodo [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) ha un numero di parametri piuttosto elevato, commentati nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-114">The [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method has a fairly large number of parameters, which are commented in the example.</span></span> <span data-ttu-id="9c9b3-115">I valori significativi per questo esempio includono:</span><span class="sxs-lookup"><span data-stu-id="9c9b3-115">The significant ones for this example include:</span></span>

-   <span data-ttu-id="9c9b3-116">Valore minimo di Merit: il filtro deve avere un valore Merit superiore a MERIT non \_ \_ \_ usare.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-116">Minimum merit value: The filter must have a merit value above MERIT\_DO\_NOT\_USE.</span></span>
-   <span data-ttu-id="9c9b3-117">Tipi di input: il chiamante passa una matrice contenente coppie di tipi e sottotipi principali.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-117">Input types: The caller passes an array containing pairs of major types and subtypes.</span></span> <span data-ttu-id="9c9b3-118">Solo i filtri che supportano almeno una di queste coppie corrisponderanno.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-118">Only filters that support at least one of these pairs will match.</span></span>
-   <span data-ttu-id="9c9b3-119">Corrispondenza esatta: un filtro può registrare i valori **null** per il tipo principale, il sottotipo, la categoria del PIN o il supporto.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-119">Exact match: A filter can register **NULL** values for major type, subtype, pin category, or medium.</span></span> <span data-ttu-id="9c9b3-120">A meno che non si specifichi la corrispondenza esatta, un valore **null** funge da carattere jolly e corrisponde a qualsiasi valore specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-120">Unless you specify exact matching, a **NULL** value acts as a wildcard, matching any value that you specify.</span></span> <span data-ttu-id="9c9b3-121">Con la corrispondenza esatta, il filtro deve corrispondere esattamente ai criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-121">With exact matching, the filter must exactly match your criteria.</span></span> <span data-ttu-id="9c9b3-122">Tuttavia, se si assegna un parametro **null** nei criteri di ricerca, viene sempre usato come carattere jolly o come valore "Don ' t Care", che corrisponde a qualsiasi filtro.</span><span class="sxs-lookup"><span data-stu-id="9c9b3-122">However, if you give a **NULL** parameter in the search criteria, it always acts as a wildcard or "don't care" value, matching any filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c9b3-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c9b3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c9b3-124">Enumerazione dei dispositivi e dei filtri</span><span class="sxs-lookup"><span data-stu-id="9c9b3-124">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="9c9b3-125">Connessione intelligente</span><span class="sxs-lookup"><span data-stu-id="9c9b3-125">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 
