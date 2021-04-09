---
description: Esempi di supporti
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Esempi di supporti (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968921"
---
# <a name="media-samples-microsoft-media-foundation"></a><span data-ttu-id="2c60f-103">Esempi di supporti (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="2c60f-103">Media Samples (Microsoft Media Foundation)</span></span>

<span data-ttu-id="2c60f-104">Un esempio di supporto è un oggetto che contiene un elenco ordinato di zero o più buffer.</span><span class="sxs-lookup"><span data-stu-id="2c60f-104">A media sample is an object that contains an ordered list of zero or more buffers.</span></span> <span data-ttu-id="2c60f-105">Gli esempi di supporti espongono l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="2c60f-105">Media samples expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="2c60f-106">La quantità di dati contenuti in un campione dipende dal componente che crea l'esempio e dal tipo di dati nei buffer.</span><span class="sxs-lookup"><span data-stu-id="2c60f-106">The amount of data contained in one sample depends on the component that creates the sample and on the type of data in the buffers.</span></span> <span data-ttu-id="2c60f-107">Per i video non compressi, un esempio include in genere un singolo fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="2c60f-107">For uncompressed video, a sample usually holds a single video frame.</span></span> <span data-ttu-id="2c60f-108">Per l'audio non compresso, la quantità di dati può variare, ma in genere un frame audio non si estende su due esempi.</span><span class="sxs-lookup"><span data-stu-id="2c60f-108">For uncompressed audio, the amount of data can vary, but usually an audio frame does not span two samples.</span></span> <span data-ttu-id="2c60f-109">Per i dati compressi, queste linee guida potrebbero non essere valide.</span><span class="sxs-lookup"><span data-stu-id="2c60f-109">For compressed data, these guidelines might not apply.</span></span>

<span data-ttu-id="2c60f-110">Un singolo campione potrebbe contenere più buffer per motivi di efficienza.</span><span class="sxs-lookup"><span data-stu-id="2c60f-110">A single sample might contain multiple buffers for reasons of efficiency.</span></span> <span data-ttu-id="2c60f-111">Ad esempio, in un file ASF, un frame video è spesso distribuito tra più pacchetti ASF.</span><span class="sxs-lookup"><span data-stu-id="2c60f-111">For example, in an ASF file, a video frame is often spread out among multiple ASF packets.</span></span> <span data-ttu-id="2c60f-112">L'origine multimediale potrebbe leggere i pacchetti in più buffer.</span><span class="sxs-lookup"><span data-stu-id="2c60f-112">The media source might read the packets into multiple buffers.</span></span> <span data-ttu-id="2c60f-113">Anziché copiare ogni frammento in un unico buffer, l'origine inserisce semplicemente tutti i buffer in un campione.</span><span class="sxs-lookup"><span data-stu-id="2c60f-113">Instead of copying each fragment into one buffer, the source simply puts all of the buffers into one sample.</span></span> <span data-ttu-id="2c60f-114">I componenti downstream possono quindi decidere se copiare i buffer più piccoli in un buffer contiguo.</span><span class="sxs-lookup"><span data-stu-id="2c60f-114">Downstream components can then decide whether to copy the smaller buffers into one contiguous buffer.</span></span> <span data-ttu-id="2c60f-115">In genere, se si sta scrivendo un componente della pipeline, è necessario presupporre che qualsiasi esempio possa contenere più di un buffer.</span><span class="sxs-lookup"><span data-stu-id="2c60f-115">Generally, if you are writing a pipeline component, you should assume that any sample might contain more than one buffer.</span></span>

<span data-ttu-id="2c60f-116">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="2c60f-116">This section contains the following topics.</span></span>



| <span data-ttu-id="2c60f-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="2c60f-117">Topic</span></span>                                                        | <span data-ttu-id="2c60f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c60f-118">Description</span></span>                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c60f-119">Utilizzo degli esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="2c60f-119">Working with Media Samples</span></span>](working-with-media-samples.md) | <span data-ttu-id="2c60f-120">Descrive il comportamento generale degli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="2c60f-120">Describes the general behavior of media samples.</span></span>                                                                         |
| [<span data-ttu-id="2c60f-121">Esempi video</span><span class="sxs-lookup"><span data-stu-id="2c60f-121">Video Samples</span></span>](video-samples.md)                           | <span data-ttu-id="2c60f-122">Descrive un'implementazione specializzata di [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) progettata per contenere frame video non compressi.</span><span class="sxs-lookup"><span data-stu-id="2c60f-122">Describes a specialized implementation of [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) designed for holding uncompressed video frames.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2c60f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c60f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c60f-124">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="2c60f-124">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="2c60f-125">Primitive Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c60f-125">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



