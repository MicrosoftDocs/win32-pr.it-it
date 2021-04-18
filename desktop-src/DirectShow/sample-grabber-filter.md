---
description: Il filtro Grabber di esempio consente di recuperare gli esempi mentre passano attraverso il grafico del filtro.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Filtro Grabber di esempio (qedit. h)
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
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325030"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="0a404-103">Filtro Grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="0a404-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="0a404-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0a404-104">\[Deprecated.</span></span> <span data-ttu-id="0a404-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a404-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a404-106">Il filtro Grabber di esempio consente di recuperare gli esempi mentre passano attraverso il grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="0a404-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="0a404-107">Si tratta di un filtro di trasformazione con un pin di input e un pin di output.</span><span class="sxs-lookup"><span data-stu-id="0a404-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="0a404-108">Passa tutti i campioni a valle senza modifiche, quindi è possibile inserirli in un grafico di filtro senza modificare il flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0a404-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="0a404-109">L'applicazione può quindi recuperare singoli esempi dal filtro chiamando i metodi sull'interfaccia [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="0a404-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="0a404-110">Se si desidera recuperare esempi senza eseguire il rendering dei dati, connettere il filtro Grabber di esempio al filtro [**renderer null**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0a404-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a404-111">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="0a404-111">Filter interfaces</span></span>                        | <span data-ttu-id="0a404-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="0a404-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="0a404-113">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="0a404-113">Input pin media types</span></span>                    | <span data-ttu-id="0a404-114">Qualsiasi tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0a404-114">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="0a404-115">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="0a404-115">Input pin interfaces</span></span>                     | <span data-ttu-id="0a404-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0a404-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="0a404-117">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="0a404-117">Output pin media types</span></span>                   | <span data-ttu-id="0a404-118">Qualsiasi tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0a404-118">Any media type.</span></span> <span data-ttu-id="0a404-119">Corrisponde al tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="0a404-119">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="0a404-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="0a404-120">Output pin interfaces</span></span>                    | <span data-ttu-id="0a404-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="0a404-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="0a404-122">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="0a404-122">Filter CLSID</span></span>                             | <span data-ttu-id="0a404-123">\_SAMPLEGRABBER CLSID</span><span class="sxs-lookup"><span data-stu-id="0a404-123">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="0a404-124">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="0a404-124">Property Page CLSID</span></span>                      | <span data-ttu-id="0a404-125">Nessuna pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a404-125">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="0a404-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="0a404-126">Executable</span></span>                               | <span data-ttu-id="0a404-127">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="0a404-127">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="0a404-128">Merito</span><span class="sxs-lookup"><span data-stu-id="0a404-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="0a404-129">il merito non viene \_ \_ \_ utilizzato</span><span class="sxs-lookup"><span data-stu-id="0a404-129">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="0a404-130">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="0a404-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0a404-131">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="0a404-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="0a404-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a404-132">Remarks</span></span>

<span data-ttu-id="0a404-133">Per usare questo filtro, aggiungerlo al grafico filtro e chiamare [**ISampleGrabber:: SetMediaType**](isamplegrabber-setmediatype.md) con il tipo di supporto desiderato.</span><span class="sxs-lookup"><span data-stu-id="0a404-133">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="0a404-134">Questo metodo specifica il tipo di supporto per le connessioni al pin di input e di output del filtro.</span><span class="sxs-lookup"><span data-stu-id="0a404-134">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="0a404-135">Connettere quindi il filtro ad altri filtri nel grafico.</span><span class="sxs-lookup"><span data-stu-id="0a404-135">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="0a404-136">Se si chiama [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) con il valore **true**, il filtro memorizza nel buffer ogni campione che riceve prima di passarlo a valle.</span><span class="sxs-lookup"><span data-stu-id="0a404-136">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="0a404-137">Chiamare il metodo [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) per recuperare il contenuto corrente del buffer.</span><span class="sxs-lookup"><span data-stu-id="0a404-137">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="0a404-138">In alternativa, è possibile chiamare [**ISampleGrabber:: tocallback**](isamplegrabber-setcallback.md) per fare in modo che il filtro richiami una funzione di callback ogni volta che viene ricevuto un campione.</span><span class="sxs-lookup"><span data-stu-id="0a404-138">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="0a404-139">Il filtro presenta le seguenti limitazioni per i formati video:</span><span class="sxs-lookup"><span data-stu-id="0a404-139">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="0a404-140">Non supporta i tipi di video con orientamento dall'alto verso il basso ( **biHeight** negativo).</span><span class="sxs-lookup"><span data-stu-id="0a404-140">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="0a404-141">Non supporta la struttura del formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (tipo di formato uguale a **Format \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="0a404-141">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="0a404-142">Rifiuta qualsiasi tipo di video in cui lo stride della superficie non corrisponde alla larghezza del video.</span><span class="sxs-lookup"><span data-stu-id="0a404-142">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="0a404-143">Di conseguenza, il grabber di esempio non si connetterà al renderer video mixing (VMR) per alcuni tipi di video.</span><span class="sxs-lookup"><span data-stu-id="0a404-143">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a404-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a404-144">Requirements</span></span>



| <span data-ttu-id="0a404-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a404-145">Requirement</span></span> | <span data-ttu-id="0a404-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0a404-146">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a404-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a404-147">Header</span></span><br/> | <dl> <span data-ttu-id="0a404-148"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a404-148"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a404-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a404-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a404-150">Oggetti dei servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="0a404-150">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="0a404-151">Uso del grabber di esempio</span><span class="sxs-lookup"><span data-stu-id="0a404-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




