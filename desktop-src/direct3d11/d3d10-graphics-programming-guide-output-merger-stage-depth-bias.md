---
title: Distorsione profondità
description: È possibile fare in modo che i poligoni complanari nello spazio 3D vengano visualizzati come se non fossero complanari aggiungendo a ognuno una distorsione z (o una distorsione di profondità).
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734935"
---
# <a name="depth-bias"></a><span data-ttu-id="f1adf-103">Distorsione profondità</span><span class="sxs-lookup"><span data-stu-id="f1adf-103">Depth Bias</span></span>

<span data-ttu-id="f1adf-104">È possibile fare in modo che i poligoni complanari nello spazio 3D vengano visualizzati come se non fossero complanari aggiungendo a ognuno una distorsione z (o una distorsione di profondità).</span><span class="sxs-lookup"><span data-stu-id="f1adf-104">Polygons that are coplanar in 3D space can be made to appear as if they are not coplanar by adding a z-bias (or depth bias) to each one.</span></span>

<span data-ttu-id="f1adf-105">Si tratta di una tecnica comunemente utilizzata per garantire che le ombre in una scena vengano visualizzate correttamente.</span><span class="sxs-lookup"><span data-stu-id="f1adf-105">This is a technique commonly used to ensure that shadows in a scene are displayed properly.</span></span> <span data-ttu-id="f1adf-106">Ad esempio, un'ombreggiatura su una parete avrà probabilmente lo stesso valore di profondità della parete.</span><span class="sxs-lookup"><span data-stu-id="f1adf-106">For instance, a shadow on a wall will likely have the same depth value as the wall.</span></span> <span data-ttu-id="f1adf-107">Se un'applicazione esegue il rendering di un muro prima e poi un'ombreggiatura, l'ombreggiatura potrebbe non essere visibile oppure gli artefatti di profondità potrebbero essere visibili.</span><span class="sxs-lookup"><span data-stu-id="f1adf-107">If an application renders a wall first and then a shadow, the shadow might not be visible, or depth artifacts might be visible.</span></span>


<span data-ttu-id="f1adf-108">Un'applicazione può garantire il rendering corretto dei poligoni complanari aggiungendo la distorsione (dal membro **DepthBias** di [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) ai valori z usati dal sistema durante il rendering dei set di poligoni complanari.</span><span class="sxs-lookup"><span data-stu-id="f1adf-108">An application can help ensure that coplanar polygons are rendered properly by adding the bias (from the **DepthBias** member of [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) to the z-values that the system uses when rendering the sets of coplanar polygons.</span></span> <span data-ttu-id="f1adf-109">I poligoni con un valore z maggiore verranno disegnati davanti ai poligoni con un valore z inferiore.</span><span class="sxs-lookup"><span data-stu-id="f1adf-109">Polygons with a larger z value will be drawn in front of polygons with a smaller z value.</span></span>

<span data-ttu-id="f1adf-110">Sono disponibili due opzioni per il calcolo della distorsione della profondità.</span><span class="sxs-lookup"><span data-stu-id="f1adf-110">There are two options for calculating depth bias.</span></span>

1.  <span data-ttu-id="f1adf-111">Se il buffer di profondità attualmente associato alla fase di Unione dell'output ha un formato **UNORM** o non è associato alcun buffer di profondità, il valore di distorsione viene calcolato in questo modo:</span><span class="sxs-lookup"><span data-stu-id="f1adf-111">If the depth buffer currently bound to the output-merger stage has a **UNORM** format or no depth buffer is bound, the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="f1adf-112">dove *r* è il valore minimo rappresentabile > 0 nel formato del buffer di profondità convertito in **float32**.</span><span class="sxs-lookup"><span data-stu-id="f1adf-112">where *r* is the minimum representable value > 0 in the depth-buffer format converted to **float32**.</span></span> <span data-ttu-id="f1adf-113">I valori **DepthBias** e **SlopeScaledDepthBias** sono membri della struttura [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) .</span><span class="sxs-lookup"><span data-stu-id="f1adf-113">The **DepthBias** and **SlopeScaledDepthBias** values are [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) structure members.</span></span> <span data-ttu-id="f1adf-114">Il valore **MaxDepthSlope** è il numero massimo di pendii orizzontali e verticali del valore di profondità al pixel.</span><span class="sxs-lookup"><span data-stu-id="f1adf-114">The **MaxDepthSlope** value is the maximum of the horizontal and vertical slopes of the depth value at the pixel.</span></span>
2.  <span data-ttu-id="f1adf-115">Se un buffer di profondità a virgola mobile è associato alla fase di Unione dell'output, il valore della distorsione viene calcolato in questo modo:</span><span class="sxs-lookup"><span data-stu-id="f1adf-115">If a floating-point depth buffer is bound to the output-merger stage the bias value is calculated like this:</span></span>
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    <span data-ttu-id="f1adf-116">dove *r* è il numero di mantissa bit nella rappresentazione a virgola mobile (escluso il bit nascosto); ad esempio, 23 per **float32**.</span><span class="sxs-lookup"><span data-stu-id="f1adf-116">where *r* is the number of mantissa bits in the floating point representation (excluding the hidden bit); for example, 23 for **float32**.</span></span>

<span data-ttu-id="f1adf-117">Il valore di distorsione viene quindi bloccato come segue:</span><span class="sxs-lookup"><span data-stu-id="f1adf-117">The bias value is then clamped like this:</span></span>


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



<span data-ttu-id="f1adf-118">Il valore di distorsione viene quindi utilizzato per calcolare la profondità dei pixel.</span><span class="sxs-lookup"><span data-stu-id="f1adf-118">The bias value is then used to calculate the pixel depth.</span></span>


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



<span data-ttu-id="f1adf-119">Le operazioni di distorsione della profondità si verificano sui vertici dopo il ritaglio, quindi la distorsione della profondità non ha alcun effetto sul ritaglio geometrico.</span><span class="sxs-lookup"><span data-stu-id="f1adf-119">Depth-bias operations occur on vertices after clipping, therefore, depth-bias has no effect on geometric clipping.</span></span> <span data-ttu-id="f1adf-120">Il valore di distorsione è costante per una determinata primitiva e viene aggiunto al valore z per ogni vertice prima del programma di installazione dell'interpolatore.</span><span class="sxs-lookup"><span data-stu-id="f1adf-120">The bias value is constant for a given primitive and is added to the z value for each vertex before interpolator setup.</span></span> <span data-ttu-id="f1adf-121">Quando si usano i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 e versioni successive, tutti i calcoli di distorsione vengono eseguiti usando l'aritmetica a virgola mobile a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f1adf-121">When you use [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 10.0 and higher, all bias calculations are performed using 32-bit floating-point arithmetic.</span></span> <span data-ttu-id="f1adf-122">La distorsione non viene applicata ad alcuna primitiva di punti o righe, ad eccezione delle linee disegnate in modalità wireframe.</span><span class="sxs-lookup"><span data-stu-id="f1adf-122">Bias is not applied to any point or line primitives, except for lines drawn in wireframe mode.</span></span>

<span data-ttu-id="f1adf-123">Uno degli artefatti con ombreggiature basate su buffer ombreggiatura è Shadow acne o una superficie ombreggiatura stessa a causa di differenze minime tra il calcolo della profondità in uno shader e la profondità della stessa superficie nel buffer di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="f1adf-123">One of the artifacts with shadow buffer based shadows is shadow acne, or a surface shadowing itself due to minor differences between the depth computation in a shader, and the depth of the same surface in the shadow buffer.</span></span> <span data-ttu-id="f1adf-124">Un modo per risolvere questo problema consiste nell'usare **DepthBias** e **SlopeScaledDepthBias** durante il rendering di un buffer Shadow.</span><span class="sxs-lookup"><span data-stu-id="f1adf-124">One way to alleviate this is to use **DepthBias** and **SlopeScaledDepthBias** when rendering a shadow buffer.</span></span> <span data-ttu-id="f1adf-125">L'idea è di effettuare il push delle superfici in modo sufficiente durante il rendering di un buffer di ombreggiatura, in modo che il risultato del confronto (tra il buffer di ombreggiatura z e lo shader z) sia coerente sulla superficie ed eviti l'ombreggiatura automatica locale.</span><span class="sxs-lookup"><span data-stu-id="f1adf-125">The idea is to push surfaces out enough while rendering a shadow buffer so that the comparison result (between the shadow buffer z and the shader z) is consistent across the surface, and avoid local self-shadowing.</span></span>

<span data-ttu-id="f1adf-126">Tuttavia, l'uso di **DepthBias** e **SlopeScaledDepthBias** può introdurre nuovi problemi di rendering quando un poligono visualizzato a un angolo estremamente acuto causa la generazione di un valore z molto grande nell'equazione di distorsione.</span><span class="sxs-lookup"><span data-stu-id="f1adf-126">However, using **DepthBias** and **SlopeScaledDepthBias** can introduce new rendering problems when a polygon viewed at an extremely sharp angle causes the bias equation to generate a very large z value.</span></span> <span data-ttu-id="f1adf-127">Questa operazione effettua il push del poligono molto lontano dalla superficie originale nella mappa Shadow.</span><span class="sxs-lookup"><span data-stu-id="f1adf-127">This in effect pushes the polygon extremely far away from the original surface in the shadow map.</span></span> <span data-ttu-id="f1adf-128">Un modo per risolvere questo particolare problema consiste nell'usare **DepthBiasClamp**, che fornisce un limite superiore (positivo o negativo) sulla grandezza della distorsione z calcolata.</span><span class="sxs-lookup"><span data-stu-id="f1adf-128">One way to help alleviate this particular problem is to use **DepthBiasClamp**, which provides an upper bound (positive or negative) on the magnitude of the z bias calculated.</span></span>

> [!Note]  
> <span data-ttu-id="f1adf-129">Per i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1adf-129">For [feature levels](overviews-direct3d-11-devices-downlevel-intro.md) 9.1, 9.2, 9.3, **DepthBiasClamp** is not supported.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f1adf-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1adf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1adf-131">Output-fase di Unione</span><span class="sxs-lookup"><span data-stu-id="f1adf-131">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




