---
title: Uso di flussi audio e video non compressi
description: Uso di flussi audio e video non compressi
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- flussi, configurazione di flussi audio e video non compressi
- codec, configurazione di flussi audio e video non compressi
- flussi video, non compressi
- flussi audio, non compressi
- flussi audio e video non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299431"
---
# <a name="using-uncompressed-audio-and-video-streams"></a><span data-ttu-id="8e8d1-108">Uso di flussi audio e video non compressi</span><span class="sxs-lookup"><span data-stu-id="8e8d1-108">Using Uncompressed Audio and Video Streams</span></span>

<span data-ttu-id="8e8d1-109">Nella maggior parte dei casi, i supporti non compressi hanno requisiti di archiviazione e di distribuzione di grandi dimensioni, ma per alcuni scenari di riproduzione locali il livello di qualità è sufficientemente importante da garantire la mancata utilizzo della compressione.</span><span class="sxs-lookup"><span data-stu-id="8e8d1-109">Under most circumstances, uncompressed media has prohibitively large storage and delivery requirements, but for some local playback scenarios, the quality level is important enough to warrant not using compression..</span></span>

<span data-ttu-id="8e8d1-110">Le impostazioni per un flusso multimediale non compresso devono riflettere le impostazioni del supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="8e8d1-110">The settings for an uncompressed media stream should reflect the settings of the source media.</span></span> <span data-ttu-id="8e8d1-111">Quando si configura un flusso non compresso, è necessario calcolare la velocità in bit del supporto e impostare il flusso in modo appropriato chiamando [**IWMStreamConfig:: bitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span><span class="sxs-lookup"><span data-stu-id="8e8d1-111">When configuring an uncompressed stream, you must calculate the bit rate of the media and set the stream appropriately by calling [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span></span> <span data-ttu-id="8e8d1-112">Poiché i flussi non compressi non possono essere usati per lo streaming, è sempre necessario impostare la finestra buffer per i flussi multimediali non compressi su zero chiamando [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span><span class="sxs-lookup"><span data-stu-id="8e8d1-112">Because uncompressed streams are not viable for streaming, you should always set the buffer window for uncompressed media streams to zero by calling [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span></span>

<span data-ttu-id="8e8d1-113">I formati pixel seguenti sono supportati per i flussi video non compressi:</span><span class="sxs-lookup"><span data-stu-id="8e8d1-113">The following pixel formats are supported for uncompressed video streams:</span></span>

-   <span data-ttu-id="8e8d1-114">\_RGB555 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-114">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="8e8d1-115">\_RGB24 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-115">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="8e8d1-116">\_Rgb32 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-116">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="8e8d1-117">\_I420 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-117">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="8e8d1-118">\_IYUV WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-118">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="8e8d1-119">\_YV12 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-119">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="8e8d1-120">\_YUY2 WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-120">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="8e8d1-121">\_UYVY WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-121">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="8e8d1-122">\_YVYU WMMEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8d1-122">WMMEDIASUBTYPE\_YVYU</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e8d1-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e8d1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e8d1-124">**Configurazione comune a tutti i flussi**</span><span class="sxs-lookup"><span data-stu-id="8e8d1-124">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="8e8d1-125">**Configurazione di flussi audio**</span><span class="sxs-lookup"><span data-stu-id="8e8d1-125">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="8e8d1-126">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="8e8d1-126">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="8e8d1-127">**Configurazione dei flussi video**</span><span class="sxs-lookup"><span data-stu-id="8e8d1-127">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




