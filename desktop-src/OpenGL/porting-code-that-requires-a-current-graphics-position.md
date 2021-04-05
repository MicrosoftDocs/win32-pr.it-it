---
title: Codice porta che necessita di una posizione grafica corrente
description: OpenGL non mantiene una posizione grafica corrente. Le funzioni di IRIS GL che dipendono dalla posizione grafica corrente, ad esempio Move, disegnato e RMV, non hanno equivalenti in OpenGL.
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- Porting di IRIS GL, posizione grafica corrente
- porting da IRIS GL, posizione grafica corrente
- porting in OpenGL da IRIS GL, posizione grafica corrente
- Porting OpenGL da IRIS GL, posizione grafica corrente
- posizione grafica corrente
- posizioni raster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/27/2019
ms.locfileid: "103719597"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a><span data-ttu-id="925d1-110">Codice porta che necessita di una posizione grafica corrente</span><span class="sxs-lookup"><span data-stu-id="925d1-110">Port code that needs a current graphics position</span></span>

<span data-ttu-id="925d1-111">OpenGL non mantiene una posizione grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="925d1-111">OpenGL does not maintain a current graphics position.</span></span> <span data-ttu-id="925d1-112">Le funzioni di IRIS GL che dipendono dalla posizione grafica corrente, ad esempio **Move**, **disegnato** e **RMV**, non hanno equivalenti in OpenGL.</span><span class="sxs-lookup"><span data-stu-id="925d1-112">IRIS GL functions that depend on the current graphics position, such as **move**, **draw**, and **rmv**, have no equivalents in OpenGL.</span></span>

<span data-ttu-id="925d1-113">Le versioni precedenti di IRIS GL includevano i comandi che si basavano sulla posizione grafica corrente, sebbene il loro utilizzo fosse sconsigliato.</span><span class="sxs-lookup"><span data-stu-id="925d1-113">Older versions of IRIS GL included drawing commands that relied upon the current graphics position, though their use has been discouraged.</span></span> <span data-ttu-id="925d1-114">Sarà necessario riscrivere il codice se si è basata sulla posizione grafica corrente in qualsiasi modo o se è stata usata una delle routine seguenti:</span><span class="sxs-lookup"><span data-stu-id="925d1-114">You will need to rewrite your code if you relied on the current graphics position in any way, or used any of the following routines:</span></span>

-   <span data-ttu-id="925d1-115">**disegni** e **spostamenti**</span><span class="sxs-lookup"><span data-stu-id="925d1-115">**draw** and **move**</span></span>
-   <span data-ttu-id="925d1-116">**PMV**, **PDR** e **PCLOS**</span><span class="sxs-lookup"><span data-stu-id="925d1-116">**pmv**, **pdr**, and **pclos**</span></span>
-   <span data-ttu-id="925d1-117">**RDR**, **RMV**, **rpdr** e **rpmv**</span><span class="sxs-lookup"><span data-stu-id="925d1-117">**rdr**, **rmv**, **rpdr**, and **rpmv**</span></span>
-   <span data-ttu-id="925d1-118">**oggetti GetGPO**</span><span class="sxs-lookup"><span data-stu-id="925d1-118">**getgpos**</span></span>

<span data-ttu-id="925d1-119">OpenGL presenta un concetto di posizione raster che corrisponde alla posizione corrente del carattere di IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="925d1-119">OpenGL has a concept of raster position that corresponds to IRIS GL's current character position.</span></span> <span data-ttu-id="925d1-120">Per altre informazioni sul posizionamento raster, vedere [porting pixel Operation](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="925d1-120">For more information on raster positioning, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="925d1-121">Questo argomento include informazioni sui seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="925d1-121">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="925d1-122">Porting dei comandi di cancellazione dello schermo e del buffer</span><span class="sxs-lookup"><span data-stu-id="925d1-122">Porting Screen and Buffer Clearing Commands</span></span>](porting-screen-and-buffer-clearing-commands.md)
-   [<span data-ttu-id="925d1-123">Porting di matrici e funzioni di trasformazione</span><span class="sxs-lookup"><span data-stu-id="925d1-123">Porting Matrix and Transformation Functions</span></span>](porting-matrix-and-transformation-functions.md)
-   [<span data-ttu-id="925d1-124">Porting del codice in modalità MSINGLE</span><span class="sxs-lookup"><span data-stu-id="925d1-124">Porting MSINGLE Mode Code</span></span>](porting-msingle-mode-code.md)
-   [<span data-ttu-id="925d1-125">Funzioni di porting che ottengono matrici e trasformazioni</span><span class="sxs-lookup"><span data-stu-id="925d1-125">Porting Functions that Get Matrices and Transformations</span></span>](porting-functions-that-get-matrices-and-transformations.md)
-   [<span data-ttu-id="925d1-126">Porting di viewport, Screenmasks e Scrboxes</span><span class="sxs-lookup"><span data-stu-id="925d1-126">Porting Viewports, Screenmasks, and Scrboxes</span></span>](porting-viewports--screenmasks--and-scrboxes.md)
-   [<span data-ttu-id="925d1-127">Porting di piani di ritaglio</span><span class="sxs-lookup"><span data-stu-id="925d1-127">Porting Clipping Planes</span></span>](porting-clipping-planes.md)

 

 




