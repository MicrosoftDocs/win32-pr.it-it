---
description: Utilizzando MFTrace, è possibile filtrare i risultati della traccia specificando un elenco di parole chiave.
ms.assetid: e7c382cb-94ac-4f90-a3dd-32f94c538396
title: Parole chiave MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d18a91aede8692209b9d5b7a2759c460e44043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130499"
---
# <a name="mftrace-keywords"></a><span data-ttu-id="2737a-103">Parole chiave MFTrace</span><span class="sxs-lookup"><span data-stu-id="2737a-103">MFTrace Keywords</span></span>

<span data-ttu-id="2737a-104">Utilizzando [MFTrace](mftrace.md), è possibile filtrare i risultati della traccia specificando un elenco di parole chiave.</span><span class="sxs-lookup"><span data-stu-id="2737a-104">Using [MFTrace](mftrace.md), you can filter the trace results by specifying a list of keywords.</span></span> <span data-ttu-id="2737a-105">Nella riga di comando usare l'argomento della riga di comando **-k** .</span><span class="sxs-lookup"><span data-stu-id="2737a-105">At the command line, use the **-k** command-line argument.</span></span> <span data-ttu-id="2737a-106">In alternativa, specificare l'elemento [**keyword**](keyword.md) nel file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2737a-106">Alternatively, specify the [**keyword**](keyword.md) element in the configuration file.</span></span> <span data-ttu-id="2737a-107">Per altre informazioni, vedere [uso di MFTrace](using-mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="2737a-107">For more information, see [Using MFTrace](using-mftrace.md).</span></span>

<span data-ttu-id="2737a-108">MFTrace supporta le parole chiave seguenti.</span><span class="sxs-lookup"><span data-stu-id="2737a-108">MFTrace supports the following keywords.</span></span> <span data-ttu-id="2737a-109">La maggior parte si riferisce a specifiche interfacce o esportazioni di librerie.</span><span class="sxs-lookup"><span data-stu-id="2737a-109">Most refer to particular interfaces or library exports.</span></span>

-   <span data-ttu-id="2737a-110">"All"</span><span class="sxs-lookup"><span data-stu-id="2737a-110">"All"</span></span>
-   <span data-ttu-id="2737a-111">Predefinita</span><span class="sxs-lookup"><span data-stu-id="2737a-111">"Default"</span></span>
-   <span data-ttu-id="2737a-112">Deviazioni</span><span class="sxs-lookup"><span data-stu-id="2737a-112">"Detours"</span></span>
-   <span data-ttu-id="2737a-113">"IFilterGraph"</span><span class="sxs-lookup"><span data-stu-id="2737a-113">"IFilterGraph"</span></span>
-   <span data-ttu-id="2737a-114">"IGraphBuilder"</span><span class="sxs-lookup"><span data-stu-id="2737a-114">"IGraphBuilder"</span></span>
-   <span data-ttu-id="2737a-115">IMediaControl</span><span class="sxs-lookup"><span data-stu-id="2737a-115">"IMediaControl"</span></span>
-   <span data-ttu-id="2737a-116">"IMediaObject"</span><span class="sxs-lookup"><span data-stu-id="2737a-116">"IMediaObject"</span></span>
-   <span data-ttu-id="2737a-117">IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="2737a-117">"IMemInputPin"</span></span>
-   <span data-ttu-id="2737a-118">"IMFActivate"</span><span class="sxs-lookup"><span data-stu-id="2737a-118">"IMFActivate"</span></span>
-   <span data-ttu-id="2737a-119">"IMFAttributes"</span><span class="sxs-lookup"><span data-stu-id="2737a-119">"IMFAttributes"</span></span>
-   <span data-ttu-id="2737a-120">"IMFByteStream"</span><span class="sxs-lookup"><span data-stu-id="2737a-120">"IMFByteStream"</span></span>
-   <span data-ttu-id="2737a-121">"IMFByteStreamHandler"</span><span class="sxs-lookup"><span data-stu-id="2737a-121">"IMFByteStreamHandler"</span></span>
-   <span data-ttu-id="2737a-122">"IMFClock"</span><span class="sxs-lookup"><span data-stu-id="2737a-122">"IMFClock"</span></span>
-   <span data-ttu-id="2737a-123">"IMFMediaEventGenerator"</span><span class="sxs-lookup"><span data-stu-id="2737a-123">"IMFMediaEventGenerator"</span></span>
-   <span data-ttu-id="2737a-124">"IMFMediaSession"</span><span class="sxs-lookup"><span data-stu-id="2737a-124">"IMFMediaSession"</span></span>
-   <span data-ttu-id="2737a-125">"IMFMediaSink"</span><span class="sxs-lookup"><span data-stu-id="2737a-125">"IMFMediaSink"</span></span>
-   <span data-ttu-id="2737a-126">"IMFMediaSource"</span><span class="sxs-lookup"><span data-stu-id="2737a-126">"IMFMediaSource"</span></span>
-   <span data-ttu-id="2737a-127">"IMFMediaStream"</span><span class="sxs-lookup"><span data-stu-id="2737a-127">"IMFMediaStream"</span></span>
-   <span data-ttu-id="2737a-128">"IMFPMediaItem"</span><span class="sxs-lookup"><span data-stu-id="2737a-128">"IMFPMediaItem"</span></span>
-   <span data-ttu-id="2737a-129">"IMFPMediaPlayer"</span><span class="sxs-lookup"><span data-stu-id="2737a-129">"IMFPMediaPlayer"</span></span>
-   <span data-ttu-id="2737a-130">"IMFPMediaPlayerCallback"</span><span class="sxs-lookup"><span data-stu-id="2737a-130">"IMFPMediaPlayerCallback"</span></span>
-   <span data-ttu-id="2737a-131">"IMFPresentationClock"</span><span class="sxs-lookup"><span data-stu-id="2737a-131">"IMFPresentationClock"</span></span>
-   <span data-ttu-id="2737a-132">"IMFQualityAdvise"</span><span class="sxs-lookup"><span data-stu-id="2737a-132">"IMFQualityAdvise"</span></span>
-   <span data-ttu-id="2737a-133">"IMFQualityAdvise2"</span><span class="sxs-lookup"><span data-stu-id="2737a-133">"IMFQualityAdvise2"</span></span>
-   <span data-ttu-id="2737a-134">"IMFQualityManager"</span><span class="sxs-lookup"><span data-stu-id="2737a-134">"IMFQualityManager"</span></span>
-   <span data-ttu-id="2737a-135">"IMFReadWriteClassFactory"</span><span class="sxs-lookup"><span data-stu-id="2737a-135">"IMFReadWriteClassFactory"</span></span>
-   <span data-ttu-id="2737a-136">"IMFSample"</span><span class="sxs-lookup"><span data-stu-id="2737a-136">"IMFSample"</span></span>
-   <span data-ttu-id="2737a-137">"IMFSchemeHandler"</span><span class="sxs-lookup"><span data-stu-id="2737a-137">"IMFSchemeHandler"</span></span>
-   <span data-ttu-id="2737a-138">"IMFSinkWriter"</span><span class="sxs-lookup"><span data-stu-id="2737a-138">"IMFSinkWriter"</span></span>
-   <span data-ttu-id="2737a-139">"IMFSourceReader"</span><span class="sxs-lookup"><span data-stu-id="2737a-139">"IMFSourceReader"</span></span>
-   <span data-ttu-id="2737a-140">"IMFSourceReaderCallback"</span><span class="sxs-lookup"><span data-stu-id="2737a-140">"IMFSourceReaderCallback"</span></span>
-   <span data-ttu-id="2737a-141">"IMFSourceResolver"</span><span class="sxs-lookup"><span data-stu-id="2737a-141">"IMFSourceResolver"</span></span>
-   <span data-ttu-id="2737a-142">"IMFStreamSink"</span><span class="sxs-lookup"><span data-stu-id="2737a-142">"IMFStreamSink"</span></span>
-   <span data-ttu-id="2737a-143">"IMFTopoLoader"</span><span class="sxs-lookup"><span data-stu-id="2737a-143">"IMFTopoLoader"</span></span>
-   <span data-ttu-id="2737a-144">"IMFTopology"</span><span class="sxs-lookup"><span data-stu-id="2737a-144">"IMFTopology"</span></span>
-   <span data-ttu-id="2737a-145">"IMFTopologyNode"</span><span class="sxs-lookup"><span data-stu-id="2737a-145">"IMFTopologyNode"</span></span>
-   <span data-ttu-id="2737a-146">"IMFTransform"</span><span class="sxs-lookup"><span data-stu-id="2737a-146">"IMFTransform"</span></span>
-   <span data-ttu-id="2737a-147">"IWMReader"</span><span class="sxs-lookup"><span data-stu-id="2737a-147">"IWMReader"</span></span>
-   <span data-ttu-id="2737a-148">"Kernel32Export"</span><span class="sxs-lookup"><span data-stu-id="2737a-148">"Kernel32Export"</span></span>
-   <span data-ttu-id="2737a-149">"MFExport"</span><span class="sxs-lookup"><span data-stu-id="2737a-149">"MFExport"</span></span>
-   <span data-ttu-id="2737a-150">"MFPlatExport"</span><span class="sxs-lookup"><span data-stu-id="2737a-150">"MFPlatExport"</span></span>
-   <span data-ttu-id="2737a-151">"MFPlayExport"</span><span class="sxs-lookup"><span data-stu-id="2737a-151">"MFPlayExport"</span></span>
-   <span data-ttu-id="2737a-152">"MFPublic"</span><span class="sxs-lookup"><span data-stu-id="2737a-152">"MFPublic"</span></span>
-   <span data-ttu-id="2737a-153">"MFReadWriteExport"</span><span class="sxs-lookup"><span data-stu-id="2737a-153">"MFReadWriteExport"</span></span>
-   <span data-ttu-id="2737a-154">"Ole32Export"</span><span class="sxs-lookup"><span data-stu-id="2737a-154">"Ole32Export"</span></span>
-   <span data-ttu-id="2737a-155">"wmvCoreExport"</span><span class="sxs-lookup"><span data-stu-id="2737a-155">"wmvCoreExport"</span></span>

## <a name="related-topics"></a><span data-ttu-id="2737a-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2737a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2737a-157">MFTrace</span><span class="sxs-lookup"><span data-stu-id="2737a-157">MFTrace</span></span>](mftrace.md)
</dt> <dt>

[<span data-ttu-id="2737a-158">Uso di MFTrace</span><span class="sxs-lookup"><span data-stu-id="2737a-158">Using MFTrace</span></span>](using-mftrace.md)
</dt> </dl>

 

 



