---
description: Uso del renderer video mixing
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Uso del renderer video mixing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314382"
---
# <a name="using-the-video-mixing-renderer"></a><span data-ttu-id="a9181-103">Uso del renderer video mixing</span><span class="sxs-lookup"><span data-stu-id="a9181-103">Using the Video Mixing Renderer</span></span>

<span data-ttu-id="a9181-104">In termini di prestazioni e di ampia gamma di funzionalità, il filtro VMR (video Mixing Renderer) rappresenta la nuova generazione di rendering video sulla piattaforma Windows.</span><span class="sxs-lookup"><span data-stu-id="a9181-104">In terms of both performance and breadth of features, the Video Mixing Renderer (VMR) filter represents the next generation in video rendering on the Windows platform.</span></span> <span data-ttu-id="a9181-105">Il VMR sostituisce il [mixer overlay](overlay-mixer-filter.md) e il [renderer video](video-renderer-filter.md)e aggiunge molte nuove funzionalità di combinazione.</span><span class="sxs-lookup"><span data-stu-id="a9181-105">The VMR replaces the [Overlay Mixer](overlay-mixer-filter.md) and [Video Renderer](video-renderer-filter.md), and adds many new mixing features.</span></span>

<span data-ttu-id="a9181-106">Sono disponibili due versioni di VMR:</span><span class="sxs-lookup"><span data-stu-id="a9181-106">There are two versions of the VMR:</span></span>

-   <span data-ttu-id="a9181-107">VMR-7, che usa DirectDraw 7 per il rendering.</span><span class="sxs-lookup"><span data-stu-id="a9181-107">The VMR-7, which uses DirectDraw 7 for rendering.</span></span>
-   <span data-ttu-id="a9181-108">VMR-9, che utilizza Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a9181-108">The VMR-9, which uses Direct3D 9.</span></span>

<span data-ttu-id="a9181-109">VMR-7 è disponibile in Windows XP e versioni successive, ma non è disponibile per la ridistribuzione.</span><span class="sxs-lookup"><span data-stu-id="a9181-109">The VMR-7 is available on Windows XP and later, but is not available for redistribution.</span></span> <span data-ttu-id="a9181-110">VMR-9 è disponibile per la ridistribuzione su tutte le piattaforme supportate da DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="a9181-110">The VMR-9 is available for redistribution on all platforms supported by DirectX 9.</span></span> <span data-ttu-id="a9181-111">I due filtri VMR sono molto simili all'implementazione e alle interfacce che espongono.</span><span class="sxs-lookup"><span data-stu-id="a9181-111">The two VMR filters are very similar in their implementation and the interfaces that they expose.</span></span>

<span data-ttu-id="a9181-112">VMR-9 ha il proprio CLSID e il proprio set di interfacce, strutture e tipi di enumerazione che non sono sempre identici ai tipi di dati corrispondenti per VMR-7, a causa delle differenze di base tra DirectDraw 7 e Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="a9181-112">The VMR-9 has its own CLSID and its own set of interfaces, structures and enumeration types which are not always identical to the corresponding data types for the VMR-7, due to the underlying differences between DirectDraw 7 and Direct3D 9.</span></span> <span data-ttu-id="a9181-113">Le interfacce VMR-9 terminano tutte con "9", ad esempio **IVMRStreamConfig9**, e le strutture e i tipi di enumerazione hanno tutti "VMR9" nel nome per distinguerli dai tipi di dati usati con VMR-7.</span><span class="sxs-lookup"><span data-stu-id="a9181-113">The VMR-9 interfaces all end with "9", for example **IVMRStreamConfig9**, and the structures and enumeration types all have "VMR9" in their name to distinguish them from the data types used with the VMR-7.</span></span>

<span data-ttu-id="a9181-114">Per garantire la compatibilità con le versioni precedenti, VMR-9 non è il renderer predefinito in alcun sistema.</span><span class="sxs-lookup"><span data-stu-id="a9181-114">To ensure backward-compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="a9181-115">Per usare VMR-9, è necessario aggiungerlo in modo esplicito al grafo del filtro usando il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) e configurarlo prima di connetterlo a tutti i filtri upstream.</span><span class="sxs-lookup"><span data-stu-id="a9181-115">To use the VMR-9, you must explicitly add it to the filter graph using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method, and configure it before connecting it to any upstream filters.</span></span>

<span data-ttu-id="a9181-116">Questo articolo include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="a9181-116">This article contains the following sections.</span></span> <span data-ttu-id="a9181-117">Eccetto dove indicato, le informazioni contenute in queste sezioni si applicano sia ai filtri VMR-7 che VMR-9.</span><span class="sxs-lookup"><span data-stu-id="a9181-117">Except where noted, the information in these sections applies to both the VMR-7 and the VMR-9 filters.</span></span>

-   [<span data-ttu-id="a9181-118">Informazioni sul rendering del mixaggio video</span><span class="sxs-lookup"><span data-stu-id="a9181-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
-   [<span data-ttu-id="a9181-119">Modalità di funzionamento VMR</span><span class="sxs-lookup"><span data-stu-id="a9181-119">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
-   [<span data-ttu-id="a9181-120">Creazione di un grafico di filtro VMR-9</span><span class="sxs-lookup"><span data-stu-id="a9181-120">Building a VMR-9 Filter Graph</span></span>](building-a-vmr-9-filter-graph.md)
-   [<span data-ttu-id="a9181-121">Uso della modalità di combinazione VMR</span><span class="sxs-lookup"><span data-stu-id="a9181-121">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
-   [<span data-ttu-id="a9181-122">Impostazione delle preferenze di deinterlacciamento</span><span class="sxs-lookup"><span data-stu-id="a9181-122">Setting Deinterlace Preferences</span></span>](setting-deinterlace-preferences.md)
-   [<span data-ttu-id="a9181-123">Uso di VMR per gli sviluppatori di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9181-123">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
-   [<span data-ttu-id="a9181-124">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="a9181-124">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a><span data-ttu-id="a9181-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9181-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9181-126">Filtro renderer video mixing 7</span><span class="sxs-lookup"><span data-stu-id="a9181-126">Video Mixing Renderer Filter 7</span></span>](video-mixing-renderer-filter-7.md)
</dt> <dt>

[<span data-ttu-id="a9181-127">Filtro renderer di video mixing 9</span><span class="sxs-lookup"><span data-stu-id="a9181-127">Video Mixing Renderer Filter 9</span></span>](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



