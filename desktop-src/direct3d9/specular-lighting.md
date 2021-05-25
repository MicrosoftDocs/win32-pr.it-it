---
description: La modellazione della reflection speculare richiede che il sistema non solo sappia in quale direzione viaggia la luce, ma anche la direzione verso l'occhio dello visualizzatore.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Illuminazione speculare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343676"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="42b2c-103">Illuminazione speculare (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="42b2c-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="42b2c-104">La modellazione della reflection speculare richiede che il sistema non solo sappia in quale direzione viaggia la luce, ma anche la direzione verso l'occhio dello visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="42b2c-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="42b2c-105">Il sistema usa una versione semplificata del modello phong specular-reflection, che usa un vettore a metà per approssimare l'intensità della reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="42b2c-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="42b2c-106">Lo stato di illuminazione predefinito non calcola le evidenziazioni speculari.</span><span class="sxs-lookup"><span data-stu-id="42b2c-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="42b2c-107">Per abilitare l'illuminazione speculare, assicurarsi di impostare D3DRS \_ SPECULARENABLE su **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="42b2c-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="42b2c-108">Equazione di illuminazione speculare</span><span class="sxs-lookup"><span data-stu-id="42b2c-108">Specular Lighting Equation</span></span>

<span data-ttu-id="42b2c-109">L'illuminazione speculare è descritta dall'equazione seguente:</span><span class="sxs-lookup"><span data-stu-id="42b2c-109">Specular Lighting is described by the following equation:</span></span>

<span data-ttu-id="42b2c-110">**Illuminazione speculare = Cs \* sum \[ Ls \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span><span class="sxs-lookup"><span data-stu-id="42b2c-110">**Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]**</span></span>



 

<span data-ttu-id="42b2c-111">La tabella seguente identifica le variabili, i relativi tipi e i relativi intervalli.</span><span class="sxs-lookup"><span data-stu-id="42b2c-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="42b2c-112">Parametro</span><span class="sxs-lookup"><span data-stu-id="42b2c-112">Parameter</span></span>    | <span data-ttu-id="42b2c-113">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="42b2c-113">Default value</span></span> | <span data-ttu-id="42b2c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="42b2c-114">Type</span></span>          | <span data-ttu-id="42b2c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b2c-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b2c-116">Cs</span><span class="sxs-lookup"><span data-stu-id="42b2c-116">Cₛ</span></span>           | <span data-ttu-id="42b2c-117">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="42b2c-117">(0,0,0,0)</span></span>     | <span data-ttu-id="42b2c-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="42b2c-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="42b2c-119">Colore speculare.</span><span class="sxs-lookup"><span data-stu-id="42b2c-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="42b2c-120">Sum</span><span class="sxs-lookup"><span data-stu-id="42b2c-120">sum</span></span>          | <span data-ttu-id="42b2c-121">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-121">N/A</span></span>           | <span data-ttu-id="42b2c-122">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-122">N/A</span></span>           | <span data-ttu-id="42b2c-123">Somma del componente speculare di ogni luce.</span><span class="sxs-lookup"><span data-stu-id="42b2c-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="42b2c-124">N</span><span class="sxs-lookup"><span data-stu-id="42b2c-124">N</span></span>            | <span data-ttu-id="42b2c-125">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-125">N/A</span></span>           | <span data-ttu-id="42b2c-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="42b2c-126">D3DVECTOR</span></span>     | <span data-ttu-id="42b2c-127">Normale vertice.</span><span class="sxs-lookup"><span data-stu-id="42b2c-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="42b2c-128">H</span><span class="sxs-lookup"><span data-stu-id="42b2c-128">H</span></span>            | <span data-ttu-id="42b2c-129">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-129">N/A</span></span>           | <span data-ttu-id="42b2c-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="42b2c-130">D3DVECTOR</span></span>     | <span data-ttu-id="42b2c-131">Vettore a metà strada.</span><span class="sxs-lookup"><span data-stu-id="42b2c-131">Half way vector.</span></span> <span data-ttu-id="42b2c-132">Vedere la sezione sul vettore a metà.</span><span class="sxs-lookup"><span data-stu-id="42b2c-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="42b2c-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="42b2c-133"><sup>P</sup></span></span> | <span data-ttu-id="42b2c-134">0,0</span><span class="sxs-lookup"><span data-stu-id="42b2c-134">0.0</span></span>           | <span data-ttu-id="42b2c-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="42b2c-135">FLOAT</span></span>         | <span data-ttu-id="42b2c-136">Potenza di reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="42b2c-136">Specular reflection power.</span></span> <span data-ttu-id="42b2c-137">L'intervallo è compreso tra 0 e +infinito</span><span class="sxs-lookup"><span data-stu-id="42b2c-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="42b2c-138">Ls</span><span class="sxs-lookup"><span data-stu-id="42b2c-138">Lₛ</span></span>           | <span data-ttu-id="42b2c-139">(0,0,0,0)</span><span class="sxs-lookup"><span data-stu-id="42b2c-139">(0,0,0,0)</span></span>     | <span data-ttu-id="42b2c-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="42b2c-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="42b2c-141">Colore speculare chiaro.</span><span class="sxs-lookup"><span data-stu-id="42b2c-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="42b2c-142">Atten</span><span class="sxs-lookup"><span data-stu-id="42b2c-142">Atten</span></span>        | <span data-ttu-id="42b2c-143">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-143">N/A</span></span>           | <span data-ttu-id="42b2c-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="42b2c-144">FLOAT</span></span>         | <span data-ttu-id="42b2c-145">Valore di attenuazione della luce.</span><span class="sxs-lookup"><span data-stu-id="42b2c-145">Light attenuation value.</span></span> <span data-ttu-id="42b2c-146">Vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)</span><span class="sxs-lookup"><span data-stu-id="42b2c-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="42b2c-147">Spot (Contante)</span><span class="sxs-lookup"><span data-stu-id="42b2c-147">Spot</span></span>         | <span data-ttu-id="42b2c-148">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-148">N/A</span></span>           | <span data-ttu-id="42b2c-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="42b2c-149">FLOAT</span></span>         | <span data-ttu-id="42b2c-150">Fattore Spotlight.</span><span class="sxs-lookup"><span data-stu-id="42b2c-150">Spotlight factor.</span></span> <span data-ttu-id="42b2c-151">Vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)</span><span class="sxs-lookup"><span data-stu-id="42b2c-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="42b2c-152">Il valore per Cs è:</span><span class="sxs-lookup"><span data-stu-id="42b2c-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="42b2c-153">vertex color1, se l'origine del materiale speculare è D3DMCS COLOR1 e il primo colore del vertice viene \_ fornito nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="42b2c-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="42b2c-154">vertex color2, se l'origine del materiale speculare è D3DMCS COLOR2 e il secondo colore del vertice viene \_ fornito nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="42b2c-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="42b2c-155">colore speculare materiale</span><span class="sxs-lookup"><span data-stu-id="42b2c-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="42b2c-156">Se si usa una delle due opzioni di origine del materiale speculare e non viene specificato il colore del vertice, viene usato il colore speculare del materiale.</span><span class="sxs-lookup"><span data-stu-id="42b2c-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="42b2c-157">I componenti speculari sono definiti in modo da essere da 0 a 255, dopo che tutte le luci vengono elaborate e interpolate separatamente.</span><span class="sxs-lookup"><span data-stu-id="42b2c-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="42b2c-158">Vettore a metà strada</span><span class="sxs-lookup"><span data-stu-id="42b2c-158">The Halfway Vector</span></span>

<span data-ttu-id="42b2c-159">Il vettore intermedio (H) si trova a metà tra due vettori: il vettore da un vertice dell'oggetto alla sorgente di luce e il vettore da un vertice dell'oggetto alla posizione della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="42b2c-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="42b2c-160">Direct3D offre due modi per calcolare il vettore a metà.</span><span class="sxs-lookup"><span data-stu-id="42b2c-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="42b2c-161">Quando D3DRS LOCALVIEWER è impostato su TRUE, il sistema calcola il vettore a metà strada usando la posizione della fotocamera e la posizione del vertice, insieme al vettore di direzione della \_ luce. </span><span class="sxs-lookup"><span data-stu-id="42b2c-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="42b2c-162">La formula seguente illustra questa operazione.</span><span class="sxs-lookup"><span data-stu-id="42b2c-162">The following formula illustrates this.</span></span>

<span data-ttu-id="42b2c-163">**H = norm(norm(Cp - Vp) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="42b2c-163">**H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)**</span></span>



 



| <span data-ttu-id="42b2c-164">Parametro</span><span class="sxs-lookup"><span data-stu-id="42b2c-164">Parameter</span></span>       | <span data-ttu-id="42b2c-165">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="42b2c-165">Default value</span></span> | <span data-ttu-id="42b2c-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="42b2c-166">Type</span></span>      | <span data-ttu-id="42b2c-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b2c-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="42b2c-168">Cp</span><span class="sxs-lookup"><span data-stu-id="42b2c-168">Cₚ</span></span>              | <span data-ttu-id="42b2c-169">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-169">N/A</span></span>           | <span data-ttu-id="42b2c-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="42b2c-170">D3DVECTOR</span></span> | <span data-ttu-id="42b2c-171">Posizione della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="42b2c-171">Camera position.</span></span>                                             |
| <span data-ttu-id="42b2c-172">Vp</span><span class="sxs-lookup"><span data-stu-id="42b2c-172">Vₚ</span></span>              | <span data-ttu-id="42b2c-173">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-173">N/A</span></span>           | <span data-ttu-id="42b2c-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="42b2c-174">D3DVECTOR</span></span> | <span data-ttu-id="42b2c-175">Posizione del vertice.</span><span class="sxs-lookup"><span data-stu-id="42b2c-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="42b2c-176">L<sub>dir</sub></span><span class="sxs-lookup"><span data-stu-id="42b2c-176">L<sub>dir</sub></span></span> | <span data-ttu-id="42b2c-177">N/D</span><span class="sxs-lookup"><span data-stu-id="42b2c-177">N/A</span></span>           | <span data-ttu-id="42b2c-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="42b2c-178">D3DVECTOR</span></span> | <span data-ttu-id="42b2c-179">Vettore di direzione dalla posizione del vertice alla posizione della luce.</span><span class="sxs-lookup"><span data-stu-id="42b2c-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="42b2c-180">Determinare il vettore a metà strada in questo modo può essere intensivo dal punto di vista del calcolo.</span><span class="sxs-lookup"><span data-stu-id="42b2c-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="42b2c-181">In alternativa, l'impostazione di D3DRS LOCALVIEWER = FALSE indica al sistema di agire come se il punto di vista \_ fosse infinitamente distante sull'asse z. </span><span class="sxs-lookup"><span data-stu-id="42b2c-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="42b2c-182">Ciò si riflette nella formula seguente.</span><span class="sxs-lookup"><span data-stu-id="42b2c-182">This is reflected in the following formula.</span></span>

<span data-ttu-id="42b2c-183">**H = norm((0,0,1) + L <sub>dir</sub>)**</span><span class="sxs-lookup"><span data-stu-id="42b2c-183">**H = norm((0,0,1) + L<sub>dir</sub>)**</span></span>



 

<span data-ttu-id="42b2c-184">Questa impostazione è meno intensiva dal punto di vista del calcolo, ma molto meno accurata, quindi viene usata meglio dalle applicazioni che usano la proiezione ortogonale.</span><span class="sxs-lookup"><span data-stu-id="42b2c-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="42b2c-185">Esempio</span><span class="sxs-lookup"><span data-stu-id="42b2c-185">Example</span></span>

<span data-ttu-id="42b2c-186">In questo esempio l'oggetto viene colorato usando il colore della luce speculare della scena e un colore speculare materiale.</span><span class="sxs-lookup"><span data-stu-id="42b2c-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="42b2c-187">Il codice è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="42b2c-187">The code is shown below.</span></span>


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="42b2c-188">In base all'equazione, il colore risultante per i vertici dell'oggetto è una combinazione del colore del materiale e del colore chiaro.</span><span class="sxs-lookup"><span data-stu-id="42b2c-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="42b2c-189">Nella figura seguente vengono illustrati il colore del materiale speculare, ovvero il grigio, e il colore chiaro speculare, ovvero il bianco.</span><span class="sxs-lookup"><span data-stu-id="42b2c-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera bianca](images/lightwhite.jpg)

<span data-ttu-id="42b2c-192">L'evidenziazione speculare risultante è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="42b2c-192">The resulting specular highlight is shown in the following illustration.</span></span>

![illustrazione dell'evidenziazione speculare](images/lights.jpg)

<span data-ttu-id="42b2c-194">La combinazione dell'evidenziazione speculare con l'illuminazione ambientale e diffusa produce la figura seguente.</span><span class="sxs-lookup"><span data-stu-id="42b2c-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="42b2c-195">Con tutti e tre i tipi di illuminazione applicati, questo oggetto è più chiaramente simile a un oggetto realistico.</span><span class="sxs-lookup"><span data-stu-id="42b2c-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![illustrazione della combinazione dell'evidenziazione speculare, dell'illuminazione ambientale e dell'illuminazione diffusa](images/lightads.jpg)

<span data-ttu-id="42b2c-197">L'illuminazione speculare è più intensiva da calcolare rispetto all'illuminazione diffusa.</span><span class="sxs-lookup"><span data-stu-id="42b2c-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="42b2c-198">Viene in genere usato per fornire indicazioni visive sul materiale della superficie.</span><span class="sxs-lookup"><span data-stu-id="42b2c-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="42b2c-199">L'evidenziazione speculare varia in base alle dimensioni e al colore del materiale della superficie.</span><span class="sxs-lookup"><span data-stu-id="42b2c-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42b2c-200">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42b2c-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42b2c-201">Matematica dell'illuminazione</span><span class="sxs-lookup"><span data-stu-id="42b2c-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



