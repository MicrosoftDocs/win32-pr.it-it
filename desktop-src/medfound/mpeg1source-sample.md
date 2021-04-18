---
description: Esempio MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Esempio MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309072"
---
# <a name="mpeg1source-sample"></a><span data-ttu-id="2ccab-103">Esempio MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="2ccab-103">MPEG1Source Sample</span></span>

<span data-ttu-id="2ccab-104">Viene illustrato come scrivere un'origine multimediale personalizzata in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2ccab-104">Shows how to write a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="2ccab-105">L'esempio implementa un'origine multimediale che analizza i flussi a livello di sistemi MPEG-1 e genera esempi che contengono payload MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="2ccab-105">The sample implements a media source that parses MPEG-1 systems-layer streams and generates samples that contain MPEG-1 payloads.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="2ccab-106">API illustrate</span><span class="sxs-lookup"><span data-stu-id="2ccab-106">APIs Demonstrated</span></span>

<span data-ttu-id="2ccab-107">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="2ccab-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="2ccab-108">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="2ccab-108">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="2ccab-109">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="2ccab-109">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="2ccab-110">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="2ccab-110">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

<span data-ttu-id="2ccab-111">Prima di esaminare questo esempio, è opportuno esaminare l' [esempio WavSource](wavsource-sample.md), che fornisce un'implementazione più semplice di un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="2ccab-111">Before examining this sample, you might want to review the [WavSource Sample](wavsource-sample.md), which provides a simpler implementation of a media source.</span></span> <span data-ttu-id="2ccab-112">L'esempio MPEG1Source aggiunge alcune funzionalità che si trovano nella maggior parte delle implementazioni reali di un'origine multimediale:</span><span class="sxs-lookup"><span data-stu-id="2ccab-112">The MPEG1Source sample adds some features that would be found in most real-world implementations of a media source:</span></span>

-   <span data-ttu-id="2ccab-113">Più flussi</span><span class="sxs-lookup"><span data-stu-id="2ccab-113">Multiple streams</span></span>
-   <span data-ttu-id="2ccab-114">Metodi asincroni</span><span class="sxs-lookup"><span data-stu-id="2ccab-114">Asynchronous methods</span></span>
-   <span data-ttu-id="2ccab-115">I/O asincrono</span><span class="sxs-lookup"><span data-stu-id="2ccab-115">Asynchronous I/O</span></span>

<span data-ttu-id="2ccab-116">Nell'Windows SDK per Windows Server 2008, questo esempio include anche un decodificatore MPEG-1 video di esempio che Visualizza il codice temporale per ogni fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="2ccab-116">In the Windows SDK for Windows Server 2008, this sample also includes a sample MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="2ccab-117">Non decodifica effettivamente il Bitstream MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="2ccab-117">(It does not actually decode the MPEG-1 bitstream.)</span></span>

<span data-ttu-id="2ccab-118">A partire da Windows SDK per Windows 7, il decodificatore è stato spostato in un esempio separato.</span><span class="sxs-lookup"><span data-stu-id="2ccab-118">Starting in the Windows SDK for Windows 7, the decoder has been moved to a separate sample.</span></span> <span data-ttu-id="2ccab-119">Vedere [esempio di decodificatore](decoder-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2ccab-119">See [Decoder Sample](decoder-sample.md).</span></span>

## <a name="usage"></a><span data-ttu-id="2ccab-120">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="2ccab-120">Usage</span></span>

<span data-ttu-id="2ccab-121">L'esempio MPEG1Source compila una DLL che è un server COM per l'origine del supporto, il gestore del flusso di byte dell'origine multimediale e il decodificatore MFT.</span><span class="sxs-lookup"><span data-stu-id="2ccab-121">The MPEG1Source sample builds a DLL that is a COM server for the media source, media source's byte-stream handler, and the decoder MFT.</span></span> <span data-ttu-id="2ccab-122">Prima di usare l'origine del supporto, è necessario registrare la DLL.</span><span class="sxs-lookup"><span data-stu-id="2ccab-122">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="2ccab-123">Per usare l'origine del supporto, è possibile eseguire l' [esempio BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ccab-123">To use the media source, you can run the [BasicPlayback Sample](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="2ccab-124">Il sistema di risoluzione di origine caricherà automaticamente l'origine del supporto se si seleziona un file MPEG-1 per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="2ccab-124">The source resolver will automatically load the media source if you select an MPEG-1 file for playback.</span></span> <span data-ttu-id="2ccab-125">Se si verifica un errore, verificare che la DLL MPEG1Source sia stata registrata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2ccab-125">(If an error occurs, make sure that you successfully registered the MPEG1Source DLL.)</span></span>

<span data-ttu-id="2ccab-126">È anche possibile usare lo strumento TopoEdit per creare una topologia di riproduzione che contiene l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="2ccab-126">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="2ccab-127">Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="2ccab-127">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ccab-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ccab-128">Requirements</span></span>



| <span data-ttu-id="2ccab-129">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2ccab-129">Product</span></span>                                                        | <span data-ttu-id="2ccab-130">Versione</span><span class="sxs-lookup"><span data-stu-id="2ccab-130">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="2ccab-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="2ccab-131">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="2ccab-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2ccab-132">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="2ccab-133">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2ccab-133">Downloading the Sample</span></span>

<span data-ttu-id="2ccab-134">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span><span class="sxs-lookup"><span data-stu-id="2ccab-134">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ccab-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2ccab-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ccab-136">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="2ccab-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="2ccab-137">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="2ccab-137">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="2ccab-138">Gestori di schemi e gestori di Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="2ccab-138">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="2ccab-139">Esercitazione: scrittura di un'origine multimediale personalizzata</span><span class="sxs-lookup"><span data-stu-id="2ccab-139">Tutorial: Writing a Custom Media Source</span></span>](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[<span data-ttu-id="2ccab-140">Esempio WavSource</span><span class="sxs-lookup"><span data-stu-id="2ccab-140">WavSource Sample</span></span>](wavsource-sample.md)
</dt> </dl>

 

 
