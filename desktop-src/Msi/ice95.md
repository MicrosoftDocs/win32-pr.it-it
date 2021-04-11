---
description: ICE95 controlla la tabella di controllo e la tabella BBControl per verificare che i controlli Billboard rientrino in tutti i tabelloni.
ms.assetid: 8ba73536-65a5-4658-846c-76356f16b81c
title: ICE95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14144c7739dfcc1f1b5e66d92d8e6c1c46ed49fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233153"
---
# <a name="ice95"></a><span data-ttu-id="e281f-103">ICE95</span><span class="sxs-lookup"><span data-stu-id="e281f-103">ICE95</span></span>

<span data-ttu-id="e281f-104">ICE95 controlla la [tabella di controllo](control-table.md) e la [tabella BBControl](bbcontrol-table.md) per verificare che i controlli Billboard rientrino in tutti i tabelloni.</span><span class="sxs-lookup"><span data-stu-id="e281f-104">ICE95 checks the [Control table](control-table.md) and [BBControl table](bbcontrol-table.md) to verify that the billboard controls fit onto all the billboards.</span></span>

## <a name="result"></a><span data-ttu-id="e281f-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="e281f-105">Result</span></span>

<span data-ttu-id="e281f-106">Se si verifica una delle condizioni seguenti, un controllo Billboard non è in grado di adattarsi a un tabellone.</span><span class="sxs-lookup"><span data-stu-id="e281f-106">If any of the following are true, a billboard control fails to fit on a billboard.</span></span> <span data-ttu-id="e281f-107">ICE95 invia gli avvisi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e281f-107">ICE95 posts the following warnings.</span></span>



| <span data-ttu-id="e281f-108">Avviso di ICE95</span><span class="sxs-lookup"><span data-stu-id="e281f-108">ICE95 warning</span></span>                                                                                                                                                                                                              | <span data-ttu-id="e281f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e281f-109">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e281f-110">Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli.</span><span class="sxs-lookup"><span data-stu-id="e281f-110">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="e281f-111">La coordinata X supera il limite della larghezza minima del controllo Billboard% s</span><span class="sxs-lookup"><span data-stu-id="e281f-111">The X coordinate exceeds the boundary of the minimum billboard control width %s</span></span>                   | <span data-ttu-id="e281f-112">La coordinata X del controllo non rientra nella larghezza del tabellone.</span><span class="sxs-lookup"><span data-stu-id="e281f-112">The control's X coordinate is outside the width of the billboard.</span></span>                          |
| <span data-ttu-id="e281f-113">Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli.</span><span class="sxs-lookup"><span data-stu-id="e281f-113">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="e281f-114">La coordinata Y supera il limite dell'altezza minima del controllo Billboard% s</span><span class="sxs-lookup"><span data-stu-id="e281f-114">The Y coordinate exceeds the boundary of the minimum billboard control height %s</span></span>                  | <span data-ttu-id="e281f-115">La coordinata Y del controllo è sotto la parte inferiore del tabellone.</span><span class="sxs-lookup"><span data-stu-id="e281f-115">The control's Y coordinate is below the bottom of the billboard.</span></span>                           |
| <span data-ttu-id="e281f-116">Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli.</span><span class="sxs-lookup"><span data-stu-id="e281f-116">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="e281f-117">La coordinata X e la larghezza combinate superano la larghezza minima del controllo Billboard% s</span><span class="sxs-lookup"><span data-stu-id="e281f-117">The X coordinate and the width combined together exceeds the minimum billboard control width %s</span></span>   | <span data-ttu-id="e281f-118">La coordinata X del controllo e la larghezza del controllo non rientrano nella larghezza del tabellone.</span><span class="sxs-lookup"><span data-stu-id="e281f-118">The control's X coordinate plus the control's width is outside the width of the billboard.</span></span> |
| <span data-ttu-id="e281f-119">Elemento BBControl ' \[ 1 \] . \[ 2 \] ' nella tabella BBControl non rientra in tutti i controlli Billboard della tabella dei controlli.</span><span class="sxs-lookup"><span data-stu-id="e281f-119">The BBControl item '\[1\].\[2\]' in the BBControl table does not fit in all the billboard controls in the Control table.</span></span> <span data-ttu-id="e281f-120">La coordinata Y e l'altezza combinate insieme superano l'altezza minima del controllo Billboard% s</span><span class="sxs-lookup"><span data-stu-id="e281f-120">The Y coordinate and the height combined together exceeds the minimum billboard control height %s</span></span> | <span data-ttu-id="e281f-121">La coordinata Y del controllo più l'altezza del controllo si trova sotto la parte inferiore del tabellone.</span><span class="sxs-lookup"><span data-stu-id="e281f-121">The control's Y coordinate plus the control's height is below the bottom of the billboard.</span></span> |



 

## <a name="example"></a><span data-ttu-id="e281f-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="e281f-122">Example</span></span>

<span data-ttu-id="e281f-123">ICE95 segnala gli avvisi seguenti per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="e281f-123">ICE95 reports the following warnings for the example:</span></span>

``` syntax
The BBControl item 'billboard1.bbcontrol1' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate exceeds the boundary of the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol2' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate exceeds the boundary of the minimum billboard control height 100
The BBControl item 'billboard1.bbcontrol3' in the BBControl table does not fit in all the billboard controls in the Control table. The X coordinate and the width combined together exceeds the minimum billboard control width 100
The BBControl item 'billboard1.bbcontrol4' in the BBControl table does not fit in all the billboard controls in the Control table. The Y coordinate and the height combined together exceeds the minimum billboard control height 100
```

<span data-ttu-id="e281f-124">Tabella di controllo (parziale) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e281f-124">Control Table (partial) (partial)</span></span>



| <span data-ttu-id="e281f-125">Control</span><span class="sxs-lookup"><span data-stu-id="e281f-125">Control</span></span>  | <span data-ttu-id="e281f-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="e281f-126">Type</span></span>      | <span data-ttu-id="e281f-127">Larghezza</span><span class="sxs-lookup"><span data-stu-id="e281f-127">Width</span></span> | <span data-ttu-id="e281f-128">Altezza</span><span class="sxs-lookup"><span data-stu-id="e281f-128">Height</span></span> |
|----------|-----------|-------|--------|
| <span data-ttu-id="e281f-129">Control1</span><span class="sxs-lookup"><span data-stu-id="e281f-129">control1</span></span> | <span data-ttu-id="e281f-130">Billboard</span><span class="sxs-lookup"><span data-stu-id="e281f-130">Billboard</span></span> | <span data-ttu-id="e281f-131">300</span><span class="sxs-lookup"><span data-stu-id="e281f-131">300</span></span>   | <span data-ttu-id="e281f-132">100</span><span class="sxs-lookup"><span data-stu-id="e281f-132">100</span></span>    |
| <span data-ttu-id="e281f-133">Controllo2</span><span class="sxs-lookup"><span data-stu-id="e281f-133">Control2</span></span> | <span data-ttu-id="e281f-134">Billboard</span><span class="sxs-lookup"><span data-stu-id="e281f-134">Billboard</span></span> | <span data-ttu-id="e281f-135">100</span><span class="sxs-lookup"><span data-stu-id="e281f-135">100</span></span>   | <span data-ttu-id="e281f-136">300</span><span class="sxs-lookup"><span data-stu-id="e281f-136">300</span></span>    |



 

[<span data-ttu-id="e281f-137">Tabella BBControl</span><span class="sxs-lookup"><span data-stu-id="e281f-137">BBControl table</span></span>](bbcontrol-table.md)



| <span data-ttu-id="e281f-138">Billboard\_</span><span class="sxs-lookup"><span data-stu-id="e281f-138">Billboard\_</span></span> | <span data-ttu-id="e281f-139">BBControl</span><span class="sxs-lookup"><span data-stu-id="e281f-139">BBControl</span></span>  | <span data-ttu-id="e281f-140">X</span><span class="sxs-lookup"><span data-stu-id="e281f-140">X</span></span>   | <span data-ttu-id="e281f-141">S</span><span class="sxs-lookup"><span data-stu-id="e281f-141">Y</span></span>   | <span data-ttu-id="e281f-142">Larghezza</span><span class="sxs-lookup"><span data-stu-id="e281f-142">Width</span></span> | <span data-ttu-id="e281f-143">Altezza</span><span class="sxs-lookup"><span data-stu-id="e281f-143">Height</span></span> |
|-------------|------------|-----|-----|-------|--------|
| <span data-ttu-id="e281f-144">billboard1</span><span class="sxs-lookup"><span data-stu-id="e281f-144">billboard1</span></span>  | <span data-ttu-id="e281f-145">bbcontrol1</span><span class="sxs-lookup"><span data-stu-id="e281f-145">bbcontrol1</span></span> | <span data-ttu-id="e281f-146">200</span><span class="sxs-lookup"><span data-stu-id="e281f-146">200</span></span> | <span data-ttu-id="e281f-147">0</span><span class="sxs-lookup"><span data-stu-id="e281f-147">0</span></span>   | <span data-ttu-id="e281f-148">100</span><span class="sxs-lookup"><span data-stu-id="e281f-148">100</span></span>   | <span data-ttu-id="e281f-149">100</span><span class="sxs-lookup"><span data-stu-id="e281f-149">100</span></span>    |
| <span data-ttu-id="e281f-150">billboard1</span><span class="sxs-lookup"><span data-stu-id="e281f-150">billboard1</span></span>  | <span data-ttu-id="e281f-151">bbcontrol2</span><span class="sxs-lookup"><span data-stu-id="e281f-151">bbcontrol2</span></span> | <span data-ttu-id="e281f-152">0</span><span class="sxs-lookup"><span data-stu-id="e281f-152">0</span></span>   | <span data-ttu-id="e281f-153">200</span><span class="sxs-lookup"><span data-stu-id="e281f-153">200</span></span> | <span data-ttu-id="e281f-154">100</span><span class="sxs-lookup"><span data-stu-id="e281f-154">100</span></span>   | <span data-ttu-id="e281f-155">100</span><span class="sxs-lookup"><span data-stu-id="e281f-155">100</span></span>    |
| <span data-ttu-id="e281f-156">billboard1</span><span class="sxs-lookup"><span data-stu-id="e281f-156">billboard1</span></span>  | <span data-ttu-id="e281f-157">bbcontrol3</span><span class="sxs-lookup"><span data-stu-id="e281f-157">bbcontrol3</span></span> | <span data-ttu-id="e281f-158">50</span><span class="sxs-lookup"><span data-stu-id="e281f-158">50</span></span>  | <span data-ttu-id="e281f-159">0</span><span class="sxs-lookup"><span data-stu-id="e281f-159">0</span></span>   | <span data-ttu-id="e281f-160">100</span><span class="sxs-lookup"><span data-stu-id="e281f-160">100</span></span>   | <span data-ttu-id="e281f-161">50</span><span class="sxs-lookup"><span data-stu-id="e281f-161">50</span></span>     |
| <span data-ttu-id="e281f-162">billboard1</span><span class="sxs-lookup"><span data-stu-id="e281f-162">billboard1</span></span>  | <span data-ttu-id="e281f-163">bbcontrol4</span><span class="sxs-lookup"><span data-stu-id="e281f-163">bbcontrol4</span></span> | <span data-ttu-id="e281f-164">0</span><span class="sxs-lookup"><span data-stu-id="e281f-164">0</span></span>   | <span data-ttu-id="e281f-165">50</span><span class="sxs-lookup"><span data-stu-id="e281f-165">50</span></span>  | <span data-ttu-id="e281f-166">50</span><span class="sxs-lookup"><span data-stu-id="e281f-166">50</span></span>    | <span data-ttu-id="e281f-167">100</span><span class="sxs-lookup"><span data-stu-id="e281f-167">100</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="e281f-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e281f-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e281f-169">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e281f-169">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



