---
title: Selezione delle velocità in bit
description: Selezione delle velocità in bit
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- profili, selezione velocità in bit
- profili, velocità in bit
- codec, scelta della velocità in bit
- codec, velocità in bit
- profili, selezione velocità in bit
- codec, selezione velocità in bit
- velocità in bit, selezione
- velocità in bit, profili
- velocità in bit, codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328239"
---
# <a name="selecting-bit-rates"></a><span data-ttu-id="ceaf9-112">Selezione delle velocità in bit</span><span class="sxs-lookup"><span data-stu-id="ceaf9-112">Selecting Bit Rates</span></span>

<span data-ttu-id="ceaf9-113">Per i file che verranno trasmessi in rete, è necessario considerare attentamente le velocità in bit da usare.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-113">For files that will be streamed over a network, you must consider carefully what bit rates you should use.</span></span> <span data-ttu-id="ceaf9-114">Nella maggior parte dei casi è possibile aggiungere insieme la velocità in bit di tutti i flussi in un file per ottenere un'idea generale della larghezza di banda disponibile necessaria per lo streaming del file.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-114">Under most circumstances you can add the bit rates of all of the streams in a file together to get a general idea of the available bandwidth required to stream the file.</span></span> <span data-ttu-id="ceaf9-115">Tuttavia, per ogni flusso è necessaria anche una certa quantità di overhead.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-115">However, a certain amount of overhead is also required for each stream.</span></span> <span data-ttu-id="ceaf9-116">Questo overhead è riepilogato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-116">This overhead is summarized in the following table.</span></span>



| <span data-ttu-id="ceaf9-117">Intervallo di velocità in bit (Kbps)</span><span class="sxs-lookup"><span data-stu-id="ceaf9-117">Bit-rate range (Kbps)</span></span> | <span data-ttu-id="ceaf9-118">Larghezza di banda aggiuntiva necessaria per l'overhead (Kbps)</span><span class="sxs-lookup"><span data-stu-id="ceaf9-118">Additional bandwidth required for overhead (Kbps)</span></span> |
|-----------------------|---------------------------------------------------|
| <span data-ttu-id="ceaf9-119">da 10 a 16</span><span class="sxs-lookup"><span data-stu-id="ceaf9-119">10 – 16</span></span>               | <span data-ttu-id="ceaf9-120">3</span><span class="sxs-lookup"><span data-stu-id="ceaf9-120">3</span></span>                                                 |
| <span data-ttu-id="ceaf9-121">17-30</span><span class="sxs-lookup"><span data-stu-id="ceaf9-121">17 – 30</span></span>               | <span data-ttu-id="ceaf9-122">4</span><span class="sxs-lookup"><span data-stu-id="ceaf9-122">4</span></span>                                                 |
| <span data-ttu-id="ceaf9-123">31 – 45</span><span class="sxs-lookup"><span data-stu-id="ceaf9-123">31 – 45</span></span>               | <span data-ttu-id="ceaf9-124">5</span><span class="sxs-lookup"><span data-stu-id="ceaf9-124">5</span></span>                                                 |
| <span data-ttu-id="ceaf9-125">46 – 70</span><span class="sxs-lookup"><span data-stu-id="ceaf9-125">46 – 70</span></span>               | <span data-ttu-id="ceaf9-126">6</span><span class="sxs-lookup"><span data-stu-id="ceaf9-126">6</span></span>                                                 |
| <span data-ttu-id="ceaf9-127">71 – 225</span><span class="sxs-lookup"><span data-stu-id="ceaf9-127">71 – 225</span></span>              | <span data-ttu-id="ceaf9-128">7</span><span class="sxs-lookup"><span data-stu-id="ceaf9-128">7</span></span>                                                 |
| <span data-ttu-id="ceaf9-129">>225</span><span class="sxs-lookup"><span data-stu-id="ceaf9-129">>225</span></span>               | <span data-ttu-id="ceaf9-130">9</span><span class="sxs-lookup"><span data-stu-id="ceaf9-130">9</span></span>                                                 |



 

<span data-ttu-id="ceaf9-131">Il sovraccarico normale necessario per un flusso non prende in considerazione le estensioni di unità dati.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-131">The normal overhead required for a stream does not take data unit extensions into account.</span></span> <span data-ttu-id="ceaf9-132">Ogni estensione di unità dati aggiunge alla dimensione dell'esempio a cui è collegato.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-132">Every data unit extension adds to the size of the sample to which it is attached.</span></span> <span data-ttu-id="ceaf9-133">A seconda del tipo di estensione dell'unità dati, questo può aumentare significativamente la velocità in bit per il flusso.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-133">Depending upon the type of data unit extension, this can greatly increase the bit rate for the stream.</span></span>

<span data-ttu-id="ceaf9-134">È inoltre necessario considerare che la larghezza di banda massima teorica disponibile su una connessione di rete non è una velocità in bit di destinazione pratica.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-134">You must also consider that the theoretical maximum bandwidth available over a network connection is not a practical target bit rate.</span></span> <span data-ttu-id="ceaf9-135">La larghezza di banda media disponibile per una determinata connessione non è sufficiente per la capacità della larghezza di banda della connessione, a causa del traffico di rete e di molti altri fattori.</span><span class="sxs-lookup"><span data-stu-id="ceaf9-135">The average available bandwidth for any given connection falls well short of the bandwidth capacity of the connection, because of network traffic and many other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceaf9-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ceaf9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceaf9-137">**Progettazione di profili**</span><span class="sxs-lookup"><span data-stu-id="ceaf9-137">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 




