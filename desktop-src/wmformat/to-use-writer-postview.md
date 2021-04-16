---
title: Per utilizzare PostView writer
description: Per utilizzare PostView writer
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Formato avanzato dei sistemi (ASF), PostView writer
- ASF (formato avanzato dei sistemi), PostView writer
- Formato avanzato dei sistemi (ASF), visualizzazione
- ASF (formato avanzato dei sistemi), visualizzazione
- PostView writer
- visualizzazione in anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516669"
---
# <a name="to-use-writer-postview"></a><span data-ttu-id="9906f-109">Per utilizzare PostView writer</span><span class="sxs-lookup"><span data-stu-id="9906f-109">To Use Writer Postview</span></span>

<span data-ttu-id="9906f-110">L'oggetto writer fornisce funzionalità di visualizzazione in modo che sia possibile verificare il contenuto scritto senza dover impostare l'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="9906f-110">The writer object provides postviewing capabilities so that you can verify written content without having to set up the reader object.</span></span> <span data-ttu-id="9906f-111">L'oggetto writer non supporta l'anteprima per il contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="9906f-111">The writer object does not support postviewing for audio content.</span></span>

<span data-ttu-id="9906f-112">Il revisore del writer funziona in modo molto simile all'oggetto Reader asincrono, solo con meno funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9906f-112">The writer postviewer works in much the same way as the asynchronous reader object, only with fewer features.</span></span> <span data-ttu-id="9906f-113">Per informazioni dettagliate sulla lettura di file multimediali digitali, vedere la pagina relativa alla [lettura di file ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="9906f-113">For detailed information about reading digital media, see [Reading ASF Files](reading-asf-files.md).</span></span>

<span data-ttu-id="9906f-114">Per implementare il postvisore, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="9906f-114">To implement the postviewer, perform the following steps.</span></span>

1.  <span data-ttu-id="9906f-115">Implementare il callback [**IWMWriterPostViewCallback:: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) .</span><span class="sxs-lookup"><span data-stu-id="9906f-115">Implement the [**IWMWriterPostViewCallback::OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) callback.</span></span> <span data-ttu-id="9906f-116">Questo metodo è essenzialmente lo stesso di [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , ad eccezione del fatto che specifica i numeri di flusso anziché gli output.</span><span class="sxs-lookup"><span data-stu-id="9906f-116">This method is essentially the same as [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it specifies stream numbers instead of outputs.</span></span>
2.  <span data-ttu-id="9906f-117">Configurare per la scrittura come di consueto.</span><span class="sxs-lookup"><span data-stu-id="9906f-117">Set up for writing as usual.</span></span>
3.  <span data-ttu-id="9906f-118">Ottenere un puntatore all'interfaccia [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) dell'oggetto writer chiamando **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9906f-118">Obtain a pointer to the [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) interface of the writer object by calling **IWMWriter::QueryInterface**.</span></span>
4.  <span data-ttu-id="9906f-119">Impostare il callback per il postvisore da utilizzare chiamando [**IWMWriterPostView:: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span><span class="sxs-lookup"><span data-stu-id="9906f-119">Set the callback for the postviewer to use by calling [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span></span>
5.  <span data-ttu-id="9906f-120">Per ogni flusso per il quale si desidera ricevere gli esempi di PostView, chiamare [**IWMWriterPostView:: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="9906f-120">For each stream for which you want to receive postview samples, call [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span></span> <span data-ttu-id="9906f-121">È possibile verificare se un flusso è impostato per ricevere esempi di PostView chiamando [**IWMWriterPostView:: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="9906f-121">You can check to see whether a stream is set to receive postview samples by calling [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span></span>
6.  <span data-ttu-id="9906f-122">È possibile modificare i formati di esempio, esattamente come i formati di output nell'oggetto Reader o nell'oggetto Reader sincrono.</span><span class="sxs-lookup"><span data-stu-id="9906f-122">You can manipulate the sample formats, just like you would the output formats in the reader object or synchronous reader object.</span></span>
7.  <span data-ttu-id="9906f-123">Quando si inizia a scrivere il file, si inizierà a ricevere esempi nell'implementazione del metodo di callback **OnPostViewSample** .</span><span class="sxs-lookup"><span data-stu-id="9906f-123">When you start writing the file, you will begin to receive samples in your implementation of the **OnPostViewSample** callback method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9906f-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9906f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9906f-125">**Interfaccia IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="9906f-125">**IWMWriterPostViewCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[<span data-ttu-id="9906f-126">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="9906f-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




