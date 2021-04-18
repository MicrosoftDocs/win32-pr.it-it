---
title: Porting del codice di fusione
description: In IRIS GL, quando si disegnano i buffer di primo e indietro, la fusione viene eseguita leggendo uno dei buffer, combinando con tale colore e quindi scrivendo il risultato in entrambi i buffer. In OpenGL, tuttavia, ogni buffer viene letto a sua volta, mescolato e quindi scritto.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Porting di IRIS GL, fusione
- porting da IRIS GL, blending
- porting in OpenGL da IRIS GL, blending
- Porting OpenGL da IRIS GL, blending
- sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298729"
---
# <a name="porting-blending-code"></a><span data-ttu-id="1bc95-109">Porting del codice di fusione</span><span class="sxs-lookup"><span data-stu-id="1bc95-109">Porting Blending Code</span></span>

<span data-ttu-id="1bc95-110">In IRIS GL, quando si disegnano i buffer di primo e indietro, la fusione viene eseguita leggendo uno dei buffer, combinando con tale colore e quindi scrivendo il risultato in entrambi i buffer.</span><span class="sxs-lookup"><span data-stu-id="1bc95-110">In IRIS GL, when drawing to both front and back buffers, blending is done by reading one of the buffers, blending with that color, and then writing the result to both buffers.</span></span> <span data-ttu-id="1bc95-111">In OpenGL, tuttavia, ogni buffer viene letto a sua volta, mescolato e quindi scritto.</span><span class="sxs-lookup"><span data-stu-id="1bc95-111">In OpenGL, however, each buffer is read in turn, blended, and then written.</span></span>

<span data-ttu-id="1bc95-112">La tabella seguente elenca le funzioni di blending IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="1bc95-112">The following table lists IRIS GL blending functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="1bc95-113">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="1bc95-113">IRIS GL function</span></span>  | <span data-ttu-id="1bc95-114">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="1bc95-114">OpenGL function</span></span>                            | <span data-ttu-id="1bc95-115">Significato</span><span class="sxs-lookup"><span data-stu-id="1bc95-115">Meaning</span></span>                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | <span data-ttu-id="1bc95-116">[**glEnable**](glenable.md) (GL \_ Blend)</span><span class="sxs-lookup"><span data-stu-id="1bc95-116">[**glEnable**](glenable.md) ( GL\_BLEND )</span></span> | <span data-ttu-id="1bc95-117">Attiva la fusione.</span><span class="sxs-lookup"><span data-stu-id="1bc95-117">Turns on blending.</span></span>          |
| <span data-ttu-id="1bc95-118">**BlendFunction**</span><span class="sxs-lookup"><span data-stu-id="1bc95-118">**blendfunction**</span></span> | [<span data-ttu-id="1bc95-119">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="1bc95-119">**glBlendFunc**</span></span>](glblendfunc.md)         | <span data-ttu-id="1bc95-120">Specifica una funzione Blend.</span><span class="sxs-lookup"><span data-stu-id="1bc95-120">Specifies a blend function.</span></span> |



 

<span data-ttu-id="1bc95-121">La funzione **glBlendFunc** di OpenGL e la funzione **BlendFunction** di Iris GL sono quasi identiche.</span><span class="sxs-lookup"><span data-stu-id="1bc95-121">The OpenGL **glBlendFunc** function and the IRIS GL **blendfunction** function are almost identical.</span></span> <span data-ttu-id="1bc95-122">La tabella seguente elenca i fattori di Blend di IRIS GL e i rispettivi equivalenti OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1bc95-122">The following table lists IRIS GL blend factors and their OpenGL equivalents.</span></span>



| <span data-ttu-id="1bc95-123">GL IRIS</span><span class="sxs-lookup"><span data-stu-id="1bc95-123">IRIS GL</span></span>          | <span data-ttu-id="1bc95-124">OpenGL</span><span class="sxs-lookup"><span data-stu-id="1bc95-124">OpenGL</span></span>                     | <span data-ttu-id="1bc95-125">Note</span><span class="sxs-lookup"><span data-stu-id="1bc95-125">Notes</span></span>             |
|------------------|----------------------------|-------------------|
| <span data-ttu-id="1bc95-126">BF \_ zero</span><span class="sxs-lookup"><span data-stu-id="1bc95-126">BF\_ZERO</span></span>         | <span data-ttu-id="1bc95-127">\_zero GL</span><span class="sxs-lookup"><span data-stu-id="1bc95-127">GL\_ZERO</span></span>                   |                   |
| <span data-ttu-id="1bc95-128">BF \_ uno</span><span class="sxs-lookup"><span data-stu-id="1bc95-128">BF\_ONE</span></span>          | <span data-ttu-id="1bc95-129">GL \_ uno</span><span class="sxs-lookup"><span data-stu-id="1bc95-129">GL\_ONE</span></span>                    |                   |
| <span data-ttu-id="1bc95-130">\_sa BF</span><span class="sxs-lookup"><span data-stu-id="1bc95-130">BF\_SA</span></span>           | <span data-ttu-id="1bc95-131">\_alfa src \_ GL</span><span class="sxs-lookup"><span data-stu-id="1bc95-131">GL\_SRC\_ALPHA</span></span>             |                   |
| <span data-ttu-id="1bc95-132">MSA di BF \_</span><span class="sxs-lookup"><span data-stu-id="1bc95-132">BF\_MSA</span></span>          | <span data-ttu-id="1bc95-133">GL \_ 1 \_ meno \_ src \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="1bc95-133">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> |                   |
| <span data-ttu-id="1bc95-134">BF \_ da</span><span class="sxs-lookup"><span data-stu-id="1bc95-134">BF\_DA</span></span>           | <span data-ttu-id="1bc95-135">\_alfa del DST GL \_</span><span class="sxs-lookup"><span data-stu-id="1bc95-135">GL\_DST\_ALPHA</span></span>             |                   |
| <span data-ttu-id="1bc95-136">\_MDA BF</span><span class="sxs-lookup"><span data-stu-id="1bc95-136">BF\_MDA</span></span>          | <span data-ttu-id="1bc95-137">GL \_ 1 \_ meno \_ DST \_ Alpha</span><span class="sxs-lookup"><span data-stu-id="1bc95-137">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> |                   |
| <span data-ttu-id="1bc95-138">BF \_ SC</span><span class="sxs-lookup"><span data-stu-id="1bc95-138">BF\_SC</span></span>           | <span data-ttu-id="1bc95-139">\_colore GL src \_</span><span class="sxs-lookup"><span data-stu-id="1bc95-139">GL\_SRC\_COLOR</span></span>             |                   |
| <span data-ttu-id="1bc95-140">BF \_ MSC</span><span class="sxs-lookup"><span data-stu-id="1bc95-140">BF\_MSC</span></span>          | <span data-ttu-id="1bc95-141">GL \_ uno \_ meno \_ il \_ colore src</span><span class="sxs-lookup"><span data-stu-id="1bc95-141">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="1bc95-142">Solo destinazione.</span><span class="sxs-lookup"><span data-stu-id="1bc95-142">Destination only.</span></span> |
| <span data-ttu-id="1bc95-143">\_DC BF</span><span class="sxs-lookup"><span data-stu-id="1bc95-143">BF\_DC</span></span>           | <span data-ttu-id="1bc95-144">\_colore GL DST \_</span><span class="sxs-lookup"><span data-stu-id="1bc95-144">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="1bc95-145">Solo origine.</span><span class="sxs-lookup"><span data-stu-id="1bc95-145">Source only.</span></span>      |
| <span data-ttu-id="1bc95-146">BF \_ MDC</span><span class="sxs-lookup"><span data-stu-id="1bc95-146">BF\_MDC</span></span>          | <span data-ttu-id="1bc95-147">GL \_ uno \_ meno \_ il \_ colore DST</span><span class="sxs-lookup"><span data-stu-id="1bc95-147">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="1bc95-148">Solo origine.</span><span class="sxs-lookup"><span data-stu-id="1bc95-148">Source only.</span></span>      |
| <span data-ttu-id="1bc95-149">\_Assistente al \_ \_ debug gestito min BF</span><span class="sxs-lookup"><span data-stu-id="1bc95-149">BF\_MIN\_SA\_MDA</span></span> | <span data-ttu-id="1bc95-150">\_ \_ satura Alpha di GL src \_</span><span class="sxs-lookup"><span data-stu-id="1bc95-150">GL\_SRC\_ALPHA\_SATURATE</span></span>   |                   |



 

<span data-ttu-id="1bc95-151">??</span><span class="sxs-lookup"><span data-stu-id="1bc95-151">??</span></span>

 

 




