---
description: Usare la raccolta SasHostParameterValue per definire la raccolta di valori dell'applicazione host, nonché il tipo e i membri esposti agli effetti.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Data binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341541"
---
# <a name="data-binding"></a><span data-ttu-id="fb16e-103">Data binding</span><span class="sxs-lookup"><span data-stu-id="fb16e-103">Data Binding</span></span>

<span data-ttu-id="fb16e-104">Usare la [raccolta SasHostParameterValue](#sashostparametervalue-collection) per definire la raccolta di valori dell'applicazione host, nonché il tipo e i membri esposti agli effetti.</span><span class="sxs-lookup"><span data-stu-id="fb16e-104">Use [SasHostParameterValue Collection](#sashostparametervalue-collection) to define the collection of host application values, as well as their type and members, exposed to effects.</span></span> <span data-ttu-id="fb16e-105">Utilizzare l'annotazione [SasBindAddress](#sasbindaddress) in un file di effetti per associare un parametro di effetto al parametro corrispondente nell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="fb16e-105">Use the [SasBindAddress](#sasbindaddress) annotation in an effect file to associate an effect parameter with its corresponding parameter in the host application.</span></span>

## <a name="sashostparametervalue-collection"></a><span data-ttu-id="fb16e-106">Raccolta SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="fb16e-106">SasHostParameterValue Collection</span></span>

<span data-ttu-id="fb16e-107">SasHostParameterValue viene definito usando la sintassi dei file effetti (con estensione FX).</span><span class="sxs-lookup"><span data-stu-id="fb16e-107">The SasHostParameterValue is defined using effect file (.fx) syntax.</span></span> <span data-ttu-id="fb16e-108">Sebbene la sintassi sia molto simile alla sintassi dei file di effetti, esistono alcune differenze.</span><span class="sxs-lookup"><span data-stu-id="fb16e-108">While the syntax is very similar to the effect file syntax, some differences exist.</span></span> <span data-ttu-id="fb16e-109">Ad esempio, i tipi di oggetto, ad esempio Texture2D, Samplers e Strings, non sono validi nei file effettivi, ma sono validi in SasHostParameterValue.</span><span class="sxs-lookup"><span data-stu-id="fb16e-109">For example, object types, such as texture2d, samplers, and strings, are not valid in actual effect files, but are valid in the SasHostParameterValue.</span></span> <span data-ttu-id="fb16e-110">Un'applicazione host può implementare SasHostParameterValue in qualsiasi modo, purché sia conforme alla descrizione riportata di seguito. la definizione effettiva si trova nel file di inclusione degli effetti standard DXSAS ( \[ /Utilities/source/SAS/SAS.fxh radice SDK \] ).</span><span class="sxs-lookup"><span data-stu-id="fb16e-110">A host application can implement SasHostParameterValue in any way so long as it conforms to the description below; the actual definition is located in the DXSAS standard effect include file (\[SDK Root\]/Utilities/Source/Sas/Sas.fxh).</span></span>

<span data-ttu-id="fb16e-111">Si noti che le matrici in SasHostParameterValue, ad esempio luci o fotocamere, hanno una lunghezza illimitata.</span><span class="sxs-lookup"><span data-stu-id="fb16e-111">Note that arrays in the SasHostParameterValue such as Lights or Cameras have unbounded length.</span></span> <span data-ttu-id="fb16e-112">Ciò significa che gli effetti possono essere associati a qualsiasi indice arbitrario in tali matrici e le applicazioni host devono fornire valori predefiniti significativi nei casi in cui non è possibile fornire alcun valore di applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb16e-112">This means that effects can bind to any arbitrary index in those arrays and host applications must provide meaningful defaults in the cases where no application value can be provided.</span></span>

<span data-ttu-id="fb16e-113">Alcuni tipi e costanti devono essere definiti nell'inclusione standard DXSAS, come indicato nella definizione dell'inclusione standard.</span><span class="sxs-lookup"><span data-stu-id="fb16e-113">Some types and constants are required to be defined in the DXSAS standard include, as noted in the definition of the standard include.</span></span> <span data-ttu-id="fb16e-114">Ciò consente agli effetti di associare facilmente i valori aggregati da SasHostParameterValue a parametri di effetto strutturati.</span><span class="sxs-lookup"><span data-stu-id="fb16e-114">This allows effects to easily bind aggregated values from the SasHostParameterValue to structured effect parameters.</span></span>



| <span data-ttu-id="fb16e-115">Raccolta SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="fb16e-115">SasHostParameterValue Collection</span></span>    | <span data-ttu-id="fb16e-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb16e-116">Type</span></span>            | <span data-ttu-id="fb16e-117">Membro</span><span class="sxs-lookup"><span data-stu-id="fb16e-117">Member</span></span>                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [<span data-ttu-id="fb16e-118">Time</span><span class="sxs-lookup"><span data-stu-id="fb16e-118">Time</span></span>](#time)                       | <span data-ttu-id="fb16e-119">float</span><span class="sxs-lookup"><span data-stu-id="fb16e-119">float</span></span>           | <span data-ttu-id="fb16e-120">SAS. Time. Now</span><span class="sxs-lookup"><span data-stu-id="fb16e-120">Sas.Time.Now</span></span>                                 |
|                                     | <span data-ttu-id="fb16e-121">float</span><span class="sxs-lookup"><span data-stu-id="fb16e-121">float</span></span>           | <span data-ttu-id="fb16e-122">SAS. Time. Last</span><span class="sxs-lookup"><span data-stu-id="fb16e-122">Sas.Time.Last</span></span>                                |
|                                     | <span data-ttu-id="fb16e-123">INT</span><span class="sxs-lookup"><span data-stu-id="fb16e-123">int</span></span>             | <span data-ttu-id="fb16e-124">SAS. Time. NumeroFrame</span><span class="sxs-lookup"><span data-stu-id="fb16e-124">Sas.Time.FrameNumber</span></span>                         |
| [<span data-ttu-id="fb16e-125">Mappa ambiente</span><span class="sxs-lookup"><span data-stu-id="fb16e-125">Environment Map</span></span>](#environment-map) | <span data-ttu-id="fb16e-126">textureCUBE</span><span class="sxs-lookup"><span data-stu-id="fb16e-126">textureCUBE</span></span>     | <span data-ttu-id="fb16e-127">SAS. EnvironmentMap</span><span class="sxs-lookup"><span data-stu-id="fb16e-127">Sas.EnvironmentMap</span></span>                           |
| [<span data-ttu-id="fb16e-128">Fotocamera</span><span class="sxs-lookup"><span data-stu-id="fb16e-128">Camera</span></span>](#camera)                   | <span data-ttu-id="fb16e-129">SasCamera</span><span class="sxs-lookup"><span data-stu-id="fb16e-129">SasCamera</span></span>       | <span data-ttu-id="fb16e-130">SAS. camera</span><span class="sxs-lookup"><span data-stu-id="fb16e-130">Sas.Camera</span></span>                                   |
|                                     | <span data-ttu-id="fb16e-131">float4x4</span><span class="sxs-lookup"><span data-stu-id="fb16e-131">float4x4</span></span>        | <span data-ttu-id="fb16e-132">SAS. camera. WorldToView</span><span class="sxs-lookup"><span data-stu-id="fb16e-132">Sas.Camera.WorldToView</span></span>                       |
|                                     | <span data-ttu-id="fb16e-133">float4x4</span><span class="sxs-lookup"><span data-stu-id="fb16e-133">float4x4</span></span>        | <span data-ttu-id="fb16e-134">SAS. camera. Projection</span><span class="sxs-lookup"><span data-stu-id="fb16e-134">Sas.Camera.Projection</span></span>                        |
|                                     | <span data-ttu-id="fb16e-135">float2</span><span class="sxs-lookup"><span data-stu-id="fb16e-135">float2</span></span>          | <span data-ttu-id="fb16e-136">SAS. camera. NearFarClipping</span><span class="sxs-lookup"><span data-stu-id="fb16e-136">Sas.Camera.NearFarClipping</span></span>                   |
| [<span data-ttu-id="fb16e-137">Chiaro</span><span class="sxs-lookup"><span data-stu-id="fb16e-137">Light</span></span>](#light)                     | <span data-ttu-id="fb16e-138">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="fb16e-138">SasAmbientLight</span></span> | <span data-ttu-id="fb16e-139">AmbientLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="fb16e-139">AmbientLight\[ZeroOrMore\];</span></span>                  |
|                                     | <span data-ttu-id="fb16e-140">INT</span><span class="sxs-lookup"><span data-stu-id="fb16e-140">int</span></span>             | <span data-ttu-id="fb16e-141">SAS. NumAmbientLights</span><span class="sxs-lookup"><span data-stu-id="fb16e-141">Sas.NumAmbientLights</span></span>                         |
|                                     | <span data-ttu-id="fb16e-142">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="fb16e-142">SasAmbientLight</span></span> | <span data-ttu-id="fb16e-143">DirectionalLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="fb16e-143">DirectionalLight\[ZeroOrMore\];</span></span>              |
|                                     | <span data-ttu-id="fb16e-144">INT</span><span class="sxs-lookup"><span data-stu-id="fb16e-144">int</span></span>             | <span data-ttu-id="fb16e-145">SAS. NumDirectionalLights</span><span class="sxs-lookup"><span data-stu-id="fb16e-145">Sas.NumDirectionalLights</span></span>                     |
|                                     | <span data-ttu-id="fb16e-146">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="fb16e-146">SasAmbientLight</span></span> | <span data-ttu-id="fb16e-147">PointLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="fb16e-147">PointLight\[ZeroOrMore\];</span></span>                    |
|                                     | <span data-ttu-id="fb16e-148">INT</span><span class="sxs-lookup"><span data-stu-id="fb16e-148">int</span></span>             | <span data-ttu-id="fb16e-149">SAS. NumPointLights</span><span class="sxs-lookup"><span data-stu-id="fb16e-149">Sas.NumPointLights</span></span>                           |
|                                     | <span data-ttu-id="fb16e-150">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="fb16e-150">SasAmbientLight</span></span> | <span data-ttu-id="fb16e-151">\[ZeroOrMore Spotlight \] ;</span><span class="sxs-lookup"><span data-stu-id="fb16e-151">SpotLight\[ZeroOrMore\];</span></span>                     |
|                                     | <span data-ttu-id="fb16e-152">INT</span><span class="sxs-lookup"><span data-stu-id="fb16e-152">int</span></span>             | <span data-ttu-id="fb16e-153">SAS. NumSpotLights</span><span class="sxs-lookup"><span data-stu-id="fb16e-153">Sas.NumSpotLights</span></span>                            |
| [<span data-ttu-id="fb16e-154">Shadow</span><span class="sxs-lookup"><span data-stu-id="fb16e-154">Shadow</span></span>](#shadow)                   | <span data-ttu-id="fb16e-155">float4x4</span><span class="sxs-lookup"><span data-stu-id="fb16e-155">float4x4</span></span>        | <span data-ttu-id="fb16e-156">ZeroOrMore SAS. \[ shadow \] . WorldToShadow</span><span class="sxs-lookup"><span data-stu-id="fb16e-156">Sas.Shadow\[ZeroOrMore\].WorldToShadow</span></span>       |
|                                     | <span data-ttu-id="fb16e-157">texture2D</span><span class="sxs-lookup"><span data-stu-id="fb16e-157">texture2D</span></span>       | <span data-ttu-id="fb16e-158">ZeroOrMore SAS. \[ shadow \] . ShadowMap</span><span class="sxs-lookup"><span data-stu-id="fb16e-158">Sas.Shadow\[ZeroOrMore\].ShadowMap</span></span>           |
| [<span data-ttu-id="fb16e-159">Struttura</span><span class="sxs-lookup"><span data-stu-id="fb16e-159">Skeleton</span></span>](#skeleton)               | <span data-ttu-id="fb16e-160">float4x4</span><span class="sxs-lookup"><span data-stu-id="fb16e-160">float4x4</span></span>        | <span data-ttu-id="fb16e-161">SAS. Skeleton. MeshToJointToWorld \[ OneOrMore\]</span><span class="sxs-lookup"><span data-stu-id="fb16e-161">Sas.Skeleton.MeshToJointToWorld\[OneOrMore\]</span></span> |
|                                     | <span data-ttu-id="fb16e-162">INT</span><span class="sxs-lookup"><span data-stu-id="fb16e-162">int</span></span>             | <span data-ttu-id="fb16e-163">SAS. Skeleton. NumJoints</span><span class="sxs-lookup"><span data-stu-id="fb16e-163">Sas.Skeleton.NumJoints</span></span>                       |



 

### <a name="time"></a><span data-ttu-id="fb16e-164">Tempo</span><span class="sxs-lookup"><span data-stu-id="fb16e-164">Time</span></span>

<span data-ttu-id="fb16e-165">Valore dell'ora o dell'orologio virtuale dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="fb16e-165">The host application's virtual clock or time value.</span></span> <span data-ttu-id="fb16e-166">I membri includono:</span><span class="sxs-lookup"><span data-stu-id="fb16e-166">Members include:</span></span>

-   <span data-ttu-id="fb16e-167">SAS. Time. Now: valore del clock virtuale dell'applicazione host nel punto in cui verrà eseguito il rendering dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="fb16e-167">Sas.Time.Now - the value of the host application virtual clock at the point at which the effect will be rendered.</span></span>
-   <span data-ttu-id="fb16e-168">SAS. Time. Last: valore di Now al rendering precedente.</span><span class="sxs-lookup"><span data-stu-id="fb16e-168">Sas.Time.Last - the value of Now at the previous render.</span></span>
-   <span data-ttu-id="fb16e-169">SAS. Time. NumeroFrame: valore del contatore che viene incrementato una volta per ogni frame sottoposto a rendering.</span><span class="sxs-lookup"><span data-stu-id="fb16e-169">Sas.Time.FrameNumber - the counter value that is incremented once per rendered frame.</span></span>

<span data-ttu-id="fb16e-170">Gli effetti devono gestire correttamente il fatto che i valori di questi membri possono potenzialmente eseguire il wrapping durante i tempi di esecuzione estremamente lunghi.</span><span class="sxs-lookup"><span data-stu-id="fb16e-170">Effects must properly handle the fact that the values of these members can potentially wrap around during extremely long execution times.</span></span> <span data-ttu-id="fb16e-171">Ora e l'ultimo possono avere valori molto grandi.</span><span class="sxs-lookup"><span data-stu-id="fb16e-171">Now and Last may have very large values.</span></span>

### <a name="environment-map"></a><span data-ttu-id="fb16e-172">Mappa ambiente</span><span class="sxs-lookup"><span data-stu-id="fb16e-172">Environment Map</span></span>

<span data-ttu-id="fb16e-173">Mappa dell'ambiente cubica.</span><span class="sxs-lookup"><span data-stu-id="fb16e-173">A cubic environment map.</span></span> <span data-ttu-id="fb16e-174">Se un effetto tenta di eseguire l'associazione a SAS. EnvironmentMap, le applicazioni host devono fornire una trama del cubo valida.</span><span class="sxs-lookup"><span data-stu-id="fb16e-174">Host applications must provide a valid cube texture if an effect attempts to bind to Sas.EnvironmentMap.</span></span>

### <a name="camera"></a><span data-ttu-id="fb16e-175">Fotocamera</span><span class="sxs-lookup"><span data-stu-id="fb16e-175">Camera</span></span>

<span data-ttu-id="fb16e-176">Fotocamera di cui è in corso il rendering.</span><span class="sxs-lookup"><span data-stu-id="fb16e-176">The camera currently being rendered.</span></span> <span data-ttu-id="fb16e-177">I membri includono:</span><span class="sxs-lookup"><span data-stu-id="fb16e-177">Members include:</span></span>

-   <span data-ttu-id="fb16e-178">SAS. camera. WorldToView: matrice di visualizzazione globale composita per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="fb16e-178">Sas.Camera.WorldToView - the composite world-view matrix for the camera.</span></span>
-   <span data-ttu-id="fb16e-179">SAS. camera. Projection: matrice di proiezione per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="fb16e-179">Sas.Camera.Projection - the projection matrix for the camera.</span></span>
-   <span data-ttu-id="fb16e-180">SAS. camera. NearFarClipping: valori dei piani di ritaglio vicini e lontani.</span><span class="sxs-lookup"><span data-stu-id="fb16e-180">Sas.Camera.NearFarClipping - the values of the near and far clipping planes.</span></span>

### <a name="light"></a><span data-ttu-id="fb16e-181">Chiaro</span><span class="sxs-lookup"><span data-stu-id="fb16e-181">Light</span></span>

<span data-ttu-id="fb16e-182">Una o più luci della scena.</span><span class="sxs-lookup"><span data-stu-id="fb16e-182">One or more scene lights.</span></span> <span data-ttu-id="fb16e-183">La raccolta di luci viene dichiarata come una matrice in cui:</span><span class="sxs-lookup"><span data-stu-id="fb16e-183">The collection of lights is declared as an array where:</span></span>

-   <span data-ttu-id="fb16e-184">Color: colore RGB.</span><span class="sxs-lookup"><span data-stu-id="fb16e-184">Color - an RGB color.</span></span> <span data-ttu-id="fb16e-185">Il valore predefinito è (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="fb16e-185">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="fb16e-186">Direzione: direzione della luce.</span><span class="sxs-lookup"><span data-stu-id="fb16e-186">Direction - the light direction.</span></span> <span data-ttu-id="fb16e-187">Il valore predefinito è (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="fb16e-187">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="fb16e-188">Intervallo: distanza dalla luce in cui i raggi luminosi non hanno effetto sulla scena.</span><span class="sxs-lookup"><span data-stu-id="fb16e-188">Range - the distance from the light where the light rays have no effect on the scene.</span></span> <span data-ttu-id="fb16e-189">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="fb16e-189">The default value is 0.</span></span>
-   <span data-ttu-id="fb16e-190">Theta: angolo del cono interno di un Spotlight, misurato in radianti.</span><span class="sxs-lookup"><span data-stu-id="fb16e-190">Theta - the inner cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="fb16e-191">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="fb16e-191">The default value is 0.</span></span>
-   <span data-ttu-id="fb16e-192">Phi: angolo del cono esterno di un Spotlight, misurato in radianti.</span><span class="sxs-lookup"><span data-stu-id="fb16e-192">Phi - the outer cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="fb16e-193">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="fb16e-193">The default value is 0.</span></span>

<span data-ttu-id="fb16e-194">Il numero di luci deve essere impostato sul numero di luci associate alla matrice associata.</span><span class="sxs-lookup"><span data-stu-id="fb16e-194">The number of lights must be set to the number of lights bound into the associated array.</span></span> <span data-ttu-id="fb16e-195">Gli effetti possono scegliere di ignorare il numero di luci e di associarle a qualsiasi elemento di una delle matrici chiare.</span><span class="sxs-lookup"><span data-stu-id="fb16e-195">Effects can choose to ignore the number of lights and bind to any element of one of the light arrays.</span></span> <span data-ttu-id="fb16e-196">Pertanto, le applicazioni host devono fornire un'associazione valida per gli elementi oltre il numero di spie nella matrice.</span><span class="sxs-lookup"><span data-stu-id="fb16e-196">Therefore, host applications must provide a valid binding for elements beyond the number of lights in the array.</span></span>

<span data-ttu-id="fb16e-197">ZeroOrMore implica che la matrice può contenere un numero qualsiasi di elementi.</span><span class="sxs-lookup"><span data-stu-id="fb16e-197">ZeroOrMore implies that the array may have any number of elements.</span></span>

### <a name="shadow"></a><span data-ttu-id="fb16e-198">Ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="fb16e-198">Shadow</span></span>

<span data-ttu-id="fb16e-199">Buffer Shadow che è costituito da:</span><span class="sxs-lookup"><span data-stu-id="fb16e-199">Shadow buffers which consists of:</span></span>

-   <span data-ttu-id="fb16e-200">WorldToShadow: matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="fb16e-200">WorldToShadow - an array of matrices.</span></span>
-   <span data-ttu-id="fb16e-201">ShadowMap: file di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="fb16e-201">ShadowMap - a 2D texture file.</span></span>

<span data-ttu-id="fb16e-202">ZeroOrMore implica che la matrice può contenere un numero qualsiasi di elementi (zero indica una matrice vuota).</span><span class="sxs-lookup"><span data-stu-id="fb16e-202">ZeroOrMore implies that the array may have any number of elements (zero means an empty array).</span></span>

<span data-ttu-id="fb16e-203">Un effetto dichiarerebbe un campionatore come segue:</span><span class="sxs-lookup"><span data-stu-id="fb16e-203">An effect would declare a sampler as follows:</span></span>


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a><span data-ttu-id="fb16e-204">Struttura</span><span class="sxs-lookup"><span data-stu-id="fb16e-204">Skeleton</span></span>

<span data-ttu-id="fb16e-205">Set di frame che costituiscono l'oggetto attualmente in fase di rendering.</span><span class="sxs-lookup"><span data-stu-id="fb16e-205">The set of frames that compose the currently rendering object.</span></span> <span data-ttu-id="fb16e-206">Gli esempi di frame sono Bones e Transforms.</span><span class="sxs-lookup"><span data-stu-id="fb16e-206">Frame examples are bones and transforms.</span></span> <span data-ttu-id="fb16e-207">ad esempio:</span><span class="sxs-lookup"><span data-stu-id="fb16e-207">This includes:</span></span>

-   <span data-ttu-id="fb16e-208">MeshToJointToWorld: matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="fb16e-208">MeshToJointToWorld - an array of matrices.</span></span>
-   <span data-ttu-id="fb16e-209">NumJoints: numero di giunzioni nello scheletro.</span><span class="sxs-lookup"><span data-stu-id="fb16e-209">NumJoints - the number of joints in the skeleton.</span></span>

<span data-ttu-id="fb16e-210">OneOrMore implica che la matrice ha almeno un oggetto e può contenere un numero qualsiasi di elementi.</span><span class="sxs-lookup"><span data-stu-id="fb16e-210">OneOrMore implies that the array has at least one and may contain any number of elements.</span></span>

<span data-ttu-id="fb16e-211">La definizione supporta sia gli oggetti mesh rigidi che quelli con skin usando lo stesso set di valori di [raccolta SasHostParameterValue](#sashostparametervalue-collection) con un'interpretazione diversa.</span><span class="sxs-lookup"><span data-stu-id="fb16e-211">The definition supports both rigid and skinned mesh objects using the same set of [SasHostParameterValue Collection](#sashostparametervalue-collection) values with different interpretation.</span></span>

## <a name="sasbindaddress"></a><span data-ttu-id="fb16e-212">SasBindAddress</span><span class="sxs-lookup"><span data-stu-id="fb16e-212">SasBindAddress</span></span>

<span data-ttu-id="fb16e-213">Questa annotazione viene aggiunta all'inizio di un file di effetti per associare un parametro di effetto al parametro corrispondente definito nella [raccolta SasHostParameterValue](#sashostparametervalue-collection).</span><span class="sxs-lookup"><span data-stu-id="fb16e-213">This annotation is added to the top of an effect file to associate an effect parameter with its corresponding parameter defined in the [SasHostParameterValue Collection](#sashostparametervalue-collection).</span></span> <span data-ttu-id="fb16e-214">L'annotazione è dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="fb16e-214">The annotation is declared like this:</span></span>


```
string SasBindAddress = "SasHostParameterValue";
```



<span data-ttu-id="fb16e-215">Questo esempio associa la matrice globale degli effetti alla matrice MeshToJointToWorld:</span><span class="sxs-lookup"><span data-stu-id="fb16e-215">This example binds the effect world matrix to the MeshToJointToWorld matrix:</span></span>


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



<span data-ttu-id="fb16e-216">Questa annotazione indica all'applicazione host che è necessario impostare il valore della matrice globale degli effetti utilizzando i dati nella matrice MeshToJointToWorld.</span><span class="sxs-lookup"><span data-stu-id="fb16e-216">This annotation tells the host application that it needs to set the value of the effect world matrix using the data in the MeshToJointToWorld matrix.</span></span>

<span data-ttu-id="fb16e-217">La sintassi dell'annotazione dell'indirizzo di binding è stata definita molto simile alla sintassi usata da [**ID3DXEffect**](id3dxeffect.md) per ottenere e impostare i parametri di effetto.</span><span class="sxs-lookup"><span data-stu-id="fb16e-217">The bind address annotation syntax was defined to be very similar with the syntax used by [**ID3DXEffect**](id3dxeffect.md) to get and set effect parameters.</span></span> <span data-ttu-id="fb16e-218">L'unica differenza tra la grammatica DXSAS e i metodi **ID3DXEffect** è l'aggiunta del token di indice asterisco.</span><span class="sxs-lookup"><span data-stu-id="fb16e-218">The only difference between the DXSAS grammar and **ID3DXEffect** methods is the addition of the asterisk index token.</span></span> <span data-ttu-id="fb16e-219">Di seguito è riportato un altro esempio di utilizzo dell'indice asterisco:</span><span class="sxs-lookup"><span data-stu-id="fb16e-219">Here is another example using the asterisk index:</span></span>


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



<span data-ttu-id="fb16e-220">Il token di indice asterisco indica che tutti gli elementi della matrice di valori envirnmant host specifica (in questo caso il colore) devono essere associati nel parametro associato.</span><span class="sxs-lookup"><span data-stu-id="fb16e-220">The asterisk index token denotes that all elements of the particular host envirnmant value array (color in this case) should be bound in the associated parameter.</span></span> <span data-ttu-id="fb16e-221">Più token di indice asterisco consentono di associare effetti a sottoelementi di una matrice di strutture senza che sia necessario associare l'intera struttura.</span><span class="sxs-lookup"><span data-stu-id="fb16e-221">Multiple asterisk index tokens allow effects to bind to sub-elements of an array of structures without the need to bind the entire structure itself.</span></span> <span data-ttu-id="fb16e-222">Questo esempio associa i valori dei colori delle prime sei luci a un parametro Effect.</span><span class="sxs-lookup"><span data-stu-id="fb16e-222">This example binds the color values of the first six lights to an effect parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb16e-223">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fb16e-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb16e-224">Informazioni di riferimento sulla semantica e le annotazioni standard DirectX</span><span class="sxs-lookup"><span data-stu-id="fb16e-224">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



