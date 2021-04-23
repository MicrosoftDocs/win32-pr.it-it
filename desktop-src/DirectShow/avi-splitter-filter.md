---
description: Filtro separatore AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro separatore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909659"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="c4ddf-103">Filtro separatore AVI</span><span class="sxs-lookup"><span data-stu-id="c4ddf-103">AVI Splitter Filter</span></span>

<span data-ttu-id="c4ddf-104">Il filtro del separatore AVI viene usato per la riproduzione di file AVI.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="c4ddf-105">Accetta i dati in formato AVI e suddivide i dati nei flussi costitutivi per un'ulteriore elaborazione e/o rendering.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



| <span data-ttu-id="c4ddf-106">Label</span><span class="sxs-lookup"><span data-stu-id="c4ddf-106">Label</span></span> | <span data-ttu-id="c4ddf-107">Valore</span><span class="sxs-lookup"><span data-stu-id="c4ddf-107">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ddf-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="c4ddf-108">Filter Interfaces</span></span>                        | <span data-ttu-id="c4ddf-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="c4ddf-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="c4ddf-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="c4ddf-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="c4ddf-111">MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Avi</span><span class="sxs-lookup"><span data-stu-id="c4ddf-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="c4ddf-112">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="c4ddf-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="c4ddf-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c4ddf-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="c4ddf-114">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="c4ddf-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="c4ddf-115">In **genere MEDIATYPE \_ Video** o **MEDIATYPE \_ Audio.**</span><span class="sxs-lookup"><span data-stu-id="c4ddf-115">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="c4ddf-116">Il tipo esatto dipende dal contenuto del file, dal fatto che il file sia compresso e dal codec usato.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-116">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="c4ddf-117">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="c4ddf-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="c4ddf-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c4ddf-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="c4ddf-119">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="c4ddf-119">Filter CLSID</span></span>                             | <span data-ttu-id="c4ddf-120">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="c4ddf-120">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="c4ddf-121">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c4ddf-121">Property Page CLSID</span></span>                      | <span data-ttu-id="c4ddf-122">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-122">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="c4ddf-123">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="c4ddf-123">Executable</span></span>                               | <span data-ttu-id="c4ddf-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c4ddf-124">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="c4ddf-125">Merito</span><span class="sxs-lookup"><span data-stu-id="c4ddf-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="c4ddf-126">MERITO \_ NORMALE</span><span class="sxs-lookup"><span data-stu-id="c4ddf-126">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="c4ddf-127">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="c4ddf-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c4ddf-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c4ddf-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c4ddf-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4ddf-129">Remarks</span></span>

<span data-ttu-id="c4ddf-130">Questo filtro è in genere connesso al filtro [Origine file asincrona](file-source--async--filter.md) sul relativo pin di input.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-130">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="c4ddf-131">Può connettersi a qualsiasi filtro il cui pin di output supporta [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e offre il tipo di supporto corretto al pin di input del filtro AVI Splitter.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-131">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="c4ddf-132">I pin di output sullo splitter AVI supportano il metodo IPropertyBag::Read per la lettura delle proprietà dai singoli flussi.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-132">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="c4ddf-133">Attualmente è definita la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-133">Currently, the following property is defined.</span></span>



| <span data-ttu-id="c4ddf-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c4ddf-134">Property</span></span> | <span data-ttu-id="c4ddf-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4ddf-135">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ddf-136">name</span><span class="sxs-lookup"><span data-stu-id="c4ddf-136">name</span></span>     | <span data-ttu-id="c4ddf-137">Restituisce il nome del flusso, tratto dal `'strn'` blocco nel file AVI.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-137">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="c4ddf-138">Se questo blocco è assente, il metodo Read restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-138">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="c4ddf-139">Il metodo IPropertyBag::Write restituisce E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-139">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="c4ddf-140">Il [filtro Mux AVI](avi-mux-filter.md) supporta IPropertyBag::Write per salvare le proprietà del flusso in un file AVI.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-140">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="c4ddf-141">Lo strumento di suddivisione AVI non consente ai filtri downstream di usare il proprio allocatore.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-141">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="c4ddf-142">La durata dell'interfoliazione nel file determina la quantità di memoria allocata dal separatore AVI per elaborarlo.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-142">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="c4ddf-143">Un file interfoliato in blocchi di un secondo richiederà molto più memoria per l'elaborazione rispetto a un file la cui durata dell'interfoliazione è impostata su uno o due fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-143">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="c4ddf-144">Nei computer moderni non si tratta in genere di un problema, a meno che non si esercitino più istanze dello splitter AVI contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-144">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="c4ddf-145">riercare</span><span class="sxs-lookup"><span data-stu-id="c4ddf-145">Seeking</span></span>

<span data-ttu-id="c4ddf-146">Se il file contiene un flusso video, lo splitter AVI supporta la ricerca in base al numero di fotogramma.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-146">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="c4ddf-147">Per abilitare la ricerca basata su frame, chiamare [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in [Filter Graph Manager](filter-graph-manager.md) con il valore TIME FORMAT **\_ \_ FRAME**.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-147">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="c4ddf-148">Se il file contiene un flusso audio, la barra di divisione AVI supporta la ricerca in base al numero di esempio.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-148">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="c4ddf-149">Per abilitare la ricerca basata sul campione, chiamare [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in Filter Graph Manager con il **valore TIME FORMAT \_ \_ SAMPLE.**</span><span class="sxs-lookup"><span data-stu-id="c4ddf-149">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="c4ddf-150">In entrambi i casi, il pin di output per tale flusso deve essere connesso a un filtro renderer.</span><span class="sxs-lookup"><span data-stu-id="c4ddf-150">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4ddf-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4ddf-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4ddf-152">DirectShow Filters</span><span class="sxs-lookup"><span data-stu-id="c4ddf-152">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



