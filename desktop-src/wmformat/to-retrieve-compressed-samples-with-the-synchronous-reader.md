---
title: Per recuperare esempi compressi con il lettore sincrono
description: Per recuperare esempi compressi con il lettore sincrono
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Formato di sistemi avanzati (ASF), recupero di esempi compressi
- ASF (formato avanzato dei sistemi), recupero di esempi compressi
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- ASF (Advanced Systems Format), esempi compressi
- ASF (Advanced Systems Format), esempi compressi
- lettori sincroni, recupero di esempi compressi
- lettori sincroni, esempi compressi
- esempi compressi, recupero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117367"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a><span data-ttu-id="ee0f9-112">Per recuperare esempi compressi con il lettore sincrono</span><span class="sxs-lookup"><span data-stu-id="ee0f9-112">To Retrieve Compressed Samples with the Synchronous Reader</span></span>

<span data-ttu-id="ee0f9-113">Analogamente al Reader asincrono, il lettore sincrono può recuperare anche esempi compressi.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-113">Like the asynchronous reader, the synchronous reader can also retrieve compressed samples.</span></span> <span data-ttu-id="ee0f9-114">Gli esempi compressi devono essere usati per la copia di flussi da un file a un altro.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-114">Compressed samples should be used when copying streams from one file to another.</span></span>

<span data-ttu-id="ee0f9-115">Windows Media Format SDK non fornisce alcun metodo per la decodifica dei dati dopo che è stato Estratto da un file ASF.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-115">The Windows Media Format SDK does not provide any methods for decoding data after it has been extracted from an ASF file.</span></span> <span data-ttu-id="ee0f9-116">Se si ricevono esempi compressi e successivamente si desidera decomprimerli, sarà necessario fornire il proprio codice a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-116">If you receive compressed samples and later want to decompress them, you will have to provide your own code to do so.</span></span> <span data-ttu-id="ee0f9-117">Per aggirare questa limitazione, è possibile scrivere gli esempi compressi in un nuovo file ASF e quindi leggerli nuovamente in campioni normali non compressi.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-117">One way to get around this limitation is to write the compressed samples to a new ASF file and then re-read them into normal, uncompressed samples.</span></span>

<span data-ttu-id="ee0f9-118">Per ricevere esempi compressi con il lettore sincrono, chiamare [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) prima o durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-118">To receive compressed samples with the synchronous reader, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) before or during playback.</span></span> <span data-ttu-id="ee0f9-119">Passare true per *fCompressed*.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-119">Pass true for *fCompressed*.</span></span>

> [!Note]  
> <span data-ttu-id="ee0f9-120">I flussi di immagini non sono validi per il recapito di flussi compressi.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-120">Image streams are not valid for compressed stream delivery.</span></span> <span data-ttu-id="ee0f9-121">Se si copia un flusso di immagini da un file a un altro, non funzionerà nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-121">If you copy an image stream from one file to another, it will not work in the new file.</span></span> <span data-ttu-id="ee0f9-122">Per copiare un flusso di immagini da un file a un altro, recuperare gli esempi di flusso dell'immagine in base al numero di output e includerli nel nuovo file come se fosse incluso un nuovo flusso di immagine.</span><span class="sxs-lookup"><span data-stu-id="ee0f9-122">To copy an image stream from file to file, retrieve the image stream samples by output number and include them in the new file as if including a new image stream.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ee0f9-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee0f9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee0f9-124">**Lettura di file con il lettore sincrono**</span><span class="sxs-lookup"><span data-stu-id="ee0f9-124">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




