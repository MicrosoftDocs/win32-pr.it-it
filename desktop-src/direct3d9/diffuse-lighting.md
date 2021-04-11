---
description: Dopo aver modificato l'intensità di luce per qualsiasi effetto di attenuazione, il motore di illuminazione calcola la quantità di luce rimanente riflessa da un vertice, dato l'angolo della normale del vertice e la direzione della luce dell'evento imprevisto.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Illuminazione diffusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123375"
---
# <a name="diffuse-lighting-direct3d-9"></a><span data-ttu-id="0b5bb-103">Illuminazione diffusa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0b5bb-103">Diffuse Lighting (Direct3D 9)</span></span>

<span data-ttu-id="0b5bb-104">Dopo aver modificato l'intensità di luce per qualsiasi effetto di attenuazione, il motore di illuminazione calcola la quantità di luce rimanente riflessa da un vertice, dato l'angolo della normale del vertice e la direzione della luce dell'evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-104">After adjusting the light intensity for any attenuation effects, the lighting engine computes how much of the remaining light reflects from a vertex, given the angle of the vertex normal and the direction of the incident light.</span></span> <span data-ttu-id="0b5bb-105">Il motore di illuminazione passa a questo passaggio per le spie direzionali perché non attenuano la distanza.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-105">The lighting engine skips to this step for directional lights because they do not attenuate over distance.</span></span> <span data-ttu-id="0b5bb-106">Il sistema considera due tipi di reflection, diffusi e speculari, e usa una formula diversa per determinare la quantità di luce che viene riflessa per ciascuna di esse.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-106">The system considers two reflection types, diffuse and specular, and uses a different formula to determine how much light is reflected for each.</span></span> <span data-ttu-id="0b5bb-107">Dopo aver calcolato la quantità di luce riflessa, Direct3D applica questi nuovi valori alle proprietà di Reflection diffusa e speculare del materiale corrente.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-107">After calculating the amounts of light reflected, Direct3D applies these new values to the diffuse and specular reflectance properties of the current material.</span></span> <span data-ttu-id="0b5bb-108">I valori dei colori risultanti sono i componenti di diffusione e speculare usati dal rasterizzatore per produrre l'ombreggiatura Gouraud e l'evidenziazione speculare.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-108">The resulting color values are the diffuse and specular components that the rasterizer uses to produce Gouraud shading and specular highlighting.</span></span>

<span data-ttu-id="0b5bb-109">L'illuminazione diffusa è descritta dalla seguente equazione.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-109">Diffuse lighting is described by the following equation.</span></span>

<span data-ttu-id="0b5bb-110">Illuminazione diffusa = somma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* atten \* spot\]</span><span class="sxs-lookup"><span data-stu-id="0b5bb-110">Diffuse Lighting = sum\[C<sub>d</sub>\*L<sub>d</sub>\*(N<sup>.</sup>L<sub>dir</sub>)\*Atten\*Spot\]</span></span>



| <span data-ttu-id="0b5bb-111">Parametro</span><span class="sxs-lookup"><span data-stu-id="0b5bb-111">Parameter</span></span>       | <span data-ttu-id="0b5bb-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="0b5bb-112">Default value</span></span> | <span data-ttu-id="0b5bb-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="0b5bb-113">Type</span></span>          | <span data-ttu-id="0b5bb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b5bb-114">Description</span></span>                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b5bb-115">Sum</span><span class="sxs-lookup"><span data-stu-id="0b5bb-115">sum</span></span>             | <span data-ttu-id="0b5bb-116">N/D</span><span class="sxs-lookup"><span data-stu-id="0b5bb-116">N/A</span></span>           | <span data-ttu-id="0b5bb-117">N/D</span><span class="sxs-lookup"><span data-stu-id="0b5bb-117">N/A</span></span>           | <span data-ttu-id="0b5bb-118">Sommatoria del componente diffuso di ogni luce.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-118">Summation of each light's diffuse component.</span></span>                                                                  |
| <span data-ttu-id="0b5bb-119">C<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="0b5bb-119">C<sub>d</sub></span></span>   | <span data-ttu-id="0b5bb-120">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="0b5bb-120">(0,0,0,0)</span></span>     | <span data-ttu-id="0b5bb-121">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="0b5bb-121">D3DCOLORVALUE</span></span> | <span data-ttu-id="0b5bb-122">Colore diffuso.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-122">Diffuse color.</span></span>                                                                                                |
| <span data-ttu-id="0b5bb-123">L<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="0b5bb-123">L<sub>d</sub></span></span>   | <span data-ttu-id="0b5bb-124">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="0b5bb-124">(0,0,0,0)</span></span>     | <span data-ttu-id="0b5bb-125">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="0b5bb-125">D3DCOLORVALUE</span></span> | <span data-ttu-id="0b5bb-126">Colore diffuso chiaro.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-126">Light diffuse color.</span></span>                                                                                          |
| <span data-ttu-id="0b5bb-127">N</span><span class="sxs-lookup"><span data-stu-id="0b5bb-127">N</span></span>               | <span data-ttu-id="0b5bb-128">N/D</span><span class="sxs-lookup"><span data-stu-id="0b5bb-128">N/A</span></span>           | <span data-ttu-id="0b5bb-129">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0b5bb-129">D3DVECTOR</span></span>     | <span data-ttu-id="0b5bb-130">Normale vertice</span><span class="sxs-lookup"><span data-stu-id="0b5bb-130">Vertex normal</span></span>                                                                                                 |
| <span data-ttu-id="0b5bb-131"><sub>Dir</sub></span><span class="sxs-lookup"><span data-stu-id="0b5bb-131">L<sub>dir</sub></span></span> | <span data-ttu-id="0b5bb-132">N/D</span><span class="sxs-lookup"><span data-stu-id="0b5bb-132">N/A</span></span>           | <span data-ttu-id="0b5bb-133">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="0b5bb-133">D3DVECTOR</span></span>     | <span data-ttu-id="0b5bb-134">Vettore di direzione dal vertice dell'oggetto alla luce.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-134">Direction vector from object vertex to the light.</span></span>                                                             |
| <span data-ttu-id="0b5bb-135">Atten</span><span class="sxs-lookup"><span data-stu-id="0b5bb-135">Atten</span></span>           | <span data-ttu-id="0b5bb-136">N/D</span><span class="sxs-lookup"><span data-stu-id="0b5bb-136">N/A</span></span>           | <span data-ttu-id="0b5bb-137">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0b5bb-137">FLOAT</span></span>         | <span data-ttu-id="0b5bb-138">Attenuazione chiara.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-138">Light attenuation.</span></span> <span data-ttu-id="0b5bb-139">Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="0b5bb-139">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="0b5bb-140">Spot (Contante)</span><span class="sxs-lookup"><span data-stu-id="0b5bb-140">Spot</span></span>            | <span data-ttu-id="0b5bb-141">N/D</span><span class="sxs-lookup"><span data-stu-id="0b5bb-141">N/A</span></span>           | <span data-ttu-id="0b5bb-142">FLOAT</span><span class="sxs-lookup"><span data-stu-id="0b5bb-142">FLOAT</span></span>         | <span data-ttu-id="0b5bb-143">Fattore Spotlight.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-143">Spotlight factor.</span></span> <span data-ttu-id="0b5bb-144">Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="0b5bb-144">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>  |



 

<span data-ttu-id="0b5bb-145">Il valore per C<sub>d</sub> è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b5bb-145">The value for C<sub>d</sub> is either:</span></span>

-   <span data-ttu-id="0b5bb-146">Vertex color1, se DIFFUSEMATERIALSOURCE = D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-146">vertex color1, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="0b5bb-147">Vertex color2, se DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, e il secondo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-147">vertex color2, if DIFFUSEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="0b5bb-148">colore diffuso materiale</span><span class="sxs-lookup"><span data-stu-id="0b5bb-148">material diffuse color</span></span>

> [!Note]  
> <span data-ttu-id="0b5bb-149">Se viene usata l'opzione DIFFUSEMATERIALSOURCE e il colore del vertice non viene specificato, viene usato il colore di materiale diffuso.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-149">If either DIFFUSEMATERIALSOURCE option is used, and the vertex color is not provided, the material diffuse color is used.</span></span>

 

<span data-ttu-id="0b5bb-150">Per calcolare l'attenuazione (atten) o le caratteristiche Spotlight (spot), vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="0b5bb-150">To calculate the attenuation (Atten) or the spotlight characteristics (Spot), see [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>

<span data-ttu-id="0b5bb-151">I componenti diffusi vengono fissati da 0 a 255, dopo che tutte le luci vengono elaborate e interpolate separatamente.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-151">Diffuse components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span> <span data-ttu-id="0b5bb-152">Il valore di illuminazione diffusa risultante è una combinazione dei valori di ambiente, diffusione e luce emissivo.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-152">The resulting diffuse lighting value is a combination of the ambient, diffuse and emissive light values.</span></span>

## <a name="example"></a><span data-ttu-id="0b5bb-153">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b5bb-153">Example</span></span>

<span data-ttu-id="0b5bb-154">In questo esempio, l'oggetto è colorato usando il colore chiaro e un colore diffuso di materiale.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-154">In this example, the object is colored using the light diffuse color and a material diffuse color.</span></span> <span data-ttu-id="0b5bb-155">Il codice è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-155">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="0b5bb-156">In base all'equazione, il colore risultante per i vertici dell'oggetto è una combinazione del colore del materiale e del colore chiaro.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-156">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="0b5bb-157">Le due illustrazioni seguenti mostrano il colore del materiale, che è grigio, e il colore chiaro, che è rosso chiaro.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-157">The following two illustrations show the material color, which is gray, and the light color, which is bright red.</span></span>

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera rossa](images/lightred.jpg)

<span data-ttu-id="0b5bb-160">La scena risultante è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-160">The resulting scene is shown in the following illustration.</span></span> <span data-ttu-id="0b5bb-161">L'unico oggetto nella scena è una sfera.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-161">The only object in the scene is a sphere.</span></span> <span data-ttu-id="0b5bb-162">Il calcolo di illuminazione diffusa prende il colore del materiale e della luce diffusa e lo modifica in base all'angolo tra la direzione della luce e la normale del vertice usando il prodotto punto.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-162">The diffuse lighting calculation takes the material and light diffuse color and modifies it by the angle between the light direction and the vertex normal using the dot product.</span></span> <span data-ttu-id="0b5bb-163">Di conseguenza, il lato posteriore della sfera diventa più scuro come la superficie delle curve della sfera fuori dalla luce.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-163">As a result, the backside of the sphere gets darker as the surface of the sphere curves away from the light.</span></span>

![illustrazione di una sfera con illuminazione diffusa](images/lightd.jpg)

<span data-ttu-id="0b5bb-165">Combinando l'illuminazione diffusa con l'illuminazione ambientale dell'esempio precedente, viene ombreggiata l'intera superficie dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-165">Combining the diffuse lighting with the ambient lighting from the previous example shades the entire surface of the object.</span></span> <span data-ttu-id="0b5bb-166">La luce di ambiente sfuma l'intera superficie e la luce diffusa consente di rivelare la forma 3D dell'oggetto, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-166">The ambient light shades the entire surface and the diffuse light helps reveal the object's 3D shape, as shown in the following illustration.</span></span>

![illustrazione di una sfera con illuminazione diffusa e illuminazione ambientale](images/lightad.jpg)

<span data-ttu-id="0b5bb-168">L'illuminazione diffusa è più impegnativa per il calcolo rispetto all'illuminazione ambientale.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-168">Diffuse lighting is more intensive to calculate than ambient lighting.</span></span> <span data-ttu-id="0b5bb-169">Poiché dipende dalle normali dei vertici e dalla direzione della luce, è possibile visualizzare la geometria degli oggetti nello spazio 3D, che produce un'illuminazione più realistica rispetto all'illuminazione ambientale.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-169">Because it depends on the vertex normals and light direction, you can see the objects geometry in 3D space, which produces a more realistic lighting than ambient lighting.</span></span> <span data-ttu-id="0b5bb-170">Per ottenere un aspetto più realistico, è possibile usare le evidenziazioni speculari.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-170">You can use specular highlights to achieve a more realistic look.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b5bb-171">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b5bb-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b5bb-172">Matematica dell'illuminazione</span><span class="sxs-lookup"><span data-stu-id="0b5bb-172">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



