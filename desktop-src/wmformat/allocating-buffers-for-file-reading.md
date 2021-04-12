---
title: Allocazione di buffer per la lettura di file
description: Allocazione di buffer per la lettura di file
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK, lettura di file ASF
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- Windows Media Format SDK, allocazione di buffer
- ASF (Advanced Systems Format), allocazione di buffer
- ASF (formato avanzato dei sistemi), allocazione di buffer
- ASF (Advanced Systems Format), allocazione di buffer
- ASF (formato avanzato dei sistemi), allocazione di buffer
- allocazione di buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398536"
---
# <a name="allocating-buffers-for-file-reading"></a><span data-ttu-id="0aaf1-112">Allocazione di buffer per la lettura di file</span><span class="sxs-lookup"><span data-stu-id="0aaf1-112">Allocating Buffers for File Reading</span></span>

<span data-ttu-id="0aaf1-113">Nello scenario di lettura dei file più semplice, i buffer utilizzati per recapitare gli esempi vengono allocati dall'oggetto di lettura (l'oggetto Reader o l'oggetto Reader sincrono).</span><span class="sxs-lookup"><span data-stu-id="0aaf1-113">In the most basic file-reading scenario, the buffers used to deliver samples are allocated by the reading object (the reader object or the synchronous reader object).</span></span> <span data-ttu-id="0aaf1-114">È tuttavia possibile allocare i buffer manualmente.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-114">You can, however, allocate buffers yourself.</span></span> <span data-ttu-id="0aaf1-115">Per ulteriori informazioni sui vantaggi dell'allocazione di buffer personalizzati, vedere Supporto di [esempio allocato dall'utente](user-allocated-sample-support.md).</span><span class="sxs-lookup"><span data-stu-id="0aaf1-115">For more information about the benefits of allocating your own buffers, see [User Allocated Sample Support](user-allocated-sample-support.md).</span></span>

<span data-ttu-id="0aaf1-116">Per usare i propri buffer per la lettura dei file, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-116">To use your own buffers for file reading, perform the following steps.</span></span>

1.  <span data-ttu-id="0aaf1-117">Implementare un callback o callback per il lettore da chiamare quando è necessario un buffer.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-117">Implement a callback or callbacks for the reader to call when it needs a buffer.</span></span> <span data-ttu-id="0aaf1-118">Se si leggono esempi di output, usare [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span><span class="sxs-lookup"><span data-stu-id="0aaf1-118">If you are reading output samples, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span></span> <span data-ttu-id="0aaf1-119">Se si leggono esempi di flusso, usare [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span><span class="sxs-lookup"><span data-stu-id="0aaf1-119">If you are reading stream samples, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span> <span data-ttu-id="0aaf1-120">Includere qualsiasi logica per la gestione dei buffer più adatti all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-120">Include whatever logic for managing buffers that suits your application.</span></span>
2.  <span data-ttu-id="0aaf1-121">Allocare un pool di buffer che si utilizzerà per la lettura dei file.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-121">Allocate a pool of buffers that you will use for file reading.</span></span>
    -   <span data-ttu-id="0aaf1-122">Trovare le dimensioni necessarie per i buffer chiamando [**IWMReaderAdvanced:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) o [**IWMReaderAdvanced:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) per ogni output e/o flusso per il quale viene usato il buffer.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-122">Find the size required for your buffers by calling [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) or [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) for each output and/or stream for which the buffer is used.</span></span> <span data-ttu-id="0aaf1-123">Se si usa il lettore sincrono, usare invece [**IWMSyncReader:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) o [**IWMSyncReader:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) .</span><span class="sxs-lookup"><span data-stu-id="0aaf1-123">If using the synchronous reader, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) or [**IWMSyncReader::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) instead.</span></span>
    -   <span data-ttu-id="0aaf1-124">Creare ogni buffer per il pool.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-124">Create each buffer for the pool.</span></span>
3.  <span data-ttu-id="0aaf1-125">Configurare il Reader o il lettore sincrono per la lettura.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-125">Set up the reader or synchronous reader for reading.</span></span> <span data-ttu-id="0aaf1-126">Per ulteriori informazioni, vedere la pagina relativa alla [lettura di file con il Reader asincrono](reading-files-with-the-asynchronous-reader.md) o la [lettura di file con il lettore sincrono](reading-files-with-the-synchronous-reader.md).</span><span class="sxs-lookup"><span data-stu-id="0aaf1-126">For more information see [Reading Files with the Asynchronous Reader](reading-files-with-the-asynchronous-reader.md) or [Reading Files with the Synchronous Reader](reading-files-with-the-synchronous-reader.md).</span></span>
4.  <span data-ttu-id="0aaf1-127">Prima di iniziare la scrittura, chiamare [**IWMReaderAdvanced:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) o [**IWMReaderAdvanced:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) per ogni output e flusso per il quale si stanno allocando buffer utilizzando l'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-127">Before beginning writing, call [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) or [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) for each output and stream for which you are allocating buffers using the reader object.</span></span> <span data-ttu-id="0aaf1-128">Per il lettore sincrono, chiamare [**IWMSyncReader2:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) o [**IWMSyncReader2:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) .</span><span class="sxs-lookup"><span data-stu-id="0aaf1-128">For the synchronous reader, call [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) or [**IWMSyncReader2::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) instead.</span></span>
5.  <span data-ttu-id="0aaf1-129">Iniziare a leggere il file.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-129">Begin reading the file.</span></span>

<span data-ttu-id="0aaf1-130">L'oggetto di lettura effettuerà chiamate al callback allocatore appropriato e otterrà esempi dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-130">The reading object will make calls to the appropriate allocator callback and get samples from your application.</span></span> <span data-ttu-id="0aaf1-131">La logica di gestione del buffer deve includere un modo per segnalare che un buffer può essere usato di nuovo.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-131">Your buffer management logic must include a way to signal that a buffer is free to be used again.</span></span> <span data-ttu-id="0aaf1-132">In genere, quando viene eseguito il rendering del relativo contenuto, un buffer viene inserito nuovamente nel pool.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-132">Typically, a buffer is put back into the pool when its contents are rendered.</span></span> <span data-ttu-id="0aaf1-133">A seconda dell'applicazione, potrebbero essere necessari solo pochi buffer nel pool o in molti.</span><span class="sxs-lookup"><span data-stu-id="0aaf1-133">Depending upon your application, you may need just a few buffers in the pool or many.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aaf1-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0aaf1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aaf1-135">**Lettura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="0aaf1-135">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




