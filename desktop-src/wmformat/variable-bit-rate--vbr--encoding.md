---
title: Codifica della velocità in bit variabile (VBR)
description: Codifica della velocità in bit variabile (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media Format SDK, codifica VBR
- Windows Media Format SDK, velocità in bit variabile (VBR)
- Windows Media Format SDK, codifica VBR basata sulla qualità
- Windows Media Format SDK, codifica VBR non vincolata
- Windows Media Format SDK, codifica VBR vincolata
- codec, codifica VBR
- codec, velocità in bit variabile (VBR)
- codec, codifica VBR basata sulla qualità
- codec, codifica VBR non vincolata
- codec, codifica VBR vincolata
- velocità in bit variabile (VBR), informazioni
- VBR (velocità in bit variabile), informazioni
- codifica VBR basata sulla qualità, informazioni
- codifica VBR non vincolata, informazioni
- codifica VBR vincolata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298917"
---
# <a name="variable-bit-rate-vbr-encoding"></a><span data-ttu-id="32839-118">Codifica della velocità in bit variabile (VBR)</span><span class="sxs-lookup"><span data-stu-id="32839-118">Variable Bit Rate (VBR) Encoding</span></span>

<span data-ttu-id="32839-119">La codifica con velocità in bit variabile (VBR) è un'alternativa a constant bit rate Encoding (CBR) ed è supportata da alcuni codec.</span><span class="sxs-lookup"><span data-stu-id="32839-119">Variable bit rate (VBR) encoding is an alternative to constant bit rate encoding (CBR) and is supported by some codecs.</span></span> <span data-ttu-id="32839-120">Quando la codifica CBR si impegna a mantenere la velocità in bit del supporto codificato, VBR tenta di ottenere la migliore qualità possibile del supporto codificato.</span><span class="sxs-lookup"><span data-stu-id="32839-120">Where CBR encoding strives to maintain the bit rate of the encoded media, VBR strives to achieve the best possible quality of the encoded media.</span></span>

<span data-ttu-id="32839-121">La qualità del contenuto codificato dipende dalla quantità di dati persi durante la compressione e decompressione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="32839-121">The quality of encoded content is determined by the amount of data that is lost when the content is compressed and decompressed.</span></span> <span data-ttu-id="32839-122">La perdita di dati durante il processo di compressione è influenzata da molti fattori, ma in genere a una maggiore la complessità dei dati originali e a un maggiore rapporto di compressione corrisponde una maggiore perdita di dettagli nel processo di compressione.</span><span class="sxs-lookup"><span data-stu-id="32839-122">Many factors affect the loss of data in the compression process, but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="32839-123">Sono disponibili tre tipi di codifica VBR: basata sulla qualità, non vincolata e vincolata.</span><span class="sxs-lookup"><span data-stu-id="32839-123">There are three types of VBR encoding: quality-based, unconstrained, and constrained.</span></span>

## <a name="quality-based-vbr-encoding"></a><span data-ttu-id="32839-124">Codifica VBR basata sulla qualità</span><span class="sxs-lookup"><span data-stu-id="32839-124">Quality-based VBR Encoding</span></span>

<span data-ttu-id="32839-125">Il primo tipo di codifica VBR è basato sulla qualità, che usa un passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="32839-125">The first type of VBR encoding is quality-based, which uses one encoding pass.</span></span> <span data-ttu-id="32839-126">La codifica VBR basata sulla qualità consente di specificare un livello di qualità per un flusso multimediale digitale anziché una velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="32839-126">Quality-based VBR encoding enables you to specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="32839-127">Il codec codifica quindi il contenuto in modo che tutti gli esempi siano di qualità paragonabile.</span><span class="sxs-lookup"><span data-stu-id="32839-127">The codec will then encode the content so that all samples are of comparable quality.</span></span>

<span data-ttu-id="32839-128">Il vantaggio principale della codifica VBR basata sulla qualità è che la qualità è coerente all'interno di un file e da un file a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="32839-128">The main advantage of quality-based VBR encoding is that quality is consistent within a file and from one file to the next.</span></span> <span data-ttu-id="32839-129">Ad esempio, è possibile scrivere un programma per copiare canzoni da CD a file ASF in un computer.</span><span class="sxs-lookup"><span data-stu-id="32839-129">For example, you can write a program to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="32839-130">In questo caso, la qualità coerente è probabilmente più importante per l'esperienza dell'utente finale rispetto alla dimensione del file coerente.</span><span class="sxs-lookup"><span data-stu-id="32839-130">In this case, consistent quality is probably more important to the end-user experience than consistent file size.</span></span> <span data-ttu-id="32839-131">L'uso della codifica VBR basata sulla qualità garantisce che tutti i brani copiati abbiano la stessa qualità.</span><span class="sxs-lookup"><span data-stu-id="32839-131">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span>

<span data-ttu-id="32839-132">Lo svantaggio della codifica VBR basata sulla qualità è che non esiste alcun modo per individuare i requisiti di larghezza di banda o di larghezza di banda del supporto codificato prima della codifica.</span><span class="sxs-lookup"><span data-stu-id="32839-132">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before encoding.</span></span> <span data-ttu-id="32839-133">Questo può rendere i file con codifica VBR basati sulla qualità inappropriati per le situazioni in cui la memoria o la larghezza di banda sono limitate, ad esempio lettori multimediali portatili o connessioni Internet a larghezza di banda ridotta.</span><span class="sxs-lookup"><span data-stu-id="32839-133">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as portable media players, or low-bandwidth Internet connections.</span></span>

<span data-ttu-id="32839-134">In generale, la codifica VBR basata sulla qualità è particolarmente adatta per la riproduzione locale o connessioni di rete a larghezza di banda elevata.</span><span class="sxs-lookup"><span data-stu-id="32839-134">In general, quality-based VBR encoding is well suited for local playback or high bandwidth network connections.</span></span> <span data-ttu-id="32839-135">In questi casi, la qualità coerente offrirà un'esperienza utente migliore.</span><span class="sxs-lookup"><span data-stu-id="32839-135">In those cases, the consistent quality will provide a better user experience.</span></span>

## <a name="unconstrained-vbr-encoding"></a><span data-ttu-id="32839-136">Codifica VBR non vincolata</span><span class="sxs-lookup"><span data-stu-id="32839-136">Unconstrained VBR Encoding</span></span>

<span data-ttu-id="32839-137">La codifica VBR non vincolata usa due sessioni di codifica.</span><span class="sxs-lookup"><span data-stu-id="32839-137">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="32839-138">Quando si usa la codifica VBR non vincolata, è possibile specificare una velocità in bit per il flusso, come si farebbe con la codifica CBR.</span><span class="sxs-lookup"><span data-stu-id="32839-138">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with CBR encoding.</span></span> <span data-ttu-id="32839-139">Tuttavia, il codec usa questo valore solo come velocità in bit media per il flusso e codifica in modo che la qualità sia il più alto possibile mantenendo la media.</span><span class="sxs-lookup"><span data-stu-id="32839-139">However, the codec uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="32839-140">La velocità in bit effettiva in qualsiasi punto del flusso codificato può variare considerevolmente dal valore medio.</span><span class="sxs-lookup"><span data-stu-id="32839-140">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span>

<span data-ttu-id="32839-141">Non viene impostata una finestra del buffer per la codifica VBR non vincolata come per un flusso con codifica CBR.</span><span class="sxs-lookup"><span data-stu-id="32839-141">You do not set a buffer window for unconstrained VBR encoding as you would for a CBR-encoded stream.</span></span> <span data-ttu-id="32839-142">Al contrario, il codec calcola le dimensioni della finestra del buffer necessaria in base ai requisiti degli esempi codificati.</span><span class="sxs-lookup"><span data-stu-id="32839-142">Instead, the codec computes the size of the required buffer window based on the requirements of the encoded samples.</span></span>

<span data-ttu-id="32839-143">Il vantaggio della codifica VBR non vincolata consiste nel fatto che il flusso compresso ha la qualità massima possibile rimanendo all'interno di una larghezza di banda media prevedibile.</span><span class="sxs-lookup"><span data-stu-id="32839-143">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span>

## <a name="constrained-vbr-encoding"></a><span data-ttu-id="32839-144">Codifica VBR vincolata</span><span class="sxs-lookup"><span data-stu-id="32839-144">Constrained VBR Encoding</span></span>

<span data-ttu-id="32839-145">La codifica VBR vincolata è identica alla codifica VBR non vincolata, con la differenza che si specifica una velocità in bit massima e una finestra massima del buffer nel profilo.</span><span class="sxs-lookup"><span data-stu-id="32839-145">Constrained VBR encoding is identical to unconstrained VBR encoding, except that you specify a maximum bit rate and a maximum buffer window in the profile.</span></span> <span data-ttu-id="32839-146">Il codec usa quindi i valori massimi per determinare come comprimere i dati.</span><span class="sxs-lookup"><span data-stu-id="32839-146">The codec then uses the maximum values to determine how to compress the data.</span></span> <span data-ttu-id="32839-147">Se si impostano i valori massimi a sufficienza, la codifica VBR vincolata produrrà lo stesso flusso codificato come codifica VBR non vincolata.</span><span class="sxs-lookup"><span data-stu-id="32839-147">If you set the maximum values high enough, constrained VBR encoding will produce the same encoded stream as unconstrained VBR encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32839-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32839-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32839-149">**Scelta di un metodo di codifica**</span><span class="sxs-lookup"><span data-stu-id="32839-149">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="32839-150">**Funzionalità di codec**</span><span class="sxs-lookup"><span data-stu-id="32839-150">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="32839-151">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="32839-151">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="32839-152">**Configurazione di flussi VBR**</span><span class="sxs-lookup"><span data-stu-id="32839-152">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> <dt>

[<span data-ttu-id="32839-153">**Codifica della velocità in bit costante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="32839-153">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="32839-154">**Codifica a due passaggi**</span><span class="sxs-lookup"><span data-stu-id="32839-154">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="32839-155">**Uso della codifica Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="32839-155">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




