---
description: Composizione
ms.assetid: b5f607b2-9cca-4eef-9c63-d2015bd10469
title: Composizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030e02ab77ec54e1e340d72db7210665d649bfb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303822"
---
# <a name="composition"></a><span data-ttu-id="3c6dc-103">Composizione</span><span class="sxs-lookup"><span data-stu-id="3c6dc-103">Composition</span></span>

> [!Note]  
> <span data-ttu-id="3c6dc-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-104">\[Deprecated.</span></span> <span data-ttu-id="3c6dc-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c6dc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3c6dc-106">L'oggetto Composition è un contenitore per le tracce.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-106">The composition object is a container for tracks.</span></span> <span data-ttu-id="3c6dc-107">Può inoltre detenere altre composizioni (per l'annidamento di tracce), effetti e transizioni.</span><span class="sxs-lookup"><span data-stu-id="3c6dc-107">It can also hold other compositions (for nesting of tracks), effects, and transitions.</span></span> <span data-ttu-id="3c6dc-108">Per creare questo oggetto, chiamare il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .</span><span class="sxs-lookup"><span data-stu-id="3c6dc-108">To create this object, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span>

<span data-ttu-id="3c6dc-109">L'oggetto Composition espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c6dc-109">The composition object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="3c6dc-110">**IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="3c6dc-110">**IAMTimelineComp**</span></span>](iamtimelinecomp.md)
-   [<span data-ttu-id="3c6dc-111">**IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="3c6dc-111">**IAMTimelineEffectable**</span></span>](iamtimelineeffectable.md)
-   [<span data-ttu-id="3c6dc-112">**IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="3c6dc-112">**IAMTimelineObj**</span></span>](iamtimelineobj.md)
-   [<span data-ttu-id="3c6dc-113">**IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="3c6dc-113">**IAMTimelineTransable**</span></span>](iamtimelinetransable.md)
-   [<span data-ttu-id="3c6dc-114">**IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="3c6dc-114">**IAMTimelineVirtualTrack**</span></span>](iamtimelinevirtualtrack.md)

## <a name="related-topics"></a><span data-ttu-id="3c6dc-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c6dc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c6dc-116">Modello di sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="3c6dc-116">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="3c6dc-117">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="3c6dc-117">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



