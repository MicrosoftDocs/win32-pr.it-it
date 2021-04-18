---
description: I componenti di illuminazione diffusa e speculare dell'equazione di illuminazione globale contengono termini che descrivono l'attenuazione chiara e il cono Spotlight. Questi termini sono descritti di seguito.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Attenuazione e fattore Spotlight (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564255"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a><span data-ttu-id="06fb5-104">Attenuazione e fattore Spotlight (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="06fb5-104">Attenuation and Spotlight Factor (Direct3D 9)</span></span>

<span data-ttu-id="06fb5-105">I componenti di illuminazione diffusa e speculare dell'equazione di illuminazione globale contengono termini che descrivono l'attenuazione chiara e il cono Spotlight.</span><span class="sxs-lookup"><span data-stu-id="06fb5-105">The diffuse and specular lighting components of the global illumination equation contain terms that describe light attenuation and the spotlight cone.</span></span> <span data-ttu-id="06fb5-106">Questi termini sono descritti di seguito.</span><span class="sxs-lookup"><span data-stu-id="06fb5-106">These terms are described below.</span></span>

## <a name="attenuation"></a><span data-ttu-id="06fb5-107">Attenuazione</span><span class="sxs-lookup"><span data-stu-id="06fb5-107">Attenuation</span></span>

<span data-ttu-id="06fb5-108">L'attenuazione di una luce dipende dal tipo di luce e dalla distanza tra la luce e la posizione del vertice.</span><span class="sxs-lookup"><span data-stu-id="06fb5-108">The attenuation of a light depends on the type of light and the distance between the light and the vertex position.</span></span> <span data-ttu-id="06fb5-109">Per calcolare l'attenuazione, usare una delle equazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="06fb5-109">To calculate attenuation, use one of the following equations.</span></span>

<span data-ttu-id="06fb5-110">Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + ATT2<sub>i</sub> \* d ²)</span><span class="sxs-lookup"><span data-stu-id="06fb5-110">Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)</span></span>

<span data-ttu-id="06fb5-111">Dove:</span><span class="sxs-lookup"><span data-stu-id="06fb5-111">Where:</span></span>



| <span data-ttu-id="06fb5-112">Parametro</span><span class="sxs-lookup"><span data-stu-id="06fb5-112">Parameter</span></span>        | <span data-ttu-id="06fb5-113">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="06fb5-113">Default value</span></span> | <span data-ttu-id="06fb5-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="06fb5-114">Type</span></span>  | <span data-ttu-id="06fb5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06fb5-115">Description</span></span>                                     | <span data-ttu-id="06fb5-116">Range</span><span class="sxs-lookup"><span data-stu-id="06fb5-116">Range</span></span>          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| <span data-ttu-id="06fb5-117">att0<sub></sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-117">att0<sub>i</sub></span></span> | <span data-ttu-id="06fb5-118">0,0</span><span class="sxs-lookup"><span data-stu-id="06fb5-118">0.0</span></span>           | <span data-ttu-id="06fb5-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-119">FLOAT</span></span> | <span data-ttu-id="06fb5-120">Fattore di attenuazione costante</span><span class="sxs-lookup"><span data-stu-id="06fb5-120">Constant attenuation factor</span></span>                     | <span data-ttu-id="06fb5-121">da 0 a + infinito</span><span class="sxs-lookup"><span data-stu-id="06fb5-121">0 to +infinity</span></span> |
| <span data-ttu-id="06fb5-122">Att1<sub></sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-122">att1<sub>i</sub></span></span> | <span data-ttu-id="06fb5-123">0,0</span><span class="sxs-lookup"><span data-stu-id="06fb5-123">0.0</span></span>           | <span data-ttu-id="06fb5-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-124">FLOAT</span></span> | <span data-ttu-id="06fb5-125">Fattore di attenuazione lineare</span><span class="sxs-lookup"><span data-stu-id="06fb5-125">Linear attenuation factor</span></span>                       | <span data-ttu-id="06fb5-126">da 0 a + infinito</span><span class="sxs-lookup"><span data-stu-id="06fb5-126">0 to +infinity</span></span> |
| <span data-ttu-id="06fb5-127">ATT2<sub></sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-127">att2<sub>i</sub></span></span> | <span data-ttu-id="06fb5-128">0,0</span><span class="sxs-lookup"><span data-stu-id="06fb5-128">0.0</span></span>           | <span data-ttu-id="06fb5-129">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-129">FLOAT</span></span> | <span data-ttu-id="06fb5-130">Fattore di attenuazione quadratica</span><span class="sxs-lookup"><span data-stu-id="06fb5-130">Quadratic attenuation factor</span></span>                    | <span data-ttu-id="06fb5-131">da 0 a + infinito</span><span class="sxs-lookup"><span data-stu-id="06fb5-131">0 to +infinity</span></span> |
| <span data-ttu-id="06fb5-132">d</span><span class="sxs-lookup"><span data-stu-id="06fb5-132">d</span></span>                | <span data-ttu-id="06fb5-133">N/D</span><span class="sxs-lookup"><span data-stu-id="06fb5-133">N/A</span></span>           | <span data-ttu-id="06fb5-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-134">FLOAT</span></span> | <span data-ttu-id="06fb5-135">Distanza dalla posizione del vertice alla posizione chiara</span><span class="sxs-lookup"><span data-stu-id="06fb5-135">Distance from vertex position to light position</span></span> | <span data-ttu-id="06fb5-136">N/D</span><span class="sxs-lookup"><span data-stu-id="06fb5-136">N/A</span></span>            |



 

-   <span data-ttu-id="06fb5-137">Atten = 1, se la luce è una luce direzionale.</span><span class="sxs-lookup"><span data-stu-id="06fb5-137">Atten = 1, if the light is a directional light.</span></span>
-   <span data-ttu-id="06fb5-138">Atten = 0, se la distanza tra la luce e il vertice supera l'intervallo della luce.</span><span class="sxs-lookup"><span data-stu-id="06fb5-138">Atten = 0, if the distance between the light and the vertex exceeds the light's range.</span></span>

<span data-ttu-id="06fb5-139">I valori att0, att1, att2 sono specificati dai membri Attenuation0, Attenuation1 e Attenuation2 di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="06fb5-139">The att0, att1, att2 values are specified by the Attenuation0, Attenuation1, and Attenuation2 members of [**D3DLIGHT9**](d3dlight9.md).</span></span>

<span data-ttu-id="06fb5-140">La distanza tra la luce e la posizione del vertice è sempre positiva.</span><span class="sxs-lookup"><span data-stu-id="06fb5-140">The distance between the light and the vertex position is always positive.</span></span>

<span data-ttu-id="06fb5-141">d = \| L<sub>dir</sub>\|</span><span class="sxs-lookup"><span data-stu-id="06fb5-141">d = \| L<sub>dir</sub> \|</span></span>

<span data-ttu-id="06fb5-142">Dove:</span><span class="sxs-lookup"><span data-stu-id="06fb5-142">Where:</span></span>



| <span data-ttu-id="06fb5-143">Parametro</span><span class="sxs-lookup"><span data-stu-id="06fb5-143">Parameter</span></span>       | <span data-ttu-id="06fb5-144">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="06fb5-144">Default value</span></span> | <span data-ttu-id="06fb5-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="06fb5-145">Type</span></span>      | <span data-ttu-id="06fb5-146">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06fb5-146">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="06fb5-147"><sub>Dir</sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-147">L<sub>dir</sub></span></span> | <span data-ttu-id="06fb5-148">N/D</span><span class="sxs-lookup"><span data-stu-id="06fb5-148">N/A</span></span>           | <span data-ttu-id="06fb5-149">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="06fb5-149">D3DVECTOR</span></span> | <span data-ttu-id="06fb5-150">Vettore direzione dalla posizione vertice alla posizione chiara</span><span class="sxs-lookup"><span data-stu-id="06fb5-150">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="06fb5-151">Se d è maggiore dell'intervallo della luce, ovvero il membro di intervallo di una struttura [**D3DLIGHT9**](d3dlight9.md) , Direct3D non esegue ulteriori calcoli di attenuazione e non applica alcun effetto dalla luce al vertice.</span><span class="sxs-lookup"><span data-stu-id="06fb5-151">If d is greater than the light's range, that is, the Range member of a [**D3DLIGHT9**](d3dlight9.md) structure, Direct3D makes no further attenuation calculations and applies no effects from the light to the vertex.</span></span>

<span data-ttu-id="06fb5-152">Le costanti di attenuazione agiscono come coefficienti nella formula: è possibile produrre una serie di curve di attenuazione apportando semplici regolazioni.</span><span class="sxs-lookup"><span data-stu-id="06fb5-152">The attenuation constants act as coefficients in the formula - you can produce a variety of attenuation curves by making simple adjustments to them.</span></span> <span data-ttu-id="06fb5-153">È possibile impostare Attenuation1 su 1,0 per creare una luce che non si attenua, ma che sia ancora limitata da intervallo, oppure è possibile sperimentare valori diversi per ottenere vari effetti di attenuazione.</span><span class="sxs-lookup"><span data-stu-id="06fb5-153">You can set Attenuation1 to 1.0 to create a light that doesn't attenuate but is still limited by range, or you can experiment with different values to achieve various attenuation effects.</span></span>

<span data-ttu-id="06fb5-154">L'attenuazione nell'intervallo massimo della luce non è 0,0.</span><span class="sxs-lookup"><span data-stu-id="06fb5-154">The attenuation at the maximum range of the light is not 0.0.</span></span> <span data-ttu-id="06fb5-155">Per evitare che le luci vengano visualizzate improvvisamente quando si trovano nell'intervallo di luce, un'applicazione può aumentare l'intervallo di luce.</span><span class="sxs-lookup"><span data-stu-id="06fb5-155">To prevent lights from suddenly appearing when they are at the light range, an application can increase the light range.</span></span> <span data-ttu-id="06fb5-156">In alternativa, l'applicazione può impostare costanti di attenuazione in modo che il fattore di attenuazione si avvicini a 0,0 nell'intervallo chiaro.</span><span class="sxs-lookup"><span data-stu-id="06fb5-156">Or, the application can set up attenuation constants so that the attenuation factor is close to 0.0 at the light range.</span></span> <span data-ttu-id="06fb5-157">Il valore di attenuazione viene moltiplicato per i componenti rosso, verde e blu del colore della luce per ridimensionare l'intensità della luce come fattore della luce della distanza che passa a un vertice.</span><span class="sxs-lookup"><span data-stu-id="06fb5-157">The attenuation value is multiplied by the red, green, and blue components of the light's color to scale the light's intensity as a factor of the distance light travels to a vertex.</span></span>

## <a name="spotlight-factor"></a><span data-ttu-id="06fb5-158">Fattore Spotlight</span><span class="sxs-lookup"><span data-stu-id="06fb5-158">Spotlight Factor</span></span>

<span data-ttu-id="06fb5-159">L'equazione seguente specifica il fattore Spotlight.</span><span class="sxs-lookup"><span data-stu-id="06fb5-159">The following equation specifies the spotlight factor.</span></span>

![equazione del fattore Spotlight](images/dx8light9.png)



| <span data-ttu-id="06fb5-161">Parametro</span><span class="sxs-lookup"><span data-stu-id="06fb5-161">Parameter</span></span>         | <span data-ttu-id="06fb5-162">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="06fb5-162">Default value</span></span> | <span data-ttu-id="06fb5-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="06fb5-163">Type</span></span>  | <span data-ttu-id="06fb5-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06fb5-164">Description</span></span>                              | <span data-ttu-id="06fb5-165">Range</span><span class="sxs-lookup"><span data-stu-id="06fb5-165">Range</span></span>                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| <span data-ttu-id="06fb5-166">Rho<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-166">rho<sub>i</sub></span></span>   | <span data-ttu-id="06fb5-167">N/D</span><span class="sxs-lookup"><span data-stu-id="06fb5-167">N/A</span></span>           | <span data-ttu-id="06fb5-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-168">FLOAT</span></span> | <span data-ttu-id="06fb5-169">coseno (angolo) per Spotlight i</span><span class="sxs-lookup"><span data-stu-id="06fb5-169">cosine(angle) for spotlight i</span></span>            | <span data-ttu-id="06fb5-170">N/D</span><span class="sxs-lookup"><span data-stu-id="06fb5-170">N/A</span></span>                      |
| <span data-ttu-id="06fb5-171"><sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-171">phi<sub>i</sub></span></span>   | <span data-ttu-id="06fb5-172">0,0</span><span class="sxs-lookup"><span data-stu-id="06fb5-172">0.0</span></span>           | <span data-ttu-id="06fb5-173">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-173">FLOAT</span></span> | <span data-ttu-id="06fb5-174">Angolo penombra del faretto i in radianti</span><span class="sxs-lookup"><span data-stu-id="06fb5-174">Penumbra angle of spotlight i in radians</span></span> | <span data-ttu-id="06fb5-175">\[Theta<sub>i</sub>, pi)</span><span class="sxs-lookup"><span data-stu-id="06fb5-175">\[theta<sub>i</sub>, pi)</span></span> |
| <span data-ttu-id="06fb5-176">Theta<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-176">theta<sub>i</sub></span></span> | <span data-ttu-id="06fb5-177">0,0</span><span class="sxs-lookup"><span data-stu-id="06fb5-177">0.0</span></span>           | <span data-ttu-id="06fb5-178">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-178">FLOAT</span></span> | <span data-ttu-id="06fb5-179">Angolo umbra del faretto i in radianti</span><span class="sxs-lookup"><span data-stu-id="06fb5-179">Umbra angle of spotlight i in radians</span></span>    | <span data-ttu-id="06fb5-180">\[0, pi greco)</span><span class="sxs-lookup"><span data-stu-id="06fb5-180">\[0, pi)</span></span>                 |
| <span data-ttu-id="06fb5-181">falloff</span><span class="sxs-lookup"><span data-stu-id="06fb5-181">falloff</span></span>           | <span data-ttu-id="06fb5-182">0,0</span><span class="sxs-lookup"><span data-stu-id="06fb5-182">0.0</span></span>           | <span data-ttu-id="06fb5-183">FLOAT</span><span class="sxs-lookup"><span data-stu-id="06fb5-183">FLOAT</span></span> | <span data-ttu-id="06fb5-184">Fattore di interruzione</span><span class="sxs-lookup"><span data-stu-id="06fb5-184">Falloff factor</span></span>                           | <span data-ttu-id="06fb5-185">(-infinito, + infinito)</span><span class="sxs-lookup"><span data-stu-id="06fb5-185">(-infinity, +infinity)</span></span>   |



 

<span data-ttu-id="06fb5-186">Dove:</span><span class="sxs-lookup"><span data-stu-id="06fb5-186">Where:</span></span>

<span data-ttu-id="06fb5-187">Rho = Norm (L<sub>DCS</sub>)<sup>.</sup> norma (L<sub>dir</sub>)</span><span class="sxs-lookup"><span data-stu-id="06fb5-187">rho = norm(L<sub>dcs</sub>)<sup>.</sup>norm(L<sub>dir</sub>)</span></span>

<span data-ttu-id="06fb5-188">e:</span><span class="sxs-lookup"><span data-stu-id="06fb5-188">and:</span></span>



| <span data-ttu-id="06fb5-189">Parametro</span><span class="sxs-lookup"><span data-stu-id="06fb5-189">Parameter</span></span>       | <span data-ttu-id="06fb5-190">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="06fb5-190">Default value</span></span> | <span data-ttu-id="06fb5-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="06fb5-191">Type</span></span>      | <span data-ttu-id="06fb5-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06fb5-192">Description</span></span>                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <span data-ttu-id="06fb5-193"><sub>Controller di dominio</sub> L</span><span class="sxs-lookup"><span data-stu-id="06fb5-193">L<sub>dcs</sub></span></span> | <span data-ttu-id="06fb5-194">N/D</span><span class="sxs-lookup"><span data-stu-id="06fb5-194">N/A</span></span>           | <span data-ttu-id="06fb5-195">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="06fb5-195">D3DVECTOR</span></span> | <span data-ttu-id="06fb5-196">Il negativo della direzione della luce nello spazio della fotocamera</span><span class="sxs-lookup"><span data-stu-id="06fb5-196">The negative of the light direction in camera space</span></span>         |
| <span data-ttu-id="06fb5-197"><sub>Dir</sub></span><span class="sxs-lookup"><span data-stu-id="06fb5-197">L<sub>dir</sub></span></span> | <span data-ttu-id="06fb5-198">N/D</span><span class="sxs-lookup"><span data-stu-id="06fb5-198">N/A</span></span>           | <span data-ttu-id="06fb5-199">D3DVECTOR</span><span class="sxs-lookup"><span data-stu-id="06fb5-199">D3DVECTOR</span></span> | <span data-ttu-id="06fb5-200">Vettore direzione dalla posizione vertice alla posizione chiara</span><span class="sxs-lookup"><span data-stu-id="06fb5-200">Direction vector from vertex position to the light position</span></span> |



 

<span data-ttu-id="06fb5-201">Una volta calcolata l'attenuazione della luce, Direct3D Considera anche gli effetti Spotlight, se applicabile, l'angolo che la luce riflette da una superficie e la reflection del materiale corrente per calcolare i componenti diffusi e speculari per il vertice.</span><span class="sxs-lookup"><span data-stu-id="06fb5-201">After computing the light attenuation, Direct3D also considers spotlight effects if applicable, the angle that the light reflects from a surface, and the reflectance of the current material to calculate the diffuse and specular components for that vertex.</span></span> <span data-ttu-id="06fb5-202">Per altre informazioni, vedere [Spotlight](light-types.md).</span><span class="sxs-lookup"><span data-stu-id="06fb5-202">For more information, see [SpotLight](light-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06fb5-203">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06fb5-203">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06fb5-204">Matematica dell'illuminazione</span><span class="sxs-lookup"><span data-stu-id="06fb5-204">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



