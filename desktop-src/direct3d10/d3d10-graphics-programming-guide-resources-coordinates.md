---
description: I sistemi di coordinate per Direct3D 10 sono definiti per pixel e Texel.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemi di coordinate (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba84cd7d807474a1ff41f873d16cbd7eee07224
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748970"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="69439-103">Sistemi di coordinate (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="69439-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="69439-104">I sistemi di coordinate per Direct3D 10 sono definiti per pixel e Texel.</span><span class="sxs-lookup"><span data-stu-id="69439-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



|                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69439-105">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="69439-105">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="69439-106">Direct3D 10 definisce l'angolo superiore sinistro del pixel superiore sinistro come origine di una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="69439-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span><br/> <span data-ttu-id="69439-107">Direct3D 9 definisce il centro del pixel superiore sinistro come origine di una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="69439-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span><br/> |



 

-   [<span data-ttu-id="69439-108">Sistema di coordinate pixel</span><span class="sxs-lookup"><span data-stu-id="69439-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
    -   [<span data-ttu-id="69439-109">Sistema di coordinate pixel per Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="69439-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)
-   [<span data-ttu-id="69439-110">Sistema di coordinate Texel</span><span class="sxs-lookup"><span data-stu-id="69439-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
    -   [<span data-ttu-id="69439-111">Sistema di coordinate Texel</span><span class="sxs-lookup"><span data-stu-id="69439-111">Texel Coordinate System</span></span>](#texel-coordinate-system)
-   [<span data-ttu-id="69439-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69439-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="69439-113">Sistema di coordinate pixel</span><span class="sxs-lookup"><span data-stu-id="69439-113">Pixel Coordinate System</span></span>

<span data-ttu-id="69439-114">Il sistema di coordinate pixel in Direct3D 10 definisce l'origine di una destinazione di rendering nell'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="69439-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="69439-115">come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="69439-115">as shown in the following diagram.</span></span> <span data-ttu-id="69439-116">I centri pixel sono offset di (0,5 f, 0,5 f) dalle posizioni intere.</span><span class="sxs-lookup"><span data-stu-id="69439-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![diagramma del sistema di coordinate pixel in Direct3D 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="69439-118">Sistema di coordinate pixel per Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="69439-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="69439-119">Come riferimento, di seguito è riportato il sistema di coordinate pixel per Direct3D 9, che ha definito l'origine o una destinazione di rendering come centro del pixel superiore sinistro, (0,5, 0,5) dall'angolo superiore sinistro, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="69439-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="69439-120">In Direct3D 9 i pixel Center si trovano in posizioni di tipo Integer.</span><span class="sxs-lookup"><span data-stu-id="69439-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![diagramma del sistema di coordinate pixel in Direct3D 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="69439-122">Sistema di coordinate Texel</span><span class="sxs-lookup"><span data-stu-id="69439-122">Texel Coordinate System</span></span>

<span data-ttu-id="69439-123">Il sistema di coordinate Texel ha origine nell'angolo superiore sinistro della trama, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="69439-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="69439-124">In questo modo si rende semplice il rendering delle trame allineate allo schermo (in Direct3D 10), perché il sistema di coordinate pixel è allineato con il sistema di coordinate Texel.</span><span class="sxs-lookup"><span data-stu-id="69439-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![diagramma del sistema di coordinate Texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="69439-126">Sistema di coordinate Texel</span><span class="sxs-lookup"><span data-stu-id="69439-126">Texel Coordinate System</span></span>

<span data-ttu-id="69439-127">Le coordinate di trama sono rappresentate con un numero normalizzato o ridimensionato; ogni coordinata di trama viene mappata a un Texel specifico, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="69439-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="69439-128">Per una coordinata normalizzata:</span><span class="sxs-lookup"><span data-stu-id="69439-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="69439-129">Campionamento di punti: Texel \# = Floor (U \* Width)</span><span class="sxs-lookup"><span data-stu-id="69439-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="69439-130">Campionamento lineare: a sinistra Texel \# = Floor (U \* Width), right Texel \# = Left Texel \# + 1</span><span class="sxs-lookup"><span data-stu-id="69439-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="69439-131">Per una coordinata ridimensionata:</span><span class="sxs-lookup"><span data-stu-id="69439-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="69439-132">Campionamento di punti: Texel \# = Floor (U)</span><span class="sxs-lookup"><span data-stu-id="69439-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="69439-133">Campionamento lineare: a sinistra Texel \# = Floor (U-0,5), right Texel \# = Left Texel \# + 1</span><span class="sxs-lookup"><span data-stu-id="69439-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="69439-134">Dove Width è la larghezza della trama (in Texels).</span><span class="sxs-lookup"><span data-stu-id="69439-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="69439-135">Il wrapping degli indirizzi di trama si verifica dopo il calcolo della posizione di Texel.</span><span class="sxs-lookup"><span data-stu-id="69439-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69439-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69439-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69439-137">Risorse (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="69439-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




