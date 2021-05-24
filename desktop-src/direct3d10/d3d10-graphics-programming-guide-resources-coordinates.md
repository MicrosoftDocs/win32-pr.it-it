---
description: I sistemi di coordinate per Direct3D 10 sono definiti per pixel e texel.
ms.assetid: c8c269e7-6e2a-4b5d-847c-6779e276b9af
title: Sistemi di coordinate (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3da846ae4b989f6d8cb4741f9df8f7228e8970
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335465"
---
# <a name="coordinate-systems-direct3d-10"></a><span data-ttu-id="e99ae-103">Sistemi di coordinate (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e99ae-103">Coordinate Systems (Direct3D 10)</span></span>

<span data-ttu-id="e99ae-104">I sistemi di coordinate per Direct3D 10 sono definiti per pixel e texel.</span><span class="sxs-lookup"><span data-stu-id="e99ae-104">Coordinate systems for Direct3D 10 are defined for pixels and texels.</span></span>



<span data-ttu-id="e99ae-105">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="e99ae-105">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="e99ae-106">Direct3D 10 definisce l'angolo superiore sinistro del pixel superiore sinistro come origine di una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e99ae-106">Direct3D 10 defines the upper-left corner of the upper-left pixel as the origin of a render target.</span></span>
- <span data-ttu-id="e99ae-107">Direct3D 9 definisce il centro del pixel superiore sinistro come origine di una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="e99ae-107">Direct3D 9 defines the center of the upper-left pixel as the origin of a render target.</span></span>



 

[<span data-ttu-id="e99ae-108">Sistema di coordinate pixel</span><span class="sxs-lookup"><span data-stu-id="e99ae-108">Pixel Coordinate System</span></span>](#pixel-coordinate-system)
- [<span data-ttu-id="e99ae-109">Sistema di coordinate pixel per Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="e99ae-109">Pixel Coordinate System for Direct3D 9</span></span>](#pixel-coordinate-system-for-direct3d-9)

[<span data-ttu-id="e99ae-110">Sistema di coordinate Texel</span><span class="sxs-lookup"><span data-stu-id="e99ae-110">Texel Coordinate System</span></span>](#texel-coordinate-system)
- [<span data-ttu-id="e99ae-111">Sistema di coordinate Texel</span><span class="sxs-lookup"><span data-stu-id="e99ae-111">Texel Coordinate System</span></span>](#texel-coordinate-system)

[<span data-ttu-id="e99ae-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e99ae-112">Related topics</span></span>](#related-topics)

## <a name="pixel-coordinate-system"></a><span data-ttu-id="e99ae-113">Sistema di coordinate pixel</span><span class="sxs-lookup"><span data-stu-id="e99ae-113">Pixel Coordinate System</span></span>

<span data-ttu-id="e99ae-114">Il sistema di coordinate pixel in Direct3D 10 definisce l'origine di una destinazione di rendering nell'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="e99ae-114">The pixel coordinate system in Direct3D 10 defines the origin of a render target at the upper-left corner.</span></span> <span data-ttu-id="e99ae-115">come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="e99ae-115">as shown in the following diagram.</span></span> <span data-ttu-id="e99ae-116">I centri pixel vengono offset da (0,5f,0,5f) dalle posizioni di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="e99ae-116">Pixel centers are offset by (0.5f,0.5f) from integer locations.</span></span>

![diagramma del sistema di coordinate pixel in direct3d 10](images/d3d10-coordspix10.png)

### <a name="pixel-coordinate-system-for-direct3d-9"></a><span data-ttu-id="e99ae-118">Sistema di coordinate pixel per Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="e99ae-118">Pixel Coordinate System for Direct3D 9</span></span>

<span data-ttu-id="e99ae-119">Come riferimento, di seguito è riportato il sistema di coordinate pixel per Direct3D 9, che ha definito l'origine o una destinazione di rendering come centro del pixel superiore sinistro,(0,5,0.5) lontano dall'angolo superiore sinistro, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="e99ae-119">For reference, here is the pixel coordinate system for Direct3D 9, which defined the origin or a render target as the center of the upper-left pixel, (0.5,0.5) away from the upper left corner, as shown in the following diagram.</span></span> <span data-ttu-id="e99ae-120">In Direct3D 9 i pixel center sono in posizioni intere.</span><span class="sxs-lookup"><span data-stu-id="e99ae-120">In Direct3D 9, pixel centers are at integer locations.</span></span>

![diagramma del sistema di coordinate pixel in direct3d 9](images/d3d10-coordspix9.png)

## <a name="texel-coordinate-system"></a><span data-ttu-id="e99ae-122">Sistema di coordinate texel</span><span class="sxs-lookup"><span data-stu-id="e99ae-122">Texel Coordinate System</span></span>

<span data-ttu-id="e99ae-123">Il sistema di coordinate texel ha l'origine nell'angolo superiore sinistro della trama, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="e99ae-123">The texel coordinate system has its origin at the top-left corner of the texture, as shown in the following diagram.</span></span> <span data-ttu-id="e99ae-124">In questo modo, il rendering delle trame allineate sullo schermo è semplice (in Direct3D 10), perché il sistema di coordinate pixel è allineato al sistema di coordinate texel.</span><span class="sxs-lookup"><span data-stu-id="e99ae-124">This makes rendering screen-aligned textures trivial (in Direct3D 10), as the pixel coordinate system is aligned with the texel coordinate system.</span></span>

![diagramma del sistema di coordinate texel](images/d3d10-coordstex10.png)

### <a name="texel-coordinate-system"></a><span data-ttu-id="e99ae-126">Sistema di coordinate texel</span><span class="sxs-lookup"><span data-stu-id="e99ae-126">Texel Coordinate System</span></span>

<span data-ttu-id="e99ae-127">Le coordinate della trama sono rappresentate con un numero normalizzato o ridimensionato. Ogni coordinata di trama viene mappata a un texel specifico come segue:</span><span class="sxs-lookup"><span data-stu-id="e99ae-127">Texture coordinates are represented with either a normalized or a scaled number; each texture coordinate is mapped to a specific texel as follows:</span></span>

<span data-ttu-id="e99ae-128">Per una coordinata normalizzata:</span><span class="sxs-lookup"><span data-stu-id="e99ae-128">For a normalized coordinate:</span></span>

-   <span data-ttu-id="e99ae-129">Campionamento dei punti: Texel \# = floor(U \* Width)</span><span class="sxs-lookup"><span data-stu-id="e99ae-129">Point sampling: Texel \# = floor(U \* Width)</span></span>
-   <span data-ttu-id="e99ae-130">Campionamento lineare: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span><span class="sxs-lookup"><span data-stu-id="e99ae-130">Linear sampling: Left Texel \# = floor(U \* Width), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="e99ae-131">Per una coordinata ridimensionata:</span><span class="sxs-lookup"><span data-stu-id="e99ae-131">For a scaled coordinate:</span></span>

-   <span data-ttu-id="e99ae-132">Campionamento dei punti: Texel \# = floor(U)</span><span class="sxs-lookup"><span data-stu-id="e99ae-132">Point sampling: Texel \# = floor(U)</span></span>
-   <span data-ttu-id="e99ae-133">Campionamento lineare: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span><span class="sxs-lookup"><span data-stu-id="e99ae-133">Linear sampling: Left Texel \# = floor(U - 0.5), Right Texel \# = Left Texel \# + 1</span></span>

<span data-ttu-id="e99ae-134">Dove larghezza, è la larghezza della trama (in texel).</span><span class="sxs-lookup"><span data-stu-id="e99ae-134">Where the width, is the width of the texture (in texels).</span></span>

<span data-ttu-id="e99ae-135">La disposizione degli indirizzi di trama si verifica dopo il calcolo della posizione del texel.</span><span class="sxs-lookup"><span data-stu-id="e99ae-135">Texture address wrapping occurs after the texel location is computed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e99ae-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e99ae-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e99ae-137">Risorse (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e99ae-137">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




