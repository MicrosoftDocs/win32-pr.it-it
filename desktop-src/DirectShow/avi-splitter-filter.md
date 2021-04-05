---
description: Filtro separatore AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro separatore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125319"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="13e69-103">Filtro separatore AVI</span><span class="sxs-lookup"><span data-stu-id="13e69-103">AVI Splitter Filter</span></span>

<span data-ttu-id="13e69-104">Il filtro separatore AVI viene usato per la riproduzione di file AVI.</span><span class="sxs-lookup"><span data-stu-id="13e69-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="13e69-105">Accetta i dati in formato AVI e li suddivide nei flussi costitutivi per un'ulteriore elaborazione e/o rendering.</span><span class="sxs-lookup"><span data-stu-id="13e69-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e69-106">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="13e69-106">Filter Interfaces</span></span>                        | <span data-ttu-id="13e69-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="13e69-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="13e69-108">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="13e69-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="13e69-109">\_Flusso MEDIATYPE, MEDIASUBTYPE \_ AVI</span><span class="sxs-lookup"><span data-stu-id="13e69-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="13e69-110">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="13e69-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="13e69-111">[**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="13e69-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="13e69-112">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="13e69-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="13e69-113">In genere **MEDIATYPE \_ video** o **\_ audio MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="13e69-113">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="13e69-114">Il tipo esatto dipende dal contenuto del file, dal fatto che il file sia compresso e da quale codec è stato usato.</span><span class="sxs-lookup"><span data-stu-id="13e69-114">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="13e69-115">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="13e69-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="13e69-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="13e69-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="13e69-117">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="13e69-117">Filter CLSID</span></span>                             | <span data-ttu-id="13e69-118">\_AVISPLITTER CLSID</span><span class="sxs-lookup"><span data-stu-id="13e69-118">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="13e69-119">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="13e69-119">Property Page CLSID</span></span>                      | <span data-ttu-id="13e69-120">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="13e69-120">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="13e69-121">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="13e69-121">Executable</span></span>                               | <span data-ttu-id="13e69-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="13e69-122">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="13e69-123">Merito</span><span class="sxs-lookup"><span data-stu-id="13e69-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="13e69-124">VALORE \_ normale</span><span class="sxs-lookup"><span data-stu-id="13e69-124">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="13e69-125">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="13e69-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="13e69-126">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="13e69-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="13e69-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="13e69-127">Remarks</span></span>

<span data-ttu-id="13e69-128">Questo filtro viene in genere connesso al filtro di [origine file asincrono](file-source--async--filter.md) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="13e69-128">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="13e69-129">Può connettersi a qualsiasi filtro il cui pin di output supporti [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e offre il tipo di supporto corretto al pin di input del filtro Splitter AVI.</span><span class="sxs-lookup"><span data-stu-id="13e69-129">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="13e69-130">I pin di output nella barra di divisione AVI supportano il metodo IPropertyBag:: Read per la lettura delle proprietà dai singoli flussi.</span><span class="sxs-lookup"><span data-stu-id="13e69-130">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="13e69-131">Attualmente, viene definita la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="13e69-131">Currently, the following property is defined.</span></span>



| <span data-ttu-id="13e69-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="13e69-132">Property</span></span> | <span data-ttu-id="13e69-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13e69-133">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e69-134">name</span><span class="sxs-lookup"><span data-stu-id="13e69-134">name</span></span>     | <span data-ttu-id="13e69-135">Restituisce il nome del flusso, tratto dal `'strn'` blocco nel file AVI.</span><span class="sxs-lookup"><span data-stu-id="13e69-135">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="13e69-136">Se questo blocco è assente, il metodo Read restituisce E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="13e69-136">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="13e69-137">Il metodo IPropertyBag:: Write restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="13e69-137">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="13e69-138">Il filtro [Mux AVI](avi-mux-filter.md) supporta IPropertyBag:: Write per salvare le proprietà del flusso in un file AVI.</span><span class="sxs-lookup"><span data-stu-id="13e69-138">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="13e69-139">Il separatore AVI non consente ai filtri downstream di usare il proprio allocatore.</span><span class="sxs-lookup"><span data-stu-id="13e69-139">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="13e69-140">La durata dell'interfoliazione nel file determina la quantità di memoria allocata dal separatore AVI per elaborarla.</span><span class="sxs-lookup"><span data-stu-id="13e69-140">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="13e69-141">Un file con interfoliazione in blocchi di un secondo richiede una quantità maggiore di memoria per l'elaborazione rispetto a un file la cui durata di interfoliazione è impostata su uno o due frame.</span><span class="sxs-lookup"><span data-stu-id="13e69-141">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="13e69-142">Nei computer moderni, questo non è in genere un problema a meno che non vengano eseguite contemporaneamente più istanze del separatore AVI.</span><span class="sxs-lookup"><span data-stu-id="13e69-142">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="13e69-143">La ricerca</span><span class="sxs-lookup"><span data-stu-id="13e69-143">Seeking</span></span>

<span data-ttu-id="13e69-144">Se il file contiene un flusso video, il separatore AVI supporta la ricerca in base al numero di frame.</span><span class="sxs-lookup"><span data-stu-id="13e69-144">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="13e69-145">Per abilitare la ricerca basata su frame, chiamare [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in [Filter Graph Manager](filter-graph-manager.md) con il valore **\_ format time format \_ frame**.</span><span class="sxs-lookup"><span data-stu-id="13e69-145">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="13e69-146">Se il file contiene un flusso audio, il separatore AVI supporta la ricerca in base al numero di campione.</span><span class="sxs-lookup"><span data-stu-id="13e69-146">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="13e69-147">Per abilitare la ricerca basata su campione, chiamare [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in Filter Graph Manager con l' **esempio valore \_ time \_ Format**.</span><span class="sxs-lookup"><span data-stu-id="13e69-147">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="13e69-148">In entrambi i casi, il pin di output per quel flusso deve essere connesso a un filtro renderer.</span><span class="sxs-lookup"><span data-stu-id="13e69-148">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13e69-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13e69-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e69-150">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="13e69-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



