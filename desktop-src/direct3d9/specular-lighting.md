---
description: Per la modellazione della reflection speculare è necessario che il sistema non conosca solo la direzione della luce che è in viaggio, ma anche la direzione dell'occhio del visualizzatore.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Illuminazione speculare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568387"
---
# <a name="specular-lighting-direct3d-9"></a><span data-ttu-id="5706f-103">Illuminazione speculare (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5706f-103">Specular Lighting (Direct3D 9)</span></span>

<span data-ttu-id="5706f-104">Per la modellazione della reflection speculare è necessario che il sistema non conosca solo la direzione della luce che è in viaggio, ma anche la direzione dell'occhio del visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="5706f-104">Modeling specular reflection requires that the system not only know in what direction light is traveling, but also the direction to the viewer's eye.</span></span> <span data-ttu-id="5706f-105">Il sistema usa una versione semplificata del modello Phong specularità-Reflection, che usa un vettore a metà per approssimare l'intensità della reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="5706f-105">The system uses a simplified version of the Phong specular-reflection model, which employs a halfway vector to approximate the intensity of specular reflection.</span></span>

<span data-ttu-id="5706f-106">Lo stato di illuminazione predefinito non calcola le evidenziazioni speculari.</span><span class="sxs-lookup"><span data-stu-id="5706f-106">The default lighting state does not calculate specular highlights.</span></span> <span data-ttu-id="5706f-107">Per abilitare l'illuminazione speculare, assicurarsi di impostare D3DRS \_ SPECULARENABLE su **true**.</span><span class="sxs-lookup"><span data-stu-id="5706f-107">To enable specular lighting, be sure to set D3DRS\_SPECULARENABLE to **TRUE**.</span></span>

## <a name="specular-lighting-equation"></a><span data-ttu-id="5706f-108">Equazione di illuminazione speculare</span><span class="sxs-lookup"><span data-stu-id="5706f-108">Specular Lighting Equation</span></span>

<span data-ttu-id="5706f-109">L'illuminazione speculare è descritta dall'equazione seguente.</span><span class="sxs-lookup"><span data-stu-id="5706f-109">Specular Lighting is described by the following equation.</span></span>



|                                                                             |
|-----------------------------------------------------------------------------|
| <span data-ttu-id="5706f-110">Illuminazione speculare = cs \* Sum \[ ls \* (N · H)<sup>P</sup> \* atten \* spot\]</span><span class="sxs-lookup"><span data-stu-id="5706f-110">Specular Lighting = Cₛ \* sum\[Lₛ \* (N · H)<sup>P</sup> \* Atten \* Spot\]</span></span> |



 

<span data-ttu-id="5706f-111">La tabella seguente identifica le variabili, i relativi tipi e i relativi intervalli.</span><span class="sxs-lookup"><span data-stu-id="5706f-111">The following table identifies the variables, their types, and their ranges.</span></span>



| <span data-ttu-id="5706f-112">Parametro</span><span class="sxs-lookup"><span data-stu-id="5706f-112">Parameter</span></span>    | <span data-ttu-id="5706f-113">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="5706f-113">Default value</span></span> | <span data-ttu-id="5706f-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="5706f-114">Type</span></span>          | <span data-ttu-id="5706f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5706f-115">Description</span></span>                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5706f-116">CS</span><span class="sxs-lookup"><span data-stu-id="5706f-116">Cₛ</span></span>           | <span data-ttu-id="5706f-117">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5706f-117">(0,0,0,0)</span></span>     | <span data-ttu-id="5706f-118">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5706f-118">D3DCOLORVALUE</span></span> | <span data-ttu-id="5706f-119">Colore speculare.</span><span class="sxs-lookup"><span data-stu-id="5706f-119">Specular color.</span></span>                                                                                                     |
| <span data-ttu-id="5706f-120">Sum</span><span class="sxs-lookup"><span data-stu-id="5706f-120">sum</span></span>          | <span data-ttu-id="5706f-121">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-121">N/A</span></span>           | <span data-ttu-id="5706f-122">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-122">N/A</span></span>           | <span data-ttu-id="5706f-123">Sommatoria del componente speculare di ogni luce.</span><span class="sxs-lookup"><span data-stu-id="5706f-123">Summation of each light's specular component.</span></span>                                                                       |
| <span data-ttu-id="5706f-124">N</span><span class="sxs-lookup"><span data-stu-id="5706f-124">N</span></span>            | <span data-ttu-id="5706f-125">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-125">N/A</span></span>           | <span data-ttu-id="5706f-126">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5706f-126">D3DVECTOR</span></span>     | <span data-ttu-id="5706f-127">Normale vertice.</span><span class="sxs-lookup"><span data-stu-id="5706f-127">Vertex normal.</span></span>                                                                                                      |
| <span data-ttu-id="5706f-128">H</span><span class="sxs-lookup"><span data-stu-id="5706f-128">H</span></span>            | <span data-ttu-id="5706f-129">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-129">N/A</span></span>           | <span data-ttu-id="5706f-130">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5706f-130">D3DVECTOR</span></span>     | <span data-ttu-id="5706f-131">Vettore a metà strada.</span><span class="sxs-lookup"><span data-stu-id="5706f-131">Half way vector.</span></span> <span data-ttu-id="5706f-132">Vedere la sezione sul vettore a metà.</span><span class="sxs-lookup"><span data-stu-id="5706f-132">See the section on the halfway vector.</span></span>                                                             |
| <span data-ttu-id="5706f-133"><sup>P</sup></span><span class="sxs-lookup"><span data-stu-id="5706f-133"><sup>P</sup></span></span> | <span data-ttu-id="5706f-134">0,0</span><span class="sxs-lookup"><span data-stu-id="5706f-134">0.0</span></span>           | <span data-ttu-id="5706f-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5706f-135">FLOAT</span></span>         | <span data-ttu-id="5706f-136">Potenza Reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="5706f-136">Specular reflection power.</span></span> <span data-ttu-id="5706f-137">L'intervallo è compreso tra 0 e + infinito</span><span class="sxs-lookup"><span data-stu-id="5706f-137">Range is 0 to +infinity</span></span>                                                                  |
| <span data-ttu-id="5706f-138">LS</span><span class="sxs-lookup"><span data-stu-id="5706f-138">Lₛ</span></span>           | <span data-ttu-id="5706f-139">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="5706f-139">(0,0,0,0)</span></span>     | <span data-ttu-id="5706f-140">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="5706f-140">D3DCOLORVALUE</span></span> | <span data-ttu-id="5706f-141">Colore speculare chiaro.</span><span class="sxs-lookup"><span data-stu-id="5706f-141">Light specular color.</span></span>                                                                                               |
| <span data-ttu-id="5706f-142">Atten</span><span class="sxs-lookup"><span data-stu-id="5706f-142">Atten</span></span>        | <span data-ttu-id="5706f-143">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-143">N/A</span></span>           | <span data-ttu-id="5706f-144">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5706f-144">FLOAT</span></span>         | <span data-ttu-id="5706f-145">Valore di attenuazione chiaro.</span><span class="sxs-lookup"><span data-stu-id="5706f-145">Light attenuation value.</span></span> <span data-ttu-id="5706f-146">Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="5706f-146">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span> |
| <span data-ttu-id="5706f-147">Spot (Contante)</span><span class="sxs-lookup"><span data-stu-id="5706f-147">Spot</span></span>         | <span data-ttu-id="5706f-148">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-148">N/A</span></span>           | <span data-ttu-id="5706f-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5706f-149">FLOAT</span></span>         | <span data-ttu-id="5706f-150">Fattore Spotlight.</span><span class="sxs-lookup"><span data-stu-id="5706f-150">Spotlight factor.</span></span> <span data-ttu-id="5706f-151">Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).</span><span class="sxs-lookup"><span data-stu-id="5706f-151">See [Attenuation and Spotlight Factor (Direct3D 9)](attenuation-and-spotlight-factor.md).</span></span>        |



 

<span data-ttu-id="5706f-152">Il valore per CS è:</span><span class="sxs-lookup"><span data-stu-id="5706f-152">The value for Cₛ is either:</span></span>


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   <span data-ttu-id="5706f-153">color1 vertice, se l'origine del materiale speculare è D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="5706f-153">vertex color1, if the specular material source is D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="5706f-154">color2 vertice, se l'origine del materiale speculare è D3DMCS \_ color2 e il secondo colore del vertice viene specificato nella dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="5706f-154">vertex color2, if specular material source is D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="5706f-155">colore speculare materiale</span><span class="sxs-lookup"><span data-stu-id="5706f-155">material specular color</span></span>

> [!Note]  
> <span data-ttu-id="5706f-156">Se viene usata l'opzione origine materiale speculare e il colore del vertice non è specificato, viene usato il colore speculare Material.</span><span class="sxs-lookup"><span data-stu-id="5706f-156">If either specular material source option is used and the vertex color is not provided, then the material specular color is used.</span></span>

 

<span data-ttu-id="5706f-157">I componenti speculari vengono fissati da 0 a 255, dopo che tutte le luci vengono elaborate e interpolate separatamente.</span><span class="sxs-lookup"><span data-stu-id="5706f-157">Specular components are clamped to be from 0 to 255, after all lights are processed and interpolated separately.</span></span>

## <a name="the-halfway-vector"></a><span data-ttu-id="5706f-158">Vettore a metà</span><span class="sxs-lookup"><span data-stu-id="5706f-158">The Halfway Vector</span></span>

<span data-ttu-id="5706f-159">Il vettore a metà (H) esiste a metà tra due vettori: il vettore da un vertice dell'oggetto alla sorgente di luce e il vettore da un vertice dell'oggetto alla posizione della camera.</span><span class="sxs-lookup"><span data-stu-id="5706f-159">The halfway vector (H) exists midway between two vectors: the vector from an object vertex to the light source, and the vector from an object vertex to the camera position.</span></span> <span data-ttu-id="5706f-160">Direct3D offre due modi per calcolare il vettore a metà.</span><span class="sxs-lookup"><span data-stu-id="5706f-160">Direct3D provides two ways to compute the halfway vector.</span></span> <span data-ttu-id="5706f-161">Quando D3DRS \_ LOCALVIEWER è impostato su **true**, il sistema calcola il vettore a metà usando la posizione della fotocamera e la posizione del vertice, insieme al vettore di direzione della luce.</span><span class="sxs-lookup"><span data-stu-id="5706f-161">When D3DRS\_LOCALVIEWER is set to **TRUE**, the system calculates the halfway vector using the position of the camera and the position of the vertex, along with the light's direction vector.</span></span> <span data-ttu-id="5706f-162">Questa operazione viene illustrata nella formula seguente.</span><span class="sxs-lookup"><span data-stu-id="5706f-162">The following formula illustrates this.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="5706f-163">H = Norm (Norm (CP-VP) + L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="5706f-163">H = norm(norm(Cₚ - Vₚ) + L<sub>dir</sub>)</span></span> |



 



| <span data-ttu-id="5706f-164">Parametro</span><span class="sxs-lookup"><span data-stu-id="5706f-164">Parameter</span></span>       | <span data-ttu-id="5706f-165">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="5706f-165">Default value</span></span> | <span data-ttu-id="5706f-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="5706f-166">Type</span></span>      | <span data-ttu-id="5706f-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5706f-167">Description</span></span>                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| <span data-ttu-id="5706f-168">CP</span><span class="sxs-lookup"><span data-stu-id="5706f-168">Cₚ</span></span>              | <span data-ttu-id="5706f-169">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-169">N/A</span></span>           | <span data-ttu-id="5706f-170">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5706f-170">D3DVECTOR</span></span> | <span data-ttu-id="5706f-171">Posizione della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="5706f-171">Camera position.</span></span>                                             |
| <span data-ttu-id="5706f-172">VP</span><span class="sxs-lookup"><span data-stu-id="5706f-172">Vₚ</span></span>              | <span data-ttu-id="5706f-173">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-173">N/A</span></span>           | <span data-ttu-id="5706f-174">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5706f-174">D3DVECTOR</span></span> | <span data-ttu-id="5706f-175">Posizione vertice.</span><span class="sxs-lookup"><span data-stu-id="5706f-175">Vertex position.</span></span>                                             |
| <span data-ttu-id="5706f-176"><sub>Dir</sub></span><span class="sxs-lookup"><span data-stu-id="5706f-176">L<sub>dir</sub></span></span> | <span data-ttu-id="5706f-177">N/D</span><span class="sxs-lookup"><span data-stu-id="5706f-177">N/A</span></span>           | <span data-ttu-id="5706f-178">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="5706f-178">D3DVECTOR</span></span> | <span data-ttu-id="5706f-179">Vettore di direzione dalla posizione del vertice alla posizione di luce.</span><span class="sxs-lookup"><span data-stu-id="5706f-179">Direction vector from vertex position to the light position.</span></span> |



 

<span data-ttu-id="5706f-180">La determinazione del vettore a metà in questo modo può essere a elevato utilizzo di calcolo.</span><span class="sxs-lookup"><span data-stu-id="5706f-180">Determining the halfway vector in this manner can be computationally intensive.</span></span> <span data-ttu-id="5706f-181">In alternativa, \_ l'impostazione di D3DRS LOCALVIEWER = **false** indica al sistema di agire come se il punto di vista fosse infinitamente distante sull'asse z.</span><span class="sxs-lookup"><span data-stu-id="5706f-181">As an alternative, setting D3DRS\_LOCALVIEWER = **FALSE** instructs the system to act as though the viewpoint is infinitely distant on the z-axis.</span></span> <span data-ttu-id="5706f-182">Questa operazione si riflette nella formula seguente.</span><span class="sxs-lookup"><span data-stu-id="5706f-182">This is reflected in the following formula.</span></span>



|                                     |
|-------------------------------------|
| <span data-ttu-id="5706f-183">H = Norm ((0, 0, 1) + L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="5706f-183">H = norm((0,0,1) + L<sub>dir</sub>)</span></span> |



 

<span data-ttu-id="5706f-184">Questa impostazione è meno complessa dal punto di vista del calcolo, ma è molto meno precisa, quindi è consigliabile usarla per le applicazioni che usano la proiezione ortogonale.</span><span class="sxs-lookup"><span data-stu-id="5706f-184">This setting is less computationally intensive, but much less accurate, so it is best used by applications that use orthogonal projection.</span></span>

## <a name="example"></a><span data-ttu-id="5706f-185">Esempio</span><span class="sxs-lookup"><span data-stu-id="5706f-185">Example</span></span>

<span data-ttu-id="5706f-186">In questo esempio, l'oggetto è colorato utilizzando il colore di luce speculare della scena e un colore speculare materiale.</span><span class="sxs-lookup"><span data-stu-id="5706f-186">In this example, the object is colored using the scene specular light color and a material specular color.</span></span> <span data-ttu-id="5706f-187">Il codice è illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5706f-187">The code is shown below.</span></span>


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



<span data-ttu-id="5706f-188">In base all'equazione, il colore risultante per i vertici dell'oggetto è una combinazione del colore del materiale e del colore chiaro.</span><span class="sxs-lookup"><span data-stu-id="5706f-188">According to the equation, the resulting color for the object vertices is a combination of the material color and the light color.</span></span>

<span data-ttu-id="5706f-189">Nella figura seguente vengono illustrati il colore del materiale speculare, che è grigio, e il colore chiaro speculare, che è bianco.</span><span class="sxs-lookup"><span data-stu-id="5706f-189">The following two illustration show the specular material color, which is gray, and the specular light color, which is white.</span></span>

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera bianca](images/lightwhite.jpg)

<span data-ttu-id="5706f-192">L'evidenziazione speculare risultante è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="5706f-192">The resulting specular highlight is shown in the following illustration.</span></span>

![illustrazione dell'evidenziazione speculare](images/lights.jpg)

<span data-ttu-id="5706f-194">La combinazione dell'evidenziazione speculare con l'illuminazione ambiente e diffusa produce la figura seguente.</span><span class="sxs-lookup"><span data-stu-id="5706f-194">Combining the specular highlight with the ambient and diffuse lighting produces the following illustration.</span></span> <span data-ttu-id="5706f-195">Con tutti e tre i tipi di illuminazione applicati, questo è più chiaramente simile a un oggetto realistico.</span><span class="sxs-lookup"><span data-stu-id="5706f-195">With all three types of lighting applied, this more clearly resembles a realistic object.</span></span>

![illustrazione della combinazione dell'evidenziazione speculare, dell'illuminazione ambientale e della luce diffusa](images/lightads.jpg)

<span data-ttu-id="5706f-197">L'illuminazione speculare è più impegnativa da calcolare rispetto all'illuminazione diffusa.</span><span class="sxs-lookup"><span data-stu-id="5706f-197">Specular lighting is more intensive to calculate than diffuse lighting.</span></span> <span data-ttu-id="5706f-198">Viene in genere usato per fornire indizi visivi sul materiale della superficie.</span><span class="sxs-lookup"><span data-stu-id="5706f-198">It is typically used to provide visual clues about the surface material.</span></span> <span data-ttu-id="5706f-199">L'evidenziazione speculare varia a seconda della dimensione e del colore del materiale della superficie.</span><span class="sxs-lookup"><span data-stu-id="5706f-199">The specular highlight varies in size and color with the material of the surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5706f-200">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5706f-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5706f-201">Matematica dell'illuminazione</span><span class="sxs-lookup"><span data-stu-id="5706f-201">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



