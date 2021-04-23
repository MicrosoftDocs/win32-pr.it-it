---
description: Il filtro Sample Grabber consente di recuperare gli esempi mentre passano attraverso il grafico dei filtri.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro Grabber di esempio (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909669"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="089f4-103">Filtro Grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="089f4-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="089f4-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="089f4-104">\[Deprecated.</span></span> <span data-ttu-id="089f4-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="089f4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="089f4-106">Il filtro Sample Grabber consente di recuperare gli esempi mentre passano attraverso il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="089f4-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="089f4-107">Si tratta di un filtro di trasformazione con un pin di input e un pin di output.</span><span class="sxs-lookup"><span data-stu-id="089f4-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="089f4-108">Passa tutti i campioni a valle senza modifiche, quindi è possibile inserirli in un grafico di filtro senza modificare il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="089f4-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="089f4-109">L'applicazione può quindi recuperare singoli esempi dal filtro chiamando i metodi [**nell'interfaccia ISampleGrabber.**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="089f4-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="089f4-110">Per recuperare gli esempi senza eseguire il rendering dei dati, connettere il filtro Sample Grabber al filtro [**Renderer**](null-renderer-filter.md) Null.</span><span class="sxs-lookup"><span data-stu-id="089f4-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



| <span data-ttu-id="089f4-111">Label</span><span class="sxs-lookup"><span data-stu-id="089f4-111">Label</span></span> | <span data-ttu-id="089f4-112">Valore</span><span class="sxs-lookup"><span data-stu-id="089f4-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="089f4-113">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="089f4-113">Filter interfaces</span></span>                        | <span data-ttu-id="089f4-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="089f4-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="089f4-115">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="089f4-115">Input pin media types</span></span>                    | <span data-ttu-id="089f4-116">Qualsiasi tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="089f4-116">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="089f4-117">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="089f4-117">Input pin interfaces</span></span>                     | <span data-ttu-id="089f4-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="089f4-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="089f4-119">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="089f4-119">Output pin media types</span></span>                   | <span data-ttu-id="089f4-120">Qualsiasi tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="089f4-120">Any media type.</span></span> <span data-ttu-id="089f4-121">Corrisponde al tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="089f4-121">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="089f4-122">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="089f4-122">Output pin interfaces</span></span>                    | <span data-ttu-id="089f4-123">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="089f4-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="089f4-124">Filtro CLSID</span><span class="sxs-lookup"><span data-stu-id="089f4-124">Filter CLSID</span></span>                             | <span data-ttu-id="089f4-125">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="089f4-125">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="089f4-126">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="089f4-126">Property Page CLSID</span></span>                      | <span data-ttu-id="089f4-127">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="089f4-127">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="089f4-128">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="089f4-128">Executable</span></span>                               | <span data-ttu-id="089f4-129">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="089f4-129">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="089f4-130">Merito</span><span class="sxs-lookup"><span data-stu-id="089f4-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="089f4-131">MERITO \_ NON \_ \_ USARE</span><span class="sxs-lookup"><span data-stu-id="089f4-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="089f4-132">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="089f4-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="089f4-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="089f4-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="089f4-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="089f4-134">Remarks</span></span>

<span data-ttu-id="089f4-135">Per usare questo filtro, aggiungerlo al grafico dei filtri e chiamare [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) con il tipo di supporto desiderato.</span><span class="sxs-lookup"><span data-stu-id="089f4-135">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="089f4-136">Questo metodo specifica il tipo di supporto per le connessioni di input e pin di output del filtro.</span><span class="sxs-lookup"><span data-stu-id="089f4-136">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="089f4-137">Connettere quindi il filtro ad altri filtri nel grafico.</span><span class="sxs-lookup"><span data-stu-id="089f4-137">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="089f4-138">Se si chiama [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **TRUE,** il filtro bufferizza ogni campione ricevuto prima di passarlo a valle.</span><span class="sxs-lookup"><span data-stu-id="089f4-138">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="089f4-139">Chiamare il [**metodo ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) per recuperare il contenuto corrente del buffer.</span><span class="sxs-lookup"><span data-stu-id="089f4-139">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="089f4-140">In alternativa, è possibile chiamare [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) per fare in modo che il filtro chiami una funzione di callback ogni volta che riceve un esempio.</span><span class="sxs-lookup"><span data-stu-id="089f4-140">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="089f4-141">Il filtro presenta le limitazioni seguenti per i formati video:</span><span class="sxs-lookup"><span data-stu-id="089f4-141">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="089f4-142">Non supporta i tipi di video con orientamento dall'alto verso il basso **(biHeight negativo).**</span><span class="sxs-lookup"><span data-stu-id="089f4-142">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="089f4-143">Non supporta la struttura di [**formato VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo di formato uguale a **FORMAT \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="089f4-143">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="089f4-144">Rifiuta qualsiasi tipo di video in cui lo stride della superficie non corrisponde alla larghezza del video.</span><span class="sxs-lookup"><span data-stu-id="089f4-144">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="089f4-145">Di conseguenza, Sample Grabber non si connetterà al renderer di combinazione di video per alcuni tipi di video.</span><span class="sxs-lookup"><span data-stu-id="089f4-145">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="089f4-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="089f4-146">Requirements</span></span>



| <span data-ttu-id="089f4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="089f4-147">Requirement</span></span> | <span data-ttu-id="089f4-148">Valore</span><span class="sxs-lookup"><span data-stu-id="089f4-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="089f4-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="089f4-149">Header</span></span><br/> | <dl> <span data-ttu-id="089f4-150"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="089f4-150"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089f4-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="089f4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089f4-152">DirectShow Editing Services Objects</span><span class="sxs-lookup"><span data-stu-id="089f4-152">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="089f4-153">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="089f4-153">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




