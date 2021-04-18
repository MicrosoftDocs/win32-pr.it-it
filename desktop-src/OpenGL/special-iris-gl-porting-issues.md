---
title: Problemi speciali di porting di IRIS GL
description: Problemi speciali di porting di IRIS GL
ms.assetid: dcf7967a-2867-4443-a1c8-8335c6fe016a
keywords:
- OpenGL per Windows, porting di IRIS GL
- porting in OpenGL, IRIS GL
- Porting OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1273a873f3a39a5d237f9a5845a72f87156e001c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298815"
---
# <a name="special-iris-gl-porting-issues"></a><span data-ttu-id="d8654-106">Problemi speciali di porting di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="d8654-106">Special IRIS GL Porting Issues</span></span>

<span data-ttu-id="d8654-107">Gli argomenti seguenti descrivono le tecniche per trasferire parti specifiche del codice di IRIS GL al codice OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d8654-107">The following topics describe techniques for porting specific parts of your IRIS GL code to OpenGL code.</span></span>

-   [<span data-ttu-id="d8654-108">Portabilità del porting</span><span class="sxs-lookup"><span data-stu-id="d8654-108">Porting greset</span></span>](porting-greset.md)
-   [<span data-ttu-id="d8654-109">Porting delle funzioni "Get" di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="d8654-109">Porting IRIS GL "Get" Functions</span></span>](porting-iris-gl-get-functions.md)
-   [<span data-ttu-id="d8654-110">Porting del codice che richiede una posizione grafica corrente</span><span class="sxs-lookup"><span data-stu-id="d8654-110">Porting Code that Requires a Current Graphics Position</span></span>](porting-code-that-requires-a-current-graphics-position.md)
-   [<span data-ttu-id="d8654-111">Porting di funzioni di disegno</span><span class="sxs-lookup"><span data-stu-id="d8654-111">Porting Drawing Functions</span></span>](porting-drawing-functions.md)
-   [<span data-ttu-id="d8654-112">Porting di colori, ombreggiatura e codice Writemask</span><span class="sxs-lookup"><span data-stu-id="d8654-112">Porting Color, Shading, and Writemask Code</span></span>](porting-color--shading--and-writemask-code.md)
-   [<span data-ttu-id="d8654-113">Porting di operazioni pixel</span><span class="sxs-lookup"><span data-stu-id="d8654-113">Porting Pixel Operations</span></span>](porting-pixel-operations.md)
-   [<span data-ttu-id="d8654-114">Porting di profondità e comandi di nebbia</span><span class="sxs-lookup"><span data-stu-id="d8654-114">Porting Depth Cueing and Fog Commands</span></span>](porting-depth-cueing-and-fog-commands.md)
-   [<span data-ttu-id="d8654-115">Curva di porting e funzioni di superficie</span><span class="sxs-lookup"><span data-stu-id="d8654-115">Porting Curve and Surface Functions</span></span>](porting-curve-and-surface-functions.md)
-   [<span data-ttu-id="d8654-116">Porting di funzioni di anti-aliasing</span><span class="sxs-lookup"><span data-stu-id="d8654-116">Porting Antialiasing Functions</span></span>](porting-antialiasing-functions.md)
-   [<span data-ttu-id="d8654-117">Porting di chiamate del buffer di accumulo</span><span class="sxs-lookup"><span data-stu-id="d8654-117">Porting Accumulation Buffer Calls</span></span>](porting-accumulation-buffer-calls.md)
-   [<span data-ttu-id="d8654-118">Porting di chiamate del piano stencil</span><span class="sxs-lookup"><span data-stu-id="d8654-118">Porting Stencil Plane Calls</span></span>](porting-stencil-plane-calls.md)
-   [<span data-ttu-id="d8654-119">Porting degli elenchi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="d8654-119">Porting Display Lists</span></span>](porting-display-lists.md)
-   [<span data-ttu-id="d8654-120">Porting di defs, binding e set</span><span class="sxs-lookup"><span data-stu-id="d8654-120">Porting Defs, Binds, and Sets</span></span>](porting-defs--binds--and-sets.md)
-   [<span data-ttu-id="d8654-121">Porting di funzioni di illuminazione e materiali</span><span class="sxs-lookup"><span data-stu-id="d8654-121">Porting Lighting and Materials Functions</span></span>](porting-lighting-and-materials-functions.md)
-   [<span data-ttu-id="d8654-122">Porting di funzioni di trama</span><span class="sxs-lookup"><span data-stu-id="d8654-122">Porting Texture Functions</span></span>](porting-texture-functions.md)
-   [<span data-ttu-id="d8654-123">Funzioni di selezione del porting</span><span class="sxs-lookup"><span data-stu-id="d8654-123">Porting Picking Functions</span></span>](porting-picking-functions.md)
-   [<span data-ttu-id="d8654-124">Porting di funzioni di feedback</span><span class="sxs-lookup"><span data-stu-id="d8654-124">Porting Feedback Functions</span></span>](porting-feedback-functions.md)

 

 




