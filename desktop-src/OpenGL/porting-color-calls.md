---
title: Chiamate di colore di porting
description: Nella tabella seguente sono elencate le funzioni dei colori IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- Porting di IRIS GL, colore
- porting da IRIS GL, color
- porting in OpenGL da IRIS GL, colore
- Porting OpenGL da IRIS GL, colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708464"
---
# <a name="porting-color-calls"></a><span data-ttu-id="9e15d-107">Chiamate di colore di porting</span><span class="sxs-lookup"><span data-stu-id="9e15d-107">Porting Color Calls</span></span>

<span data-ttu-id="9e15d-108">Nella tabella seguente sono elencate le funzioni dei colori IRIS GL e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="9e15d-108">The following table lists IRIS GL color functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="9e15d-109">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9e15d-109">IRIS GL function</span></span>                  | <span data-ttu-id="9e15d-110">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="9e15d-110">OpenGL function</span></span>                                                                                                                               | <span data-ttu-id="9e15d-111">Significato</span><span class="sxs-lookup"><span data-stu-id="9e15d-111">Meaning</span></span>                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e15d-112">**c**</span><span class="sxs-lookup"><span data-stu-id="9e15d-112">**c**</span></span>                             | [<span data-ttu-id="9e15d-113">glColor</span><span class="sxs-lookup"><span data-stu-id="9e15d-113">glColor</span></span>](glcolor-functions.md)                                                                                                              | <span data-ttu-id="9e15d-114">Imposta il colore RGB.</span><span class="sxs-lookup"><span data-stu-id="9e15d-114">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="9e15d-115">**color**</span><span class="sxs-lookup"><span data-stu-id="9e15d-115">**color**</span></span>                         | [<span data-ttu-id="9e15d-116">glIndex</span><span class="sxs-lookup"><span data-stu-id="9e15d-116">glIndex</span></span>](glindex-functions.md)                                                                                                              | <span data-ttu-id="9e15d-117">Imposta l'indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="9e15d-117">Sets the color index.</span></span>                                |
| <span data-ttu-id="9e15d-118">**GetColor**</span><span class="sxs-lookup"><span data-stu-id="9e15d-118">**getcolor**</span></span>                      | <span data-ttu-id="9e15d-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ indice corrente GL \_ )</span><span class="sxs-lookup"><span data-stu-id="9e15d-119">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_CURRENT\_INDEX )</span></span>                                               | <span data-ttu-id="9e15d-120">Restituisce l'indice dei colori corrente.</span><span class="sxs-lookup"><span data-stu-id="9e15d-120">Returns the current color index.</span></span>                     |
| <span data-ttu-id="9e15d-121">**getmcolor**</span><span class="sxs-lookup"><span data-stu-id="9e15d-121">**getmcolor**</span></span>                     |                                                                                                                                               | <span data-ttu-id="9e15d-122">Ottiene una copia dei valori RGB per una voce della mappa colori.</span><span class="sxs-lookup"><span data-stu-id="9e15d-122">Gets a copy of the RGB values for a color map entry.</span></span> |
| <span data-ttu-id="9e15d-123">**gRGBcolor**</span><span class="sxs-lookup"><span data-stu-id="9e15d-123">**gRGBcolor**</span></span>                     | <span data-ttu-id="9e15d-124">**glGet**( \_ colore corrente GL \_ )</span><span class="sxs-lookup"><span data-stu-id="9e15d-124">**glGet**( GL\_CURRENT\_COLOR )</span></span>                                                                                                               | <span data-ttu-id="9e15d-125">Ottiene i valori dei colori RGB correnti.</span><span class="sxs-lookup"><span data-stu-id="9e15d-125">Gets the current RGB color values.</span></span>                   |
| <span data-ttu-id="9e15d-126">**mapcolor**</span><span class="sxs-lookup"><span data-stu-id="9e15d-126">**mapcolor**</span></span>                      |                                                                                                                                               |                                                      |
| <span data-ttu-id="9e15d-127">**RGBcolor**</span><span class="sxs-lookup"><span data-stu-id="9e15d-127">**RGBcolor**</span></span>                      | <span data-ttu-id="9e15d-128">**glColor**</span><span class="sxs-lookup"><span data-stu-id="9e15d-128">**glColor**</span></span>                                                                                                                                   | <span data-ttu-id="9e15d-129">Imposta il colore RGB.</span><span class="sxs-lookup"><span data-stu-id="9e15d-129">Sets RGB color.</span></span>                                      |
| <span data-ttu-id="9e15d-130">**writemask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-130">**writemask**</span></span>                     | [<span data-ttu-id="9e15d-131">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-131">**glIndexMask**</span></span>](glindexmask.md)                                                                                                            | <span data-ttu-id="9e15d-132">Imposta la maschera colori della modalità di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="9e15d-132">Sets the color-index mode color mask.</span></span>                |
| <span data-ttu-id="9e15d-133">**wmpackRGBwritemask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-133">**wmpackRGBwritemask**</span></span><br/> | [<span data-ttu-id="9e15d-134">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-134">**glColorMask**</span></span>](glcolormask.md)                                                                                                            | <span data-ttu-id="9e15d-135">Imposta la maschera della modalità colori RGB.</span><span class="sxs-lookup"><span data-stu-id="9e15d-135">Sets the RGB color mode mask.</span></span>                        |
| <span data-ttu-id="9e15d-136">**getwritemask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-136">**getwritemask**</span></span>                  | <span data-ttu-id="9e15d-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (GL \_ Color \_ WRITEMASK)**glGet**(GL \_ index \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="9e15d-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_COLOR\_WRITEMASK )**glGet**( GL\_INDEX\_WRITEMASK )</span></span><br/> | <span data-ttu-id="9e15d-138">Ottiene la maschera dei colori.</span><span class="sxs-lookup"><span data-stu-id="9e15d-138">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="9e15d-139">**gRGBmask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-139">**gRGBmask**</span></span>                      | <span data-ttu-id="9e15d-140">**glGet**(GL \_ Color \_ WRITEMASK)</span><span class="sxs-lookup"><span data-stu-id="9e15d-140">**glGet**( GL\_COLOR\_WRITEMASK )</span></span>                                                                                                             | <span data-ttu-id="9e15d-141">Ottiene la maschera dei colori.</span><span class="sxs-lookup"><span data-stu-id="9e15d-141">Gets the color mask.</span></span>                                 |
| <span data-ttu-id="9e15d-142">**zwritemask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-142">**zwritemask**</span></span>                    | [<span data-ttu-id="9e15d-143">**glDepthMask**</span><span class="sxs-lookup"><span data-stu-id="9e15d-143">**glDepthMask**</span></span>](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> <span data-ttu-id="9e15d-144">Prestare attenzione quando si sostituisce **zwritemask** con [**glDepthMask**](gldepthmask.md); **glDepthMask** accetta un argomento booleano, mentre **zwritemask** accetta un campo di bit.</span><span class="sxs-lookup"><span data-stu-id="9e15d-144">Be careful when replacing **zwritemask** with [**glDepthMask**](gldepthmask.md); **glDepthMask** takes a Boolean argument, whereas **zwritemask** takes a bit field.</span></span>

 

<span data-ttu-id="9e15d-145">Se si desidera utilizzare più mappe a colori, è necessario utilizzare le funzioni mappa colori di Windows appropriate.</span><span class="sxs-lookup"><span data-stu-id="9e15d-145">If you want to use multiple color maps, you need to use the appropriate Windows color map functions.</span></span> <span data-ttu-id="9e15d-146">Pertanto, **multimap**, **OneMap**, **getcmmode**, **setmap** e **GetMap** non dispongono di equivalenti OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9e15d-146">Therefore, **multimap**, **onemap**, **getcmmode**, **setmap**, and **getmap** have no OpenGL equivalents.</span></span>

 

 





