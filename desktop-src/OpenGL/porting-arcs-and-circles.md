---
title: Porting di archi e cerchi
description: Con OpenGL, gli archi e i cerchi pieni vengono disegnati con le stesse chiamate degli archi e dei cerchi non riempiti. La tabella seguente elenca le funzioni di arco e cerchio IRIS GL e le relative funzioni OpenGL (GLU) equivalenti.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Porting di IRIS GL, archi
- porting da IRIS GL, archi
- porting in OpenGL da IRIS GL, archi
- Porting OpenGL da IRIS GL, archi
- funzioni di disegno, archi
- Porting di IRIS GL, cerchi
- porting da IRIS GL, cerchi
- porting in OpenGL da IRIS GL, cerchi
- Porting OpenGL da IRIS GL, cerchi
- disegno di funzioni, cerchi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396834"
---
# <a name="porting-arcs-and-circles"></a><span data-ttu-id="f4f83-114">Porting di archi e cerchi</span><span class="sxs-lookup"><span data-stu-id="f4f83-114">Porting Arcs and Circles</span></span>

<span data-ttu-id="f4f83-115">Con OpenGL, gli archi e i cerchi pieni vengono disegnati con le stesse chiamate degli archi e dei cerchi non riempiti.</span><span class="sxs-lookup"><span data-stu-id="f4f83-115">With OpenGL, filled arcs and circles are drawn with the same calls as unfilled arcs and circles.</span></span> <span data-ttu-id="f4f83-116">La tabella seguente elenca le funzioni di arco e cerchio IRIS GL e le relative funzioni OpenGL (GLU) equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f4f83-116">The following table lists the IRIS GL arc and circle functions and their equivalent OpenGL (GLU) functions.</span></span>



| <span data-ttu-id="f4f83-117">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="f4f83-117">IRIS GL function</span></span> | <span data-ttu-id="f4f83-118">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4f83-118">OpenGL function</span></span>                          | <span data-ttu-id="f4f83-119">Significato</span><span class="sxs-lookup"><span data-stu-id="f4f83-119">Meaning</span></span>                 |
|------------------|------------------------------------------|-------------------------|
| <span data-ttu-id="f4f83-120">**arcarcf**</span><span class="sxs-lookup"><span data-stu-id="f4f83-120">**arcarcf**</span></span>      | [<span data-ttu-id="f4f83-121">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="f4f83-121">**gluPartialDisk**</span></span>](glupartialdisk.md) | <span data-ttu-id="f4f83-122">Disegna un arco.</span><span class="sxs-lookup"><span data-stu-id="f4f83-122">Draws an arc.</span></span>           |
| <span data-ttu-id="f4f83-123">**circcircf**</span><span class="sxs-lookup"><span data-stu-id="f4f83-123">**circcircf**</span></span>    | [<span data-ttu-id="f4f83-124">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="f4f83-124">**gluDisk**</span></span>](gludisk.md)               | <span data-ttu-id="f4f83-125">Disegna un cerchio o un disco.</span><span class="sxs-lookup"><span data-stu-id="f4f83-125">Draws a circle or disk.</span></span> |



 

<span data-ttu-id="f4f83-126">È possibile eseguire alcune operazioni con archi e cerchi OpenGL che non possono essere eseguite con IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="f4f83-126">You can do some things with OpenGL arcs and circles that you can't do with IRIS GL.</span></span> <span data-ttu-id="f4f83-127">OpenGL chiama archi e cerchi, dischi e dischi parziali rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="f4f83-127">OpenGL calls arcs and circles, disks and partial disks respectively.</span></span>

<span data-ttu-id="f4f83-128">Quando si portano archi e cerchi, tenere presenti i seguenti aspetti di OpenGL:</span><span class="sxs-lookup"><span data-stu-id="f4f83-128">When porting arcs and circles, keep the following points about OpenGL in mind:</span></span>

-   <span data-ttu-id="f4f83-129">Gli angoli sono misurati in gradi e non in decimi di gradi.</span><span class="sxs-lookup"><span data-stu-id="f4f83-129">Angles are measured in degrees, and not in tenths of degrees.</span></span>
-   <span data-ttu-id="f4f83-130">L'angolo iniziale viene misurato dall'asse y positivo e non dall'asse x.</span><span class="sxs-lookup"><span data-stu-id="f4f83-130">The start angle is measured from the positive y-axis, and not from the x-axis.</span></span>
-   <span data-ttu-id="f4f83-131">L'angolo di sweep è ora in senso orario anziché in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="f4f83-131">The sweep angle is now clockwise instead of counterclockwise.</span></span>

<span data-ttu-id="f4f83-132">??</span><span class="sxs-lookup"><span data-stu-id="f4f83-132">??</span></span>

 

 




