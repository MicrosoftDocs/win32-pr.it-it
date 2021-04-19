---
title: Scelta di un metodo di codifica
description: Scelta di un metodo di codifica
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- profili, scelta dei metodi di codifica
- profili, metodi di codifica
- codec, scelta di metodi di codifica
- codec, metodi di codifica
- profili, selezione dei metodi di codifica
- codec, selezione di metodi di codifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298147"
---
# <a name="choosing-an-encoding-method"></a><span data-ttu-id="66b3c-109">Scelta di un metodo di codifica</span><span class="sxs-lookup"><span data-stu-id="66b3c-109">Choosing an Encoding Method</span></span>

<span data-ttu-id="66b3c-110">Alcuni codec, come il codec Windows Media Video 9, supportano più metodi di codifica.</span><span class="sxs-lookup"><span data-stu-id="66b3c-110">Some codecs, like the Windows Media Video 9 codec, support multiple encoding methods.</span></span> <span data-ttu-id="66b3c-111">Il metodo di codifica scelto per un flusso dipende dal modo in cui deve essere recapitato il flusso.</span><span class="sxs-lookup"><span data-stu-id="66b3c-111">The encoding method that you choose for a stream will depend upon how the stream is to be delivered.</span></span> <span data-ttu-id="66b3c-112">Nella tabella seguente viene descritto quando utilizzare i vari metodi di codifica.</span><span class="sxs-lookup"><span data-stu-id="66b3c-112">The following table describes when to use the various encoding methods.</span></span>



| <span data-ttu-id="66b3c-113">Metodo di codifica</span><span class="sxs-lookup"><span data-stu-id="66b3c-113">Encoding method</span></span>                | <span data-ttu-id="66b3c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66b3c-114">Description</span></span>                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66b3c-115">Velocità in bit costante (CBR) a 1 pass</span><span class="sxs-lookup"><span data-stu-id="66b3c-115">1-pass Constant Bit Rate (CBR)</span></span> | <span data-ttu-id="66b3c-116">L'unica opzione per lo streaming live.</span><span class="sxs-lookup"><span data-stu-id="66b3c-116">The only option for live streaming.</span></span> <span data-ttu-id="66b3c-117">Codifica a una velocità in bit prevedibile e offre la qualità più bassa di tutti i metodi di codifica.</span><span class="sxs-lookup"><span data-stu-id="66b3c-117">Encodes to a predictable bit rate and delivers the lowest quality of all encoding methods.</span></span>                                                                    |
| <span data-ttu-id="66b3c-118">2-pass CBR</span><span class="sxs-lookup"><span data-stu-id="66b3c-118">2-pass CBR</span></span>                     | <span data-ttu-id="66b3c-119">Utilizzare per i file che verranno trasmessi in rete a un lettore client, ma che non vengono trasmessi da un'origine live.</span><span class="sxs-lookup"><span data-stu-id="66b3c-119">Use for files that will be streamed over a network to a client reader, but that are not broadcast from a live source.</span></span> <span data-ttu-id="66b3c-120">Codifica a una velocità in bit prevedibile, ma con una qualità migliore rispetto a 1-pass CBR.</span><span class="sxs-lookup"><span data-stu-id="66b3c-120">Encodes to a predictable bit rate, but with better quality than 1-pass CBR.</span></span> |
| <span data-ttu-id="66b3c-121">Velocità in bit della variabile 1-pass (VBR)</span><span class="sxs-lookup"><span data-stu-id="66b3c-121">1-pass Variable Bit Rate (VBR)</span></span> | <span data-ttu-id="66b3c-122">Usare quando è necessario specificare la qualità dell'output codificato.</span><span class="sxs-lookup"><span data-stu-id="66b3c-122">Use when you need to specify the quality of the encoded output.</span></span> <span data-ttu-id="66b3c-123">Offre la qualità più uniforme di tutti i metodi di codifica.</span><span class="sxs-lookup"><span data-stu-id="66b3c-123">Delivers the most consistent quality of all encoding methods.</span></span> <span data-ttu-id="66b3c-124">Usare solo per i file locali o per il download.</span><span class="sxs-lookup"><span data-stu-id="66b3c-124">Use only for local files or for downloading.</span></span>                        |
| <span data-ttu-id="66b3c-125">2-pass VBR-non vincolato</span><span class="sxs-lookup"><span data-stu-id="66b3c-125">2-pass VBR – unconstrained</span></span>     | <span data-ttu-id="66b3c-126">Usare quando è necessario specificare una larghezza di banda, ma le fluttuazioni intorno alla larghezza di banda specificata sono accettabili.</span><span class="sxs-lookup"><span data-stu-id="66b3c-126">Use when you need to specify a bandwidth, but fluctuations around the specified bandwidth are acceptable.</span></span> <span data-ttu-id="66b3c-127">Per i file locali o solo per il download.</span><span class="sxs-lookup"><span data-stu-id="66b3c-127">For local files or downloading only.</span></span>                                                    |
| <span data-ttu-id="66b3c-128">2-pass VBR-vincolato</span><span class="sxs-lookup"><span data-stu-id="66b3c-128">2-pass VBR – constrained</span></span>       | <span data-ttu-id="66b3c-129">Utilizzare le stesse circostanze come non vincolate, ma quando è necessario specificare una frequenza di bit momentanea massima.</span><span class="sxs-lookup"><span data-stu-id="66b3c-129">Use under the same circumstances as unconstrained, but when you need to specify a maximum momentary bit rate.</span></span> <span data-ttu-id="66b3c-130">Per i file locali o solo per il download.</span><span class="sxs-lookup"><span data-stu-id="66b3c-130">For local files or downloading only.</span></span>                                                |



 

<span data-ttu-id="66b3c-131">Nella tabella seguente sono elencati i metodi di codifica supportati dai codec forniti con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="66b3c-131">The following table lists the encoding methods that are supported by the codecs that ship with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="66b3c-132">Codec</span><span class="sxs-lookup"><span data-stu-id="66b3c-132">Codec</span></span>                                  | <span data-ttu-id="66b3c-133">CBR</span><span class="sxs-lookup"><span data-stu-id="66b3c-133">CBR</span></span> | <span data-ttu-id="66b3c-134">2-pass CBR</span><span class="sxs-lookup"><span data-stu-id="66b3c-134">2-pass CBR</span></span> | <span data-ttu-id="66b3c-135">VBR</span><span class="sxs-lookup"><span data-stu-id="66b3c-135">VBR</span></span> | <span data-ttu-id="66b3c-136">2-pass VBR</span><span class="sxs-lookup"><span data-stu-id="66b3c-136">2-pass VBR</span></span> |
|----------------------------------------|-----|------------|-----|------------|
| <span data-ttu-id="66b3c-137">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="66b3c-137">Windows Media Video 9</span></span>                  | <span data-ttu-id="66b3c-138">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-138">X</span></span>   | <span data-ttu-id="66b3c-139">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-139">X</span></span>          | <span data-ttu-id="66b3c-140">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-140">X</span></span>   | <span data-ttu-id="66b3c-141">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-141">X</span></span>          |
| <span data-ttu-id="66b3c-142">Windows Media Audio 9 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="66b3c-142">Windows Media Audio 9 and later</span></span>        | <span data-ttu-id="66b3c-143">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-143">X</span></span>   | <span data-ttu-id="66b3c-144">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-144">X</span></span>          | <span data-ttu-id="66b3c-145">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-145">X</span></span>   | <span data-ttu-id="66b3c-146">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-146">X</span></span>          |
| <span data-ttu-id="66b3c-147">Schermata Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="66b3c-147">Windows Media Video 9 Screen</span></span>           | <span data-ttu-id="66b3c-148">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-148">X</span></span>   |            | <span data-ttu-id="66b3c-149">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-149">X</span></span>   |            |
| <span data-ttu-id="66b3c-150">Windows Media Audio 9 Voice</span><span class="sxs-lookup"><span data-stu-id="66b3c-150">Windows Media Audio 9 Voice</span></span>            | <span data-ttu-id="66b3c-151">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-151">X</span></span>   |            |     |            |
| <span data-ttu-id="66b3c-152">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="66b3c-152">Windows Media Audio Professional</span></span>       | <span data-ttu-id="66b3c-153">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-153">X</span></span>   | <span data-ttu-id="66b3c-154">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-154">X</span></span>          | <span data-ttu-id="66b3c-155">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-155">X</span></span>   | <span data-ttu-id="66b3c-156">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-156">X</span></span>          |
| <span data-ttu-id="66b3c-157">Windows Media Audio senza perdita di perdite</span><span class="sxs-lookup"><span data-stu-id="66b3c-157">Windows Media Audio Lossless</span></span>           |     |            | <span data-ttu-id="66b3c-158">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-158">X</span></span>   |            |
| <span data-ttu-id="66b3c-159">Windows Media Video 9 Image e versioni successive</span><span class="sxs-lookup"><span data-stu-id="66b3c-159">Windows Media Video 9 Image and later</span></span>  | <span data-ttu-id="66b3c-160">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-160">X</span></span>   |            | <span data-ttu-id="66b3c-161">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-161">X</span></span>   |            |
| <span data-ttu-id="66b3c-162">Profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="66b3c-162">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="66b3c-163">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-163">X</span></span>   | <span data-ttu-id="66b3c-164">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-164">X</span></span>          | <span data-ttu-id="66b3c-165">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-165">X</span></span>   | <span data-ttu-id="66b3c-166">X</span><span class="sxs-lookup"><span data-stu-id="66b3c-166">X</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="66b3c-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66b3c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66b3c-168">**Progettazione di profili**</span><span class="sxs-lookup"><span data-stu-id="66b3c-168">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="66b3c-169">**Codifica della velocità in bit costante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="66b3c-169">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="66b3c-170">**Codifica a due passaggi**</span><span class="sxs-lookup"><span data-stu-id="66b3c-170">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="66b3c-171">**Codifica della velocità in bit variabile (VBR)**</span><span class="sxs-lookup"><span data-stu-id="66b3c-171">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




