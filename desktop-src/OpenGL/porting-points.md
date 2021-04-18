---
title: Punti di porting
description: OpenGL non ha alcun comando per creare un singolo punto. In caso contrario, le funzioni del punto di porting sono semplici. La tabella seguente elenca le funzioni di IRIS GL per i punti di disegno e le relative funzioni OpenGL equivalenti.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- Porting di IRIS GL, punti
- porting da IRIS GL, punti
- porting in OpenGL da IRIS GL, punti
- Porting OpenGL da IRIS GL, punti
- disegno di funzioni, punti
- punti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298538"
---
# <a name="porting-points"></a><span data-ttu-id="75b0b-111">Punti di porting</span><span class="sxs-lookup"><span data-stu-id="75b0b-111">Porting Points</span></span>

<span data-ttu-id="75b0b-112">OpenGL non ha alcun comando per creare un singolo punto.</span><span class="sxs-lookup"><span data-stu-id="75b0b-112">OpenGL has no command to draw a single point.</span></span> <span data-ttu-id="75b0b-113">In caso contrario, le funzioni del punto di porting sono semplici.</span><span class="sxs-lookup"><span data-stu-id="75b0b-113">Otherwise, porting point functions is straightforward.</span></span> <span data-ttu-id="75b0b-114">La tabella seguente elenca le funzioni di IRIS GL per i punti di disegno e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="75b0b-114">The following table lists IRIS GL functions for drawing points and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="75b0b-115">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="75b0b-115">IRIS GL function</span></span>           | <span data-ttu-id="75b0b-116">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="75b0b-116">OpenGL function</span></span>                                                   | <span data-ttu-id="75b0b-117">Significato</span><span class="sxs-lookup"><span data-stu-id="75b0b-117">Meaning</span></span>                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b0b-118">**PNT**</span><span class="sxs-lookup"><span data-stu-id="75b0b-118">**pnt**</span></span>                    |                                                                   | <span data-ttu-id="75b0b-119">Disegna un singolo punto.</span><span class="sxs-lookup"><span data-stu-id="75b0b-119">Draws a single point.</span></span>                                                                                                                                |
| <span data-ttu-id="75b0b-120">**bgnpoint**, **endpoint**</span><span class="sxs-lookup"><span data-stu-id="75b0b-120">**bgnpoint**, **endpoint**</span></span> | <span data-ttu-id="75b0b-121">[**glBegin**](glbegin.md) ( \_ punti GL), [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="75b0b-121">[**glBegin**](glbegin.md) ( GL\_POINTS ), [**glEnd**](glend.md)</span></span> | <span data-ttu-id="75b0b-122">Interpreta i vertici come punti.</span><span class="sxs-lookup"><span data-stu-id="75b0b-122">Interprets vertices as points.</span></span>                                                                                                                       |
| <span data-ttu-id="75b0b-123">**pntsize**</span><span class="sxs-lookup"><span data-stu-id="75b0b-123">**pntsize**</span></span>                | [<span data-ttu-id="75b0b-124">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="75b0b-124">**glPointSize**</span></span>](glpointsize.md)                                | <span data-ttu-id="75b0b-125">Imposta la dimensione del punto in pixel.</span><span class="sxs-lookup"><span data-stu-id="75b0b-125">Sets point size in pixels.</span></span>                                                                                                                           |
| <span data-ttu-id="75b0b-126">**pntsmooth**</span><span class="sxs-lookup"><span data-stu-id="75b0b-126">**pntsmooth**</span></span>              | <span data-ttu-id="75b0b-127">[**glEnable**](glenable.md) ( \_ punto GL \_ smussato)</span><span class="sxs-lookup"><span data-stu-id="75b0b-127">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>                | <span data-ttu-id="75b0b-128">Attiva l'anti-aliasing del punto.</span><span class="sxs-lookup"><span data-stu-id="75b0b-128">Turns on point antialiasing.</span></span> <span data-ttu-id="75b0b-129">Per ulteriori informazioni sull'anti-aliasing dei punti, vedere [porting anti-aliasing Functions](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="75b0b-129">(For more information on point antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="75b0b-130">Per informazioni sulle funzioni Get correlate, vedere [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="75b0b-130">For information about related get functions, see [**glPointSize**](glpointsize.md).</span></span>

<span data-ttu-id="75b0b-131">??</span><span class="sxs-lookup"><span data-stu-id="75b0b-131">??</span></span>

 

 




