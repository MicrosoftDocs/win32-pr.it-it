---
description: Buffer multimediali
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Buffer multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320776"
---
# <a name="media-buffers"></a><span data-ttu-id="0c7d3-103">Buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="0c7d3-103">Media Buffers</span></span>

<span data-ttu-id="0c7d3-104">Un buffer multimediale è un oggetto COM che gestisce un blocco di memoria, in genere per memorizzare i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-104">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="0c7d3-105">I buffer multimediali vengono usati per spostare i dati da un componente della pipeline a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-105">Media buffers are used to move data from one pipeline component to the next.</span></span> <span data-ttu-id="0c7d3-106">La maggior parte delle applicazioni non usa direttamente i buffer multimediali, perché la sessione multimediale gestisce tutto il flusso di dati tra oggetti pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-106">Most applications do not use media buffers directly, because the Media Session handles all of the data flow between pipeline objects.</span></span> <span data-ttu-id="0c7d3-107">È necessario utilizzare i buffer multimediali se si sta scrivendo un componente della pipeline personalizzato o se si utilizza direttamente un componente della pipeline senza la sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-107">You must use media buffers if you are writing your own pipeline component, or if you are using a pipeline component directly without the Media Session.</span></span>

<span data-ttu-id="0c7d3-108">Buffer multimediali espone l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="0c7d3-108">Media buffers exposes the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="0c7d3-109">Questa interfaccia è progettata per la lettura o la scrittura di qualsiasi tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-109">This interface is designed for reading or writing any type of data.</span></span> <span data-ttu-id="0c7d3-110">I frame video non compressi richiedono una gestione speciale, perché possono essere archiviati in superfici Direct3D situate nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-110">Uncompressed video frames require special handling, because they might be stored in Direct3D surfaces located in video memory.</span></span>

<span data-ttu-id="0c7d3-111">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-111">This section contains the following topics.</span></span>



| <span data-ttu-id="0c7d3-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="0c7d3-112">Topic</span></span>                                                        | <span data-ttu-id="0c7d3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c7d3-113">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="0c7d3-114">Uso dei buffer multimediali</span><span class="sxs-lookup"><span data-stu-id="0c7d3-114">Working with Media Buffers</span></span>](working-with-media-buffers.md) | <span data-ttu-id="0c7d3-115">Descrive il comportamento generale dei buffer multimediali per tutti i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-115">Describes the general behavior of media buffers for all media types.</span></span> |
| [<span data-ttu-id="0c7d3-116">Buffer video non compressi</span><span class="sxs-lookup"><span data-stu-id="0c7d3-116">Uncompressed Video Buffers</span></span>](uncompressed-video-buffers.md) | <span data-ttu-id="0c7d3-117">Come usare i buffer multimediali che contengono frame video non compressi.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-117">How work with media buffers that contain uncompressed video frames.</span></span>  |
| [<span data-ttu-id="0c7d3-118">Buffer della superficie DirectX</span><span class="sxs-lookup"><span data-stu-id="0c7d3-118">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)         | <span data-ttu-id="0c7d3-119">Viene descritto come archiviare una superficie Direct3D in un buffer multimediale.</span><span class="sxs-lookup"><span data-stu-id="0c7d3-119">Describes how to store a Direct3D surface in a media buffer.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="0c7d3-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c7d3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c7d3-121">Primitive Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c7d3-121">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



