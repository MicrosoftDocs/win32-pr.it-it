---
title: Porting delle curve di taglio
description: Le curve di trimming OpenGL sono molto simili alle curve di taglio GL di IRIS. La tabella seguente elenca le funzioni di IRIS GL per la definizione delle curve di taglio e delle funzioni OpenGL equivalenti.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Porting di IRIS GL, curve di taglio
- porting da IRIS GL, curve di taglio
- porting in OpenGL da IRIS GL, taglio delle curve
- Porting OpenGL da IRIS GL, curve di taglio
- taglio di curve
- curve
- Porting di IRIS GL, curve
- porting da IRIS GL, curve
- porting in OpenGL da IRIS GL, curve
- Porting OpenGL da IRIS GL, curve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221819"
---
# <a name="porting-trimming-curves"></a><span data-ttu-id="62740-114">Porting delle curve di taglio</span><span class="sxs-lookup"><span data-stu-id="62740-114">Porting Trimming Curves</span></span>

<span data-ttu-id="62740-115">Le curve di trimming OpenGL sono molto simili alle curve di taglio GL di IRIS.</span><span class="sxs-lookup"><span data-stu-id="62740-115">OpenGL trimming curves are very similar to IRIS GL trimming curves.</span></span> <span data-ttu-id="62740-116">La tabella seguente elenca le funzioni di IRIS GL per la definizione delle curve di taglio e delle funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="62740-116">The following table lists the IRIS GL functions for defining trimming curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="62740-117">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="62740-117">IRIS GL function</span></span> | <span data-ttu-id="62740-118">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="62740-118">OpenGL function</span></span>                        | <span data-ttu-id="62740-119">Significato</span><span class="sxs-lookup"><span data-stu-id="62740-119">Meaning</span></span>                              |
|------------------|----------------------------------------|--------------------------------------|
| <span data-ttu-id="62740-120">**bgntrim**</span><span class="sxs-lookup"><span data-stu-id="62740-120">**bgntrim**</span></span>      | [<span data-ttu-id="62740-121">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="62740-121">**gluBeginTrim**</span></span>](glubegintrim.md)   | <span data-ttu-id="62740-122">Inizia la definizione della curva di taglio.</span><span class="sxs-lookup"><span data-stu-id="62740-122">Begins trimming-curve definition.</span></span>    |
| <span data-ttu-id="62740-123">**pwlcurve**</span><span class="sxs-lookup"><span data-stu-id="62740-123">**pwlcurve**</span></span>     | [<span data-ttu-id="62740-124">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="62740-124">**gluPwlCurve**</span></span>](glupwlcurve.md)     | <span data-ttu-id="62740-125">Definisce una curva lineare a tratti.</span><span class="sxs-lookup"><span data-stu-id="62740-125">Defines a piecewise linear curve.</span></span>    |
| <span data-ttu-id="62740-126">**NurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="62740-126">**nurbscurve**</span></span>   | [<span data-ttu-id="62740-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="62740-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="62740-128">Specifica gli attributi della curva di taglio.</span><span class="sxs-lookup"><span data-stu-id="62740-128">Specifies trimming-curve attributes.</span></span> |
| <span data-ttu-id="62740-129">**endtrim**</span><span class="sxs-lookup"><span data-stu-id="62740-129">**endtrim**</span></span>      | [<span data-ttu-id="62740-130">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="62740-130">**gluEndTrim**</span></span>](gluendtrim.md)       | <span data-ttu-id="62740-131">Termina la definizione della curva di taglio.</span><span class="sxs-lookup"><span data-stu-id="62740-131">Ends trimming-curve definition.</span></span>      |



 

<span data-ttu-id="62740-132">??</span><span class="sxs-lookup"><span data-stu-id="62740-132">??</span></span>

 

 




