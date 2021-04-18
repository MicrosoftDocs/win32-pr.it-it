---
description: Il livello della pipeline in Microsoft Media Foundation è il livello dell'architettura che genera o elabora direttamente i dati multimediali.
ms.assetid: d6396246-ddc4-4e24-9371-35ddbef59b8a
title: Pipeline Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f307049d7f88ca6b50479bdb261c75ba20f9b41e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320496"
---
# <a name="media-foundation-pipeline"></a><span data-ttu-id="3780e-103">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3780e-103">Media Foundation Pipeline</span></span>

<span data-ttu-id="3780e-104">Il livello della *pipeline* in Microsoft Media Foundation è il livello dell'architettura che genera o elabora direttamente i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="3780e-104">The *pipeline* layer in Microsoft Media Foundation is the layer of the architecture that directly generates or processes media data.</span></span>

<span data-ttu-id="3780e-105">La maggior parte delle applicazioni non chiama i metodi direttamente sui componenti della pipeline, anche se è possibile farlo.</span><span class="sxs-lookup"><span data-stu-id="3780e-105">Most applications do not call methods directly on the pipeline components, although it is possible to do so.</span></span> <span data-ttu-id="3780e-106">Leggere questi argomenti se si sta scrivendo un componente personalizzato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="3780e-106">Read these topics if you are writing a custom pipeline component.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3780e-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3780e-107">In this section</span></span>



| <span data-ttu-id="3780e-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="3780e-108">Topic</span></span>                                                                     | <span data-ttu-id="3780e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3780e-109">Description</span></span>                                                                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3780e-110">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="3780e-110">Media Sources</span></span>](media-sources.md)<br/>                             | <span data-ttu-id="3780e-111">Le origini supporti generano dati multimediali, in genere da un file, un dispositivo di acquisizione o un flusso di rete.</span><span class="sxs-lookup"><span data-stu-id="3780e-111">Media sources generate media data, typically from a file, capture device, or network stream.</span></span> <br/>                              |
| [<span data-ttu-id="3780e-112">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3780e-112">Media Foundation Transforms</span></span>](media-foundation-transforms.md)<br/> | <span data-ttu-id="3780e-113">Media Foundation Transforms (MFTs) elabora i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="3780e-113">Media Foundation transforms (MFTs) process media data.</span></span> <span data-ttu-id="3780e-114">I codec in Media Foundation, ad esempio, vengono implementati come MFTs.</span><span class="sxs-lookup"><span data-stu-id="3780e-114">For example, codecs in Media Foundation are implemented as MFTs.</span></span> <br/>   |
| [<span data-ttu-id="3780e-115">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="3780e-115">Media Sinks</span></span>](media-sinks.md)<br/>                                 | <span data-ttu-id="3780e-116">I sink multimediali utilizzano dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="3780e-116">Media sinks consume media data.</span></span> <span data-ttu-id="3780e-117">Ad esempio, un sink multimediale potrebbe scrivere i dati in un file o inviare i dati in una rete.</span><span class="sxs-lookup"><span data-stu-id="3780e-117">For example, a media sink might write the data to a file, or send the data over a network.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3780e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3780e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3780e-119">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="3780e-119">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="3780e-120">Architettura di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3780e-120">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




