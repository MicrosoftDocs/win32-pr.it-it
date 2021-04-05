---
title: Porting di piani di ritaglio
description: OpenGL implementa i piani di ritaglio in modo analogo a IRIS GL. In OpenGL è inoltre possibile eseguire query sui piani di ritaglio. La tabella seguente elenca le funzioni del piano di ritaglio di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Porting di IRIS GL, piani di ritaglio
- porting da IRIS GL, piani di ritaglio
- porting in OpenGL da IRIS GL, piani di ritaglio
- Porting OpenGL da IRIS GL, piani di ritaglio
- ritaglio di piani
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713582"
---
# <a name="porting-clipping-planes"></a><span data-ttu-id="96c06-110">Porting di piani di ritaglio</span><span class="sxs-lookup"><span data-stu-id="96c06-110">Porting Clipping Planes</span></span>

<span data-ttu-id="96c06-111">OpenGL implementa i piani di ritaglio in modo analogo a IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="96c06-111">OpenGL implements clipping planes similarly to IRIS GL.</span></span> <span data-ttu-id="96c06-112">In OpenGL è inoltre possibile eseguire query sui piani di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="96c06-112">In addition, in OpenGL you can query clipping planes.</span></span> <span data-ttu-id="96c06-113">La tabella seguente elenca le funzioni del piano di ritaglio di IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="96c06-113">The following table lists IRIS GL clipping plane functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="96c06-114">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="96c06-114">IRIS GL function</span></span>                          | <span data-ttu-id="96c06-115">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="96c06-115">OpenGL function</span></span>                                                                               | <span data-ttu-id="96c06-116">Significato</span><span class="sxs-lookup"><span data-stu-id="96c06-116">Meaning</span></span>                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="96c06-117">**clipplane** (i, **CP \_ on**, params)</span><span class="sxs-lookup"><span data-stu-id="96c06-117">**clipplane** (i, **CP\_ON**, params)</span></span>     | <span data-ttu-id="96c06-118">[**glEnable**](glenable.md) (GL \_ clip \_ planei)</span><span class="sxs-lookup"><span data-stu-id="96c06-118">[**glEnable**](glenable.md) ( GL\_CLIP\_PLANEi )</span></span>                                             | <span data-ttu-id="96c06-119">Abilita il ritaglio sul piano i.</span><span class="sxs-lookup"><span data-stu-id="96c06-119">Enables clipping on plane i.</span></span>             |
| <span data-ttu-id="96c06-120">**clipplane**(i, **CP \_ define**, Plane)</span><span class="sxs-lookup"><span data-stu-id="96c06-120">**clipplane**( i, **CP\_DEFINE**, plane )</span></span> | <span data-ttu-id="96c06-121">[**glClipPlane**](glclipplane.md) (GL \_ clip \_ Planes, Plane)</span><span class="sxs-lookup"><span data-stu-id="96c06-121">[**glClipPlane**](glclipplane.md) ( GL\_CLIP\_PLANEi, plane )</span></span>                                | <span data-ttu-id="96c06-122">Definisce il piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="96c06-122">Defines clipping plane.</span></span>                  |
|                                           | [<span data-ttu-id="96c06-123">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="96c06-123">**glGetClipPlane**</span></span>](glgetclipplane.md)                                                      | <span data-ttu-id="96c06-124">Restituisce l'equazione del piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="96c06-124">Returns clipping plane equation.</span></span>         |
|                                           | <span data-ttu-id="96c06-125">[**glIsEnabled**](glisenabled.md) (GL \_ clip \_ planei)</span><span class="sxs-lookup"><span data-stu-id="96c06-125">[**glIsEnabled**](glisenabled.md) ( GL\_CLIP\_PLANEi )</span></span>                                       | <span data-ttu-id="96c06-126">Restituisce true se il piano di ritaglio i è abilitato.</span><span class="sxs-lookup"><span data-stu-id="96c06-126">Returns true if clip plane i is enabled.</span></span> |
| <span data-ttu-id="96c06-127">**scrmask**</span><span class="sxs-lookup"><span data-stu-id="96c06-127">**scrmask**</span></span>                               | [<span data-ttu-id="96c06-128">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="96c06-128">**glScissor**</span></span>](glscissor.md)                                                                | <span data-ttu-id="96c06-129">Definisce la casella a forbice.</span><span class="sxs-lookup"><span data-stu-id="96c06-129">Defines the scissor box.</span></span>                 |
| <span data-ttu-id="96c06-130">**getscrmask**</span><span class="sxs-lookup"><span data-stu-id="96c06-130">**getscrmask**</span></span>                            | <span data-ttu-id="96c06-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ casella GL Scissor \_ )</span><span class="sxs-lookup"><span data-stu-id="96c06-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_SCISSOR\_BOX )</span></span> | <span data-ttu-id="96c06-132">Restituisce la casella a forbice corrente.</span><span class="sxs-lookup"><span data-stu-id="96c06-132">Returns the current scissor box.</span></span>         |



 

<span data-ttu-id="96c06-133">Per attivare il test a forbice, chiamare **glEnable** usando \_ \_ la casella della forbice GL come parametro.</span><span class="sxs-lookup"><span data-stu-id="96c06-133">To turn on the scissor test, call **glEnable** using GL\_SCISSOR\_BOX as the parameter.</span></span>

<span data-ttu-id="96c06-134">??</span><span class="sxs-lookup"><span data-stu-id="96c06-134">??</span></span>

 

 




