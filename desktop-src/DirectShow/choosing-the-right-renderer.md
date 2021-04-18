---
description: Scelta del renderer video corretto
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Scelta del renderer video corretto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304330"
---
# <a name="choosing-the-right-video-renderer"></a><span data-ttu-id="c44af-103">Scelta del renderer video corretto</span><span class="sxs-lookup"><span data-stu-id="c44af-103">Choosing the Right Video Renderer</span></span>

<span data-ttu-id="c44af-104">DirectShow fornisce diversi filtri per renderer video, riepilogati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c44af-104">DirectShow provides several video renderer filters, summarized in the following table.</span></span>



| <span data-ttu-id="c44af-105">Filtra</span><span class="sxs-lookup"><span data-stu-id="c44af-105">Filter</span></span>                                                                  | <span data-ttu-id="c44af-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="c44af-106">Remarks</span></span>                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c44af-107">[**Renderer video migliorato**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="c44af-107">[**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR)</span></span> | <span data-ttu-id="c44af-108">USA Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c44af-108">Uses Direct3D 9.</span></span> <span data-ttu-id="c44af-109">Richiede Windows Vista o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c44af-109">Requires Windows Vista or later.</span></span> |
| <span data-ttu-id="c44af-110">[Renderer di mixaggio video 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="c44af-110">[Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>   | <span data-ttu-id="c44af-111">USA Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c44af-111">Uses Direct3D 9.</span></span> <span data-ttu-id="c44af-112">Richiede Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c44af-112">Requires Windows XP or later.</span></span>    |
| <span data-ttu-id="c44af-113">[Filtro di mixaggio video 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="c44af-113">[Video Mixing Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>     | <span data-ttu-id="c44af-114">Usa DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c44af-114">Uses DirectDraw.</span></span> <span data-ttu-id="c44af-115">Richiede Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c44af-115">Requires Windows XP or later.</span></span>    |
| [<span data-ttu-id="c44af-116">Mixer overlay</span><span class="sxs-lookup"><span data-stu-id="c44af-116">Overlay Mixer</span></span>](using-the-overlay-mixer-in-video-capture.md)           | <span data-ttu-id="c44af-117">Supporta le sovrapposizioni hardware tramite DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="c44af-117">Supports hardware overlays through DirectDraw.</span></span>    |
| <span data-ttu-id="c44af-118">Filtro [renderer video](video-renderer-filter.md) legacy.</span><span class="sxs-lookup"><span data-stu-id="c44af-118">Legacy [Video Renderer](video-renderer-filter.md) filter.</span></span>              | <span data-ttu-id="c44af-119">Usa DirectDraw o (raramente) GDI</span><span class="sxs-lookup"><span data-stu-id="c44af-119">Uses DirectDraw or (rarely) GDI</span></span>                   |



 

<span data-ttu-id="c44af-120">Il renderer da usare dipende in gran parte dalle versioni di Windows che è necessario supportare.</span><span class="sxs-lookup"><span data-stu-id="c44af-120">Which renderer to use depends largely on which versions of Windows you need to support.</span></span>

-   <span data-ttu-id="c44af-121">In Windows Vista e versioni successive, le applicazioni devono utilizzare EVR se l'hardware lo supporta.</span><span class="sxs-lookup"><span data-stu-id="c44af-121">In Windows Vista and later, applications should use the EVR if the hardware supports it.</span></span> <span data-ttu-id="c44af-122">In caso contrario, eseguire il fallback a VMR-9 o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="c44af-122">Otherwise, fall back to the VMR-9 or VMR-7.</span></span> <span data-ttu-id="c44af-123">Il EVR offre prestazioni migliori e una migliore qualità dei video rispetto ai renderer precedenti.</span><span class="sxs-lookup"><span data-stu-id="c44af-123">The EVR offers better performance and better video quality than previous renderers.</span></span> <span data-ttu-id="c44af-124">Inoltre, è progettato per funzionare con la Gestione finestre desktop (DWM).</span><span class="sxs-lookup"><span data-stu-id="c44af-124">Also, it is designed to work with the Desktop Window Manager (DWM).</span></span>
-   <span data-ttu-id="c44af-125">Prima di Windows Vista, utilizzare VMR-9 se l'hardware lo supporta e la funzionalità della porta video non è necessaria.</span><span class="sxs-lookup"><span data-stu-id="c44af-125">Prior to Windows Vista, use the VMR-9 if the hardware supports it and video port functionality is not required.</span></span> <span data-ttu-id="c44af-126">In caso contrario, usare VMR-7.</span><span class="sxs-lookup"><span data-stu-id="c44af-126">Otherwise, use the VMR-7.</span></span>
-   <span data-ttu-id="c44af-127">Nei sistemi meno recenti potrebbe essere necessario usare il mixer overlay (per la porta video o il supporto della sovrimpressione hardware) o il filtro renderer video legacy.</span><span class="sxs-lookup"><span data-stu-id="c44af-127">On older systems, you might need to use the Overlay Mixer (for video port or hardware overlay support) or the legacy Video Renderer filter.</span></span>

<span data-ttu-id="c44af-128">Per impostazione predefinita, i metodi [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) e [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) usano VMR-7.</span><span class="sxs-lookup"><span data-stu-id="c44af-128">The [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) and [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) methods use the VMR-7 by default.</span></span> <span data-ttu-id="c44af-129">Se l'hardware non supporta VMR-7, questi metodi eseguono il fallback al filtro renderer video legacy.</span><span class="sxs-lookup"><span data-stu-id="c44af-129">If the hardware does not support the VMR-7, these methods fall back to the legacy Video Renderer filter.</span></span> <span data-ttu-id="c44af-130">EVR e VMR-9 non sono mai i renderer predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c44af-130">The EVR and VMR-9 are never the default renderers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c44af-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c44af-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c44af-132">Rendering video</span><span class="sxs-lookup"><span data-stu-id="c44af-132">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



