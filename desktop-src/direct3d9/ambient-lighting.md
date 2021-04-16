---
description: Illuminazione ambientale fornisce illuminazione costante per una scena.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Illuminazione ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523841"
---
# <a name="ambient-lighting-direct3d-9"></a><span data-ttu-id="1608a-103">Illuminazione ambiente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1608a-103">Ambient Lighting (Direct3D 9)</span></span>

<span data-ttu-id="1608a-104">Illuminazione ambientale fornisce illuminazione costante per una scena.</span><span class="sxs-lookup"><span data-stu-id="1608a-104">Ambient lighting provides constant lighting for a scene.</span></span> <span data-ttu-id="1608a-105">Illumina tutti i vertici degli oggetti allo stesso modo perché non dipende da altri fattori di illuminazione quali le normali dei vertici, la direzione della luce, la posizione della luce, l'intervallo o l'attenuazione.</span><span class="sxs-lookup"><span data-stu-id="1608a-105">It lights all object vertices the same because it is not dependent on any other lighting factors such as vertex normals, light direction, light position, range, or attenuation.</span></span> <span data-ttu-id="1608a-106">Si tratta del tipo di illuminazione più veloce, ma produce i risultati meno realistici.</span><span class="sxs-lookup"><span data-stu-id="1608a-106">It is the fastest type of lighting but it produces the least realistic results.</span></span> <span data-ttu-id="1608a-107">Direct3D contiene una singola proprietà di ambiente chiaro globale che è possibile usare senza creare alcuna luce.</span><span class="sxs-lookup"><span data-stu-id="1608a-107">Direct3D contains a single global ambient light property that you can use without creating any light.</span></span> <span data-ttu-id="1608a-108">In alternativa, è possibile impostare qualsiasi oggetto chiaro per fornire l'illuminazione ambientale.</span><span class="sxs-lookup"><span data-stu-id="1608a-108">Alternatively, you can set any light object to provide ambient lighting.</span></span> <span data-ttu-id="1608a-109">L'illuminazione ambientale per una scena è descritta dall'equazione seguente.</span><span class="sxs-lookup"><span data-stu-id="1608a-109">The ambient lighting for a scene is described by the following equation.</span></span>

<span data-ttu-id="1608a-110">Illuminazione ambiente = C ₐ \* \[ g ₐ + Sum (atten<sub>io</sub> \* spot<sub>i</sub> \* L<sub>ai</sub>)\]</span><span class="sxs-lookup"><span data-stu-id="1608a-110">Ambient Lighting = Cₐ\*\[Gₐ + sum(Atten<sub>i</sub>\*Spot<sub>i</sub>\*L<sub>ai</sub>)\]</span></span>

<span data-ttu-id="1608a-111">Dove:</span><span class="sxs-lookup"><span data-stu-id="1608a-111">Where:</span></span>



| <span data-ttu-id="1608a-112">Parametro</span><span class="sxs-lookup"><span data-stu-id="1608a-112">Parameter</span></span>         | <span data-ttu-id="1608a-113">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="1608a-113">Default value</span></span> | <span data-ttu-id="1608a-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="1608a-114">Type</span></span>          | <span data-ttu-id="1608a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1608a-115">Description</span></span>                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1608a-116">C ₐ</span><span class="sxs-lookup"><span data-stu-id="1608a-116">Cₐ</span></span>                | <span data-ttu-id="1608a-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="1608a-117">(0,0,0,0)</span></span>     | <span data-ttu-id="1608a-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="1608a-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="1608a-119">Colore ambiente materiale</span><span class="sxs-lookup"><span data-stu-id="1608a-119">Material ambient color</span></span>                                                                                                         |
| <span data-ttu-id="1608a-120">G ₐ</span><span class="sxs-lookup"><span data-stu-id="1608a-120">Gₐ</span></span>                | <span data-ttu-id="1608a-121">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="1608a-121">(0,0,0,0)</span></span>     | <span data-ttu-id="1608a-122">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="1608a-122">D3DCOLORVALUE</span></span> | <span data-ttu-id="1608a-123">Colore ambiente globale</span><span class="sxs-lookup"><span data-stu-id="1608a-123">Global ambient color</span></span>                                                                                                           |
| <span data-ttu-id="1608a-124">Atten<sub></sub></span><span class="sxs-lookup"><span data-stu-id="1608a-124">Atten<sub>i</sub></span></span> | <span data-ttu-id="1608a-125">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="1608a-125">(0,0,0,0)</span></span>     | <span data-ttu-id="1608a-126">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="1608a-126">D3DCOLORVALUE</span></span> | <span data-ttu-id="1608a-127">Attenuazione chiara della luce del ith.</span><span class="sxs-lookup"><span data-stu-id="1608a-127">Light attenuation of the ith light.</span></span> <span data-ttu-id="1608a-128">Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="1608a-128">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="1608a-129">Spot<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="1608a-129">Spot<sub>i</sub></span></span>  | <span data-ttu-id="1608a-130">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="1608a-130">(0,0,0,0)</span></span>     | <span data-ttu-id="1608a-131">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1608a-131">D3DVECTOR</span></span>     | <span data-ttu-id="1608a-132">Fattore di Spotlight della luce di Ith.</span><span class="sxs-lookup"><span data-stu-id="1608a-132">Spotlight factor of the ith light.</span></span> <span data-ttu-id="1608a-133">Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="1608a-133">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |
| <span data-ttu-id="1608a-134">Sum</span><span class="sxs-lookup"><span data-stu-id="1608a-134">sum</span></span>               | <span data-ttu-id="1608a-135">N/D</span><span class="sxs-lookup"><span data-stu-id="1608a-135">N/A</span></span>           | <span data-ttu-id="1608a-136">N/D</span><span class="sxs-lookup"><span data-stu-id="1608a-136">N/A</span></span>           | <span data-ttu-id="1608a-137">Somma della luce di ambiente</span><span class="sxs-lookup"><span data-stu-id="1608a-137">Sum of the ambient light</span></span>                                                                                                       |
| <span data-ttu-id="1608a-138">L<sub>ai</sub></span><span class="sxs-lookup"><span data-stu-id="1608a-138">L<sub>ai</sub></span></span>    | <span data-ttu-id="1608a-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="1608a-139">(0,0,0,0)</span></span>     | <span data-ttu-id="1608a-140">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="1608a-140">D3DVECTOR</span></span>     | <span data-ttu-id="1608a-141">Colore di ambiente chiaro della luce del ith</span><span class="sxs-lookup"><span data-stu-id="1608a-141">Light ambient color of the ith light</span></span>                                                                                           |



 

<span data-ttu-id="1608a-142">Il valore per C ₐ è:</span><span class="sxs-lookup"><span data-stu-id="1608a-142">The value for Cₐ is either:</span></span>

-   <span data-ttu-id="1608a-143">Vertex color1, se AMBIENTMATERIALSOURCE = D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="1608a-143">vertex color1, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="1608a-144">Vertex color2, se AMBIENTMATERIALSOURCE = D3DMCS \_ color2, e il secondo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="1608a-144">vertex color2, if AMBIENTMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in vertex declaration.</span></span>
-   <span data-ttu-id="1608a-145">colore ambiente materiale.</span><span class="sxs-lookup"><span data-stu-id="1608a-145">material ambient color.</span></span>

> [!Note]  
> <span data-ttu-id="1608a-146">Se si usa l'opzione AMBIENTMATERIALSOURCE e il colore del vertice non viene specificato, viene usato il colore di ambiente Material.</span><span class="sxs-lookup"><span data-stu-id="1608a-146">If either AMBIENTMATERIALSOURCE option is used, and the vertex color is not provided, then the material ambient color is used.</span></span>

 

<span data-ttu-id="1608a-147">Per utilizzare il colore di ambiente Material, utilizzare sematerial come illustrato nel codice di esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="1608a-147">To use the material ambient color, use SetMaterial as shown in the example code below.</span></span>

<span data-ttu-id="1608a-148">G ₐ è il colore di ambiente globale.</span><span class="sxs-lookup"><span data-stu-id="1608a-148">Gₐ is the global ambient color.</span></span> <span data-ttu-id="1608a-149">Viene impostato mediante SetRenderState (D3DRS \_ Ambient).</span><span class="sxs-lookup"><span data-stu-id="1608a-149">It is set using SetRenderState(D3DRS\_AMBIENT).</span></span> <span data-ttu-id="1608a-150">In una scena Direct3D esiste un solo colore di ambiente globale.</span><span class="sxs-lookup"><span data-stu-id="1608a-150">There is one global ambient color in a Direct3D scene.</span></span> <span data-ttu-id="1608a-151">Questo parametro non è associato a un oggetto Direct3D Light.</span><span class="sxs-lookup"><span data-stu-id="1608a-151">This parameter is not associated with a Direct3D light object.</span></span>

<span data-ttu-id="1608a-152">L<sub>ai</sub> è il colore di ambiente della luce del ith nella scena.</span><span class="sxs-lookup"><span data-stu-id="1608a-152">L<sub>ai</sub> is the ambient color of the ith light in the scene.</span></span> <span data-ttu-id="1608a-153">Ogni Direct3D Light ha un set di proprietà, uno dei quali è il colore di ambiente.</span><span class="sxs-lookup"><span data-stu-id="1608a-153">Each Direct3D light has a set of properties, one of which is the ambient color.</span></span> <span data-ttu-id="1608a-154">Il termine Sum (L<sub>ai</sub>) è una somma di tutti i colori di ambiente nella scena.</span><span class="sxs-lookup"><span data-stu-id="1608a-154">The term, sum(L<sub>ai</sub>) is a sum of all the ambient colors in the scene.</span></span>

## <a name="example"></a><span data-ttu-id="1608a-155">Esempio</span><span class="sxs-lookup"><span data-stu-id="1608a-155">Example</span></span>

<span data-ttu-id="1608a-156">In questo esempio, l'oggetto è colorato usando la luce ambientale della scena e un colore di ambiente di materiale.</span><span class="sxs-lookup"><span data-stu-id="1608a-156">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span>


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



<span data-ttu-id="1608a-157">In base all'equazione, il colore risultante per i vertici dell'oggetto è una combinazione del colore del materiale e del colore chiaro.</span><span class="sxs-lookup"><span data-stu-id="1608a-157">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="1608a-158">Le due illustrazioni seguenti mostrano il colore del materiale, che è grigio, e il colore chiaro, che è rosso chiaro.</span><span class="sxs-lookup"><span data-stu-id="1608a-158">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera rossa](images/lightred.jpg)

<span data-ttu-id="1608a-161">La scena risultante è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="1608a-161">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="1608a-162">L'unico oggetto nella scena è una sfera.</span><span class="sxs-lookup"><span data-stu-id="1608a-162">The only object in the scene is a sphere.</span></span> <span data-ttu-id="1608a-163">La luce di ambiente illumina tutti i vertici degli oggetti con lo stesso colore.</span><span class="sxs-lookup"><span data-stu-id="1608a-163">Ambient light lights all object vertices with the same color.</span></span> <span data-ttu-id="1608a-164">Non dipende dal vertice normale o dalla direzione della luce.</span><span class="sxs-lookup"><span data-stu-id="1608a-164">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="1608a-165">Di conseguenza, la sfera appare come un cerchio 2D perché non esiste alcuna differenza nell'ombreggiatura intorno alla superficie dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1608a-165">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![illustrazione di una sfera con illuminazione ambientale](images/lighta.jpg)

<span data-ttu-id="1608a-167">Per fornire agli oggetti un aspetto più realistico, applicare un'illuminazione diffusa o speculare oltre all'illuminazione ambientale.</span><span class="sxs-lookup"><span data-stu-id="1608a-167">To give objects a more realistic look, apply diffuse or specular lighting in addition to ambient lighting.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1608a-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1608a-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1608a-169">Matematica dell'illuminazione</span><span class="sxs-lookup"><span data-stu-id="1608a-169">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



