---
description: Esempio WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Esempio WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880566"
---
# <a name="wavsource-sample"></a><span data-ttu-id="f61df-103">Esempio WavSource</span><span class="sxs-lookup"><span data-stu-id="f61df-103">WavSource Sample</span></span>

<span data-ttu-id="f61df-104">Viene illustrato come creare un'origine multimediale personalizzata in Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f61df-104">Shows how to create a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="f61df-105">Nell'esempio viene implementata un'origine multimediale che analizza i file audio WAV.</span><span class="sxs-lookup"><span data-stu-id="f61df-105">The sample implements a media source that parses .wav audio files.</span></span>

<span data-ttu-id="f61df-106">Questo esempio è un esempio relativamente semplice di un'origine multimediale:</span><span class="sxs-lookup"><span data-stu-id="f61df-106">This sample is a relatively simple example of a media source:</span></span>

-   <span data-ttu-id="f61df-107">Esiste un solo flusso, pertanto non è disponibile codice per implementare la selezione del flusso.</span><span class="sxs-lookup"><span data-stu-id="f61df-107">There is only one stream, so there is no code to implement stream selection.</span></span>
-   <span data-ttu-id="f61df-108">L'origine multimediale non implementa il controllo della frequenza, ovvero la riproduzione veloce o inversa.</span><span class="sxs-lookup"><span data-stu-id="f61df-108">The media source does not implement rate control (that is, fast forward or reverse playback).</span></span>
-   <span data-ttu-id="f61df-109">Tutti i metodi source e Stream vengono implementati come metodi sincroni.</span><span class="sxs-lookup"><span data-stu-id="f61df-109">All source and stream methods are implemented as synchronous methods.</span></span>
-   <span data-ttu-id="f61df-110">Poiché la parte relativa ai dati di un file WAV è costituita da un singolo blocco di audio PCM non compresso, non è necessario che l'origine supporti legga le intestazioni dei pacchetti né analizzi il flusso durante la riproduzione, oltre a leggere l'intestazione [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) iniziale.</span><span class="sxs-lookup"><span data-stu-id="f61df-110">Because the data portion of a .wav file is a single block of uncompressed PCM audio, the media source does not need to read packet headers or otherwise parse the stream during playback, other than reading the initial [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) header.</span></span>

<span data-ttu-id="f61df-111">Per un esempio più avanzato di un'origine multimediale, vedere l'esempio [MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f61df-111">For a more advanced example of a media source, see the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="f61df-112">API illustrate</span><span class="sxs-lookup"><span data-stu-id="f61df-112">APIs Demonstrated</span></span>

<span data-ttu-id="f61df-113">In questo esempio vengono illustrate le interfacce Media Foundation seguenti:</span><span class="sxs-lookup"><span data-stu-id="f61df-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="f61df-114">**IMFByteStreamHandler**</span><span class="sxs-lookup"><span data-stu-id="f61df-114">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="f61df-115">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="f61df-115">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="f61df-116">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="f61df-116">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a><span data-ttu-id="f61df-117">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f61df-117">Usage</span></span>

<span data-ttu-id="f61df-118">L'esempio WavSource compila una DLL che è un server COM per il gestore del flusso di byte di origine multimediale e di origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="f61df-118">The WavSource sample builds a DLL that is a COM server for both the media source and media source's byte-stream handler.</span></span> <span data-ttu-id="f61df-119">Prima di usare l'origine del supporto, è necessario registrare la DLL.</span><span class="sxs-lookup"><span data-stu-id="f61df-119">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="f61df-120">Per usare l'origine del supporto, è possibile eseguire [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f61df-120">To use the media source, you can run the [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="f61df-121">Il resolver di origine caricherà automaticamente l'origine del supporto se si seleziona un file WAV per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f61df-121">The source resolver will automatically load the media source if you select a .wav file for playback.</span></span> <span data-ttu-id="f61df-122">Se si verifica un errore, verificare che la DLL WavSource sia stata registrata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f61df-122">(If an error occurs, make sure that you successfully registered the WavSource DLL.)</span></span>

<span data-ttu-id="f61df-123">È anche possibile usare lo strumento TopoEdit per creare una topologia di riproduzione che contiene l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="f61df-123">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="f61df-124">Per ulteriori informazioni su TopoEdit, vedere [TopoEdit](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="f61df-124">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f61df-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f61df-125">Requirements</span></span>



| <span data-ttu-id="f61df-126">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f61df-126">Product</span></span>                                                        | <span data-ttu-id="f61df-127">Versione</span><span class="sxs-lookup"><span data-stu-id="f61df-127">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="f61df-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f61df-128">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="f61df-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f61df-129">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f61df-130">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="f61df-130">Downloading the Sample</span></span>

<span data-ttu-id="f61df-131">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span><span class="sxs-lookup"><span data-stu-id="f61df-131">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f61df-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f61df-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f61df-133">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="f61df-133">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="f61df-134">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="f61df-134">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="f61df-135">Esempio MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="f61df-135">MPEG1Source Sample</span></span>](mpeg1source-sample.md)
</dt> <dt>

[<span data-ttu-id="f61df-136">Gestori di schemi e gestori di Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="f61df-136">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="f61df-137">Scrittura di un'origine multimediale personalizzata</span><span class="sxs-lookup"><span data-stu-id="f61df-137">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
