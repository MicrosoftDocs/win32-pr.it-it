---
title: Per implementare il callback OnSample
description: Per implementare il callback OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- Advanced Systems Format (ASF), implementazione del callback di OnStatus
- ASF (Advanced Systems Format), implementazione del callback di OnStatus
- ASF (Advanced Systems Format), callback di OnStatus
- ASF (formato avanzato dei sistemi), callback OnStatus
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, implementazione del callback di OnStatus
- Metodo di callback OnStatus, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336649"
---
# <a name="to-implement-the-onsample-callback"></a><span data-ttu-id="ede99-111">Per implementare il callback OnSample</span><span class="sxs-lookup"><span data-stu-id="ede99-111">To Implement the OnSample Callback</span></span>

<span data-ttu-id="ede99-112">Il lettore asincrono recapita esempi all'applicazione di controllo in base all'ordine in fase di presentazione effettuando chiamate al metodo di callback [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="ede99-112">The asynchronous reader delivers samples to the controlling application in presentation-time order by making calls to the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) callback method.</span></span> <span data-ttu-id="ede99-113">Quando si crea un'applicazione utilizzando il Reader asincrono, è necessario implementare **OnSample** per gestire gli esempi non compressi.</span><span class="sxs-lookup"><span data-stu-id="ede99-113">When you create an application using the asynchronous reader, you must implement **OnSample** to deal with uncompressed samples.</span></span> <span data-ttu-id="ede99-114">In genere, le funzioni o i metodi creati per eseguire il rendering del contenuto verranno chiamati dall'interno di **OnSample**.</span><span class="sxs-lookup"><span data-stu-id="ede99-114">Typically, functions or methods created to render content will be called from within **OnSample**.</span></span>

<span data-ttu-id="ede99-115">L'implementazione tipica del callback **OnSample** include i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ede99-115">Typical implementation of the **OnSample** callback includes the following steps.</span></span>

1.  <span data-ttu-id="ede99-116">Recuperare il percorso e le dimensioni del buffer che contiene l'esempio chiamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) sul buffer passato come *pSample*.</span><span class="sxs-lookup"><span data-stu-id="ede99-116">Retrieve the location and size of the buffer containing the sample by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) on the buffer passed as *pSample*.</span></span>
2.  <span data-ttu-id="ede99-117">Creare un ramo della logica a seconda del numero di output.</span><span class="sxs-lookup"><span data-stu-id="ede99-117">Branch your logic depending upon the output number.</span></span> <span data-ttu-id="ede99-118">Il numero di output viene passato a **OnSample** come *dwOutputNumber*.</span><span class="sxs-lookup"><span data-stu-id="ede99-118">The output number is passed to **OnSample** as *dwOutputNumber*.</span></span>
3.  <span data-ttu-id="ede99-119">Includere la logica di rendering per ogni numero di output che si desidera supportare.</span><span class="sxs-lookup"><span data-stu-id="ede99-119">Include rendering logic for each output number you want to support.</span></span> <span data-ttu-id="ede99-120">Se si esegue il rendering di esempi da più output, potrebbe essere necessario sincronizzare il rendering.</span><span class="sxs-lookup"><span data-stu-id="ede99-120">If you are rendering samples from multiple outputs, you may need to synchronize your rendering.</span></span>

<span data-ttu-id="ede99-121">Le applicazioni che recapitano esempi compressi dai file ASF devono implementare il metodo di callback [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="ede99-121">Applications that deliver compressed samples from ASF files need to implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span> <span data-ttu-id="ede99-122">**OnStreamSample** funziona in modo quasi identico a **OnSample**, ad eccezione del fatto che riceve campioni compressi per numero di flusso anziché campioni non compressi per numero di output.</span><span class="sxs-lookup"><span data-stu-id="ede99-122">**OnStreamSample** functions almost identically to **OnSample**, except that it receives compressed samples by stream number instead of uncompressed samples by output number.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ede99-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ede99-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ede99-124">**Interfaccia IWMReaderCallback**</span><span class="sxs-lookup"><span data-stu-id="ede99-124">**IWMReaderCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[<span data-ttu-id="ede99-125">**Interfaccia IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="ede99-125">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="ede99-126">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="ede99-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="ede99-127">**Utilizzo dei metodi di callback**</span><span class="sxs-lookup"><span data-stu-id="ede99-127">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




