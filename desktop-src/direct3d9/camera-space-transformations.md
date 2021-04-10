---
description: I vertici nello spazio della fotocamera vengono calcolati trasformando i vertici degli oggetti con la matrice di visualizzazione globale.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Trasformazioni dello spazio della fotocamera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126883"
---
# <a name="camera-space-transformations-direct3d-9"></a><span data-ttu-id="c32d1-103">Trasformazioni dello spazio della fotocamera (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c32d1-103">Camera Space Transformations (Direct3D 9)</span></span>

<span data-ttu-id="c32d1-104">I vertici nello spazio della fotocamera vengono calcolati trasformando i vertici degli oggetti con la matrice di visualizzazione globale.</span><span class="sxs-lookup"><span data-stu-id="c32d1-104">Vertices in the camera space are computed by transforming the object vertices with the world view matrix.</span></span>

<span data-ttu-id="c32d1-105">V = V \* wvMatrix</span><span class="sxs-lookup"><span data-stu-id="c32d1-105">V = V \* wvMatrix</span></span>

<span data-ttu-id="c32d1-106">Le normali dei vertici, nello spazio della fotocamera, vengono calcolate trasformando le normali dell'oggetto con la trasformazione inversa della matrice di visualizzazione globale.</span><span class="sxs-lookup"><span data-stu-id="c32d1-106">Vertex normals, in camera space, are computed by transforming the object normals with the inverse transpose of the world view matrix.</span></span> <span data-ttu-id="c32d1-107">La matrice della vista globale può essere o non essere ortogonale.</span><span class="sxs-lookup"><span data-stu-id="c32d1-107">The world view matrix may or may not be orthogonal.</span></span>

<span data-ttu-id="c32d1-108">N = N \* (wvMatrix ⁻ ¹)<sup>T</sup></span><span class="sxs-lookup"><span data-stu-id="c32d1-108">N = N \* (wvMatrix⁻¹)<sup>T</sup></span></span>

<span data-ttu-id="c32d1-109">La matrice inversion e la matrice TRANSPOSE operano su una matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="c32d1-109">The matrix inversion and matrix transpose operate on a 4x4 matrix.</span></span> <span data-ttu-id="c32d1-110">L'oggetto Multiply combina il normale con la parte 3x3 della matrice 4x4 risultante.</span><span class="sxs-lookup"><span data-stu-id="c32d1-110">The multiply combines the normal with the 3x3 portion of the resulting 4x4 matrix.</span></span>

<span data-ttu-id="c32d1-111">Se lo stato di rendering, D3DRENDERSTATE \_ NORMALIZENORMALS è impostato su **true**, i vettori normali dei vertici vengono normalizzati dopo la trasformazione nello spazio della fotocamera, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c32d1-111">If the render state, D3DRENDERSTATE\_NORMALIZENORMALS is set to **TRUE**, vertex normal vectors are normalized after transformation to camera space as follows:</span></span>

<span data-ttu-id="c32d1-112">N = Norm (N)</span><span class="sxs-lookup"><span data-stu-id="c32d1-112">N = norm(N)</span></span>

<span data-ttu-id="c32d1-113">La posizione della luce nello spazio della fotocamera viene calcolata trasformando la posizione di origine della luce con la matrice di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c32d1-113">Light position in camera space is computed by transforming the light source position with the view matrix.</span></span>

<span data-ttu-id="c32d1-114">LP = LP \* vMatrix</span><span class="sxs-lookup"><span data-stu-id="c32d1-114">Lₚ = Lₚ \* vMatrix</span></span>

<span data-ttu-id="c32d1-115">La direzione verso la luce nello spazio della fotocamera per una luce direzionale viene calcolata moltiplicando la direzione della sorgente di luce per la matrice di visualizzazione, normalizzando e negando il risultato.</span><span class="sxs-lookup"><span data-stu-id="c32d1-115">The direction to the light in camera space for a directional light is computed by multiplying the light source direction by the view matrix, normalizing, and negating the result.</span></span>

<span data-ttu-id="c32d1-116">L<sub>dir</sub> =-Norm (L<sub>dir</sub> \* wvMatrix)</span><span class="sxs-lookup"><span data-stu-id="c32d1-116">L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)</span></span>

<span data-ttu-id="c32d1-117">Per il \_ punto di D3DLIGHT e D3DLIGHT, \_ la direzione verso la luce viene calcolata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="c32d1-117">For the D3DLIGHT\_POINT and D3DLIGHT\_SPOT the direction to light is computed as follows:</span></span>

<span data-ttu-id="c32d1-118">L<sub>dir</sub> = Norm (V \* LP), in cui i parametri sono definiti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c32d1-118">L<sub>dir</sub> = norm(V \* Lₚ), where the parameters are defined in the following table.</span></span>



| <span data-ttu-id="c32d1-119">Parametro</span><span class="sxs-lookup"><span data-stu-id="c32d1-119">Parameter</span></span>       | <span data-ttu-id="c32d1-120">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c32d1-120">Default value</span></span> | <span data-ttu-id="c32d1-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c32d1-121">Type</span></span>      | <span data-ttu-id="c32d1-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c32d1-122">Description</span></span>                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <span data-ttu-id="c32d1-123"><sub>Dir</sub></span><span class="sxs-lookup"><span data-stu-id="c32d1-123">L<sub>dir</sub></span></span> | <span data-ttu-id="c32d1-124">N/D</span><span class="sxs-lookup"><span data-stu-id="c32d1-124">N/A</span></span>           | <span data-ttu-id="c32d1-125">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c32d1-125">D3DVECTOR</span></span> | <span data-ttu-id="c32d1-126">Vettore direzione dal vertice dell'oggetto alla luce</span><span class="sxs-lookup"><span data-stu-id="c32d1-126">Direction vector from object vertex to the light</span></span>          |
| <span data-ttu-id="c32d1-127">V</span><span class="sxs-lookup"><span data-stu-id="c32d1-127">V</span></span>               | <span data-ttu-id="c32d1-128">N/D</span><span class="sxs-lookup"><span data-stu-id="c32d1-128">N/A</span></span>           | <span data-ttu-id="c32d1-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c32d1-129">D3DVECTOR</span></span> | <span data-ttu-id="c32d1-130">Posizione vertice nello spazio della fotocamera</span><span class="sxs-lookup"><span data-stu-id="c32d1-130">Vertex position in camera space</span></span>                           |
| <span data-ttu-id="c32d1-131">wvMatrix</span><span class="sxs-lookup"><span data-stu-id="c32d1-131">wvMatrix</span></span>        | <span data-ttu-id="c32d1-132">Identità</span><span class="sxs-lookup"><span data-stu-id="c32d1-132">Identity</span></span>      | <span data-ttu-id="c32d1-133">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="c32d1-133">D3DMATRIX</span></span> | <span data-ttu-id="c32d1-134">Matrice composita contenente le trasformazioni globali e di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="c32d1-134">Composite matrix containing the world and view transforms</span></span> |
| <span data-ttu-id="c32d1-135">N</span><span class="sxs-lookup"><span data-stu-id="c32d1-135">N</span></span>               | <span data-ttu-id="c32d1-136">N/D</span><span class="sxs-lookup"><span data-stu-id="c32d1-136">N/A</span></span>           | <span data-ttu-id="c32d1-137">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c32d1-137">D3DVECTOR</span></span> | <span data-ttu-id="c32d1-138">Normale vertice</span><span class="sxs-lookup"><span data-stu-id="c32d1-138">Vertex normal</span></span>                                             |
| <span data-ttu-id="c32d1-139">LP</span><span class="sxs-lookup"><span data-stu-id="c32d1-139">Lₚ</span></span>              | <span data-ttu-id="c32d1-140">N/D</span><span class="sxs-lookup"><span data-stu-id="c32d1-140">N/A</span></span>           | <span data-ttu-id="c32d1-141">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="c32d1-141">D3DVECTOR</span></span> | <span data-ttu-id="c32d1-142">Posizione chiara nello spazio della fotocamera</span><span class="sxs-lookup"><span data-stu-id="c32d1-142">Light position in camera space</span></span>                            |
| <span data-ttu-id="c32d1-143">vMatrix</span><span class="sxs-lookup"><span data-stu-id="c32d1-143">vMatrix</span></span>         | <span data-ttu-id="c32d1-144">Identità</span><span class="sxs-lookup"><span data-stu-id="c32d1-144">Identity</span></span>      | <span data-ttu-id="c32d1-145">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="c32d1-145">D3DMATRIX</span></span> | <span data-ttu-id="c32d1-146">Matrice contenente la trasformazione visualizzazione</span><span class="sxs-lookup"><span data-stu-id="c32d1-146">Matrix containing the view transform</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="c32d1-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c32d1-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c32d1-148">Matematica dell'illuminazione</span><span class="sxs-lookup"><span data-stu-id="c32d1-148">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



