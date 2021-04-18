---
description: I volumi shadow vengono utilizzati per disegnare le ombre con il buffer dello stencil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Stencil Two-Sided (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304361"
---
# <a name="two-sided-stencil-direct3d-9"></a><span data-ttu-id="86880-103">Stencil Two-Sided (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="86880-103">Two-Sided Stencil (Direct3D 9)</span></span>

<span data-ttu-id="86880-104">I volumi shadow vengono utilizzati per disegnare le ombre con il buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="86880-104">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="86880-105">Tramite l'applicazione vengono calcolati i volumi shadow di cui viene eseguito il cast dalla geometria occlusione, calcolando i bordi della siluetta e estrattando i bordi dalla luce in un set di volumi 3D.</span><span class="sxs-lookup"><span data-stu-id="86880-105">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="86880-106">Questi volumi vengono quindi sottoposti a rendering due volte nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="86880-106">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="86880-107">Il primo rendering disegna i poligoni rivolte verso il futuro e incrementa i valori del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="86880-107">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="86880-108">Il secondo oggetto render disegna i poligoni sul retro del volume shadow e decrementa i valori del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="86880-108">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="86880-109">In genere, tutti i valori incrementati e decrementati vengono annullati. Tuttavia, la scena è già stata sottoposta a rendering con la geometria normale causando la mancata riuscita del test del buffer z durante il rendering del volume shadow.</span><span class="sxs-lookup"><span data-stu-id="86880-109">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="86880-110">I valori rimanenti nel buffer dello stencil corrispondono ai pixel presenti nell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="86880-110">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="86880-111">Questi rimanenti contenuti del buffer dello stencil vengono usati come maschera, per alfa-blend di un quadrato nero di grandi dimensioni, che include tutto il doppio nella scena.</span><span class="sxs-lookup"><span data-stu-id="86880-111">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="86880-112">Con il buffer dello stencil che funge da maschera, il risultato è quello di scurire i pixel presenti nelle ombreggiature.</span><span class="sxs-lookup"><span data-stu-id="86880-112">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="86880-113">Ciò significa che la geometria dell'ombreggiatura viene disegnata due volte per ogni sorgente di luce, di conseguenza la pressione sulla velocità effettiva del vertice della GPU.</span><span class="sxs-lookup"><span data-stu-id="86880-113">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="86880-114">La funzionalità stencil a due lati è stata progettata per attenuare questa situazione.</span><span class="sxs-lookup"><span data-stu-id="86880-114">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="86880-115">In questo approccio sono disponibili due set di stato dello stencil, denominati di seguito, uno per i triangoli in primo piano e l'altro per i triangoli rivolti verso il retro.</span><span class="sxs-lookup"><span data-stu-id="86880-115">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="86880-116">In questo modo viene disegnato un solo passaggio per ogni volume ombreggiato, per luce.</span><span class="sxs-lookup"><span data-stu-id="86880-116">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="86880-117">Le modifiche all'API sono limitate a un nuovo set di Stati di rendering.</span><span class="sxs-lookup"><span data-stu-id="86880-117">The API changes are restricted to a new set of render states.</span></span> <span data-ttu-id="86880-118">Il nuovo stato di rendering \_ D3DRS \_ \_ StencilMODE a due lati può essere impostato su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="86880-118">The new render state D3DRS\_Two\_Sided\_StencilMODE can be set to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="86880-119">È **false** per impostazione predefinita, ovvero il comportamento corrente (DirectX 8).</span><span class="sxs-lookup"><span data-stu-id="86880-119">It is **FALSE** by default, meaning current (DirectX 8) behavior.</span></span> <span data-ttu-id="86880-120">Quando questa impostazione è impostata su **true** (funzionerà solo se \_ è impostato D3DSTENCILCAPS TWOSIDED), gli Stati di rendering seguenti si applicano solo ai triangoli anteriori (in senso orario).</span><span class="sxs-lookup"><span data-stu-id="86880-120">When this is set to **TRUE** (it will work only if D3DSTENCILCAPS\_TWOSIDED is set), the following render states will apply only to the front-facing (clockwise) triangles.</span></span>



| <span data-ttu-id="86880-121">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="86880-121">Render state</span></span>        | <span data-ttu-id="86880-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86880-122">Description</span></span>                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86880-123">\_STENCILFAIL D3DRS</span><span class="sxs-lookup"><span data-stu-id="86880-123">D3DRS\_STENCILFAIL</span></span>  | <span data-ttu-id="86880-124">D3DSTENCILOP da eseguire se il test dello stencil non riesce.</span><span class="sxs-lookup"><span data-stu-id="86880-124">D3DSTENCILOP to do if stencil test fails.</span></span>                                                |
| <span data-ttu-id="86880-125">\_STENCILZFAIL D3DRS</span><span class="sxs-lookup"><span data-stu-id="86880-125">D3DRS\_STENCILZFAIL</span></span> | <span data-ttu-id="86880-126">D3DSTENCILOP da eseguire se il test di stencil supera e il test z ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="86880-126">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                              |
| <span data-ttu-id="86880-127">\_STENCILPASS D3DRS</span><span class="sxs-lookup"><span data-stu-id="86880-127">D3DRS\_STENCILPASS</span></span>  | <span data-ttu-id="86880-128">D3DSTENCILOP da eseguire se vengono superati sia lo stencil che i test z.</span><span class="sxs-lookup"><span data-stu-id="86880-128">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                     |
| <span data-ttu-id="86880-129">\_STENCILFUNC D3DRS</span><span class="sxs-lookup"><span data-stu-id="86880-129">D3DRS\_STENCILFUNC</span></span>  | <span data-ttu-id="86880-130">D3DCMPFUNC FN.</span><span class="sxs-lookup"><span data-stu-id="86880-130">D3DCMPFUNC fn.</span></span> <span data-ttu-id="86880-131">Il test di stencil viene superato se ((Ref & mask) stencilfn (stencil & mask)) è true.</span><span class="sxs-lookup"><span data-stu-id="86880-131">Stencil Test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="86880-132">Un nuovo set di Stati di rendering si applica ai triangoli rivolti al back-end (in senso antiorario).</span><span class="sxs-lookup"><span data-stu-id="86880-132">A new set of render states apply to the back-facing (counterclockwise) triangles.</span></span>



| <span data-ttu-id="86880-133">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="86880-133">Render state</span></span>             | <span data-ttu-id="86880-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86880-134">Description</span></span>                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86880-135">D3DRS \_ CCW \_ STENCILFAIL</span><span class="sxs-lookup"><span data-stu-id="86880-135">D3DRS\_CCW\_STENCILFAIL</span></span>  | <span data-ttu-id="86880-136">D3DSTENCILOP da eseguire se il test dello stencil non riesce.</span><span class="sxs-lookup"><span data-stu-id="86880-136">D3DSTENCILOP to do if stencil test fails.</span></span>                                                      |
| <span data-ttu-id="86880-137">D3DRS \_ CCW \_ STENCILZFAIL</span><span class="sxs-lookup"><span data-stu-id="86880-137">D3DRS\_CCW\_STENCILZFAIL</span></span> | <span data-ttu-id="86880-138">D3DSTENCILOP da eseguire se il test di stencil supera e il test z ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="86880-138">D3DSTENCILOP to do if stencil test passes and z-test fails.</span></span>                                    |
| <span data-ttu-id="86880-139">D3DRS \_ CCW \_ STENCILPASS</span><span class="sxs-lookup"><span data-stu-id="86880-139">D3DRS\_CCW\_STENCILPASS</span></span>  | <span data-ttu-id="86880-140">D3DSTENCILOP da eseguire se vengono superati sia lo stencil che i test z.</span><span class="sxs-lookup"><span data-stu-id="86880-140">D3DSTENCILOP to do if both stencil and z-tests pass.</span></span>                                           |
| <span data-ttu-id="86880-141">D3DRS \_ CCW \_ STENCILFUNC</span><span class="sxs-lookup"><span data-stu-id="86880-141">D3DRS\_CCW\_STENCILFUNC</span></span>  | <span data-ttu-id="86880-142">Funzione D3DCMPFUNC.</span><span class="sxs-lookup"><span data-stu-id="86880-142">D3DCMPFUNC function.</span></span> <span data-ttu-id="86880-143">Il test di stencil viene superato se ((Ref & mask) stencilfn (stencil & mask)) è true.</span><span class="sxs-lookup"><span data-stu-id="86880-143">Stencil test passes if ((ref & mask) stencilfn (stencil & mask)) is true.</span></span> |



 

<span data-ttu-id="86880-144">Gli Stati di rendering degli stencil rimanenti si applicano sempre ai triangoli in senso orario e in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="86880-144">The remaining stencil render states always apply to both clockwise and counterclockwise triangles.</span></span>

<span data-ttu-id="86880-145">\_Il D3DRS \_ a due lati \_ StencilMODE viene ignorato per gli sprite di linee e punti, il che significa che il comportamento è invariato da DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="86880-145">D3DRS\_Two\_Sided\_StencilMODE is ignored for lines and point sprites, which means that the behavior is unchanged from DirectX 8.</span></span> <span data-ttu-id="86880-146">Gli \_ Stati di rendering dello stencil D3DRS CCW \_ \* vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="86880-146">The D3DRS\_CCW\_STENCIL\* render states are ignored.</span></span>

<span data-ttu-id="86880-147">Un nuovo bit di estremità indica se il dispositivo supporta questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="86880-147">A new cap bit indicates if the device supports this feature.</span></span> <span data-ttu-id="86880-148">Si prevede che i driver che non supportano questa funzionalità ignorino questi nuovi Stati di rendering.</span><span class="sxs-lookup"><span data-stu-id="86880-148">Drivers that do not support this feature are expected to ignore these new render states.</span></span> <span data-ttu-id="86880-149">Tutti gli altri bit di estremità dello stencil si applicano a entrambe le modalità di memorizzazione nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="86880-149">All other stencil cap bits apply to both modes of stencil buffering.</span></span> <span data-ttu-id="86880-150">Poiché lo \_ \_ stencil con due lati implica la possibilità di creare con D3DCULLMODE \_ None set, il limite corrispondente deve essere impostato dal driver se supporta questa nuova modalità stencil.</span><span class="sxs-lookup"><span data-stu-id="86880-150">Because Two\_Sided\_Stencil implies the ability to draw with D3DCULLMODE\_NONE set, the corresponding cap must be set by the driver if it supports this new stencil mode.</span></span> <span data-ttu-id="86880-151">Microsoft Windows Hardware Quality Labs (WHQL) dovrebbe applicare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="86880-151">Microsoft Windows Hardware Quality Labs (WHQL) should enforce this.</span></span>

<span data-ttu-id="86880-152">Nuovi Stati di rendering:</span><span class="sxs-lookup"><span data-stu-id="86880-152">New render states:</span></span>


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



<span data-ttu-id="86880-153">Nuovo Cap:</span><span class="sxs-lookup"><span data-stu-id="86880-153">New cap:</span></span>


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a><span data-ttu-id="86880-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="86880-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86880-155">Tecniche del buffer dello stencil</span><span class="sxs-lookup"><span data-stu-id="86880-155">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> <dt>

[<span data-ttu-id="86880-156">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="86880-156">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
