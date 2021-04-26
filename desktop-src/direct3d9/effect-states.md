---
description: Gli stati degli effetti vengono usati per inizializzare gli stati della pipeline in preparazione per l'elaborazione di vertici e pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Stati di effetto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe92661fda82bd7dfa47ead0061ef8606e422a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998868"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="34c38-103">Stati di effetto (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="34c38-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="34c38-104">Gli stati degli effetti vengono usati per inizializzare gli stati della pipeline in preparazione per l'elaborazione di vertici e pixel.</span><span class="sxs-lookup"><span data-stu-id="34c38-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="34c38-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="34c38-105">Where:</span></span>

-   <span data-ttu-id="34c38-106">stato dell'effetto: simile agli stati tradizionali della pipeline di funzioni fisse.</span><span class="sxs-lookup"><span data-stu-id="34c38-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="34c38-107">Di seguito è riportato un elenco completo degli stati.</span><span class="sxs-lookup"><span data-stu-id="34c38-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="34c38-108">\[\[ \] index \] - Indice integer facoltativo.</span><span class="sxs-lookup"><span data-stu-id="34c38-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="34c38-109">L'indice identifica uno stato specifico all'interno di una matrice di stati di effetto.</span><span class="sxs-lookup"><span data-stu-id="34c38-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="34c38-110">Le parentesi esterne indicano che un indice è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="34c38-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="34c38-111">Se viene usato un indice, assicurarsi di usare le parentesi interne.</span><span class="sxs-lookup"><span data-stu-id="34c38-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="34c38-112">expression : espressione di assegnazione di stato.</span><span class="sxs-lookup"><span data-stu-id="34c38-112">expression - State assignment expression.</span></span> <span data-ttu-id="34c38-113">Vedere [Espressioni (Direct3D 9).](expressions.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="34c38-114">Ogni stato ha un tipo di dati nativo.</span><span class="sxs-lookup"><span data-stu-id="34c38-114">Each state has a native data type.</span></span> <span data-ttu-id="34c38-115">Si tratta del tipo di dati in cui lo stato prevede valori quando vengono assegnati dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="34c38-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="34c38-116">I tipi di dati previsti per ogni stato sono elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="34c38-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="34c38-117">Si noti che l'interfaccia dell'effetto tenterà di eseguire il cast dei valori nel tipo appropriato il prima possibile.</span><span class="sxs-lookup"><span data-stu-id="34c38-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="34c38-118">È possibile eseguire il cast dei valori letterali in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="34c38-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="34c38-119">Quando vengono chiamati i metodi Set appropriati, è necessario eseguire il cast dei valori non letterali (ad esempio variabili regolari).</span><span class="sxs-lookup"><span data-stu-id="34c38-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="34c38-120">Ad esempio, l'interfaccia dell'effetto esegue il cast dei valori impostati usando [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)e altre funzioni simili, se necessario.</span><span class="sxs-lookup"><span data-stu-id="34c38-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="34c38-121">Per ottenere prestazioni migliori, assicurarsi che i valori passati all'interfaccia dell'effetto siano già del tipo corretto e che non sia necessario eseguire il cast.</span><span class="sxs-lookup"><span data-stu-id="34c38-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="34c38-122">Se il runtime non è in grado di eseguire il cast di un valore, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="34c38-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="34c38-123">Gli stati degli effetti possono essere suddivisi nelle categorie seguenti:</span><span class="sxs-lookup"><span data-stu-id="34c38-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="34c38-124">Stati di luce</span><span class="sxs-lookup"><span data-stu-id="34c38-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="34c38-125">Stati dei materiali</span><span class="sxs-lookup"><span data-stu-id="34c38-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="34c38-126">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="34c38-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="34c38-127">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="34c38-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="34c38-128">Stati di rendering della pipe di vertice</span><span class="sxs-lookup"><span data-stu-id="34c38-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="34c38-129">Stati del campionatore</span><span class="sxs-lookup"><span data-stu-id="34c38-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="34c38-130">Stati della fase del campionatore</span><span class="sxs-lookup"><span data-stu-id="34c38-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="34c38-131">Stati dello shader</span><span class="sxs-lookup"><span data-stu-id="34c38-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="34c38-132">Stati costanti shader</span><span class="sxs-lookup"><span data-stu-id="34c38-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="34c38-133">Stati di trama</span><span class="sxs-lookup"><span data-stu-id="34c38-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="34c38-134">Stati della fase di trama</span><span class="sxs-lookup"><span data-stu-id="34c38-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="34c38-135">Stati di trasformazione</span><span class="sxs-lookup"><span data-stu-id="34c38-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="34c38-136">Stati di luce</span><span class="sxs-lookup"><span data-stu-id="34c38-136">Light States</span></span>

<span data-ttu-id="34c38-137">Per abilitare le prestazioni migliori per l'applicazione di un effetto, tutti i componenti di una luce o di un materiale devono essere specificati nel file dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="34c38-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="34c38-138">Gli stati che non è possibile dichiarare sono impostati su un valore predefinito perché Direct3D non è in grado di impostare singolarmente gli stati di luce.</span><span class="sxs-lookup"><span data-stu-id="34c38-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



| <span data-ttu-id="34c38-139">Stato chiaro</span><span class="sxs-lookup"><span data-stu-id="34c38-139">Light State</span></span>            | <span data-ttu-id="34c38-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-140">Type</span></span>   | <span data-ttu-id="34c38-141">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-141">Values</span></span>                                                                                                              |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c38-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="34c38-143">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-143">float4</span></span> | <span data-ttu-id="34c38-144">Vedere il membro ambiente di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="34c38-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="34c38-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="34c38-146">float</span><span class="sxs-lookup"><span data-stu-id="34c38-146">float</span></span>  | <span data-ttu-id="34c38-147">Vedere il membro Attenuation0 di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="34c38-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="34c38-149">float</span><span class="sxs-lookup"><span data-stu-id="34c38-149">float</span></span>  | <span data-ttu-id="34c38-150">Vedere il membro Attenuation1 di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="34c38-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="34c38-152">float</span><span class="sxs-lookup"><span data-stu-id="34c38-152">float</span></span>  | <span data-ttu-id="34c38-153">Vedere il membro Attenuation2 di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="34c38-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="34c38-155">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-155">float4</span></span> | <span data-ttu-id="34c38-156">Vedere il membro Diffuse di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="34c38-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="34c38-158">float3</span><span class="sxs-lookup"><span data-stu-id="34c38-158">float3</span></span> | <span data-ttu-id="34c38-159">Vedere il membro Direction di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="34c38-160">LightEnable \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="34c38-161">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-161">bool</span></span>   | <span data-ttu-id="34c38-162">**TRUE** o **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="34c38-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="34c38-163">Vedere l'argomento bEnable in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="34c38-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="34c38-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="34c38-165">float</span><span class="sxs-lookup"><span data-stu-id="34c38-165">float</span></span>  | <span data-ttu-id="34c38-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="34c38-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="34c38-167">Vedere il membro Falloff di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="34c38-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="34c38-169">float</span><span class="sxs-lookup"><span data-stu-id="34c38-169">float</span></span>  | <span data-ttu-id="34c38-170">Vedere il membro Phi di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="34c38-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="34c38-172">float3</span><span class="sxs-lookup"><span data-stu-id="34c38-172">float3</span></span> | <span data-ttu-id="34c38-173">Vedere il membro Position di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="34c38-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-174">LightRange\[n\]</span></span>        | <span data-ttu-id="34c38-175">float</span><span class="sxs-lookup"><span data-stu-id="34c38-175">float</span></span>  | <span data-ttu-id="34c38-176">Vedere il membro Range di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="34c38-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="34c38-178">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-178">float4</span></span> | <span data-ttu-id="34c38-179">Vedere il membro Specular di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="34c38-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="34c38-181">float</span><span class="sxs-lookup"><span data-stu-id="34c38-181">float</span></span>  | <span data-ttu-id="34c38-182">Vedere il membro Theta di [**D3DLIGHT9.**](d3dlight9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="34c38-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="34c38-183">LightType\[n\]</span></span>         | <span data-ttu-id="34c38-184">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-184">dword</span></span>  | <span data-ttu-id="34c38-185">Stesso valore della matrice di un massimo di n [**valori D3DLIGHTTYPE**](./d3dlighttype.md) senza il prefisso D3DLIGHT. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="34c38-186">Esempio:</span><span class="sxs-lookup"><span data-stu-id="34c38-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="34c38-187">In questo modo si abiliterà l'illuminazione, si accenderà il tipo, si imposta la posizione della luce su float3<10.0f, 1.0f, 23.0f> e si imposta il colore di ambiente su float4<0,7f, 0,0f, 0,0f, 1,0f>.</span><span class="sxs-lookup"><span data-stu-id="34c38-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="34c38-188">Stati dei materiali</span><span class="sxs-lookup"><span data-stu-id="34c38-188">Material States</span></span>

<span data-ttu-id="34c38-189">Gli stati che non è possibile dichiarare sono impostati su un valore predefinito perché Direct3D non può impostare gli stati dei materiali singolarmente.</span><span class="sxs-lookup"><span data-stu-id="34c38-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



| <span data-ttu-id="34c38-190">Stato del materiale</span><span class="sxs-lookup"><span data-stu-id="34c38-190">Material State</span></span>   | <span data-ttu-id="34c38-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-191">Type</span></span>   | <span data-ttu-id="34c38-192">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-192">Values</span></span>                                         |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="34c38-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="34c38-193">MaterialAmbient</span></span>  | <span data-ttu-id="34c38-194">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-194">float4</span></span> | <span data-ttu-id="34c38-195">Stesso valore di [ **Ambiente**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="34c38-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="34c38-196">MaterialDiffuse</span></span>  | <span data-ttu-id="34c38-197">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-197">float4</span></span> | <span data-ttu-id="34c38-198">Stesso valore di [ **Diffuse**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="34c38-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="34c38-199">MaterialEmissive</span></span> | <span data-ttu-id="34c38-200">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-200">float4</span></span> | <span data-ttu-id="34c38-201">Stesso valore di [ **Emissive**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="34c38-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="34c38-202">MaterialPower</span></span>    | <span data-ttu-id="34c38-203">float</span><span class="sxs-lookup"><span data-stu-id="34c38-203">float</span></span>  | <span data-ttu-id="34c38-204">Stesso valore di [ **Power**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="34c38-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="34c38-205">MaterialSpecular</span></span> | <span data-ttu-id="34c38-206">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-206">float4</span></span> | <span data-ttu-id="34c38-207">Stesso valore di [ **Specular**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="34c38-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="34c38-208">Esempio:</span><span class="sxs-lookup"><span data-stu-id="34c38-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="34c38-209">Il colore diffuso verrà impostato su float4<0,7f, 0,0f, 0,0f, 1,0f> e la potenza del materiale sarà 3,0f.</span><span class="sxs-lookup"><span data-stu-id="34c38-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="34c38-210">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="34c38-210">Render States</span></span>

<span data-ttu-id="34c38-211">Esistono due tipi di stati di rendering:</span><span class="sxs-lookup"><span data-stu-id="34c38-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="34c38-212">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="34c38-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="34c38-213">Stati di rendering delle pipe dei vertici</span><span class="sxs-lookup"><span data-stu-id="34c38-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="34c38-214">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="34c38-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="34c38-215">Gli stati di rendering dei file degli effetti hanno nomi simili agli stati della pipeline di funzioni fisse, spesso con il prefisso rimosso.</span><span class="sxs-lookup"><span data-stu-id="34c38-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34c38-216">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="34c38-216">Render State</span></span></td>
<td><span data-ttu-id="34c38-217">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-217">Type</span></span></td>
<td><span data-ttu-id="34c38-218">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="34c38-220">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-220">bool</span></span></td>
<td><span data-ttu-id="34c38-221">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-221">True or False.</span></span> <span data-ttu-id="34c38-222">Gli stessi valori D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="34c38-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="34c38-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="34c38-224">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-224">dword</span></span></td>
<td><span data-ttu-id="34c38-225">Stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il D3DCMP_ predefinito.</span><span class="sxs-lookup"><span data-stu-id="34c38-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="34c38-226">Vedere D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="34c38-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="34c38-227">AlphaRef</span></span></td>
<td><span data-ttu-id="34c38-228">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-228">dword</span></span></td>
<td><span data-ttu-id="34c38-229">Stessi valori di D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="34c38-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="34c38-231">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-231">dword</span></span></td>
<td><span data-ttu-id="34c38-232">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-232">True or False.</span></span> <span data-ttu-id="34c38-233">Vedere D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="34c38-234">BlendOp</span></span></td>
<td><span data-ttu-id="34c38-235">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-235">dword</span></span></td>
<td><span data-ttu-id="34c38-236">Stessi valori di <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> senza il D3DBLENDOP_ prefisso.</span><span class="sxs-lookup"><span data-stu-id="34c38-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="34c38-238">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-238">dword</span></span></td>
<td><span data-ttu-id="34c38-239">Combinazione bit per bit di RED| VERDE| BLU| Alfa.</span><span class="sxs-lookup"><span data-stu-id="34c38-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="34c38-240">Vedere D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="34c38-241">DepthBias</span></span></td>
<td><span data-ttu-id="34c38-242">float</span><span class="sxs-lookup"><span data-stu-id="34c38-242">float</span></span></td>
<td><span data-ttu-id="34c38-243">Stessi valori di D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="34c38-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="34c38-244">DestBlend</span></span></td>
<td><span data-ttu-id="34c38-245">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-245">dword</span></span></td>
<td><span data-ttu-id="34c38-246">Stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="34c38-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-247">DitherEnable</span></span></td>
<td><span data-ttu-id="34c38-248">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-248">bool</span></span></td>
<td><span data-ttu-id="34c38-249">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-249">True or False.</span></span> <span data-ttu-id="34c38-250">Stessi valori di D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-251">Fillmode</span><span class="sxs-lookup"><span data-stu-id="34c38-251">FillMode</span></span></td>
<td><span data-ttu-id="34c38-252">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-252">dword</span></span></td>
<td><span data-ttu-id="34c38-253">Stessi valori di <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> senza il D3DFILL_ predefinito.</span><span class="sxs-lookup"><span data-stu-id="34c38-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="34c38-254">LastPixel</span></span></td>
<td><span data-ttu-id="34c38-255">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-255">dword</span></span></td>
<td><span data-ttu-id="34c38-256">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-256">True or False.</span></span> <span data-ttu-id="34c38-257">Vedere D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="34c38-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-258">ShadeMode</span><span class="sxs-lookup"><span data-stu-id="34c38-258">ShadeMode</span></span></td>
<td><span data-ttu-id="34c38-259">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-259">dword</span></span></td>
<td><span data-ttu-id="34c38-260">Stessi valori di <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> senza D3DSHADE_ prefisso.</span><span class="sxs-lookup"><span data-stu-id="34c38-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="34c38-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="34c38-262">float</span><span class="sxs-lookup"><span data-stu-id="34c38-262">float</span></span></td>
<td><span data-ttu-id="34c38-263">Stessi valori di D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="34c38-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="34c38-264">SrcBlend</span></span></td>
<td><span data-ttu-id="34c38-265">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-265">dword</span></span></td>
<td><span data-ttu-id="34c38-266">Stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="34c38-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="34c38-268">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-268">bool</span></span></td>
<td><span data-ttu-id="34c38-269">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-269">True or False.</span></span> <span data-ttu-id="34c38-270">Stessi valori di D3DRS_SRGBWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-271">StencilEnable</span></span></td>
<td><span data-ttu-id="34c38-272">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-272">bool</span></span></td>
<td><span data-ttu-id="34c38-273">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-273">True or False.</span></span> <span data-ttu-id="34c38-274">Stessi valori di D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="34c38-275">StencilFail</span></span></td>
<td><span data-ttu-id="34c38-276">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-276">dword</span></span></td>
<td><span data-ttu-id="34c38-277">Stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il D3DSTENCILCAP_ prefisso.</span><span class="sxs-lookup"><span data-stu-id="34c38-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="34c38-278">Vedere D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="34c38-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="34c38-279">StencilFunc</span></span></td>
<td><span data-ttu-id="34c38-280">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-280">dword</span></span></td>
<td><span data-ttu-id="34c38-281">Stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il D3DCMP_ predefinito.</span><span class="sxs-lookup"><span data-stu-id="34c38-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="34c38-282">Vedere D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="34c38-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-283">Maschera di stencil</span><span class="sxs-lookup"><span data-stu-id="34c38-283">StencilMask</span></span></td>
<td><span data-ttu-id="34c38-284">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-284">dword</span></span></td>
<td><span data-ttu-id="34c38-285">Stessi valori di D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="34c38-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="34c38-286">StencilPass</span></span></td>
<td><span data-ttu-id="34c38-287">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-287">dword</span></span></td>
<td><span data-ttu-id="34c38-288">Stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il D3DSTENCILCAP_ prefisso.</span><span class="sxs-lookup"><span data-stu-id="34c38-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="34c38-289">Vedere D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="34c38-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="34c38-290">StencilRef</span></span></td>
<td><span data-ttu-id="34c38-291">INT</span><span class="sxs-lookup"><span data-stu-id="34c38-291">int</span></span></td>
<td><span data-ttu-id="34c38-292">Stessi valori di D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="34c38-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="34c38-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="34c38-294">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-294">dword</span></span></td>
<td><span data-ttu-id="34c38-295">Stessi valori di D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="34c38-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="34c38-296">StencilZFail</span></span></td>
<td><span data-ttu-id="34c38-297">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-297">dword</span></span></td>
<td><span data-ttu-id="34c38-298">Stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza D3DSTENCILCAP_ prefisso.</span><span class="sxs-lookup"><span data-stu-id="34c38-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="34c38-299">Vedere D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="34c38-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="34c38-300">TextureFactor</span></span></td>
<td><span data-ttu-id="34c38-301">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-301">dword</span></span></td>
<td><span data-ttu-id="34c38-302">Stessi valori di <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="34c38-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="34c38-303">Stessi valori di D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="34c38-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="34c38-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="34c38-305">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-305">dword</span></span></td>
<td><span data-ttu-id="34c38-306">I valori sono gli stessi usati da D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="34c38-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="34c38-307">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="34c38-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="34c38-308">COORD0 (che corrisponde a D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="34c38-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="34c38-309">COORD1 (che corrisponde a D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="34c38-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="34c38-310">COORD2 (che corrisponde a D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="34c38-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="34c38-311">COORD3 (che corrisponde a D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="34c38-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="34c38-312">U (che corrisponde a D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="34c38-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="34c38-313">V (che corrisponde a D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="34c38-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="34c38-314">W (che corrisponde a D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="34c38-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-315">ZEnable</span></span></td>
<td><span data-ttu-id="34c38-316">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-316">dword</span></span></td>
<td><span data-ttu-id="34c38-317">Stessi valori di <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> senza D3DZB_ prefisso.</span><span class="sxs-lookup"><span data-stu-id="34c38-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34c38-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="34c38-318">ZFunc</span></span></td>
<td><span data-ttu-id="34c38-319">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-319">dword</span></span></td>
<td><span data-ttu-id="34c38-320">Stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il D3DCMP_ predefinito.</span><span class="sxs-lookup"><span data-stu-id="34c38-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="34c38-321">Vedere D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="34c38-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34c38-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="34c38-323">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-323">bool</span></span></td>
<td><span data-ttu-id="34c38-324">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-324">True or False.</span></span> <span data-ttu-id="34c38-325">Vedere D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="34c38-326">Esempio:</span><span class="sxs-lookup"><span data-stu-id="34c38-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="34c38-327">In questo modo verrà abilitata la fusione alfa e verrà eseguito il rendering di tutte le geometrie in wireframe.</span><span class="sxs-lookup"><span data-stu-id="34c38-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="34c38-328">Stati di rendering delle pipe dei vertici</span><span class="sxs-lookup"><span data-stu-id="34c38-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="34c38-329">Gli stati di rendering dei file degli effetti hanno nomi simili agli stati della pipeline di funzioni fisse, spesso con il prefisso rimosso.</span><span class="sxs-lookup"><span data-stu-id="34c38-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



| <span data-ttu-id="34c38-330">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="34c38-330">Render State</span></span>             | <span data-ttu-id="34c38-331">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-331">Type</span></span>   | <span data-ttu-id="34c38-332">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-332">Values</span></span>                                                                                                                                        |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c38-333">Di ambiente</span><span class="sxs-lookup"><span data-stu-id="34c38-333">Ambient</span></span>                  | <span data-ttu-id="34c38-334">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-334">float4</span></span> | <span data-ttu-id="34c38-335">Stessi valori dell'ambiente D3DRS \_ AMBIENT.</span><span class="sxs-lookup"><span data-stu-id="34c38-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="34c38-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="34c38-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="34c38-337">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-337">dword</span></span>  | <span data-ttu-id="34c38-338">Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="34c38-339">Vedere D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="34c38-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="34c38-340">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="34c38-340">Clipping</span></span>                 | <span data-ttu-id="34c38-341">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-341">bool</span></span>   | <span data-ttu-id="34c38-342">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-342">True or False.</span></span> <span data-ttu-id="34c38-343">Stessi valori di D3DRS \_ CLIPPING.</span><span class="sxs-lookup"><span data-stu-id="34c38-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="34c38-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="34c38-345">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-345">dword</span></span>  | <span data-ttu-id="34c38-346">Combinazione bit per bit delle macro D3DCLIPPLANE0 - D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="34c38-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="34c38-347">Vedere [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="34c38-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="34c38-348">ColorVertex</span></span>              | <span data-ttu-id="34c38-349">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-349">bool</span></span>   | <span data-ttu-id="34c38-350">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-350">True or False.</span></span> <span data-ttu-id="34c38-351">Stessi valori di D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="34c38-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="34c38-352">CullMode</span><span class="sxs-lookup"><span data-stu-id="34c38-352">CullMode</span></span>                 | <span data-ttu-id="34c38-353">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-353">dword</span></span>  | <span data-ttu-id="34c38-354">Stessi valori di [**D3DCULL**](./d3dcull.md) senza il prefisso D3DCULL. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="34c38-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="34c38-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="34c38-356">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-356">dword</span></span>  | <span data-ttu-id="34c38-357">Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="34c38-358">Vedere D3DRS \_ DIFFUSEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="34c38-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="34c38-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="34c38-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="34c38-360">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-360">dword</span></span>  | <span data-ttu-id="34c38-361">Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="34c38-362">Vedere D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="34c38-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="34c38-363">Colore della taschia</span><span class="sxs-lookup"><span data-stu-id="34c38-363">FogColor</span></span>                 | <span data-ttu-id="34c38-364">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-364">dword</span></span>  | <span data-ttu-id="34c38-365">Stessi valori di [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="34c38-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="34c38-366">Vedere D3DRS \_ FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="34c38-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="34c38-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="34c38-367">FogDensity</span></span>               | <span data-ttu-id="34c38-368">float</span><span class="sxs-lookup"><span data-stu-id="34c38-368">float</span></span>  | <span data-ttu-id="34c38-369">Stessi valori di D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="34c38-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="34c38-370">Non si può fare altro che non essere in tempo</span><span class="sxs-lookup"><span data-stu-id="34c38-370">FogEnable</span></span>                | <span data-ttu-id="34c38-371">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-371">bool</span></span>   | <span data-ttu-id="34c38-372">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-372">True or False.</span></span> <span data-ttu-id="34c38-373">Stessi valori di D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="34c38-374">NebbieEnd</span><span class="sxs-lookup"><span data-stu-id="34c38-374">FogEnd</span></span>                   | <span data-ttu-id="34c38-375">float</span><span class="sxs-lookup"><span data-stu-id="34c38-375">float</span></span>  | <span data-ttu-id="34c38-376">Stessi valori di D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="34c38-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="34c38-377">NebbieStart</span><span class="sxs-lookup"><span data-stu-id="34c38-377">FogStart</span></span>                 | <span data-ttu-id="34c38-378">float</span><span class="sxs-lookup"><span data-stu-id="34c38-378">float</span></span>  | <span data-ttu-id="34c38-379">Stessi valori di D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="34c38-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="34c38-380">Modalità tabella di gonfiabili</span><span class="sxs-lookup"><span data-stu-id="34c38-380">FogTableMode</span></span>             | <span data-ttu-id="34c38-381">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-381">dword</span></span>  | <span data-ttu-id="34c38-382">Stessi valori di [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="34c38-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="34c38-383">Vedere D3DRS \_ FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="34c38-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="34c38-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="34c38-384">FogVertexMode</span></span>            | <span data-ttu-id="34c38-385">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-385">dword</span></span>  | <span data-ttu-id="34c38-386">Stessi valori di [**D3DFOGMODE**](./d3dfogmode.md) senza il prefisso D3DFOG. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="34c38-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="34c38-388">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-388">bool</span></span>   | <span data-ttu-id="34c38-389">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-389">True or False.</span></span> <span data-ttu-id="34c38-390">Stessi valori di D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="34c38-391">Luce</span><span class="sxs-lookup"><span data-stu-id="34c38-391">Lighting</span></span>                 | <span data-ttu-id="34c38-392">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-392">bool</span></span>   | <span data-ttu-id="34c38-393">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-393">True or False.</span></span> <span data-ttu-id="34c38-394">Stessi valori dell'illuminazione \_ D3DRS.</span><span class="sxs-lookup"><span data-stu-id="34c38-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="34c38-395">Controllo LocalViewer</span><span class="sxs-lookup"><span data-stu-id="34c38-395">LocalViewer</span></span>              | <span data-ttu-id="34c38-396">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-396">bool</span></span>   | <span data-ttu-id="34c38-397">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-397">True or False.</span></span> <span data-ttu-id="34c38-398">Stessi valori di D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="34c38-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="34c38-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="34c38-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="34c38-400">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-400">bool</span></span>   | <span data-ttu-id="34c38-401">Stessi valori di D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="34c38-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="34c38-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="34c38-402">MultiSampleMask</span></span>          | <span data-ttu-id="34c38-403">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-403">dword</span></span>  | <span data-ttu-id="34c38-404">Stessi valori di D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="34c38-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="34c38-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="34c38-405">NormalizeNormals</span></span>         | <span data-ttu-id="34c38-406">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-406">bool</span></span>   | <span data-ttu-id="34c38-407">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-407">True or False.</span></span> <span data-ttu-id="34c38-408">Stessi valori di D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="34c38-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="34c38-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="34c38-409">PatchSegments</span></span>            | <span data-ttu-id="34c38-410">float</span><span class="sxs-lookup"><span data-stu-id="34c38-410">float</span></span>  | <span data-ttu-id="34c38-411">Stessi valori di nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="34c38-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="34c38-412">PointScale \_ A</span><span class="sxs-lookup"><span data-stu-id="34c38-412">PointScale\_A</span></span>            | <span data-ttu-id="34c38-413">float</span><span class="sxs-lookup"><span data-stu-id="34c38-413">float</span></span>  | <span data-ttu-id="34c38-414">Stessi valori di D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="34c38-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="34c38-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="34c38-415">PointScale\_B</span></span>            | <span data-ttu-id="34c38-416">float</span><span class="sxs-lookup"><span data-stu-id="34c38-416">float</span></span>  | <span data-ttu-id="34c38-417">Stessi valori di D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="34c38-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="34c38-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="34c38-418">PointScale\_C</span></span>            | <span data-ttu-id="34c38-419">float</span><span class="sxs-lookup"><span data-stu-id="34c38-419">float</span></span>  | <span data-ttu-id="34c38-420">Stessi valori di D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="34c38-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="34c38-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-421">PointScaleEnable</span></span>         | <span data-ttu-id="34c38-422">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-422">bool</span></span>   | <span data-ttu-id="34c38-423">Stessi valori di D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="34c38-424">PointSize</span><span class="sxs-lookup"><span data-stu-id="34c38-424">PointSize</span></span>                | <span data-ttu-id="34c38-425">float</span><span class="sxs-lookup"><span data-stu-id="34c38-425">float</span></span>  | <span data-ttu-id="34c38-426">Stessi valori di D3DRS \_ POINTSIZE.</span><span class="sxs-lookup"><span data-stu-id="34c38-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="34c38-427">PointSize \_ Min</span><span class="sxs-lookup"><span data-stu-id="34c38-427">PointSize\_Min</span></span>           | <span data-ttu-id="34c38-428">float</span><span class="sxs-lookup"><span data-stu-id="34c38-428">float</span></span>  | <span data-ttu-id="34c38-429">Stessi valori di D3DRS \_ POINTSIZE \_ MIN.</span><span class="sxs-lookup"><span data-stu-id="34c38-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="34c38-430">PointSize \_ Max</span><span class="sxs-lookup"><span data-stu-id="34c38-430">PointSize\_Max</span></span>           | <span data-ttu-id="34c38-431">float</span><span class="sxs-lookup"><span data-stu-id="34c38-431">float</span></span>  | <span data-ttu-id="34c38-432">Stessi valori di D3DRS \_ POINTSIZE \_ MAX senza il prefisso D3DRS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="34c38-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-433">PointSpriteEnable</span></span>        | <span data-ttu-id="34c38-434">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-434">bool</span></span>   | <span data-ttu-id="34c38-435">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-435">True or False.</span></span> <span data-ttu-id="34c38-436">Stessi valori di D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="34c38-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-437">RangeFogEnable</span></span>           | <span data-ttu-id="34c38-438">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-438">bool</span></span>   | <span data-ttu-id="34c38-439">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-439">True or False.</span></span> <span data-ttu-id="34c38-440">Stessi valori di D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="34c38-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="34c38-441">SpecularEnable</span></span>           | <span data-ttu-id="34c38-442">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-442">bool</span></span>   | <span data-ttu-id="34c38-443">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="34c38-443">True or False.</span></span> <span data-ttu-id="34c38-444">Stessi valori di D3DRS \_ SPECULARENABLE.</span><span class="sxs-lookup"><span data-stu-id="34c38-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="34c38-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="34c38-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="34c38-446">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-446">dword</span></span>  | <span data-ttu-id="34c38-447">Stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il prefisso D3DMCS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="34c38-448">Vedere \_ SPECULARMATERIALSOURCE D3DRS.</span><span class="sxs-lookup"><span data-stu-id="34c38-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="34c38-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="34c38-449">TweenFactor</span></span>              | <span data-ttu-id="34c38-450">float</span><span class="sxs-lookup"><span data-stu-id="34c38-450">float</span></span>  | <span data-ttu-id="34c38-451">Stessi valori di D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="34c38-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="34c38-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="34c38-452">VertexBlend</span></span>              | <span data-ttu-id="34c38-453">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-453">dword</span></span>  | <span data-ttu-id="34c38-454">Stessi valori di [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) senza il prefisso D3DVBF. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="34c38-455">Vedere \_ VERTEXBLEND D3DRS.</span><span class="sxs-lookup"><span data-stu-id="34c38-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="34c38-456">Esempio:</span><span class="sxs-lookup"><span data-stu-id="34c38-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="34c38-457">In questo modo, il colore di ambiente float4<0.7f, 0.0f, 0.0f, 1.0f>, imposta la modalità di culling del backface in senso antiorario e imposta il colore del colore blu su rosso.</span><span class="sxs-lookup"><span data-stu-id="34c38-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="34c38-458">Stati del campionatore</span><span class="sxs-lookup"><span data-stu-id="34c38-458">Sampler States</span></span>

<span data-ttu-id="34c38-459">Uno stato del campionatore rappresenta un oggetto campionatore.</span><span class="sxs-lookup"><span data-stu-id="34c38-459">A sampler state represents a sampler object.</span></span>



| <span data-ttu-id="34c38-460">State</span><span class="sxs-lookup"><span data-stu-id="34c38-460">State</span></span>   | <span data-ttu-id="34c38-461">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-461">Type</span></span>    | <span data-ttu-id="34c38-462">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-462">Values</span></span>                              |
|---------|---------|-------------------------------------|
| <span data-ttu-id="34c38-463">Campionatore</span><span class="sxs-lookup"><span data-stu-id="34c38-463">Sampler</span></span> | <span data-ttu-id="34c38-464">Campionatore</span><span class="sxs-lookup"><span data-stu-id="34c38-464">sampler</span></span> | <span data-ttu-id="34c38-465">**NULL** o blocco di stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="34c38-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="34c38-466">Stati delle fasi del campionatore</span><span class="sxs-lookup"><span data-stu-id="34c38-466">Sampler Stage States</span></span>

<span data-ttu-id="34c38-467">Gli stati della fase del campionatore vengono usati per campionare le trame.</span><span class="sxs-lookup"><span data-stu-id="34c38-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="34c38-468">Lo stato del campionatore determina i tipi di filtro e le modalità di indirizzamento della trama.</span><span class="sxs-lookup"><span data-stu-id="34c38-468">Sampler state determines filtering types and texture addressing modes.</span></span>



| <span data-ttu-id="34c38-469">Stato del campionatore</span><span class="sxs-lookup"><span data-stu-id="34c38-469">Sampler State</span></span>       | <span data-ttu-id="34c38-470">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-470">Type</span></span>                         | <span data-ttu-id="34c38-471">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-471">Values</span></span>                                                                                                                            |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c38-472">AddressU \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-472">AddressU\[16\]</span></span>      | <span data-ttu-id="34c38-473">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-473">dword</span></span>                        | <span data-ttu-id="34c38-474">Stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il prefisso D3DTADDRESS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="34c38-475">Vedere D3DSAMP \_ ADDRESSU.</span><span class="sxs-lookup"><span data-stu-id="34c38-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="34c38-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-476">AddressV\[16\]</span></span>      | <span data-ttu-id="34c38-477">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-477">dword</span></span>                        | <span data-ttu-id="34c38-478">Stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il prefisso D3DTADDRESS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="34c38-479">Vedere D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="34c38-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="34c38-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-480">AddressW\[16\]</span></span>      | <span data-ttu-id="34c38-481">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-481">dword</span></span>                        | <span data-ttu-id="34c38-482">Stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il prefisso D3DTADDRESS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="34c38-483">Vedere D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="34c38-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="34c38-484">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="34c38-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="34c38-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="34c38-486">Stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il prefisso D3DTEXF. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="34c38-487">Vedere D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="34c38-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="34c38-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="34c38-489">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-489">dword</span></span>                        | <span data-ttu-id="34c38-490">Stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il prefisso D3DTEXF. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="34c38-491">Vedere D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="34c38-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="34c38-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="34c38-493">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-493">dword</span></span>                        | <span data-ttu-id="34c38-494">Stessi valori di D3DSAMP \_ MAXANISOTROPY senza il prefisso \_ D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="34c38-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="34c38-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="34c38-496">INT</span><span class="sxs-lookup"><span data-stu-id="34c38-496">int</span></span>                          | <span data-ttu-id="34c38-497">Stessi valori di D3DSAMP \_ MAXMIPLEVEL senza il prefisso D3DSAMP. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="34c38-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="34c38-499">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-499">dword</span></span>                        | <span data-ttu-id="34c38-500">Stessi valori di D3DSAMP \_ MINFILTER senza il prefisso D3DSAMP. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="34c38-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="34c38-502">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-502">dword</span></span>                        | <span data-ttu-id="34c38-503">Stessi valori di D3DSAMP \_ MIPFILTER senza il prefisso D3DSAMP. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="34c38-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="34c38-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="34c38-505">float</span><span class="sxs-lookup"><span data-stu-id="34c38-505">float</span></span>                        | <span data-ttu-id="34c38-506">Stessi valori di D3DSAMP \_ MIPMAPLODBIAS senza il prefisso \_ D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="34c38-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="34c38-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="34c38-507">SRGBTexture</span></span>         | <span data-ttu-id="34c38-508">bool</span><span class="sxs-lookup"><span data-stu-id="34c38-508">bool</span></span>                         | <span data-ttu-id="34c38-509">Stesso valore di D3DSAMP \_ SRGBTEXTURE senza il prefisso D3DSAMP. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="34c38-510">Esempio:</span><span class="sxs-lookup"><span data-stu-id="34c38-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="34c38-511">Questo fa in modo che i valori UVW siano compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="34c38-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="34c38-512">Stati dello shader</span><span class="sxs-lookup"><span data-stu-id="34c38-512">Shader States</span></span>

<span data-ttu-id="34c38-513">Esistono solo due stati di effetto shader: uno associato a un oggetto vertex shader e l'altro associato a un oggetto pixel shader corrente.</span><span class="sxs-lookup"><span data-stu-id="34c38-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



| <span data-ttu-id="34c38-514">Stato shader</span><span class="sxs-lookup"><span data-stu-id="34c38-514">Shader State</span></span> | <span data-ttu-id="34c38-515">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-515">Type</span></span>         | <span data-ttu-id="34c38-516">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-516">Values</span></span>                                                                      |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="34c38-517">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="34c38-517">PixelShader</span></span>  | <span data-ttu-id="34c38-518">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="34c38-518">pixelshader</span></span>  | <span data-ttu-id="34c38-519">**NULL,** blocco di assembly, destinazione di compilazione o pixel shader parametro.</span><span class="sxs-lookup"><span data-stu-id="34c38-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="34c38-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="34c38-520">VertexShader</span></span> | <span data-ttu-id="34c38-521">vertexshader</span><span class="sxs-lookup"><span data-stu-id="34c38-521">vertexshader</span></span> | <span data-ttu-id="34c38-522">**NULL,** blocco di assembly, destinazione di compilazione o pixel shader parametro.</span><span class="sxs-lookup"><span data-stu-id="34c38-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="34c38-523">Esempio:</span><span class="sxs-lookup"><span data-stu-id="34c38-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="34c38-524">Verrà compilato VSTexture, un vertex shader definito in precedenza nel file con estensione fx, nel vertex shader versione 1.1 e quindi lo shader compilato verrà impostato come vertex shader.</span><span class="sxs-lookup"><span data-stu-id="34c38-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="34c38-525">Il pixel shader viene assegnato a **NULL.**</span><span class="sxs-lookup"><span data-stu-id="34c38-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="34c38-526">Stati costanti shader</span><span class="sxs-lookup"><span data-stu-id="34c38-526">Shader Constant States</span></span>

<span data-ttu-id="34c38-527">Gli stati delle costanti shader vengono usati per accedere ai parametri costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="34c38-527">Shader constant states are used to access shader constant parameters.</span></span>



| <span data-ttu-id="34c38-528">Stato costante shader</span><span class="sxs-lookup"><span data-stu-id="34c38-528">Shader Constant State</span></span> | <span data-ttu-id="34c38-529">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-529">Type</span></span>            | <span data-ttu-id="34c38-530">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-530">Values</span></span>                                       |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="34c38-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="34c38-531">PixelShaderConstant</span></span>   | <span data-ttu-id="34c38-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="34c38-533">m x n matrice di float; m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="34c38-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="34c38-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="34c38-535">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-535">float4</span></span>          | <span data-ttu-id="34c38-536">Un float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-536">One 4D float.</span></span>                                |
| <span data-ttu-id="34c38-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="34c38-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="34c38-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="34c38-538">float4x2</span></span>        | <span data-ttu-id="34c38-539">Due float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="34c38-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="34c38-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="34c38-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="34c38-541">float4x3</span></span>        | <span data-ttu-id="34c38-542">Tre float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="34c38-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="34c38-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="34c38-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="34c38-544">float4x4</span></span>        | <span data-ttu-id="34c38-545">Quattro float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="34c38-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="34c38-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="34c38-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="34c38-548">m x n matrice di tipi di dati; m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="34c38-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="34c38-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="34c38-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="34c38-551">m x n matrice di ints.</span><span class="sxs-lookup"><span data-stu-id="34c38-551">m x n array of ints.</span></span> <span data-ttu-id="34c38-552">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-552">m and n are optional.</span></span>   |
| <span data-ttu-id="34c38-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="34c38-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="34c38-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="34c38-555">m x n matrice di valori float.</span><span class="sxs-lookup"><span data-stu-id="34c38-555">m x n array of floats.</span></span> <span data-ttu-id="34c38-556">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-556">m and n are optional.</span></span> |
| <span data-ttu-id="34c38-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="34c38-557">VertexShaderConstant</span></span>  | <span data-ttu-id="34c38-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="34c38-559">m x n matrice di valori float.</span><span class="sxs-lookup"><span data-stu-id="34c38-559">m x n array of floats.</span></span> <span data-ttu-id="34c38-560">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-560">m and n are optional.</span></span> |
| <span data-ttu-id="34c38-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="34c38-561">VertexShaderConstant1</span></span> | <span data-ttu-id="34c38-562">float4</span><span class="sxs-lookup"><span data-stu-id="34c38-562">float4</span></span>          | <span data-ttu-id="34c38-563">Un float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-563">One 4D float.</span></span>                                |
| <span data-ttu-id="34c38-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="34c38-564">VertexShaderConstant2</span></span> | <span data-ttu-id="34c38-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="34c38-565">float4x2</span></span>        | <span data-ttu-id="34c38-566">Due float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="34c38-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="34c38-567">VertexShaderConstant3</span></span> | <span data-ttu-id="34c38-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="34c38-568">float4x3</span></span>        | <span data-ttu-id="34c38-569">Tre float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="34c38-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="34c38-570">VertexShaderConstant4</span></span> | <span data-ttu-id="34c38-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="34c38-571">float4x4</span></span>        | <span data-ttu-id="34c38-572">Quattro float 4D.</span><span class="sxs-lookup"><span data-stu-id="34c38-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="34c38-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="34c38-573">VertexShaderConstantB</span></span> | <span data-ttu-id="34c38-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="34c38-575">m x n matrice di liste.</span><span class="sxs-lookup"><span data-stu-id="34c38-575">m x n array of bools.</span></span> <span data-ttu-id="34c38-576">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-576">m and n are optional.</span></span>  |
| <span data-ttu-id="34c38-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="34c38-577">VertexShaderConstantI</span></span> | <span data-ttu-id="34c38-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="34c38-579">m x n matrice di valori ints.</span><span class="sxs-lookup"><span data-stu-id="34c38-579">m x n array of ints.</span></span> <span data-ttu-id="34c38-580">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-580">m and n are optional.</span></span>   |
| <span data-ttu-id="34c38-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="34c38-581">VertexShaderConstantF</span></span> | <span data-ttu-id="34c38-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="34c38-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="34c38-583">m x n matrice di valori float.</span><span class="sxs-lookup"><span data-stu-id="34c38-583">m x n array of floats.</span></span> <span data-ttu-id="34c38-584">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="34c38-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="34c38-585">Stati di trama</span><span class="sxs-lookup"><span data-stu-id="34c38-585">Texture States</span></span>

<span data-ttu-id="34c38-586">Gli stati di trama inizializzano le trame usate dal blender multitexture.</span><span class="sxs-lookup"><span data-stu-id="34c38-586">Texture states initialize textures used by the multitexture blender.</span></span>



| <span data-ttu-id="34c38-587">Stato trama</span><span class="sxs-lookup"><span data-stu-id="34c38-587">Texture State</span></span> | <span data-ttu-id="34c38-588">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-588">Type</span></span>    | <span data-ttu-id="34c38-589">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-589">Values</span></span>                            |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="34c38-590">Trama \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-590">Texture\[8\]</span></span>  | <span data-ttu-id="34c38-591">trama</span><span class="sxs-lookup"><span data-stu-id="34c38-591">texture</span></span> | <span data-ttu-id="34c38-592">**NULL** o un parametro di trama.</span><span class="sxs-lookup"><span data-stu-id="34c38-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="34c38-593">Stati della fase di trama</span><span class="sxs-lookup"><span data-stu-id="34c38-593">Texture Stage States</span></span>

<span data-ttu-id="34c38-594">Gli stati della fase trama configurano le trame e le fasi della trama nel blender multitexture.</span><span class="sxs-lookup"><span data-stu-id="34c38-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



| <span data-ttu-id="34c38-595">Stato della fase di trama</span><span class="sxs-lookup"><span data-stu-id="34c38-595">Texture Stage State</span></span>        | <span data-ttu-id="34c38-596">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-596">Type</span></span>  | <span data-ttu-id="34c38-597">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-597">Values</span></span>                                                                                                                                                    |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c38-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="34c38-599">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-599">dword</span></span> | <span data-ttu-id="34c38-600">Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il prefisso D3DTOP. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="34c38-601">Vedere D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="34c38-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="34c38-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="34c38-603">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-603">dword</span></span> | <span data-ttu-id="34c38-604">Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="34c38-605">Vedere D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="34c38-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="34c38-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="34c38-607">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-607">dword</span></span> | <span data-ttu-id="34c38-608">Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="34c38-609">Vedere D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="34c38-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="34c38-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="34c38-611">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-611">dword</span></span> | <span data-ttu-id="34c38-612">Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="34c38-613">Vedere D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="34c38-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="34c38-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="34c38-615">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-615">dword</span></span> | <span data-ttu-id="34c38-616">Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="34c38-617">Vedere D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="34c38-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="34c38-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="34c38-619">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-619">dword</span></span> | <span data-ttu-id="34c38-620">Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="34c38-621">Vedere D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="34c38-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="34c38-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="34c38-623">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-623">dword</span></span> | <span data-ttu-id="34c38-624">Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="34c38-625">Vedere D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="34c38-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="34c38-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="34c38-627">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-627">dword</span></span> | <span data-ttu-id="34c38-628">Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il prefisso D3DTOP. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="34c38-629">Vedere D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="34c38-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="34c38-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="34c38-631">float</span><span class="sxs-lookup"><span data-stu-id="34c38-631">float</span></span> | <span data-ttu-id="34c38-632">Stessi valori di D3DTSS \_ BUMPENVLSCALE senza il prefisso \_ TCI D3DTSS.</span><span class="sxs-lookup"><span data-stu-id="34c38-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="34c38-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="34c38-634">float</span><span class="sxs-lookup"><span data-stu-id="34c38-634">float</span></span> | <span data-ttu-id="34c38-635">Stessi valori di D3DTSS \_ BUMPENVLOFFSET senza il prefisso \_ TCI D3DTSS.</span><span class="sxs-lookup"><span data-stu-id="34c38-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="34c38-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="34c38-637">float</span><span class="sxs-lookup"><span data-stu-id="34c38-637">float</span></span> | <span data-ttu-id="34c38-638">Stessi valori di D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="34c38-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="34c38-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="34c38-640">float</span><span class="sxs-lookup"><span data-stu-id="34c38-640">float</span></span> | <span data-ttu-id="34c38-641">Stessi valori di D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="34c38-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="34c38-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="34c38-643">float</span><span class="sxs-lookup"><span data-stu-id="34c38-643">float</span></span> | <span data-ttu-id="34c38-644">Stessi valori di D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="34c38-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="34c38-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="34c38-646">float</span><span class="sxs-lookup"><span data-stu-id="34c38-646">float</span></span> | <span data-ttu-id="34c38-647">Stessi valori di D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="34c38-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="34c38-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="34c38-649">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-649">dword</span></span> | <span data-ttu-id="34c38-650">Uguale a [D3DTA](d3dta.md) senza il prefisso D3DTA. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="34c38-651">Vedere D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="34c38-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="34c38-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="34c38-653">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-653">dword</span></span> | <span data-ttu-id="34c38-654">Stessi valori di D3DTSS \_ TEXCOORDINDEX senza il prefisso \_ TCI D3DTSS.</span><span class="sxs-lookup"><span data-stu-id="34c38-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="34c38-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="34c38-656">dword</span><span class="sxs-lookup"><span data-stu-id="34c38-656">dword</span></span> | <span data-ttu-id="34c38-657">Stessi valori dei [**valori D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) senza il prefisso D3DTTFF. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="34c38-658">Vedere \_ TEXTURETRANSFORMFLAGS D3DTSS.</span><span class="sxs-lookup"><span data-stu-id="34c38-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="34c38-659">Stati di trasformazione</span><span class="sxs-lookup"><span data-stu-id="34c38-659">Transform States</span></span>

<span data-ttu-id="34c38-660">Impostare gli stati di trasformazione per inizializzare le matrici di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="34c38-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="34c38-661">Gli effetti usano matrici trasposte per migliorare l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="34c38-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="34c38-662">È possibile fornire matrici trasposte a un effetto oppure un effetto trassporrà automaticamente le matrici prima di usarle.</span><span class="sxs-lookup"><span data-stu-id="34c38-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



| <span data-ttu-id="34c38-663">Stato trasformazione</span><span class="sxs-lookup"><span data-stu-id="34c38-663">Transform State</span></span>       | <span data-ttu-id="34c38-664">Tipo</span><span class="sxs-lookup"><span data-stu-id="34c38-664">Type</span></span>     | <span data-ttu-id="34c38-665">Valori</span><span class="sxs-lookup"><span data-stu-id="34c38-665">Values</span></span>                                                                                                                          |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34c38-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="34c38-666">ProjectionTransform</span></span>   | <span data-ttu-id="34c38-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="34c38-667">float4x4</span></span> | <span data-ttu-id="34c38-668">Matrice 4x4 di valori float.</span><span class="sxs-lookup"><span data-stu-id="34c38-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="34c38-669">Stessi valori di D3DTS \_ PROJECTION senza il prefisso D3DTS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="34c38-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="34c38-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="34c38-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="34c38-671">float4x4</span></span> | <span data-ttu-id="34c38-672">Matrice 4x4 di valori float.</span><span class="sxs-lookup"><span data-stu-id="34c38-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="34c38-673">Stessi valori di [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) senza il prefisso D3DTS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="34c38-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="34c38-674">ViewTransform</span></span>         | <span data-ttu-id="34c38-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="34c38-675">float4x4</span></span> | <span data-ttu-id="34c38-676">Matrice 4x4 di valori float.</span><span class="sxs-lookup"><span data-stu-id="34c38-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="34c38-677">Stessi valori di D3DTS \_ VIEW senza il prefisso D3DTS. \_</span><span class="sxs-lookup"><span data-stu-id="34c38-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="34c38-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="34c38-678">WorldTransform</span></span>        | <span data-ttu-id="34c38-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="34c38-679">float4x4</span></span> | <span data-ttu-id="34c38-680">Matrice 4x4 di valori float.</span><span class="sxs-lookup"><span data-stu-id="34c38-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="34c38-681">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34c38-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34c38-682">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="34c38-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
