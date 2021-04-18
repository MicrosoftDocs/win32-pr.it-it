---
title: Per gestire la latenza del writer
description: Per gestire la latenza del writer
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Formato di sistemi avanzati (ASF), gestione della latenza del writer
- ASF (formato di sistemi avanzati), gestione della latenza del writer
- ASF (Advanced Systems Format), latenza writer
- ASF (formato avanzato dei sistemi), latenza writer
- latenza writer
- latenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299398"
---
# <a name="to-manage-writer-latency"></a><span data-ttu-id="5aa97-109">Per gestire la latenza del writer</span><span class="sxs-lookup"><span data-stu-id="5aa97-109">To Manage Writer Latency</span></span>

<span data-ttu-id="5aa97-110">Per elaborare gli esempi, il writer richiede tempo.</span><span class="sxs-lookup"><span data-stu-id="5aa97-110">It takes time for the writer to process samples.</span></span> <span data-ttu-id="5aa97-111">La quantità di tempo che intercorre tra il passaggio di un campione di input e la scrittura di un campione di output è detta latenza del writer.</span><span class="sxs-lookup"><span data-stu-id="5aa97-111">The amount of time between passing an input sample and the writing of an output sample is called the latency of the writer.</span></span> <span data-ttu-id="5aa97-112">Una serie di fattori contribuisce alla latenza del writer ed è possibile ridurla in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="5aa97-112">A number of factors contribute to writer latency, and you can reduce it in several ways.</span></span>

<span data-ttu-id="5aa97-113">Il fattore più ovvio implicato nella latenza del writer è il tempo necessario per comprimere un campione.</span><span class="sxs-lookup"><span data-stu-id="5aa97-113">The most obvious factor involved in writer latency is the time it takes to compress a sample.</span></span> <span data-ttu-id="5aa97-114">Nella maggior parte dei casi, l'utente non avrà alcun controllo sufficiente.</span><span class="sxs-lookup"><span data-stu-id="5aa97-114">Under most circumstances, you will have little or no control over this.</span></span> <span data-ttu-id="5aa97-115">Se la larghezza di banda non costituisce un problema, è possibile ridurre la latenza utilizzando una minore compressione.</span><span class="sxs-lookup"><span data-stu-id="5aa97-115">If bandwidth is not a big concern, you can reduce latency by using less compression.</span></span> <span data-ttu-id="5aa97-116">Naturalmente, è possibile ottenere la latenza minima passando esempi già compressi.</span><span class="sxs-lookup"><span data-stu-id="5aa97-116">Of course, you can achieve the least latency by passing samples that are already compressed.</span></span>

<span data-ttu-id="5aa97-117">Il fattore successivo, e uno su cui si ha in genere il controllo, è l'ordine in cui gli esempi vengono passati al lettore.</span><span class="sxs-lookup"><span data-stu-id="5aa97-117">The next factor, and one over which you usually do have control, is the order in which samples are passed to the reader.</span></span> <span data-ttu-id="5aa97-118">È possibile ottenere una latenza migliore passando esempi in ordine di tempo di presentazione e assicurandosi che gli esempi di input siano sincronizzati correttamente tra tutti i flussi di input.</span><span class="sxs-lookup"><span data-stu-id="5aa97-118">You can achieve better latency by passing samples in order of presentation time, and by ensuring that the input samples are well synchronized between all input streams.</span></span> <span data-ttu-id="5aa97-119">Maggiore è la discrepanza nei tempi di presentazione tra gli esempi per flussi diversi, maggiore sarà il risultato della latenza.</span><span class="sxs-lookup"><span data-stu-id="5aa97-119">The greater the discrepancy in presentation times between the samples for different streams, the more latency will result.</span></span> <span data-ttu-id="5aa97-120">È possibile impostare un massimo per la discrepanza tra gli esempi di input chiamando [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="5aa97-120">You can set a maximum for the discrepancy between input samples by calling [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa97-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5aa97-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa97-122">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="5aa97-122">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




