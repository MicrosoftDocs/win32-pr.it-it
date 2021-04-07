---
title: Configurazione dei flussi video per le prestazioni di ricerca
description: Configurazione dei flussi video per le prestazioni di ricerca
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- flussi, configurazione di flussi video
- codec, configurazione dei flussi video
- flussi video, configurazione
- flussi video, prestazioni
- prestazioni, flussi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723438"
---
# <a name="configuring-video-streams-for-seeking-performance"></a><span data-ttu-id="00b0f-108">Configurazione dei flussi video per le prestazioni di ricerca</span><span class="sxs-lookup"><span data-stu-id="00b0f-108">Configuring Video Streams for Seeking Performance</span></span>

<span data-ttu-id="00b0f-109">Alcune applicazioni di riproduzione eseguono molte ricerche nei singoli flussi.</span><span class="sxs-lookup"><span data-stu-id="00b0f-109">Some playback applications perform a lot of seeking on individual streams.</span></span> <span data-ttu-id="00b0f-110">La ricerca è un'area in cui le prestazioni possono variare significativamente a seconda delle impostazioni del flusso.</span><span class="sxs-lookup"><span data-stu-id="00b0f-110">Seeking is an area where performance can vary greatly depending upon the settings of the stream.</span></span> <span data-ttu-id="00b0f-111">Se si sa che il contenuto deve essere ottimizzato per la ricerca rapida, è possibile personalizzare la configurazione del flusso per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="00b0f-111">If you know your content needs to be optimized for quick seeking, you can tailor your stream configuration to improve performance.</span></span>

<span data-ttu-id="00b0f-112">Il fattore più importante che influisce sulla velocità delle operazioni di ricerca nel video è la spaziatura dei fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="00b0f-112">The biggest factor affecting the speed of seeking operations in video is the spacing of the key frames.</span></span> <span data-ttu-id="00b0f-113">Poiché ogni frame tra fotogrammi chiave deve essere ricostruito in base ai frame che lo precedono, i fotogrammi chiave con spazi ampi risultano più lunghi.</span><span class="sxs-lookup"><span data-stu-id="00b0f-113">Because every frame between key frames needs to be reconstructed based on the frames that come before it, widely spaced key frames result longer seek times.</span></span> <span data-ttu-id="00b0f-114">Se, ad esempio, un flusso video con 30 fotogrammi al secondo ha una spaziatura massima con fotogrammi chiave di 10 secondi, esistono potenzialmente 300 di frame tra fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="00b0f-114">For example, if a video stream with 30 frames per second has a maximum key-frame spacing of 10 seconds, there are potentially 300 frames between key frames.</span></span> <span data-ttu-id="00b0f-115">Se si cerca l'ultimo [*frame Delta*](wmformat-glossary.md), è necessario ricostruire i frame 299 per la decompressione del fotogramma.</span><span class="sxs-lookup"><span data-stu-id="00b0f-115">If you seek to the last [*delta frame*](wmformat-glossary.md), 299 frames have to be reconstructed for the frame to be decompressed.</span></span> <span data-ttu-id="00b0f-116">Se ogni ricostruzione di frame ha richiesto .01 secondi, la ricerca richiederebbe circa 3 secondi.</span><span class="sxs-lookup"><span data-stu-id="00b0f-116">If each frame reconstruction took .01 second, the seek would take almost 3 seconds.</span></span> <span data-ttu-id="00b0f-117">Se si desidera aumentare l'efficienza della ricerca, è possibile ridurre la spaziatura dei fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="00b0f-117">If you want to increase the efficiency of seeking, lowering the key-frame spacing can help.</span></span> <span data-ttu-id="00b0f-118">Tuttavia, se si impostano i fotogrammi chiave troppo vicini, è possibile perdere la qualità.</span><span class="sxs-lookup"><span data-stu-id="00b0f-118">However, if you set the key frames too close together, you can lose quality.</span></span>

<span data-ttu-id="00b0f-119">È possibile impostare la spaziatura massima del fotogramma chiave chiamando [**IWMVideoMediaProps:: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span><span class="sxs-lookup"><span data-stu-id="00b0f-119">You can set the maximum key-frame spacing by calling [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span></span> <span data-ttu-id="00b0f-120">I valori consigliati, in base alla velocità in bit del flusso, sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="00b0f-120">The recommended values, based on the bit rate of the stream, are listed in the following table.</span></span> <span data-ttu-id="00b0f-121">Questi valori rappresentano un equilibrio efficace tra la ricerca di prestazioni e qualità.</span><span class="sxs-lookup"><span data-stu-id="00b0f-121">These values provide a good balance of seeking performance and quality.</span></span> <span data-ttu-id="00b0f-122">L'SDK non impone alcun limite per il tempo tra i fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="00b0f-122">The SDK does not enforce any limit on the time between key frames.</span></span> <span data-ttu-id="00b0f-123">In generale, i tempi più lunghi di 30 secondi possono influire negativamente sui tempi di ricerca sia quando il contenuto viene trasmesso su una rete che quando viene riprodotto localmente.</span><span class="sxs-lookup"><span data-stu-id="00b0f-123">In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally.</span></span>



| <span data-ttu-id="00b0f-124">Velocità in bit</span><span class="sxs-lookup"><span data-stu-id="00b0f-124">Bit rate</span></span>             | <span data-ttu-id="00b0f-125">Spaziatura massima consigliata per i fotogrammi chiave</span><span class="sxs-lookup"><span data-stu-id="00b0f-125">Suggested maximum key-frame spacing</span></span> |
|----------------------|-------------------------------------|
| <span data-ttu-id="00b0f-126">da 22 kbps a 300 kbps</span><span class="sxs-lookup"><span data-stu-id="00b0f-126">22 Kbps to 300 Kbps</span></span>  | <span data-ttu-id="00b0f-127">8 secondi</span><span class="sxs-lookup"><span data-stu-id="00b0f-127">8 seconds</span></span>                           |
| <span data-ttu-id="00b0f-128">300 kbps a 600 Kbps</span><span class="sxs-lookup"><span data-stu-id="00b0f-128">300 Kbps to 600 Kbps</span></span> | <span data-ttu-id="00b0f-129">6 secondi</span><span class="sxs-lookup"><span data-stu-id="00b0f-129">6 seconds</span></span>                           |
| <span data-ttu-id="00b0f-130">da 600 kbps a 2 Mbps</span><span class="sxs-lookup"><span data-stu-id="00b0f-130">600 Kbps to 2 Mbps</span></span>   | <span data-ttu-id="00b0f-131">4 secondi</span><span class="sxs-lookup"><span data-stu-id="00b0f-131">4 seconds</span></span>                           |
| <span data-ttu-id="00b0f-132">2 Mbps e versioni successive</span><span class="sxs-lookup"><span data-stu-id="00b0f-132">2 Mbps and higher</span></span>    | <span data-ttu-id="00b0f-133">3 secondi</span><span class="sxs-lookup"><span data-stu-id="00b0f-133">3 seconds</span></span>                           |



 

<span data-ttu-id="00b0f-134">Per ulteriori informazioni su come ottenere prestazioni ottimali durante la ricerca di file video, vedere [ottenere le migliori prestazioni di ricerca dei video](getting-the-best-video-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="00b0f-134">For more information about getting the best performance when seeking video files, see [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00b0f-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00b0f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b0f-136">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="00b0f-136">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




