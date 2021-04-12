---
title: Codifica della velocità in bit costante (CBR)
description: Codifica della velocità in bit costante (CBR)
ms.assetid: f87277a5-55f1-46c7-a6a4-5824f3904d60
keywords:
- Windows Media Format SDK, codifica CBR
- Windows Media Format SDK, velocità in bit costante (CBR)
- codec, codifica CBR
- codec, velocità in bit costante (CBR)
- velocità in bit costante (CBR)
- CBR (velocità in bit costante)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3ded3709e2e7a3e5b567b91a127ad3486a0b66
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396682"
---
# <a name="constant-bit-rate-cbr-encoding"></a><span data-ttu-id="82c70-109">Codifica della velocità in bit costante (CBR)</span><span class="sxs-lookup"><span data-stu-id="82c70-109">Constant Bit Rate (CBR) Encoding</span></span>

<span data-ttu-id="82c70-110">La codifica della velocità in bit costante (CBR) è il metodo predefinito di codifica con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="82c70-110">Constant bit rate (CBR) encoding is the default method of encoding with the Windows Media Format SDK.</span></span> <span data-ttu-id="82c70-111">Quando si usa la codifica CBR, si specifica la velocità in bit di destinazione per un flusso e il codec usa qualsiasi quantità di compressione necessaria per ottenerlo.</span><span class="sxs-lookup"><span data-stu-id="82c70-111">When using CBR encoding, you specify the target bit rate for a stream, and the codec uses whatever amount of compression is necessary to achieve it.</span></span>

<span data-ttu-id="82c70-112">Con la codifica CBR la velocità in bit e le dimensioni del flusso codificato sono note prima della codifica.</span><span class="sxs-lookup"><span data-stu-id="82c70-112">With CBR encoding the bit rate and size of the encoded stream are known prior to encoding.</span></span> <span data-ttu-id="82c70-113">Se, ad esempio, si codifica un brano di tre minuti a 32.000 bit al secondo, si è certi che le dimensioni del file saranno pari a circa 704 kilobyte (32.000 bps x 180 secondi/8 bit per byte/1.024).</span><span class="sxs-lookup"><span data-stu-id="82c70-113">For example, if you are encoding a three minute song at 32,000 bits per second, you know that the file size will be about 704 kilobytes (32,000 bps x 180 seconds / 8 bits per byte / 1,024).</span></span> <span data-ttu-id="82c70-114">Si sa anche che la larghezza di banda necessaria per trasmettere il contenuto codificato è di circa 32.000 bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="82c70-114">You also know that the bandwidth required to stream the encoded content is about 32,000 bits per second.</span></span>

<span data-ttu-id="82c70-115">La codifica della velocità in bit variabile vincolata (descritta nella sezione seguente) consente anche di stabilire la velocità in bit prima della codifica, ma poiché la frequenza è variabile, il file risultante non può essere trasmesso in modo efficiente come un file codificato in modalità CBR.</span><span class="sxs-lookup"><span data-stu-id="82c70-115">Constrained variable bit rate encoding (described in the following section) also enables you to know the bit rate prior to encoding, but since the rate is variable, the resulting file cannot be streamed as efficiently as a file encoded in CBR mode.</span></span> <span data-ttu-id="82c70-116">Con CBR, la velocità in bit nel tempo rimane sempre vicina alla velocità in bit media o di destinazione e la quantità di variazione può essere specificata.</span><span class="sxs-lookup"><span data-stu-id="82c70-116">With CBR, the bit rate over time always remains close to the average or target bit rate, and the amount of variation can be specified.</span></span>

<span data-ttu-id="82c70-117">Lo svantaggio della codifica CBR è che la qualità del contenuto codificato non sarà costante.</span><span class="sxs-lookup"><span data-stu-id="82c70-117">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="82c70-118">Poiché alcuni contenuti sono più difficili da comprimere, le parti di un flusso CBR saranno di qualità inferiore rispetto ad altri.</span><span class="sxs-lookup"><span data-stu-id="82c70-118">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="82c70-119">Un film tipico, ad esempio, presenta alcune scene piuttosto statiche e alcune scene che sono piene di azioni.</span><span class="sxs-lookup"><span data-stu-id="82c70-119">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="82c70-120">Se si codifica un film usando CBR, le scene statiche e pertanto semplici da codificare in modo efficiente saranno di qualità superiore rispetto a quelle delle azioni, che risultano molto più difficili da codificare in modo efficiente.</span><span class="sxs-lookup"><span data-stu-id="82c70-120">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which are much more difficult to encode efficiently.</span></span>

<span data-ttu-id="82c70-121">La codifica CBR può anche causare una qualità incoerente da un file a un altro.</span><span class="sxs-lookup"><span data-stu-id="82c70-121">CBR encoding can also result in inconsistent quality from one file to another.</span></span> <span data-ttu-id="82c70-122">Se si usa CBR per codificare diversi brani di genere diversi alla stessa velocità in bit, è possibile notare una certa differenza di qualità tra di essi.</span><span class="sxs-lookup"><span data-stu-id="82c70-122">If you use CBR to encode several songs of different genres at the same bit rate, you may notice some difference in quality between them.</span></span>

<span data-ttu-id="82c70-123">In generale, le variazioni nella qualità di un file CBR sono più pronunciate a velocità in bit inferiori.</span><span class="sxs-lookup"><span data-stu-id="82c70-123">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="82c70-124">A una velocità in bit superiore, la qualità di un file con codifica CBR sarà comunque diversa, ma i problemi di qualità saranno meno evidenti per l'utente.</span><span class="sxs-lookup"><span data-stu-id="82c70-124">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="82c70-125">Quando si usa la codifica CBR, è consigliabile impostare la larghezza di banda massima come consentito dallo scenario di recapito.</span><span class="sxs-lookup"><span data-stu-id="82c70-125">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82c70-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82c70-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82c70-127">**Scelta di un metodo di codifica**</span><span class="sxs-lookup"><span data-stu-id="82c70-127">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="82c70-128">**Funzionalità di codec**</span><span class="sxs-lookup"><span data-stu-id="82c70-128">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="82c70-129">**Codifica della velocità in bit variabile (VBR)**</span><span class="sxs-lookup"><span data-stu-id="82c70-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




