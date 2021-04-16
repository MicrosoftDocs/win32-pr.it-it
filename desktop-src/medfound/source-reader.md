---
description: Il lettore di origine rappresenta un'alternativa all'uso della sessione multimediale e della pipeline Microsoft Media Foundation per elaborare i dati multimediali.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lettore di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527829"
---
# <a name="source-reader"></a><span data-ttu-id="c1ed8-103">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="c1ed8-103">Source Reader</span></span>

<span data-ttu-id="c1ed8-104">Il lettore di origine rappresenta un'alternativa all'uso della [sessione multimediale](media-session.md) e della pipeline Microsoft Media Foundation per elaborare i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-104">The Source Reader is an alternative to using the [Media Session](media-session.md) and the Microsoft Media Foundation pipeline to process media data.</span></span>

## <a name="why-use-the-source-reader"></a><span data-ttu-id="c1ed8-105">Perché usare il lettore di origine?</span><span class="sxs-lookup"><span data-stu-id="c1ed8-105">Why Use the Source Reader?</span></span>

<span data-ttu-id="c1ed8-106">Media Foundation fornisce una pipeline ottimizzata per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-106">Media Foundation provides a pipeline that is optimized for playback.</span></span> <span data-ttu-id="c1ed8-107">La pipeline è end-to-end, ovvero gestisce il flusso di dati dall'origine, ad esempio un file video, fino alla destinazione, ad esempio la visualizzazione grafica.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-107">The pipeline is end-to-end, meaning it handles data flow from the source (such as a video file) all the way to the destination (such as the graphics display).</span></span> <span data-ttu-id="c1ed8-108">Tuttavia, se si desidera leggere o modificare i dati durante la pipeline, è necessario scrivere un plug-in personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-108">However, if you want to read or modify the data as it goes through the pipeline, you must write a custom plug-in.</span></span> <span data-ttu-id="c1ed8-109">Questa operazione richiede una conoscenza abbastanza approfondita della pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-109">That requires a fairly deep knowledge of the Media Foundation pipeline.</span></span> <span data-ttu-id="c1ed8-110">Per alcune attività, la creazione di un nuovo plug-in è un sovraccarico eccessivo.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-110">For certain tasks, creating a new plug-in is too much overhead.</span></span> <span data-ttu-id="c1ed8-111">Il lettore di origine è progettato per questo tipo di situazione, quando si desidera ottenere i dati non elaborati da un'origine senza l'overhead dell'intera pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-111">The source reader is designed for this type of situation, when you want to get the raw data from a source without the overhead of the entire pipeline.</span></span>

<span data-ttu-id="c1ed8-112">Internamente, il lettore di origine include un puntatore a un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-112">Internally, the source reader holds a pointer to a media source.</span></span> <span data-ttu-id="c1ed8-113">Un' *origine multimediale* è un oggetto Media Foundation che genera dati multimediali da un'origine esterna, ad esempio un file multimediale o un dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-113">A *media source* is a Media Foundation object that generates media data from an external source, such as a media file or video capture device.</span></span> <span data-ttu-id="c1ed8-114">Il lettore di origine gestisce tutte le chiamate al metodo all'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-114">The source reader manages all of the method calls to the media source.</span></span> <span data-ttu-id="c1ed8-115">Per altre informazioni sulle origini multimediali, vedere [origini multimediali](media-sources.md).</span><span class="sxs-lookup"><span data-stu-id="c1ed8-115">(For more information about media sources, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="c1ed8-116">Se l'origine multimediale recapita dati compressi, è possibile usare il lettore di origine per decodificare i dati.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-116">If the media source delivers compressed data, you can use the source reader to decode the data.</span></span> <span data-ttu-id="c1ed8-117">In tal caso, il lettore di origine caricherà il decoder corretto e gestirà il flusso di dati tra l'origine multimediale e il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-117">In that case, the source reader will load the correct decoder and manage the data flow between the media source and the decoder.</span></span> <span data-ttu-id="c1ed8-118">Il lettore di origine può anche eseguire un'elaborazione video limitata: conversione dei colori da YUV a RGB-32 e deinterlacciamento software, anche se queste operazioni non sono consigliate per il rendering video in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-118">The source reader can also perform some limited video processing: color conversion from YUV to RGB-32, and software deinterlacing, although these operations are not recommended for real-time video rendering.</span></span> <span data-ttu-id="c1ed8-119">Questo processo è illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-119">The following image illustrates this process.</span></span>

![diagramma del lettore di origine](images/sourcereader.png)

<span data-ttu-id="c1ed8-121">Il lettore di origine non invia i dati a una destinazione. è necessario che l'applicazione utilizzi i dati.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-121">The source reader does not send the data to a destination; it is up to the application to consume the data.</span></span> <span data-ttu-id="c1ed8-122">Ad esempio, il lettore di origine può leggere un file video, ma non eseguirà il rendering del video sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-122">For example, the source reader can read a video file, but it will not render the video to the screen.</span></span> <span data-ttu-id="c1ed8-123">Inoltre, il lettore di origine non gestisce un clock di presentazione, gestisce problemi di temporizzazione o Sincronizza video con audio.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-123">Also, the source reader does not manage a presentation clock, handle timing issues, or synchronize video with audio.</span></span>

<span data-ttu-id="c1ed8-124">Provare a usare il lettore di origine nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1ed8-124">Consider using the source reader when:</span></span>

-   <span data-ttu-id="c1ed8-125">Si desidera ottenere dati da un file multimediale senza preoccuparsi della struttura di file sottostante.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-125">You want to get data from a media file without worrying about the underlying file structure.</span></span>
-   <span data-ttu-id="c1ed8-126">Si desidera ottenere dati da un dispositivo di acquisizione audio o video.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-126">You want to get data from an audio or video capture device.</span></span>
-   <span data-ttu-id="c1ed8-127">Le attività di elaborazione dati non sono sensibili al tempo oppure non è necessario un clock di presentazione.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-127">Your data-processing tasks are not time sensitive, or you do not require a presentation clock.</span></span>
-   <span data-ttu-id="c1ed8-128">Si dispone già di una pipeline multimediale che non si basa su Media Foundation e si desidera incorporare i Media Foundation origini multimediali nella propria pipeline.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-128">You already have a media pipeline that is not based on Media Foundation, and you want to incorporate the Media Foundation media sources into your own pipeline.</span></span>

<span data-ttu-id="c1ed8-129">Il lettore di origine non è consigliato nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1ed8-129">The source reader is not recommended in the following situations:</span></span>

-   <span data-ttu-id="c1ed8-130">Per il contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-130">For protected content.</span></span> <span data-ttu-id="c1ed8-131">Il lettore di origine non supporta Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="c1ed8-131">The source reader does not support digital rights management (DRM).</span></span>
-   <span data-ttu-id="c1ed8-132">Se si è interessati ai dettagli della struttura di file sottostante.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-132">If you care about the details of the underlying file structure.</span></span> <span data-ttu-id="c1ed8-133">Il lettore di origine nasconde quel tipo di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-133">The source reader hides that type of detail.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c1ed8-134">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c1ed8-134">In this section</span></span>



| <span data-ttu-id="c1ed8-135">Argomento</span><span class="sxs-lookup"><span data-stu-id="c1ed8-135">Topic</span></span>                                                                                                        | <span data-ttu-id="c1ed8-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1ed8-136">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1ed8-137">Utilizzo del lettore di origine per l'elaborazione dei dati multimediali</span><span class="sxs-lookup"><span data-stu-id="c1ed8-137">Using the Source Reader to Process Media Data</span></span>](processing-media-data-with-the-source-reader.md)<br/> | <span data-ttu-id="c1ed8-138">In questo argomento viene descritto come utilizzare il lettore di origine per elaborare i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-138">This topic describes how to use the Source Reader to process media data.</span></span><br/>                                               |
| [<span data-ttu-id="c1ed8-139">Utilizzo del lettore di origine in modalità asincrona</span><span class="sxs-lookup"><span data-stu-id="c1ed8-139">Using the Source Reader in Asynchronous Mode</span></span>](using-the-source-reader-in-asynchronous-mode.md)<br/>  | <span data-ttu-id="c1ed8-140">In questo argomento viene descritto come utilizzare il lettore di origine in modalità asincrona.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-140">This topic describes how to use the Source Reader in asynchronous mode.</span></span><br/>                                                |
| [<span data-ttu-id="c1ed8-141">Esercitazione: decodifica audio</span><span class="sxs-lookup"><span data-stu-id="c1ed8-141">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)<br/>                                          | <span data-ttu-id="c1ed8-142">Questa esercitazione illustra come usare il lettore di origine per decodificare l'audio da un file multimediale e scrivere l'audio in un file WAVE.</span><span class="sxs-lookup"><span data-stu-id="c1ed8-142">This tutorial shows how to use the Source Reader to decode audio from a media file and write the audio to a WAVE file.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c1ed8-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1ed8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1ed8-144">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1ed8-144">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="c1ed8-145">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1ed8-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="c1ed8-146">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="c1ed8-146">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




