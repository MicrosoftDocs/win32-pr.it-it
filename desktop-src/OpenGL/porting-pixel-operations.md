---
title: Porting di operazioni pixel
description: Porting di operazioni pixel
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Porting di IRIS GL, pixel
- porting da IRIS GL, pixel
- porting in OpenGL da IRIS GL, pixel
- Porting OpenGL da IRIS GL, pixel
- pixel, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712508"
---
# <a name="porting-pixel-operations"></a><span data-ttu-id="4674d-108">Porting di operazioni pixel</span><span class="sxs-lookup"><span data-stu-id="4674d-108">Porting Pixel Operations</span></span>

<span data-ttu-id="4674d-109">Quando si esegue il porting di codice che coinvolge operazioni in pixel, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="4674d-109">When porting code that involves pixel operations, keep the following points in mind:</span></span>

-   <span data-ttu-id="4674d-110">Le operazioni di pixel logici non vengono applicate ai buffer dei colori RGBA.</span><span class="sxs-lookup"><span data-stu-id="4674d-110">Logical pixel operations are not applied to RGBA color buffers.</span></span> <span data-ttu-id="4674d-111">Per ulteriori informazioni, vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="4674d-111">For more information, see [**glLogicOp**](gllogicop.md).</span></span>
-   <span data-ttu-id="4674d-112">In generale, IRIS GL usa il formato ABGR per pixel, mentre OpenGL USA RGBA.</span><span class="sxs-lookup"><span data-stu-id="4674d-112">In general, IRIS GL uses the format ABGR for pixels, whereas OpenGL uses RGBA.</span></span> <span data-ttu-id="4674d-113">È possibile modificare il formato con [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="4674d-113">You can change the format with [**glPixelStore**](glpixelstore-functions.md).</span></span>
-   <span data-ttu-id="4674d-114">Quando si esegue il porting delle funzioni **lrectwrite** , prestare attenzione a prendere nota del percorso di scrittura di **lrectwrite** (ad esempio, potrebbe scrivere nel buffer di profondità).</span><span class="sxs-lookup"><span data-stu-id="4674d-114">When porting **lrectwrite** functions, be careful to note where **lrectwrite** is writing (for example, it could be writing to the depth buffer).</span></span>

<span data-ttu-id="4674d-115">OpenGL offre una maggiore flessibilità nelle operazioni pixel.</span><span class="sxs-lookup"><span data-stu-id="4674d-115">OpenGL gives you some additional flexibility in pixel operations.</span></span> <span data-ttu-id="4674d-116">La tabella seguente elenca le funzioni di IRIS GL per le operazioni pixel e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="4674d-116">The following table lists IRIS GL functions for pixel operations and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="4674d-117">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="4674d-117">IRIS GL function</span></span>                                   | <span data-ttu-id="4674d-118">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="4674d-118">OpenGL function</span></span>                                                                           | <span data-ttu-id="4674d-119">Significato</span><span class="sxs-lookup"><span data-stu-id="4674d-119">Meaning</span></span>                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4674d-120">**lrectread**, **rectread**,**readRGB**</span><span class="sxs-lookup"><span data-stu-id="4674d-120">**lrectread**, **rectread**,**readRGB**</span></span><br/> | [<span data-ttu-id="4674d-121">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="4674d-121">**glReadPixels**</span></span>](glreadpixels.md)                                                      | <span data-ttu-id="4674d-122">Legge un blocco di pixel dal framebuffer.</span><span class="sxs-lookup"><span data-stu-id="4674d-122">Reads a block of pixels from the framebuffer.</span></span>                           |
| <span data-ttu-id="4674d-123">**lrectwrite**, **rectwrite**</span><span class="sxs-lookup"><span data-stu-id="4674d-123">**lrectwrite**, **rectwrite**</span></span>                      | [<span data-ttu-id="4674d-124">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="4674d-124">**glDrawPixels**</span></span>](gldrawpixels.md)                                                      | <span data-ttu-id="4674d-125">Scrive un blocco di pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="4674d-125">Writes a block of pixels to the framebuffer.</span></span>                            |
| <span data-ttu-id="4674d-126">**rectcopy**</span><span class="sxs-lookup"><span data-stu-id="4674d-126">**rectcopy**</span></span>                                       | [<span data-ttu-id="4674d-127">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="4674d-127">**glCopyPixels**</span></span>](glcopypixels.md)                                                      | <span data-ttu-id="4674d-128">Copia i pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="4674d-128">Copies pixels in the framebuffer.</span></span>                                       |
| <span data-ttu-id="4674d-129">**rectzoom**</span><span class="sxs-lookup"><span data-stu-id="4674d-129">**rectzoom**</span></span>                                       | [<span data-ttu-id="4674d-130">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="4674d-130">**glPixelZoom**</span></span>](glpixelzoom.md)                                                        | <span data-ttu-id="4674d-131">Specifica i fattori di zoom pixel per **glDrawPixels** e **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="4674d-131">Specifies pixel zoom factors for **glDrawPixels** and **glCopyPixels**.</span></span> |
| <span data-ttu-id="4674d-132">**CMOV**</span><span class="sxs-lookup"><span data-stu-id="4674d-132">**cmov**</span></span>                                           | [<span data-ttu-id="4674d-133">glRasterPos</span><span class="sxs-lookup"><span data-stu-id="4674d-133">glRasterPos</span></span>](glrasterpos-functions.md)                                                  | <span data-ttu-id="4674d-134">Specifica la posizione raster per le operazioni pixel.</span><span class="sxs-lookup"><span data-stu-id="4674d-134">Specifies raster position for pixel operations.</span></span>                         |
| <span data-ttu-id="4674d-135">**readsource**</span><span class="sxs-lookup"><span data-stu-id="4674d-135">**readsource**</span></span>                                     | [<span data-ttu-id="4674d-136">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="4674d-136">**glReadBuffer**</span></span>](glreadbuffer.md)                                                      | <span data-ttu-id="4674d-137">Consente di selezionare un'origine del buffer dei colori per i pixel.</span><span class="sxs-lookup"><span data-stu-id="4674d-137">Selects a color buffer source for pixels.</span></span>                               |
| <span data-ttu-id="4674d-138">**pixmode**</span><span class="sxs-lookup"><span data-stu-id="4674d-138">**pixmode**</span></span>                                        | <span data-ttu-id="4674d-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span><span class="sxs-lookup"><span data-stu-id="4674d-139">[**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md)</span></span> | <span data-ttu-id="4674d-140">Imposta le modalità di archiviazione pixel. Impostare le modalità di trasferimento pixel.</span><span class="sxs-lookup"><span data-stu-id="4674d-140">Sets pixel storage modes.Set pixel transfer modes.</span></span>                      |
| <span data-ttu-id="4674d-141">**logicop**</span><span class="sxs-lookup"><span data-stu-id="4674d-141">**logicop**</span></span>                                        | [<span data-ttu-id="4674d-142">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="4674d-142">**glLogicOp**</span></span>](gllogicop.md)                                                            | <span data-ttu-id="4674d-143">Specifica un'operazione logica per le Scritture in pixel.</span><span class="sxs-lookup"><span data-stu-id="4674d-143">Specifies a logical operation for pixel writes.</span></span>                         |
|                                                    | <span data-ttu-id="4674d-144">[**glEnable**](glenable.md) ( \_ op logica GL \_ )</span><span class="sxs-lookup"><span data-stu-id="4674d-144">[**glEnable**](glenable.md) ( GL\_LOGIC\_OP )</span></span>                                            | <span data-ttu-id="4674d-145">Attiva le operazioni della logica pixel.</span><span class="sxs-lookup"><span data-stu-id="4674d-145">Turns on pixel logic operations.</span></span>                                        |



 

<span data-ttu-id="4674d-146">Per un elenco completo delle possibili operazioni logiche, vedere [**glLogicOp**](gllogicop.md).</span><span class="sxs-lookup"><span data-stu-id="4674d-146">For a complete list of possible logical operations, see [**glLogicOp**](gllogicop.md).</span></span>

<span data-ttu-id="4674d-147">Questo esempio di codice IRIS GL Mostra una tipica scrittura in pixel:</span><span class="sxs-lookup"><span data-stu-id="4674d-147">This IRIS GL code sample shows a typical pixel write:</span></span>

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

<span data-ttu-id="4674d-148">Il codice precedente ha un aspetto simile al seguente quando viene convertito in OpenGL:</span><span class="sxs-lookup"><span data-stu-id="4674d-148">The preceding code looks like this when translated to OpenGL:</span></span>

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





