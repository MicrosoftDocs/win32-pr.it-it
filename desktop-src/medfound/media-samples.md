---
description: Informazioni sugli esempi multimediali in Microsoft Media Foundation. Un campione multimediale è un oggetto che contiene un elenco ordinato di zero o più buffer.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Esempi di supporti (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989156"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="1871d-104">Esempi di supporti (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="1871d-104">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="1871d-105">Un campione multimediale è un oggetto che contiene un elenco ordinato di zero o più buffer.</span><span class="sxs-lookup"><span data-stu-id="1871d-105">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="1871d-106">Gli esempi multimediali espongono [**l'interfaccia IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)</span><span class="sxs-lookup"><span data-stu-id="1871d-106">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="1871d-107">La quantità di dati contenuti in un campione dipende dal componente che crea il campione e dal tipo di dati nei buffer.</span><span class="sxs-lookup"><span data-stu-id="1871d-107">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="1871d-108">Per i video non compressi, un esempio contiene in genere un singolo fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="1871d-108">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="1871d-109">Per l'audio non compresso, la quantità di dati può variare, ma in genere un frame audio non si estende su due campioni.</span><span class="sxs-lookup"><span data-stu-id="1871d-109">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="1871d-110">Per i dati compressi, queste linee guida potrebbero non essere applicabili.</span><span class="sxs-lookup"><span data-stu-id="1871d-110">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="1871d-111">Un singolo campione può contenere più buffer per motivi di efficienza.</span><span class="sxs-lookup"><span data-stu-id="1871d-111">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="1871d-112">In un file ASF, ad esempio, un fotogramma video viene spesso distribuito tra più pacchetti ASF.</span><span class="sxs-lookup"><span data-stu-id="1871d-112">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="1871d-113">L'origine multimediale potrebbe leggere i pacchetti in più buffer.</span><span class="sxs-lookup"><span data-stu-id="1871d-113">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="1871d-114">Invece di copiare ogni frammento in un unico buffer, l'origine inserisce semplicemente tutti i buffer in un unico campione.</span><span class="sxs-lookup"><span data-stu-id="1871d-114">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="1871d-115">I componenti downstream possono quindi decidere se copiare i buffer più piccoli in un unico buffer contiguo.</span><span class="sxs-lookup"><span data-stu-id="1871d-115">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="1871d-116">In genere, se si scrive un componente della pipeline, è consigliabile presupporre che qualsiasi esempio possa contenere più di un buffer.</span><span class="sxs-lookup"><span data-stu-id="1871d-116">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="1871d-117">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="1871d-117">This section contains the following topics.</span></span>



| <span data-ttu-id="1871d-118">Argomento</span><span class="sxs-lookup"><span data-stu-id="1871d-118">Topic</span></span>                                                        | <span data-ttu-id="1871d-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1871d-119">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1871d-120">Uso di esempi multimediali</span><span class="sxs-lookup"><span data-stu-id="1871d-120">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="1871d-121">Descrive il comportamento generale degli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="1871d-121">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="1871d-122">Esempi video</span><span class="sxs-lookup"><span data-stu-id="1871d-122">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="1871d-123">Descrive un'implementazione specializzata di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) progettata per contenere fotogrammi video non compressi.</span><span class="sxs-lookup"><span data-stu-id="1871d-123">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1871d-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1871d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1871d-125">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="1871d-125">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="1871d-126">Media Foundation primitive</span><span class="sxs-lookup"><span data-stu-id="1871d-126">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



