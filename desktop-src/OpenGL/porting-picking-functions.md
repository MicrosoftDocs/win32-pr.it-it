---
title: Funzioni di selezione del porting
description: Tutte le funzioni di selezione di IRIS GL hanno equivalenti OpenGL, ad eccezione di clearhitcode. La tabella seguente elenca le funzioni di selezione di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Porting di IRIS GL, selezione
- porting da IRIS GL, selezione
- porting in OpenGL da IRIS GL, selezione
- Porting OpenGL da IRIS GL, selezione
- selezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298541"
---
# <a name="porting-picking-functions"></a><span data-ttu-id="0fa2e-109">Funzioni di selezione del porting</span><span class="sxs-lookup"><span data-stu-id="0fa2e-109">Porting Picking Functions</span></span>

<span data-ttu-id="0fa2e-110">Tutte le funzioni di selezione di IRIS GL hanno equivalenti OpenGL, ad eccezione di **clearhitcode**.</span><span class="sxs-lookup"><span data-stu-id="0fa2e-110">All IRIS GL picking functions have OpenGL equivalents, with the exception of **clearhitcode**.</span></span> <span data-ttu-id="0fa2e-111">La tabella seguente elenca le funzioni di selezione di IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="0fa2e-111">The following table lists the IRIS GL picking functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0fa2e-112">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="0fa2e-112">IRIS GL function</span></span>                | <span data-ttu-id="0fa2e-113">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="0fa2e-113">OpenGL function</span></span>                                                                           | <span data-ttu-id="0fa2e-114">Significato</span><span class="sxs-lookup"><span data-stu-id="0fa2e-114">Meaning</span></span>                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="0fa2e-115">**clearhitcode**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-115">**clearhitcode**</span></span>                | <span data-ttu-id="0fa2e-116">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="0fa2e-116">Not supported.</span></span>                                                                            | <span data-ttu-id="0fa2e-117">Cancella la variabile globale e hitcode.</span><span class="sxs-lookup"><span data-stu-id="0fa2e-117">Clears global variable and hitcode.</span></span>    |
| <span data-ttu-id="0fa2e-118">**pickselect**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-118">**pickselect**</span></span><br/>       | <span data-ttu-id="0fa2e-119">[**glRenderMode**](glrendermode.md) ( \_ selezione GL)</span><span class="sxs-lookup"><span data-stu-id="0fa2e-119">[**glRenderMode**](glrendermode.md) ( GL\_SELECT )</span></span>                                       | <span data-ttu-id="0fa2e-120">Passa alla modalità selezione o selezione.</span><span class="sxs-lookup"><span data-stu-id="0fa2e-120">Switches to selection or picking mode.</span></span> |
| <span data-ttu-id="0fa2e-121">**endpickendselect**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-121">**endpickendselect**</span></span><br/> | <span data-ttu-id="0fa2e-122">[**glRenderMode**](glrendermode.md) ( \_ rendering GL)</span><span class="sxs-lookup"><span data-stu-id="0fa2e-122">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )</span></span>                                       | <span data-ttu-id="0fa2e-123">Passa alla modalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="0fa2e-123">Switches to rendering mode.</span></span>            |
| <span data-ttu-id="0fa2e-124">**picksize**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-124">**picksize**</span></span>                    | <span data-ttu-id="0fa2e-125">[](glupickmatrix.md)[**glSelectBuffer** gluPickMatrix](glselectbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="0fa2e-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span></span><br/> | <span data-ttu-id="0fa2e-126">Imposta la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="0fa2e-126">Sets the return array.</span></span>                 |
| <span data-ttu-id="0fa2e-127">**initnames**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-127">**initnames**</span></span>                   | [<span data-ttu-id="0fa2e-128">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-128">**glInitNames**</span></span>](glinitnames.md)                                                        |                                        |
| <span data-ttu-id="0fa2e-129">**pushnamepopname**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-129">**pushnamepopname**</span></span><br/>  | <span data-ttu-id="0fa2e-130">[](glpushname.md)[**glPopName** glPushName](glpopname.md)</span><span class="sxs-lookup"><span data-stu-id="0fa2e-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span></span><br/>                 |                                        |
| <span data-ttu-id="0fa2e-131">**loadname**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-131">**loadname**</span></span>                    | [<span data-ttu-id="0fa2e-132">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="0fa2e-132">**glLoadName**</span></span>](glloadname.md)                                                          |                                        |



 

<span data-ttu-id="0fa2e-133">Per ulteriori informazioni sulla selezione, vedere [**gluPickMatrix**](glupickmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="0fa2e-133">For more information on picking, see [**gluPickMatrix**](glupickmatrix.md).</span></span>

 

 





