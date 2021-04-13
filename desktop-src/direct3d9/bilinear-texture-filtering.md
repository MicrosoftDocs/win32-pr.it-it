---
description: Le trame vengono sempre risolte in modo lineare da (0,0, 0,0) nell'angolo superiore sinistro a (1,0, 1,0) nell'angolo inferiore destro, come illustrato nella figura seguente.
ms.assetid: 16fb04b9-4476-4dbe-a24f-51c0813a7917
title: Filtraggio bilineare della trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51213e5187c775963de2fa740847d55084c5be2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401492"
---
# <a name="bilinear-texture-filtering-direct3d-9"></a><span data-ttu-id="38955-103">Filtraggio bilineare della trama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="38955-103">Bilinear Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="38955-104">Le trame vengono sempre risolte in modo lineare da (0,0, 0,0) nell'angolo superiore sinistro a (1,0, 1,0) nell'angolo inferiore destro, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="38955-104">Textures are always linearly addressed from (0.0, 0.0) at the top-left corner to (1.0, 1.0) at the bottom-right corner, as shown in the following illustration.</span></span>

![illustrazione della trama 4x4 con blocchi di colore solidi](images/bilinear-fig7a.png)

<span data-ttu-id="38955-106">Le trame vengono in genere rappresentate come se fossero composte da blocchi di colore solidi, ma in realtà è più corretto pensare alle trame nello stesso modo in cui si pensa alla visualizzazione raster: ogni Texel è definito al centro esatto di una cella della griglia, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="38955-106">Textures are usually represented as if they were composed of solid blocks of color, but it's actually more correct to think of textures the same way you should think of the raster display: Each texel is defined at the exact center of a grid cell, as shown in the following illustration.</span></span>

![illustrazione della trama 4x4 con Texel definiti al centro delle celle della griglia](images/bilinear-fig7b.png)

<span data-ttu-id="38955-108">Se si chiede al campionatore di trame il colore di questa trama a coordinate UV (0,375, 0,375), si otterrà un rosso solido (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="38955-108">If you ask the texture sampler for this texture's color at UV coordinates (0.375, 0.375) you'll get solid red (255, 0, 0).</span></span> <span data-ttu-id="38955-109">Ciò ha un senso perfetto perché il centro esatto della cella rossa del Texel è a UV (0,375, 0,375).</span><span class="sxs-lookup"><span data-stu-id="38955-109">That makes perfect sense because the exact center of the red texel cell is at UV (0.375, 0.375).</span></span> <span data-ttu-id="38955-110">Cosa accade se si chiede al campionatore il colore della trama a UV (0,25, 0,25)?</span><span class="sxs-lookup"><span data-stu-id="38955-110">What if you ask the sampler for the texture's color at UV (0.25, 0.25)?</span></span> <span data-ttu-id="38955-111">Non è altrettanto semplice, perché il punto a UV (0,25, 0,25) si trova nell'angolo esatto di 4 Texel.</span><span class="sxs-lookup"><span data-stu-id="38955-111">That's not quite as easy, because the point at UV (0.25, 0.25) lies at the exact corner of 4 texels.</span></span>

<span data-ttu-id="38955-112">Lo schema più semplice consiste nel fare in modo che il campionatore restituisca il colore del Texel più vicino; Questa operazione è denominata filtro punti (vedere [campionamento dei punti più vicini (Direct3D 9)](nearest-point-sampling.md)) ed è in genere indesiderato a causa di risultati granulari o di blocco.</span><span class="sxs-lookup"><span data-stu-id="38955-112">The simplest scheme is simply to have the sampler return the color of the closest texel; this is called Point filtering (see [Nearest-Point Sampling (Direct3D 9)](nearest-point-sampling.md)), and is usually undesirable due to grainy or blocky results.</span></span> <span data-ttu-id="38955-113">Il campionamento dei punti con la trama a UV (0,25, 0,25) Mostra un altro problema sottile con il filtro dei punti più vicini: i quattro Texel sono equidistanti dal punto di campionamento, quindi non esiste un singolo Texel più vicino.</span><span class="sxs-lookup"><span data-stu-id="38955-113">Point-sampling our texture at UV (0.25, 0.25) shows another subtle problem with nearest-point filtering: there are four texels equidistant from the sampling point, so there's no single nearest texel.</span></span> <span data-ttu-id="38955-114">Uno di questi quattro Texel verrà scelto come colore restituito, ma la selezione dipenderà dalla modalità di arrotondamento della coordinata, che può comportare l'inserimento di elementi di strappo (vedere l'articolo di campionamento Nearest-Point nell'SDK).</span><span class="sxs-lookup"><span data-stu-id="38955-114">One of those four texels will be chosen as the returned color, but the selection depends on how the coordinate is rounded, which may introduce tearing artifacts (see the Nearest-Point Sampling article in the SDK).</span></span>

<span data-ttu-id="38955-115">Uno schema di filtro leggermente più preciso e più comune consiste nel calcolare la media ponderata dei 4 Texel più vicini al punto di campionamento. si tratta di un filtro bilineare e il costo di calcolo aggiuntivo è in genere trascurabile perché questa routine viene implementata nell'hardware grafico moderno.</span><span class="sxs-lookup"><span data-stu-id="38955-115">A slightly more accurate and more common filtering scheme is to calculate the weighted average of the 4 texels closest to the sampling point; this is called Bilinear filtering, and the extra computational cost is usually negligible because this routine is implemented in modern graphics hardware.</span></span> <span data-ttu-id="38955-116">Ecco i colori ottenibili in alcuni punti di campionamento diversi usando i filtri bilineari:</span><span class="sxs-lookup"><span data-stu-id="38955-116">Here are the colors we get at a few different sample points using bilinear filtering:</span></span>


```
UV: (0.5, 0.5)
```



<span data-ttu-id="38955-117">Questo punto è al bordo esatto tra i Texel rosso, verde, blu e bianco.</span><span class="sxs-lookup"><span data-stu-id="38955-117">This point is at the exact border between red, green, blue, and white texels.</span></span> <span data-ttu-id="38955-118">Il colore restituito dal campionatore è grigio:</span><span class="sxs-lookup"><span data-stu-id="38955-118">The color the sampler returns is gray:</span></span>


```
  0.25 * (255, 0, 0)
  0.25 * (0, 255, 0) 
  0.25 * (0, 0, 255) 
## + 0.25 * (255, 255, 255) 
------------------------
= (128, 128, 128)
```




```
UV: (0.5, 0.375)
```



<span data-ttu-id="38955-119">Questo punto si trova al punto medio del bordo tra i Texel rossi e verdi.</span><span class="sxs-lookup"><span data-stu-id="38955-119">This point is at the midpoint of the border between red and green texels.</span></span> <span data-ttu-id="38955-120">Il colore restituito dal campionatore è giallo-grigio (si noti che i contributi dei Texel blu e bianco vengono ridimensionati a 0):</span><span class="sxs-lookup"><span data-stu-id="38955-120">The color the sampler returns is yellow-gray (note that the contributions of the blue and white texels are scaled to 0):</span></span>


```
  0.5 * (255, 0, 0)
  0.5 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (128, 128, 0)
```




```
UV: (0.375, 0.375)
```



<span data-ttu-id="38955-121">Si tratta dell'indirizzo del Texel rosso, che corrisponde al colore restituito (tutti gli altri Texel nel calcolo di filtro vengono ponderati in 0):</span><span class="sxs-lookup"><span data-stu-id="38955-121">This is the address of the red texel, which is the returned color (all other texels in the filtering calculation are weighted to 0):</span></span>


```
  1.0 * (255, 0, 0)
  0.0 * (0, 255, 0) 
  0.0 * (0, 0, 255) 
## + 0.0 * (255, 255, 255) 
------------------------
= (255, 0, 0)
```



<span data-ttu-id="38955-122">Confrontare questi calcoli con la figura seguente, che mostra cosa accade se il calcolo del filtro bilineare viene eseguito a ogni indirizzo di trama nella trama 4x4.</span><span class="sxs-lookup"><span data-stu-id="38955-122">Compare these calculations against the following illustration, which shows what happens if the bilinear filtering calculation is performed at every texture address across the 4x4 texture.</span></span>

![illustrazione della trama 4x4 con filtro bilineare eseguito a ogni indirizzo di trama](images/bilinear-fig7c.jpg)

## <a name="related-topics"></a><span data-ttu-id="38955-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="38955-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38955-125">Filtraggio trama</span><span class="sxs-lookup"><span data-stu-id="38955-125">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 



