---
title: Porting di chiamate del piano stencil
description: In OpenGL è possibile allocare i piani dello stencil richiedendo il formato pixel appropriato con OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Porting di IRIS GL, piani stencil
- porting da IRIS GL, piani stencil
- porting in OpenGL da IRIS GL, piani stencil
- Porting OpenGL da IRIS GL, piani stencil
- piani stencil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330999"
---
# <a name="porting-stencil-plane-calls"></a><span data-ttu-id="e3266-108">Porting di chiamate del piano stencil</span><span class="sxs-lookup"><span data-stu-id="e3266-108">Porting Stencil Plane Calls</span></span>

<span data-ttu-id="e3266-109">In OpenGL è possibile allocare i piani dello stencil richiedendo il formato pixel appropriato con OpenGL **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="e3266-109">In OpenGL, you allocate stencil planes by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span> <span data-ttu-id="e3266-110">funzioni.</span><span class="sxs-lookup"><span data-stu-id="e3266-110">functions.</span></span> <span data-ttu-id="e3266-111">La tabella seguente elenca le funzioni di IRIS GL che interessano i piani degli stencil e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="e3266-111">The following table lists IRIS GL functions that affect the stencil planes and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="e3266-112">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="e3266-112">IRIS GL function</span></span>             | <span data-ttu-id="e3266-113">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="e3266-113">OpenGL function</span></span>                                         | <span data-ttu-id="e3266-114">Significato</span><span class="sxs-lookup"><span data-stu-id="e3266-114">Meaning</span></span>                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e3266-115">**stensize**</span><span class="sxs-lookup"><span data-stu-id="e3266-115">**stensize**</span></span>                 | <span data-ttu-id="e3266-116">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="e3266-116">**ChoosePixelFormat**</span></span>                                   |                                                        |
| <span data-ttu-id="e3266-117">**stencil**( **true**,...)</span><span class="sxs-lookup"><span data-stu-id="e3266-117">**stencil**( **TRUE**, ... )</span></span> | <span data-ttu-id="e3266-118">[**glEnable**](glenable.md) ( \_ test di stencil GL \_ )</span><span class="sxs-lookup"><span data-stu-id="e3266-118">[**glEnable**](glenable.md) ( GL\_STENCIL\_TEST )</span></span>      | <span data-ttu-id="e3266-119">Abilita i test di stencil.</span><span class="sxs-lookup"><span data-stu-id="e3266-119">Enables stencil tests.</span></span>                                 |
| <span data-ttu-id="e3266-120">**stencil**</span><span class="sxs-lookup"><span data-stu-id="e3266-120">**stencil**</span></span>                  | [<span data-ttu-id="e3266-121">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="e3266-121">**glStencilOp**</span></span>](glstencilop.md)                      | <span data-ttu-id="e3266-122">Imposta le azioni di test dello stencil.</span><span class="sxs-lookup"><span data-stu-id="e3266-122">Sets stencil test actions.</span></span>                             |
| <span data-ttu-id="e3266-123">**stencil**(... Func,...)</span><span class="sxs-lookup"><span data-stu-id="e3266-123">**stencil**(... func, ... )</span></span>  | [<span data-ttu-id="e3266-124">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="e3266-124">**glStencilFunc**</span></span>](glstencilfunc.md)                  | <span data-ttu-id="e3266-125">Imposta la funzione e il valore di riferimento per il test di stencil.</span><span class="sxs-lookup"><span data-stu-id="e3266-125">Sets function and reference value for stencil testing.</span></span> |
| <span data-ttu-id="e3266-126">**swritemask**</span><span class="sxs-lookup"><span data-stu-id="e3266-126">**swritemask**</span></span>               | [<span data-ttu-id="e3266-127">**glStencilMask**</span><span class="sxs-lookup"><span data-stu-id="e3266-127">**glStencilMask**</span></span>](glstencilmask.md)                  | <span data-ttu-id="e3266-128">Specifica quali bit di stencil è possibile scrivere.</span><span class="sxs-lookup"><span data-stu-id="e3266-128">Specifies which stencil bits can be written.</span></span>           |
|                              | [<span data-ttu-id="e3266-129">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="e3266-129">**glClearStencil**</span></span>](glclearstencil.md)                | <span data-ttu-id="e3266-130">Specifica il valore Clear per il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="e3266-130">Specifies the clear value for the stencil buffer.</span></span>      |
| <span data-ttu-id="e3266-131">**sclear**</span><span class="sxs-lookup"><span data-stu-id="e3266-131">**sclear**</span></span>                   | <span data-ttu-id="e3266-132">[**glClear**](glclear.md) ( \_ bit del buffer dello stencil GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="e3266-132">[**glClear**](glclear.md) ( GL\_STENCIL\_BUFFER\_BIT )</span></span> |                                                        |



 

<span data-ttu-id="e3266-133">Le funzioni di confronto stencil e le operazioni di passaggio/errore stencil sono quasi equivalenti in OpenGL e IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="e3266-133">Stencil-comparison functions and stencil pass/fail operations are nearly equivalent in OpenGL and IRIS GL.</span></span> <span data-ttu-id="e3266-134">I flag di funzione dello stencil GL di IRIS sono preceduti da SF; flag OpenGL con GL.</span><span class="sxs-lookup"><span data-stu-id="e3266-134">The IRIS GL stencil-function flags are prefaced with SF; the OpenGL flags with GL.</span></span> <span data-ttu-id="e3266-135">I flag di operazione di superamento/errore di IRIS GL sono preceduti da ST; flag OpenGL con GL.</span><span class="sxs-lookup"><span data-stu-id="e3266-135">IRIS GL pass/fail operation flags are prefaced with ST; the OpenGL flags with GL.</span></span>

 

 




