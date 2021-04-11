---
description: Uso di DMOs in DirectShow
ms.assetid: 47d75b9c-8b0d-4235-8ac1-02ae1502c0e7
title: Uso di DMOs in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c90513649756a49067e523390292d4b44e1eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131886"
---
# <a name="using-dmos-in-directshow"></a><span data-ttu-id="2fe06-103">Uso di DMOs in DirectShow</span><span class="sxs-lookup"><span data-stu-id="2fe06-103">Using DMOs in DirectShow</span></span>

<span data-ttu-id="2fe06-104">Le applicazioni basate su DirectShow possono usare DMOs in un grafico di filtro, tramite il filtro del [wrapper DMO](dmo-wrapper-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="2fe06-104">Applications based on DirectShow can use DMOs in a filter graph, through the [DMO Wrapper](dmo-wrapper-filter.md) filter.</span></span> <span data-ttu-id="2fe06-105">Questo filtro aggrega un DMO e gestisce tutti i dettagli dell'uso di DMO, ad esempio il passaggio di dati da e verso DMO, l'allocazione di oggetti [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) e così via.</span><span class="sxs-lookup"><span data-stu-id="2fe06-105">This filter aggregates a DMO and handles all the details of using the DMO, such as passing data to and from the DMO, allocating [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) objects, and so forth.</span></span>

<span data-ttu-id="2fe06-106">Poiché il DMO è aggregato dal filtro, l'applicazione può eseguire una query sul filtro per qualsiasi interfaccia COM esposta da DMO.</span><span class="sxs-lookup"><span data-stu-id="2fe06-106">Because the DMO is aggregated by the filter, the application can query the filter for any COM interfaces that the DMO exposes.</span></span> <span data-ttu-id="2fe06-107">Tuttavia, l'applicazione deve consentire al filtro di gestire tutte le operazioni di streaming sul DMO.</span><span class="sxs-lookup"><span data-stu-id="2fe06-107">However, the application should let the filter handle all streaming operations on the DMO.</span></span> <span data-ttu-id="2fe06-108">Ad esempio, non impostare i tipi di supporto, elaborare i buffer, scaricare il DMO, bloccare il DMO, abilitare o disabilitare il controllo qualità o impostare le ottimizzazioni video.</span><span class="sxs-lookup"><span data-stu-id="2fe06-108">For example, do not set media types, process any buffers, flush the DMO, lock the DMO, enable or disable quality control, or set video optimizations.</span></span>

<span data-ttu-id="2fe06-109">Se si conosce l'identificatore di classe (CLSID) di un DMO specifico che si vuole usare, è possibile inizializzare il filtro del wrapper DMO con tale DMO, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2fe06-109">If you know the class identifier (CLSID) of a specific DMO that you want to use, you can initialize the DMO Wrapper filter with that DMO, as follows:</span></span>

1.  <span data-ttu-id="2fe06-110">Chiamare **CoCreateInstance** per creare il filtro del wrapper DMO.</span><span class="sxs-lookup"><span data-stu-id="2fe06-110">Call **CoCreateInstance** to create the DMO Wrapper filter.</span></span>
2.  <span data-ttu-id="2fe06-111">Eseguire una query sul filtro del wrapper DMO per l'interfaccia [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="2fe06-111">Query the DMO Wrapper filter for the [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/Dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="2fe06-112">Chiamare il metodo [**IDMOWrapperFilter:: init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) .</span><span class="sxs-lookup"><span data-stu-id="2fe06-112">Call the [**IDMOWrapperFilter::Init**](/previous-versions/windows/desktop/api/Dmodshow/nf-dmodshow-idmowrapperfilter-init) method.</span></span> <span data-ttu-id="2fe06-113">Specificare il CLSID di DMO e il GUID della categoria DMO.</span><span class="sxs-lookup"><span data-stu-id="2fe06-113">Specify the CLSID of the DMO and the GUID of the DMO's category.</span></span> <span data-ttu-id="2fe06-114">Per un elenco di categorie DMO, vedere [GUID DMO](dmo-guids.md).</span><span class="sxs-lookup"><span data-stu-id="2fe06-114">For a list of DMO categories, see [DMO GUIDs](dmo-guids.md).</span></span>

<span data-ttu-id="2fe06-115">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="2fe06-115">The following code shows these steps:</span></span>


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



<span data-ttu-id="2fe06-116">La funzione [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) enumera DMOS nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2fe06-116">The [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function enumerates DMOs in the registry.</span></span> <span data-ttu-id="2fe06-117">Questa funzione usa un set di GUID di categoria diverso da quelli usati per i filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2fe06-117">This function uses a different set of category GUIDs from the ones used for DirectShow filters.</span></span>

<span data-ttu-id="2fe06-118">**Uso di System Device Enumerator con DMOs**</span><span class="sxs-lookup"><span data-stu-id="2fe06-118">**Using the System Device Enumerator with DMOs**</span></span>

<span data-ttu-id="2fe06-119">Anziché creare direttamente un DMO, è possibile usare l' [enumeratore del dispositivo di sistema](system-device-enumerator.md), che può enumerare qualsiasi categoria DMO supportata dal metodo **DMOEnum** .</span><span class="sxs-lookup"><span data-stu-id="2fe06-119">Instead of creating a DMO directly, you can use the [System Device Enumerator](system-device-enumerator.md), which can enumerate any DMO category that is supported by the **DMOEnum** method.</span></span> <span data-ttu-id="2fe06-120">L'enumeratore di dispositivo di sistema include anche DMOs quando enumera determinate categorie di filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2fe06-120">The System Device Enumerator also includes DMOs when it enumerates certain DirectShow filter categories.</span></span> <span data-ttu-id="2fe06-121">La tabella seguente illustra il mapping tra le categorie DMO e le categorie DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2fe06-121">The following table shows the mapping between DMO categories and DirectShow categories.</span></span>



|                             |                                |
|-----------------------------|--------------------------------|
| <span data-ttu-id="2fe06-122">Categoria DMO</span><span class="sxs-lookup"><span data-stu-id="2fe06-122">DMO Category</span></span>                | <span data-ttu-id="2fe06-123">Equivalente DirectShow</span><span class="sxs-lookup"><span data-stu-id="2fe06-123">DirectShow Equivalent</span></span>          |
| <span data-ttu-id="2fe06-124">\_ \_ codificatore audio DMOCATEGORY</span><span class="sxs-lookup"><span data-stu-id="2fe06-124">DMOCATEGORY\_AUDIO\_ENCODER</span></span> | <span data-ttu-id="2fe06-125">\_AUDIOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="2fe06-125">CLSID\_AudioCompressorCategory</span></span> |
| <span data-ttu-id="2fe06-126">\_decodificatore audio DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="2fe06-126">DMOCATEGORY\_AUDIO\_DECODER</span></span> | <span data-ttu-id="2fe06-127">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="2fe06-127">CLSID\_LegacyAmFilterCategory</span></span>  |
| <span data-ttu-id="2fe06-128">\_ \_ codificatore video DMOCATEGORY</span><span class="sxs-lookup"><span data-stu-id="2fe06-128">DMOCATEGORY\_VIDEO\_ENCODER</span></span> | <span data-ttu-id="2fe06-129">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="2fe06-129">CLSID\_VideoCompressorCategory</span></span> |
| <span data-ttu-id="2fe06-130">\_decodificatore video DMOCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="2fe06-130">DMOCATEGORY\_VIDEO\_DECODER</span></span> | <span data-ttu-id="2fe06-131">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="2fe06-131">CLSID\_LegacyAmFilterCategory</span></span>  |



 

<span data-ttu-id="2fe06-132">L'enumeratore System Device restituisce un elenco di oggetti moniker.</span><span class="sxs-lookup"><span data-stu-id="2fe06-132">The System Device Enumerator returns a list of moniker objects.</span></span> <span data-ttu-id="2fe06-133">Se il moniker rappresenta un DMO, il metodo **IMoniker:: BindToObject** crea automaticamente il filtro del wrapper DMO e lo inizializza con tale DMO.</span><span class="sxs-lookup"><span data-stu-id="2fe06-133">If the moniker represents a DMO, the **IMoniker::BindToObject** method automatically creates the DMO Wrapper filter and initializes it with that DMO.</span></span> <span data-ttu-id="2fe06-134">Pertanto, il fatto che un DMO sia presente è trasparente per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2fe06-134">Thus, the fact that a DMO is involved is transparent to the application.</span></span> <span data-ttu-id="2fe06-135">Per ulteriori informazioni sull'utilizzo di System Device Enumerator, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="2fe06-135">For more information on using the System Device Enumerator, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="2fe06-136">**Limitazioni**</span><span class="sxs-lookup"><span data-stu-id="2fe06-136">**Limitations**</span></span>

<span data-ttu-id="2fe06-137">L'uso di DMOs in DirectShow presenta alcune limitazioni:</span><span class="sxs-lookup"><span data-stu-id="2fe06-137">There are some limitations when using DMOs in DirectShow:</span></span>

-   <span data-ttu-id="2fe06-138">Il filtro del wrapper DMO non supporta DMOs con zero input, più input o zero output.</span><span class="sxs-lookup"><span data-stu-id="2fe06-138">The DMO Wrapper filter does not support DMOs with zero inputs, multiple inputs, or zero outputs.</span></span>
-   <span data-ttu-id="2fe06-139">Tutte le connessioni pin sul filtro del wrapper DMO usano l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="2fe06-139">All pin connections on the DMO Wrapper Filter use the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="2fe06-140">I servizi di modifica DirectShow non supportano gli effetti o le transizioni basati su DMO.</span><span class="sxs-lookup"><span data-stu-id="2fe06-140">DirectShow Editing Services does not support DMO-based effects or transitions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fe06-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2fe06-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fe06-142">Uso di DMOs</span><span class="sxs-lookup"><span data-stu-id="2fe06-142">Using DMOs</span></span>](using-dmos.md)
</dt> </dl>

 

 



