---
description: Uso di DMO in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso di DMO in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdddc643d39798dc09807e9ecfa15c38a6e0c2cf
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908689"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="c0bd2-103">Uso di DMO in DirectShow</span><span class="sxs-lookup"><span data-stu-id="c0bd2-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="c0bd2-104">Le applicazioni basate su DirectShow possono usare dmo in un grafico di filtro tramite il filtro [Wrapper DMO.](dmo-wrapper-filter.md)</span><span class="sxs-lookup"><span data-stu-id="c0bd2-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="c0bd2-105">Questo filtro aggrega un DMO e gestisce tutti i dettagli dell'uso di DMO, ad esempio il passaggio di dati da e verso il DMO, l'allocazione di oggetti [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e così via.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="c0bd2-106">Poiché il DMO viene aggregato dal filtro, l'applicazione può eseguire una query sul filtro per qualsiasi interfaccia COM esponga L'oggetto DMO.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="c0bd2-107">Tuttavia, l'applicazione deve consentire al filtro di gestire tutte le operazioni di streaming nel DMO.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="c0bd2-108">Ad esempio, non impostare tipi di supporti, elaborare buffer, scaricare il DMO, bloccare il DMO, abilitare o disabilitare il controllo di qualità o impostare ottimizzazioni video.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="c0bd2-109">Se si conosce l'identificatore di classe (CLSID) di un DMO specifico che si vuole usare, è possibile inizializzare il filtro wrapper DMO con tale DMO, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c0bd2-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="c0bd2-110">Chiamare **CoCreateInstance per** creare il filtro wrapper DMO.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="c0bd2-111">Eseguire una query sul filtro wrapper DMO per [**l'interfaccia IDMOWrapperFilter.**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter)</span><span class="sxs-lookup"><span data-stu-id="c0bd2-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="c0bd2-112">Chiamare il [**metodo IDMOWrapperFilter::Init.**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init)</span><span class="sxs-lookup"><span data-stu-id="c0bd2-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="c0bd2-113">Specificare il CLSID del DMO e il GUID della categoria del DMO.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="c0bd2-114">Per un elenco delle categorie DMO, vedere [GUID DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="c0bd2-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="c0bd2-115">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="c0bd2-115">The following code shows these steps:</span></span>


```C++
// Create the DMO Wrapper filter.
IBaseFilter *pFilter;
HRESULT hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, 
    CLSCTX_INPROC_SERVER, IID_IBaseFilter, 
    reinterpret_cast<void**>(&pFilter));

if (SUCCEEDED(hr)) 
{
    // Query for IDMOWrapperFilter.
    IDMOWrapperFilter *pDmoWrapper;
    hr = pFilter->QueryInterface(IID_IDMOWrapperFilter, 
        reinterpret_cast<void**>(&pDmoWrapper));

    if (SUCCEEDED(hr)) 
    {     
        // Initialize the filter.
        hr = pDmoWrapper->Init(CLSID_MyDMO, DMOCATEGORY_VIDEO_EFFECT); 
        pDmoWrapper->Release();

        if (SUCCEEDED(hr)) 
        {
            // Add the filter to the graph.
            hr = pGraph->AddFilter(pFilter, L"My DMO");
        }
    }
    pFilter->Release();
}
```



<span data-ttu-id="c0bd2-116">La [**funzione DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera i DMO nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="c0bd2-117">Questa funzione usa un set diverso di GUID di categoria rispetto a quelli usati per i filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="c0bd2-118">**Uso dell'enumeratore del dispositivo di sistema con dmo**</span><span class="sxs-lookup"><span data-stu-id="c0bd2-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="c0bd2-119">Anziché creare direttamente un DMO, è possibile usare [l'enumeratore](system-device-enumerator.md)dispositivo di sistema , che può enumerare qualsiasi categoria DMO supportata dal **metodo DMOEnum.**</span><span class="sxs-lookup"><span data-stu-id="c0bd2-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="c0bd2-120">L'enumeratore del dispositivo di sistema include anche dmo quando enumera determinate categorie di filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="c0bd2-121">La tabella seguente illustra il mapping tra le categorie DMO e le categorie DirectShow.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



| <span data-ttu-id="c0bd2-122">Label</span><span class="sxs-lookup"><span data-stu-id="c0bd2-122">Label</span></span> | <span data-ttu-id="c0bd2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c0bd2-123">Value</span></span> |
|-----------------------------|--------------------------------|
| <span data-ttu-id="c0bd2-124">Categoria DMO</span><span class="sxs-lookup"><span data-stu-id="c0bd2-124">DMO Category</span></span>                | <span data-ttu-id="c0bd2-125">DirectShow equivalente</span><span class="sxs-lookup"><span data-stu-id="c0bd2-125">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="c0bd2-126">CODIFICATORE AUDIO DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="c0bd2-126">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="c0bd2-127">CLSID \_ AudioCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="c0bd2-127">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="c0bd2-128">DECODIFICATORE AUDIO DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="c0bd2-128">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="c0bd2-129">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c0bd2-129">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="c0bd2-130">CODIFICATORE \_ VIDEO \_ DMOCATEGORY</span><span class="sxs-lookup"><span data-stu-id="c0bd2-130">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="c0bd2-131">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="c0bd2-131">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="c0bd2-132">DECODIFICATORE VIDEO DMOCATEGORY \_ \_</span><span class="sxs-lookup"><span data-stu-id="c0bd2-132">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="c0bd2-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c0bd2-133">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="c0bd2-134">System Device Enumerator restituisce un elenco di oggetti moniker.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-134">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="c0bd2-135">Se il moniker rappresenta un DMO, il metodo **IMoniker::BindToObject** crea automaticamente il filtro wrapper DMO e lo inizializza con tale DMO.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-135">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="c0bd2-136">Di conseguenza, il fatto che sia coinvolto un DMO è trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-136">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="c0bd2-137">Per altre informazioni sull'uso di System Device Enumerator, vedere [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="c0bd2-137">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="c0bd2-138">**Limitazioni**</span><span class="sxs-lookup"><span data-stu-id="c0bd2-138">**Limitations**</span></span>

<span data-ttu-id="c0bd2-139">Esistono alcune limitazioni quando si usano gli oggetti DMO in DirectShow:</span><span class="sxs-lookup"><span data-stu-id="c0bd2-139">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="c0bd2-140">Il filtro wrapper DMO non supporta gli oggetti DMO con zero input, più input o zero output.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-140">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="c0bd2-141">Tutte le connessioni pin nel filtro wrapper DMO usano [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)</span><span class="sxs-lookup"><span data-stu-id="c0bd2-141">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="c0bd2-142">DirectShow Editing Services non supporta effetti o transizioni basati su DMO.</span><span class="sxs-lookup"><span data-stu-id="c0bd2-142">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0bd2-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0bd2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0bd2-144">Uso di dmo</span><span class="sxs-lookup"><span data-stu-id="c0bd2-144">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



