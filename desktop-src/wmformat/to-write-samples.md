---
title: Per scrivere esempi
description: Per scrivere esempi
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- ASF (Advanced Systems Format), scrittura di esempi
- ASF (Advanced Systems Format), scrittura di esempi
- ASF (Advanced Systems Format), passaggio di campioni al writer
- ASF (Advanced Systems Format), passaggio di campioni al writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398566"
---
# <a name="to-write-samples"></a><span data-ttu-id="c9788-107">Per scrivere esempi</span><span class="sxs-lookup"><span data-stu-id="c9788-107">To Write Samples</span></span>

<span data-ttu-id="c9788-108">Dopo aver identificato e configurato gli input per il file che si sta scrivendo, è possibile iniziare a passare gli esempi al writer.</span><span class="sxs-lookup"><span data-stu-id="c9788-108">When you have identified and configured the inputs for the file you are writing, you can begin passing samples to the writer.</span></span> <span data-ttu-id="c9788-109">Per rendere più efficiente il processo di scrittura, è necessario passare gli esempi in ordine temporale di presentazione, se possibile.</span><span class="sxs-lookup"><span data-stu-id="c9788-109">You should pass samples in presentation-time order, if possible, to make the writing process more efficient.</span></span>

<span data-ttu-id="c9788-110">Prima di passare gli esempi, è necessario impostare il writer affinché li accetti chiamando [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="c9788-110">Before passing any samples, you must set the writer to accept them by calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="c9788-111">Per passare un esempio al writer, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="c9788-111">To pass a sample to the writer, perform the following steps:</span></span>

1.  <span data-ttu-id="c9788-112">Allocare un buffer e recuperare un puntatore all'interfaccia [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) chiamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="c9788-112">Allocate a buffer and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="c9788-113">Recuperare l'indirizzo del buffer creato nel passaggio 1 chiamando [**INSSBuffer:: GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span><span class="sxs-lookup"><span data-stu-id="c9788-113">Retrieve the address of the buffer created in step 1 by calling [**INSSBuffer::GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).</span></span>
3.  <span data-ttu-id="c9788-114">Copiare i dati di esempio nella posizione del buffer, assicurandosi che l'esempio passato venga inserito nel buffer allocato.</span><span class="sxs-lookup"><span data-stu-id="c9788-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="c9788-115">Per copiare i dati, è possibile usare qualsiasi funzione di copia della memoria.</span><span class="sxs-lookup"><span data-stu-id="c9788-115">You can use any memory copying function to copy your data.</span></span> <span data-ttu-id="c9788-116">Una scelta comune è memcpy, inclusa nella libreria di runtime del linguaggio C standard.</span><span class="sxs-lookup"><span data-stu-id="c9788-116">A common choice is memcpy, which is included in the standard C run-time library.</span></span>
4.  <span data-ttu-id="c9788-117">Aggiornare la quantità di dati utilizzati nel buffer in modo da riflettere le dimensioni effettive dell'esempio chiamando [**INSSBuffer:: selength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="c9788-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="c9788-118">Passare l'interfaccia del buffer al writer insieme al numero di input e al tempo di campionamento usando il metodo [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="c9788-118">Pass the buffer interface to the writer along with the input number and sample time using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="c9788-119">Tutti gli esempi audio di un input rappresentano la stessa durata del contenuto, pertanto è possibile calcolare l'ora di esempio aggiungendo la durata del campione a un totale parziale.</span><span class="sxs-lookup"><span data-stu-id="c9788-119">All audio samples for an input represent the same duration of content, so you can figure the sample time by adding the sample duration to a running total.</span></span> <span data-ttu-id="c9788-120">Per i video, è necessario calcolare il tempo in base alla frequenza dei fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="c9788-120">For video, you need to calculate the time based on the frame rate.</span></span>

<span data-ttu-id="c9788-121">**WriteSample** funziona in modo asincrono e potrebbe non terminare la scrittura dei dati dal buffer prima che l'applicazione sia pronta per chiamare nuovamente il metodo.</span><span class="sxs-lookup"><span data-stu-id="c9788-121">**WriteSample** works asynchronously and might not finish writing the data from the buffer before your application is ready to call the method again.</span></span> <span data-ttu-id="c9788-122">È quindi importante chiamare **AllocateSample** una volta per ogni chiamata a **WriteSample**.</span><span class="sxs-lookup"><span data-stu-id="c9788-122">Therefore, it is important to call **AllocateSample** once for each call to **WriteSample**.</span></span> <span data-ttu-id="c9788-123">Tuttavia, è possibile rilasciare l'interfaccia **INSSBuffer** immediatamente dopo aver chiamato **WriteSample**.</span><span class="sxs-lookup"><span data-stu-id="c9788-123">However, you can release the **INSSBuffer** interface immediately after calling **WriteSample**.</span></span>

<span data-ttu-id="c9788-124">Al termine del passaggio degli esempi, chiamare [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span><span class="sxs-lookup"><span data-stu-id="c9788-124">When you have finished passing samples, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).</span></span>

<span data-ttu-id="c9788-125">**Nota** È importante che gli esempi di tutti i flussi nel file vengano passati al writer in sincronizzazione tra loro.</span><span class="sxs-lookup"><span data-stu-id="c9788-125">**Note** It is important that samples from all streams in the file are passed to the writer in synchronization with one another.</span></span> <span data-ttu-id="c9788-126">Ovvero, quando possibile, è necessario passare campioni al writer in ordine di tempo di presentazione entro la tolleranza di sincronizzazione specificata in [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="c9788-126">That is, whenever possible you should pass samples to the writer in presentation-time order within the sync tolerance specified in [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span> <span data-ttu-id="c9788-127">I risultati migliori si ottengono quando i dati vengono recapitati a ogni flusso in unità di un secondo o meno.</span><span class="sxs-lookup"><span data-stu-id="c9788-127">Best results are achieved when data is delivered to each stream in units of one second or less.</span></span>

<span data-ttu-id="c9788-128">I flussi devono terminare anche approssimativamente allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="c9788-128">Streams should also end at approximately the same time.</span></span> <span data-ttu-id="c9788-129">Ad esempio, non è consigliabile scrivere un file con un flusso audio di 45 secondi e un flusso video di lunghezza pari a 50 secondi.</span><span class="sxs-lookup"><span data-stu-id="c9788-129">For example, you should not write a file with an audio stream that is 45 seconds long and a video stream that is 50 seconds long.</span></span> <span data-ttu-id="c9788-130">Se si codifica un file di questo tipo con input non modificati, alcuni dati audio alla fine del flusso verranno eliminati (anche se si tratta del flusso più breve).</span><span class="sxs-lookup"><span data-stu-id="c9788-130">If you encode such a file with unaltered inputs, some of the audio data at the end of the stream will be dropped (even though it is the shorter stream).</span></span> <span data-ttu-id="c9788-131">Per fare in modo che la codifica dei file funzioni, è necessario aggiungere 5 secondi di silenzio all'input audio, in modo che un flusso non termini alcuni secondi prima di un altro.</span><span class="sxs-lookup"><span data-stu-id="c9788-131">To make the file encoding work, you should add 5 seconds of silence to the audio input so that one stream does not end several seconds before another.</span></span> <span data-ttu-id="c9788-132">Non è necessario che i tipi di flusso con esempi intermittenti, ad esempio flussi di testo o immagini, vengano riempiti in questo modo.</span><span class="sxs-lookup"><span data-stu-id="c9788-132">It is not necessary for stream types with intermittent samples, like text or image streams, to be padded in this way.</span></span> <span data-ttu-id="c9788-133">I flussi del comando per script devono seguire anche tutte queste regole.</span><span class="sxs-lookup"><span data-stu-id="c9788-133">Script command streams should also follow all these rules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9788-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9788-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9788-135">**Interfaccia INSSBuffer**</span><span class="sxs-lookup"><span data-stu-id="c9788-135">**INSSBuffer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[<span data-ttu-id="c9788-136">**Interfaccia IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="c9788-136">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="c9788-137">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="c9788-137">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




