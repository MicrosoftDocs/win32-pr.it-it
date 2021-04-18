---
title: Sovrapposizione, sottoposto e piani principali
description: Nelle applicazioni è possibile usare i piani a livello di hardware, ovvero i piani sovrapposti e quelli sottoposti.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL in Windows, piani livello hardware
- livelli hardware OpenGL
- sovrapposizione di piani OpenGL
- piani di sottofondo OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298204"
---
# <a name="overlay-underlay-and-main-planes"></a><span data-ttu-id="e5cb6-107">Sovrapposizione, sottoposto e piani principali</span><span class="sxs-lookup"><span data-stu-id="e5cb6-107">Overlay, Underlay, and Main Planes</span></span>

<span data-ttu-id="e5cb6-108">Nelle applicazioni è possibile usare i piani a livello di hardware, ovvero i piani sovrapposti e quelli sottoposti.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-108">You can use hardware layer planes (overlay and underlay planes) in your applications.</span></span> <span data-ttu-id="e5cb6-109">Con Windows, i formati pixel descrivono le configurazioni in pixel di un dispositivo grafico.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-109">With Windows, pixel formats describe the pixel configurations of a graphics device.</span></span> <span data-ttu-id="e5cb6-110">Ogni formato pixel descrive la profondità e altre caratteristiche dei buffer dei colori principali e descrive i buffer aggiuntivi (ad esempio profondità, accumulo, stencil e ausiliario) usati dal piano principale.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-110">Each pixel format describes the depth and other characteristics of the main color buffers and describes additional buffers (such as depth, accumulation, stencil, and auxiliary) that the main plane uses.</span></span> <span data-ttu-id="e5cb6-111">I formati pixel sono ora estesi per includere i buffer sovrapposti e di sottofondo.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-111">Pixel formats are now extended to include overlay and underlay buffers.</span></span>

<span data-ttu-id="e5cb6-112">I piani di livello hanno sempre un buffer di colore in primo piano e possono includere buffer di colore anteriore e posteriore.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-112">Layer planes always have a front-left color buffer and also can include front-right and back color buffers.</span></span> <span data-ttu-id="e5cb6-113">Ogni piano di livello dispone di un contesto di rendering specifico di cui eseguire il rendering nei buffer del livello.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-113">Each layer plane has a specific rendering context to render into the layer buffers.</span></span> <span data-ttu-id="e5cb6-114">Non è possibile utilizzare le funzioni di disegno GDI nei piani di livello.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-114">You cannot use GDI drawing functions in layer planes.</span></span>

<span data-ttu-id="e5cb6-115">Una finestra gestisce i buffer dei colori dei piani di livello in modo analogo al modo in cui gestisce i buffer dei colori del piano principale.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-115">A window manages the color buffers of layer planes similarly to the way it manages main-plane color buffers.</span></span> <span data-ttu-id="e5cb6-116">È possibile visualizzare più finestre con piani sovrapposti e/o sottoposti allo stesso tempo.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-116">You can display multiple windows with overlay and/or underlay planes at the same time.</span></span> <span data-ttu-id="e5cb6-117">Non è possibile avere finestre sovrapposte a virgola mobile gratuite che possono spostarsi in qualsiasi finestra del piano di disegno principale.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-117">You cannot have free-floating overlay windows that can move over any window in the main drawing plane.</span></span> <span data-ttu-id="e5cb6-118">Inoltre, poiché in ogni momento i piani sottostanti vengono nascosti in una finestra, non è possibile utilizzare i piani popup hardware privi di colore trasparente.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-118">In addition, because it would obscure underlying planes in a window at all times, you cannot use hardware pop-up planes that have no transparent color.</span></span>

<span data-ttu-id="e5cb6-119">A ogni piano di livello in una finestra è associata una tavolozza.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-119">Each layer plane in a window has an associated palette.</span></span> <span data-ttu-id="e5cb6-120">È possibile impostare la tavolozza di un piano del livello di indice colore, ma la tavolozza di un piano di colore RGBA è fissa.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-120">You can set the palette of a color-index layer plane, but the palette of an RGBA color plane is fixed.</span></span> <span data-ttu-id="e5cb6-121">È necessario realizzare la tavolozza appropriata quando una finestra è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-121">You must realize the appropriate palette when a window is in the foreground.</span></span> <span data-ttu-id="e5cb6-122">I piani di livello hanno un colore o un indice di pixel trasparente che consente la visualizzazione di tutti i piani di livello sottostante.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-122">Layer planes have a transparent pixel color or index that enables any underlying layer planes to show through.</span></span>

<span data-ttu-id="e5cb6-123">È possibile copiare lo stato di un contesto di rendering in un altro contesto di rendering in un piano di livello separato.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-123">You can copy the state of a rendering context to another rendering context in a separate layer plane.</span></span> <span data-ttu-id="e5cb6-124">È anche possibile condividere elenchi di visualizzazione tra contesti di rendering in diversi piani di livello.</span><span class="sxs-lookup"><span data-stu-id="e5cb6-124">You can also share display lists among rendering contexts in different layer planes.</span></span>

<span data-ttu-id="e5cb6-125">Con i piani di livello vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e5cb6-125">The following functions are used with layer planes:</span></span>

-   [<span data-ttu-id="e5cb6-126">**wglCopyContext**</span><span class="sxs-lookup"><span data-stu-id="e5cb6-126">**wglCopyContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [<span data-ttu-id="e5cb6-127">**wglCreateLayerContext**</span><span class="sxs-lookup"><span data-stu-id="e5cb6-127">**wglCreateLayerContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [<span data-ttu-id="e5cb6-128">**wglDescribeLayerPlane**</span><span class="sxs-lookup"><span data-stu-id="e5cb6-128">**wglDescribeLayerPlane**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [<span data-ttu-id="e5cb6-129">**wglGetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="e5cb6-129">**wglGetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [<span data-ttu-id="e5cb6-130">**wglRealizeLayerPalette**</span><span class="sxs-lookup"><span data-stu-id="e5cb6-130">**wglRealizeLayerPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [<span data-ttu-id="e5cb6-131">**wglSetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="e5cb6-131">**wglSetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [<span data-ttu-id="e5cb6-132">**wglSwapLayerBuffers**</span><span class="sxs-lookup"><span data-stu-id="e5cb6-132">**wglSwapLayerBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




