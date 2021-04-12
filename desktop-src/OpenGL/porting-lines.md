---
title: Linee di porting
description: Il porting di codice IRIS GL che disegna linee è piuttosto semplice, anche se è opportuno notare le differenze nel modo in cui OpenGL stipples. La tabella seguente elenca le funzioni di IRIS GL per le linee di disegno e le relative funzioni OpenGL equivalenti.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Porting di IRIS GL, righe
- porting da IRIS GL, righe
- porting in OpenGL da IRIS GL, righe
- Porting OpenGL da IRIS GL, righe
- disegno di funzioni, righe
- lines
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c97593d0230d6830cf3d3ce8fa2c13466e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221821"
---
# <a name="porting-lines"></a><span data-ttu-id="f1dc3-110">Linee di porting</span><span class="sxs-lookup"><span data-stu-id="f1dc3-110">Porting Lines</span></span>

<span data-ttu-id="f1dc3-111">Il porting di codice IRIS GL che disegna linee è piuttosto semplice, anche se è opportuno notare le differenze nel modo in cui OpenGL stipples.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-111">Porting IRIS GL code that draws lines is fairly straightforward, though you should note the differences in the way OpenGL stipples.</span></span> <span data-ttu-id="f1dc3-112">La tabella seguente elenca le funzioni di IRIS GL per le linee di disegno e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-112">The following table lists IRIS GL functions for drawing lines and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="f1dc3-113">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="f1dc3-113">IRIS GL function</span></span>                               | <span data-ttu-id="f1dc3-114">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="f1dc3-114">OpenGL function</span></span>                                                                                         | <span data-ttu-id="f1dc3-115">Significato</span><span class="sxs-lookup"><span data-stu-id="f1dc3-115">Meaning</span></span>                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1dc3-116">**bgnclosedline**,**endclosedline**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-116">**bgnclosedline**,**endclosedline**</span></span><br/> | <span data-ttu-id="f1dc3-117">[**glBegin**](glbegin.md) ( \_ ciclo linea GL \_ )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="f1dc3-117">[**glBegin**](glbegin.md) ( GL\_LINE\_LOOP )[**glEnd**](glend.md)</span></span><br/>                          | <span data-ttu-id="f1dc3-118">Disegna una linea chiusa.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-118">Draws a closed line.</span></span>                                                                                                                         |
| <span data-ttu-id="f1dc3-119">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-119">**bgnline**</span></span>                                    | <span data-ttu-id="f1dc3-120">[**glBegin**](glbegin.md) ( \_ striscia di riga GL \_ )</span><span class="sxs-lookup"><span data-stu-id="f1dc3-120">[**glBegin**](glbegin.md) ( GL\_LINE\_STRIP )</span></span>                                                          | <span data-ttu-id="f1dc3-121">Disegna segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-121">Draws line segments.</span></span>                                                                                                                         |
| <span data-ttu-id="f1dc3-122">**LineWidth**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-122">**linewidth**</span></span>                                  | [<span data-ttu-id="f1dc3-123">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-123">**glLineWidth**</span></span>](gllinewidth.md)                                                                      | <span data-ttu-id="f1dc3-124">Imposta la lunghezza riga.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-124">Sets line width.</span></span>                                                                                                                             |
| <span data-ttu-id="f1dc3-125">**getlwidth**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-125">**getlwidth**</span></span>                                  | <span data-ttu-id="f1dc3-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ lunghezza riga GL \_ )</span><span class="sxs-lookup"><span data-stu-id="f1dc3-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_WIDTH )</span></span>            | <span data-ttu-id="f1dc3-127">Restituisce la lunghezza della riga corrente.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-127">Returns current line width.</span></span>                                                                                                                  |
| <span data-ttu-id="f1dc3-128">**deflinestyle**,**setlinestyle**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-128">**deflinestyle**,**setlinestyle**</span></span><br/>   | [<span data-ttu-id="f1dc3-129">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-129">**glLineStipple**</span></span>](gllinestipple.md)                                                                  | <span data-ttu-id="f1dc3-130">Specifica un modello di stipple di linea.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-130">Specifies a line stipple pattern.</span></span>                                                                                                            |
| <span data-ttu-id="f1dc3-131">**lsrepeat**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-131">**lsrepeat**</span></span>                                   | <span data-ttu-id="f1dc3-132">argomento factor di **glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-132">factor argument of **glLineStipple**</span></span>                                                                    | <span data-ttu-id="f1dc3-133">Imposta un fattore di ripetizione per lo stile di linea.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-133">Sets a repeat factor for the line style.</span></span>                                                                                                     |
| <span data-ttu-id="f1dc3-134">**getlstyle**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-134">**getlstyle**</span></span>                                  | <span data-ttu-id="f1dc3-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modello di \_ stipple linea GL \_ )</span><span class="sxs-lookup"><span data-stu-id="f1dc3-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_PATTERN )</span></span> | <span data-ttu-id="f1dc3-136">Restituisce il pattern stipple della riga.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-136">Returns line stipple pattern.</span></span>                                                                                                                |
| <span data-ttu-id="f1dc3-137">**getlsrepeat**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-137">**getlsrepeat**</span></span>                                | <span data-ttu-id="f1dc3-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ riga GL \_ stipple \_ ripetizione)</span><span class="sxs-lookup"><span data-stu-id="f1dc3-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_LINE\_STIPPLE\_REPEAT )</span></span>  | <span data-ttu-id="f1dc3-139">Restituisce il fattore di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-139">Returns repeat factor.</span></span>                                                                                                                       |
| <span data-ttu-id="f1dc3-140">**linesmooth**, **a linee smussate**</span><span class="sxs-lookup"><span data-stu-id="f1dc3-140">**linesmooth**, **smoothline**</span></span>                 | <span data-ttu-id="f1dc3-141">[**glEnable**](glenable.md) ( \_ linea GL \_ smussata)</span><span class="sxs-lookup"><span data-stu-id="f1dc3-141">[**glEnable**](glenable.md) ( GL\_LINE\_SMOOTH )</span></span>                                                       | <span data-ttu-id="f1dc3-142">Attiva l'anti-aliasing della riga. per ulteriori informazioni sull'anti-aliasing, vedere [porting anti-aliasing Functions](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f1dc3-142">Turns on line antialiasing (For more information on antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="f1dc3-143">OpenGL non usa le tabelle per la riga stipples; mantiene solo un modello line-stipple.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-143">OpenGL doesn't use tables for line stipples; it maintains only one line-stipple pattern.</span></span> <span data-ttu-id="f1dc3-144">È possibile usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per passare da un modello di stipple all'altro.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-144">You can use [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md) to switch between different stipple patterns.</span></span>

<span data-ttu-id="f1dc3-145">Le funzioni di stile linea IRIS GL precedenti (ad esempio, **Disegna**, **lsbackup**, **getlsbackup** e così via) non sono supportate da OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f1dc3-145">Older IRIS GL line style functions (such as **draw**, **lsbackup**, **getlsbackup**, and so on) are not supported by OpenGL.</span></span>

<span data-ttu-id="f1dc3-146">Per informazioni sul disegno di linee con antialias, vedere [porting anti-aliasing Functions](porting-antialiasing-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f1dc3-146">For information on drawing antialiased lines, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).</span></span>

<span data-ttu-id="f1dc3-147">??</span><span class="sxs-lookup"><span data-stu-id="f1dc3-147">??</span></span>

 

 





