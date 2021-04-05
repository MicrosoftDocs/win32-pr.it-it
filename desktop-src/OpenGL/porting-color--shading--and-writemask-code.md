---
title: Porting di colori, ombreggiatura e codice Writemask
description: Porting di colori, ombreggiatura e codice Writemask
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Porting di IRIS GL, colore
- porting da IRIS GL, color
- porting in OpenGL da IRIS GL, colore
- Porting OpenGL da IRIS GL, colore
- Porting di IRIS GL, ombreggiatura
- porting da IRIS GL, ombreggiatura
- porting in OpenGL da IRIS GL, ombreggiatura
- Porting OpenGL da IRIS GL, ombreggiatura
- Porting di IRIS GL, writemask
- porting da IRIS GL, writemask
- porting in OpenGL da IRIS GL, writemask
- Porting OpenGL da IRIS GL, writemask
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708467"
---
# <a name="porting-color-shading-and-writemask-code"></a><span data-ttu-id="ca646-115">Porting di colori, ombreggiatura e codice Writemask</span><span class="sxs-lookup"><span data-stu-id="ca646-115">Porting Color, Shading, and Writemask Code</span></span>

<span data-ttu-id="ca646-116">Quando si portano il codice di colore, ombreggiatura e writemask in OpenGL, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="ca646-116">When porting color, shading, and writemask code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="ca646-117">Sebbene sia possibile impostare gli indici mappa colori con la funzione OpenGL [glIndex](glindex-functions.md) , OpenGL non dispone di una funzione per il caricamento degli indici mappa colori.</span><span class="sxs-lookup"><span data-stu-id="ca646-117">Though you can set color-map indexes with the OpenGL [glIndex](glindex-functions.md) function, OpenGL does not have a function for loading color-map indexes.</span></span>
-   <span data-ttu-id="ca646-118">I valori dei colori vengono normalizzati in base al tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="ca646-118">Color values are normalized to their data type.</span></span> <span data-ttu-id="ca646-119">Per informazioni sui valori dei colori, vedere [glColor](glcolor-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ca646-119">(For information about color values, see [glColor](glcolor-functions.md)).</span></span>
-   <span data-ttu-id="ca646-120">Non esiste un equivalente semplice per **CPack**.</span><span class="sxs-lookup"><span data-stu-id="ca646-120">There is no simple equivalent for **cpack**.</span></span>
-   <span data-ttu-id="ca646-121">Potrebbe essere necessario tradurre il codice che include le funzioni **c** o **color** in [**glClearColor**](glclearcolor.md) o [**glClearIndex**](glclearindex.md) anziché **glColor** o **glIndex**.</span><span class="sxs-lookup"><span data-stu-id="ca646-121">You may have to translate code that includes the **c** or **color** functions to [**glClearColor**](glclearcolor.md) or [**glClearIndex**](glclearindex.md) instead of **glColor** or **glIndex**.</span></span>
-   <span data-ttu-id="ca646-122">Il writemask RGBA viene applicato a ogni componente, ma non a ogni bit.</span><span class="sxs-lookup"><span data-stu-id="ca646-122">The RGBA writemask applies to each component but not for each bit.</span></span>
-   <span data-ttu-id="ca646-123">IRIS GL fornisce costanti di colore definite: nero, blu, rosso, verde, MAGENTA, ciano, giallo e bianco.</span><span class="sxs-lookup"><span data-stu-id="ca646-123">IRIS GL provides defined color constants: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW, and WHITE.</span></span> <span data-ttu-id="ca646-124">OpenGL non fornisce queste costanti.</span><span class="sxs-lookup"><span data-stu-id="ca646-124">OpenGL does not provide these constants.</span></span>

<span data-ttu-id="ca646-125">Questo argomento include informazioni sui seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="ca646-125">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="ca646-126">Chiamate di colore di porting</span><span class="sxs-lookup"><span data-stu-id="ca646-126">Porting Color Calls</span></span>](porting-color-calls.md)
-   [<span data-ttu-id="ca646-127">Porting di modelli di ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="ca646-127">Porting Shading Models</span></span>](porting-shading-models.md)

 

 




