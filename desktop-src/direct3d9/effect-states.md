---
description: Gli Stati degli effetti vengono utilizzati per inizializzare gli Stati della pipeline in preparazione all'elaborazione dei vertici e dei pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Stati degli effetti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674e72d818cd280bfe75a2cb02733576bc68319e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048996"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="74d11-103">Stati degli effetti (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="74d11-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="74d11-104">Gli Stati degli effetti vengono utilizzati per inizializzare gli Stati della pipeline in preparazione all'elaborazione dei vertici e dei pixel.</span><span class="sxs-lookup"><span data-stu-id="74d11-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="74d11-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="74d11-105">Where:</span></span>

-   <span data-ttu-id="74d11-106">stato dell'effetto, simile agli Stati tradizionali della pipeline della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="74d11-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="74d11-107">Di seguito è riportato un elenco completo di Stati.</span><span class="sxs-lookup"><span data-stu-id="74d11-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="74d11-108">\[\[ \] indice \] di -Indice integer facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74d11-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="74d11-109">L'indice identifica un determinato stato all'interno di una matrice di Stati di effetto.</span><span class="sxs-lookup"><span data-stu-id="74d11-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="74d11-110">Le parentesi esterne indicano che un indice è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74d11-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="74d11-111">Se viene utilizzato un indice, assicurarsi di utilizzare le parentesi interne.</span><span class="sxs-lookup"><span data-stu-id="74d11-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="74d11-112">espressione di assegnazione dello stato di espressione.</span><span class="sxs-lookup"><span data-stu-id="74d11-112">expression - State assignment expression.</span></span> <span data-ttu-id="74d11-113">Vedere [espressioni (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="74d11-114">Ogni stato ha un tipo di dati nativo.</span><span class="sxs-lookup"><span data-stu-id="74d11-114">Each state has a native data type.</span></span> <span data-ttu-id="74d11-115">Si tratta del tipo di dati in cui lo stato prevede che i valori siano presenti quando vengono assegnati dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="74d11-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="74d11-116">Di seguito sono elencati i tipi di dati previsti da ogni stato.</span><span class="sxs-lookup"><span data-stu-id="74d11-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="74d11-117">Si noti che l'interfaccia Effect tenterà di eseguire il cast dei valori nel tipo appropriato il prima possibile.</span><span class="sxs-lookup"><span data-stu-id="74d11-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="74d11-118">È possibile eseguire il cast dei valori letterali in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="74d11-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="74d11-119">Quando vengono chiamati i metodi set appropriati, è necessario eseguire il cast delle variabili non letterali, ad esempio le variabili regolari.</span><span class="sxs-lookup"><span data-stu-id="74d11-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="74d11-120">Ad esempio, l'interfaccia Effect eseguirà il cast dei valori impostati utilizzando SetValue, [**SetValue**](id3dxbaseeffect--setvalue.md)e altre funzioni [**simili, se**](id3dxbaseeffect--setbool.md)necessario.</span><span class="sxs-lookup"><span data-stu-id="74d11-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="74d11-121">Per prestazioni ottimali, assicurarsi che i valori passati all'interfaccia effetto siano già del tipo corretto e che non sia necessario eseguire il cast.</span><span class="sxs-lookup"><span data-stu-id="74d11-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="74d11-122">Se il runtime non è in grado di eseguire il cast di un valore, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="74d11-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="74d11-123">Gli Stati degli effetti possono essere suddivisi nelle categorie seguenti:</span><span class="sxs-lookup"><span data-stu-id="74d11-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="74d11-124">Stati leggeri</span><span class="sxs-lookup"><span data-stu-id="74d11-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="74d11-125">Stati del materiale</span><span class="sxs-lookup"><span data-stu-id="74d11-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="74d11-126">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="74d11-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="74d11-127">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="74d11-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="74d11-128">Stati di rendering della pipe del vertice</span><span class="sxs-lookup"><span data-stu-id="74d11-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="74d11-129">Stati campionatore</span><span class="sxs-lookup"><span data-stu-id="74d11-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="74d11-130">Stati fase campionatore</span><span class="sxs-lookup"><span data-stu-id="74d11-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="74d11-131">Stati shader</span><span class="sxs-lookup"><span data-stu-id="74d11-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="74d11-132">Stati costanti shader</span><span class="sxs-lookup"><span data-stu-id="74d11-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="74d11-133">Stati di trama</span><span class="sxs-lookup"><span data-stu-id="74d11-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="74d11-134">Stati della fase trama</span><span class="sxs-lookup"><span data-stu-id="74d11-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="74d11-135">Stati di trasformazione</span><span class="sxs-lookup"><span data-stu-id="74d11-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="74d11-136">Stati leggeri</span><span class="sxs-lookup"><span data-stu-id="74d11-136">Light States</span></span>

<span data-ttu-id="74d11-137">Per garantire prestazioni ottimali per l'applicazione di un effetto, è necessario specificare nel file degli effetti tutti i componenti di una luce o di un materiale.</span><span class="sxs-lookup"><span data-stu-id="74d11-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="74d11-138">Gli Stati che non vengono dichiarati sono impostati su un valore predefinito perché non è possibile impostare gli Stati di luce singolarmente da Direct3D.</span><span class="sxs-lookup"><span data-stu-id="74d11-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d11-139">Stato chiaro</span><span class="sxs-lookup"><span data-stu-id="74d11-139">Light State</span></span>            | <span data-ttu-id="74d11-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-140">Type</span></span>   | <span data-ttu-id="74d11-141">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="74d11-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="74d11-143">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-143">float4</span></span> | <span data-ttu-id="74d11-144">Vedere il membro di ambiente di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="74d11-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="74d11-146">float</span><span class="sxs-lookup"><span data-stu-id="74d11-146">float</span></span>  | <span data-ttu-id="74d11-147">Vedere il membro Attenuation0 di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="74d11-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="74d11-149">float</span><span class="sxs-lookup"><span data-stu-id="74d11-149">float</span></span>  | <span data-ttu-id="74d11-150">Vedere il membro Attenuation1 di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="74d11-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="74d11-152">float</span><span class="sxs-lookup"><span data-stu-id="74d11-152">float</span></span>  | <span data-ttu-id="74d11-153">Vedere il membro Attenuation2 di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="74d11-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="74d11-155">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-155">float4</span></span> | <span data-ttu-id="74d11-156">Vedere il membro Diffusion di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="74d11-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="74d11-158">float3</span><span class="sxs-lookup"><span data-stu-id="74d11-158">float3</span></span> | <span data-ttu-id="74d11-159">Vedere il membro direction di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="74d11-160">N Alleggeribile \[\]</span><span class="sxs-lookup"><span data-stu-id="74d11-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="74d11-161">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-161">bool</span></span>   | <span data-ttu-id="74d11-162">**True** o **false**.</span><span class="sxs-lookup"><span data-stu-id="74d11-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="74d11-163">Vedere l'argomento bEnable in [**schiarente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="74d11-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="74d11-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="74d11-165">float</span><span class="sxs-lookup"><span data-stu-id="74d11-165">float</span></span>  | <span data-ttu-id="74d11-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="74d11-167">Vedere il membro di interruzione di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="74d11-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="74d11-169">float</span><span class="sxs-lookup"><span data-stu-id="74d11-169">float</span></span>  | <span data-ttu-id="74d11-170">Vedere il membro Phi di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="74d11-171">Posizioneilluminazione \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="74d11-172">float3</span><span class="sxs-lookup"><span data-stu-id="74d11-172">float3</span></span> | <span data-ttu-id="74d11-173">Vedere il membro Position di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="74d11-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-174">LightRange\[n\]</span></span>        | <span data-ttu-id="74d11-175">float</span><span class="sxs-lookup"><span data-stu-id="74d11-175">float</span></span>  | <span data-ttu-id="74d11-176">Vedere il membro di intervallo di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="74d11-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="74d11-178">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-178">float4</span></span> | <span data-ttu-id="74d11-179">Vedere il membro speculare di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="74d11-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="74d11-181">float</span><span class="sxs-lookup"><span data-stu-id="74d11-181">float</span></span>  | <span data-ttu-id="74d11-182">Vedere il membro theta di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="74d11-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="74d11-183">LightType\[n\]</span></span>         | <span data-ttu-id="74d11-184">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-184">dword</span></span>  | <span data-ttu-id="74d11-185">Stesso valore della matrice di un massimo di n valori [**D3DLIGHTTYPE**](./d3dlighttype.md) senza il \_ prefisso D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="74d11-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="74d11-186">Esempio:</span><span class="sxs-lookup"><span data-stu-id="74d11-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="74d11-187">Questa operazione consentirà di accendere il tipo, impostare la posizione della luce su float3<10.0 f, 1.0 f, 23.0 f> e impostare il colore di ambiente su float4<0.7 f, 0,0 f, 0,0 f, 1.0 f>.</span><span class="sxs-lookup"><span data-stu-id="74d11-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="74d11-188">Stati del materiale</span><span class="sxs-lookup"><span data-stu-id="74d11-188">Material States</span></span>

<span data-ttu-id="74d11-189">Gli Stati che non vengono dichiarati sono impostati su un valore predefinito perché non è possibile impostare gli Stati del materiale singolarmente tramite Direct3D.</span><span class="sxs-lookup"><span data-stu-id="74d11-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="74d11-190">Stato del materiale</span><span class="sxs-lookup"><span data-stu-id="74d11-190">Material State</span></span>   | <span data-ttu-id="74d11-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-191">Type</span></span>   | <span data-ttu-id="74d11-192">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-192">Values</span></span>                                         |
| <span data-ttu-id="74d11-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="74d11-193">MaterialAmbient</span></span>  | <span data-ttu-id="74d11-194">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-194">float4</span></span> | <span data-ttu-id="74d11-195">Stesso valore di [ **ambiente**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="74d11-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="74d11-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="74d11-196">MaterialDiffuse</span></span>  | <span data-ttu-id="74d11-197">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-197">float4</span></span> | <span data-ttu-id="74d11-198">Stesso valore di [ **Diffusion**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="74d11-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="74d11-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="74d11-199">MaterialEmissive</span></span> | <span data-ttu-id="74d11-200">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-200">float4</span></span> | <span data-ttu-id="74d11-201">Stesso valore di [ **emissivo**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="74d11-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="74d11-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="74d11-202">MaterialPower</span></span>    | <span data-ttu-id="74d11-203">float</span><span class="sxs-lookup"><span data-stu-id="74d11-203">float</span></span>  | <span data-ttu-id="74d11-204">Stesso valore di [ **Power**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="74d11-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="74d11-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="74d11-205">MaterialSpecular</span></span> | <span data-ttu-id="74d11-206">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-206">float4</span></span> | <span data-ttu-id="74d11-207">Stesso valore di [ **speculare**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="74d11-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="74d11-208">Esempio:</span><span class="sxs-lookup"><span data-stu-id="74d11-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="74d11-209">Il colore di diffusione verrà impostato su float4<0.7 f, 0,0 f, 0,0 f, 1.0 f> e apporterà la potenza del materiale 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="74d11-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="74d11-210">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="74d11-210">Render States</span></span>

<span data-ttu-id="74d11-211">Esistono due tipi di Stati di rendering:</span><span class="sxs-lookup"><span data-stu-id="74d11-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="74d11-212">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="74d11-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="74d11-213">Stati di rendering della pipe del vertice</span><span class="sxs-lookup"><span data-stu-id="74d11-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="74d11-214">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="74d11-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="74d11-215">Gli Stati di rendering dei file degli effetti hanno nomi simili agli Stati della pipeline della funzione fissa, spesso con il prefisso rimosso.</span><span class="sxs-lookup"><span data-stu-id="74d11-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74d11-216">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="74d11-216">Render State</span></span></td>
<td><span data-ttu-id="74d11-217">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-217">Type</span></span></td>
<td><span data-ttu-id="74d11-218">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="74d11-220">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-220">bool</span></span></td>
<td><span data-ttu-id="74d11-221">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-221">True or False.</span></span> <span data-ttu-id="74d11-222">Gli stessi valori di D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="74d11-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="74d11-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="74d11-224">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-224">dword</span></span></td>
<td><span data-ttu-id="74d11-225">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="74d11-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="74d11-226">Vedere D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="74d11-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="74d11-227">AlphaRef</span></span></td>
<td><span data-ttu-id="74d11-228">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-228">dword</span></span></td>
<td><span data-ttu-id="74d11-229">Stessi valori di D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="74d11-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="74d11-231">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-231">dword</span></span></td>
<td><span data-ttu-id="74d11-232">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-232">True or False.</span></span> <span data-ttu-id="74d11-233">Vedere D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="74d11-234">BlendOp</span></span></td>
<td><span data-ttu-id="74d11-235">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-235">dword</span></span></td>
<td><span data-ttu-id="74d11-236">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> senza il prefisso D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="74d11-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="74d11-238">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-238">dword</span></span></td>
<td><span data-ttu-id="74d11-239">Combinazione bit per bit di rosso | VERDE | BLU | Alfa.</span><span class="sxs-lookup"><span data-stu-id="74d11-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="74d11-240">Vedere D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="74d11-241">DepthBias</span></span></td>
<td><span data-ttu-id="74d11-242">float</span><span class="sxs-lookup"><span data-stu-id="74d11-242">float</span></span></td>
<td><span data-ttu-id="74d11-243">Stessi valori di D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="74d11-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="74d11-244">DestBlend</span></span></td>
<td><span data-ttu-id="74d11-245">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-245">dword</span></span></td>
<td><span data-ttu-id="74d11-246">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="74d11-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-247">DitherEnable</span></span></td>
<td><span data-ttu-id="74d11-248">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-248">bool</span></span></td>
<td><span data-ttu-id="74d11-249">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-249">True or False.</span></span> <span data-ttu-id="74d11-250">Stessi valori di D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="74d11-251">FillMode</span></span></td>
<td><span data-ttu-id="74d11-252">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-252">dword</span></span></td>
<td><span data-ttu-id="74d11-253">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> senza il prefisso D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="74d11-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="74d11-254">LastPixel</span></span></td>
<td><span data-ttu-id="74d11-255">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-255">dword</span></span></td>
<td><span data-ttu-id="74d11-256">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-256">True or False.</span></span> <span data-ttu-id="74d11-257">Vedere D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="74d11-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-258">MODOOMBRA</span><span class="sxs-lookup"><span data-stu-id="74d11-258">ShadeMode</span></span></td>
<td><span data-ttu-id="74d11-259">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-259">dword</span></span></td>
<td><span data-ttu-id="74d11-260">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> senza il prefisso D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="74d11-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="74d11-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="74d11-262">float</span><span class="sxs-lookup"><span data-stu-id="74d11-262">float</span></span></td>
<td><span data-ttu-id="74d11-263">Stessi valori di D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="74d11-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="74d11-264">SrcBlend</span></span></td>
<td><span data-ttu-id="74d11-265">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-265">dword</span></span></td>
<td><span data-ttu-id="74d11-266">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="74d11-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-267">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-267">StencilEnable</span></span></td>
<td><span data-ttu-id="74d11-268">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-268">bool</span></span></td>
<td><span data-ttu-id="74d11-269">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-269">True or False.</span></span> <span data-ttu-id="74d11-270">Stessi valori di D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-270">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-271">StencilFail</span><span class="sxs-lookup"><span data-stu-id="74d11-271">StencilFail</span></span></td>
<td><span data-ttu-id="74d11-272">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-272">dword</span></span></td>
<td><span data-ttu-id="74d11-273">Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="74d11-273">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="74d11-274">Vedere D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="74d11-274">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-275">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="74d11-275">StencilFunc</span></span></td>
<td><span data-ttu-id="74d11-276">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-276">dword</span></span></td>
<td><span data-ttu-id="74d11-277">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="74d11-277">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="74d11-278">Vedere D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="74d11-278">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-279">StencilMask</span><span class="sxs-lookup"><span data-stu-id="74d11-279">StencilMask</span></span></td>
<td><span data-ttu-id="74d11-280">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-280">dword</span></span></td>
<td><span data-ttu-id="74d11-281">Stessi valori di D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="74d11-281">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-282">StencilPass</span><span class="sxs-lookup"><span data-stu-id="74d11-282">StencilPass</span></span></td>
<td><span data-ttu-id="74d11-283">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-283">dword</span></span></td>
<td><span data-ttu-id="74d11-284">Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="74d11-284">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="74d11-285">Vedere D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="74d11-285">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-286">StencilRef</span><span class="sxs-lookup"><span data-stu-id="74d11-286">StencilRef</span></span></td>
<td><span data-ttu-id="74d11-287">INT</span><span class="sxs-lookup"><span data-stu-id="74d11-287">int</span></span></td>
<td><span data-ttu-id="74d11-288">Stessi valori di D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="74d11-288">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-289">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="74d11-289">StencilWriteMask</span></span></td>
<td><span data-ttu-id="74d11-290">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-290">dword</span></span></td>
<td><span data-ttu-id="74d11-291">Stessi valori di D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="74d11-291">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-292">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="74d11-292">StencilZFail</span></span></td>
<td><span data-ttu-id="74d11-293">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-293">dword</span></span></td>
<td><span data-ttu-id="74d11-294">Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="74d11-294">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="74d11-295">Vedere D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="74d11-295">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-296">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="74d11-296">TextureFactor</span></span></td>
<td><span data-ttu-id="74d11-297">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-297">dword</span></span></td>
<td><span data-ttu-id="74d11-298">Stessi valori di <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="74d11-298">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="74d11-299">Stessi valori di D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="74d11-299">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-300">Wrap0-Wrap15</span><span class="sxs-lookup"><span data-stu-id="74d11-300">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="74d11-301">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-301">dword</span></span></td>
<td><span data-ttu-id="74d11-302">I valori corrispondono ai valori utilizzati da D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="74d11-302">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="74d11-303">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="74d11-303">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="74d11-304">COORD0 (che corrisponde a D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="74d11-304">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="74d11-305">COORD1 (che corrisponde a D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="74d11-305">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="74d11-306">COORD2 (che corrisponde a D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="74d11-306">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="74d11-307">COORD3 (che corrisponde a D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="74d11-307">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="74d11-308">U (che corrisponde a D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="74d11-308">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="74d11-309">V (che corrisponde a D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="74d11-309">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="74d11-310">W (che corrisponde a D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="74d11-310">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-311">ZEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-311">ZEnable</span></span></td>
<td><span data-ttu-id="74d11-312">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-312">dword</span></span></td>
<td><span data-ttu-id="74d11-313">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> senza il prefisso D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="74d11-313">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74d11-314">ZFunc</span><span class="sxs-lookup"><span data-stu-id="74d11-314">ZFunc</span></span></td>
<td><span data-ttu-id="74d11-315">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-315">dword</span></span></td>
<td><span data-ttu-id="74d11-316">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="74d11-316">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="74d11-317">Vedere D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="74d11-317">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74d11-318">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-318">ZWriteEnable</span></span></td>
<td><span data-ttu-id="74d11-319">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-319">bool</span></span></td>
<td><span data-ttu-id="74d11-320">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-320">True or False.</span></span> <span data-ttu-id="74d11-321">Vedere D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-321">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="74d11-322">Esempio:</span><span class="sxs-lookup"><span data-stu-id="74d11-322">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="74d11-323">In questo modo verrà abilitata la fusione alfa e verrà eseguito il rendering di tutte le geometrie in wireframe.</span><span class="sxs-lookup"><span data-stu-id="74d11-323">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="74d11-324">Stati di rendering della pipe del vertice</span><span class="sxs-lookup"><span data-stu-id="74d11-324">Vertex Pipe Render States</span></span>

<span data-ttu-id="74d11-325">Gli Stati di rendering dei file degli effetti hanno nomi simili agli Stati della pipeline della funzione fissa, spesso con il prefisso rimosso.</span><span class="sxs-lookup"><span data-stu-id="74d11-325">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d11-326">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="74d11-326">Render State</span></span>             | <span data-ttu-id="74d11-327">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-327">Type</span></span>   | <span data-ttu-id="74d11-328">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-328">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="74d11-329">Di ambiente</span><span class="sxs-lookup"><span data-stu-id="74d11-329">Ambient</span></span>                  | <span data-ttu-id="74d11-330">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-330">float4</span></span> | <span data-ttu-id="74d11-331">Stessi valori dell' \_ ambiente D3DRS.</span><span class="sxs-lookup"><span data-stu-id="74d11-331">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="74d11-332">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="74d11-332">AmbientMaterialSource</span></span>    | <span data-ttu-id="74d11-333">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-333">dword</span></span>  | <span data-ttu-id="74d11-334">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="74d11-334">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="74d11-335">Vedere D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="74d11-335">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="74d11-336">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="74d11-336">Clipping</span></span>                 | <span data-ttu-id="74d11-337">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-337">bool</span></span>   | <span data-ttu-id="74d11-338">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-338">True or False.</span></span> <span data-ttu-id="74d11-339">Stessi valori del \_ ritaglio D3DRS.</span><span class="sxs-lookup"><span data-stu-id="74d11-339">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="74d11-340">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-340">ClipPlaneEnable</span></span>          | <span data-ttu-id="74d11-341">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-341">dword</span></span>  | <span data-ttu-id="74d11-342">Combinazione bit per bit di macro D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="74d11-342">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="74d11-343">Vedere [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-343">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="74d11-344">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="74d11-344">ColorVertex</span></span>              | <span data-ttu-id="74d11-345">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-345">bool</span></span>   | <span data-ttu-id="74d11-346">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-346">True or False.</span></span> <span data-ttu-id="74d11-347">Stessi valori di D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="74d11-347">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="74d11-348">CullMode</span><span class="sxs-lookup"><span data-stu-id="74d11-348">CullMode</span></span>                 | <span data-ttu-id="74d11-349">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-349">dword</span></span>  | <span data-ttu-id="74d11-350">Gli stessi valori di [**D3DCULL**](./d3dcull.md) senza il \_ prefisso D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="74d11-350">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="74d11-351">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="74d11-351">DiffuseMaterialSource</span></span>    | <span data-ttu-id="74d11-352">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-352">dword</span></span>  | <span data-ttu-id="74d11-353">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="74d11-353">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="74d11-354">Vedere D3DRS \_ DIFFUSEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="74d11-354">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="74d11-355">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="74d11-355">EmissiveMaterialSource</span></span>   | <span data-ttu-id="74d11-356">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-356">dword</span></span>  | <span data-ttu-id="74d11-357">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="74d11-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="74d11-358">Vedere D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="74d11-358">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="74d11-359">FogColor</span><span class="sxs-lookup"><span data-stu-id="74d11-359">FogColor</span></span>                 | <span data-ttu-id="74d11-360">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-360">dword</span></span>  | <span data-ttu-id="74d11-361">Stessi valori di [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-361">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="74d11-362">Vedere D3DRS \_ FogColor.</span><span class="sxs-lookup"><span data-stu-id="74d11-362">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="74d11-363">FogDensity</span><span class="sxs-lookup"><span data-stu-id="74d11-363">FogDensity</span></span>               | <span data-ttu-id="74d11-364">float</span><span class="sxs-lookup"><span data-stu-id="74d11-364">float</span></span>  | <span data-ttu-id="74d11-365">Stessi valori di D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="74d11-365">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="74d11-366">FogEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-366">FogEnable</span></span>                | <span data-ttu-id="74d11-367">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-367">bool</span></span>   | <span data-ttu-id="74d11-368">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-368">True or False.</span></span> <span data-ttu-id="74d11-369">Stessi valori di D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-369">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="74d11-370">FogEnd</span><span class="sxs-lookup"><span data-stu-id="74d11-370">FogEnd</span></span>                   | <span data-ttu-id="74d11-371">float</span><span class="sxs-lookup"><span data-stu-id="74d11-371">float</span></span>  | <span data-ttu-id="74d11-372">Stessi valori di D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="74d11-372">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="74d11-373">FogStart</span><span class="sxs-lookup"><span data-stu-id="74d11-373">FogStart</span></span>                 | <span data-ttu-id="74d11-374">float</span><span class="sxs-lookup"><span data-stu-id="74d11-374">float</span></span>  | <span data-ttu-id="74d11-375">Stessi valori di D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="74d11-375">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="74d11-376">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="74d11-376">FogTableMode</span></span>             | <span data-ttu-id="74d11-377">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-377">dword</span></span>  | <span data-ttu-id="74d11-378">Stessi valori di [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-378">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="74d11-379">Vedere D3DRS \_ FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="74d11-379">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="74d11-380">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="74d11-380">FogVertexMode</span></span>            | <span data-ttu-id="74d11-381">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-381">dword</span></span>  | <span data-ttu-id="74d11-382">Gli stessi valori di [**D3DFOGMODE**](./d3dfogmode.md) senza il \_ prefisso D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="74d11-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="74d11-383">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-383">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="74d11-384">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-384">bool</span></span>   | <span data-ttu-id="74d11-385">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-385">True or False.</span></span> <span data-ttu-id="74d11-386">Stessi valori di D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-386">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="74d11-387">Luce</span><span class="sxs-lookup"><span data-stu-id="74d11-387">Lighting</span></span>                 | <span data-ttu-id="74d11-388">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-388">bool</span></span>   | <span data-ttu-id="74d11-389">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-389">True or False.</span></span> <span data-ttu-id="74d11-390">Stessi valori dell' \_ illuminazione D3DRS.</span><span class="sxs-lookup"><span data-stu-id="74d11-390">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="74d11-391">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="74d11-391">LocalViewer</span></span>              | <span data-ttu-id="74d11-392">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-392">bool</span></span>   | <span data-ttu-id="74d11-393">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-393">True or False.</span></span> <span data-ttu-id="74d11-394">Stessi valori di D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="74d11-394">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="74d11-395">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="74d11-395">MultiSampleAntialias</span></span>     | <span data-ttu-id="74d11-396">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-396">bool</span></span>   | <span data-ttu-id="74d11-397">Stessi valori di D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="74d11-397">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="74d11-398">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="74d11-398">MultiSampleMask</span></span>          | <span data-ttu-id="74d11-399">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-399">dword</span></span>  | <span data-ttu-id="74d11-400">Stessi valori di D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="74d11-400">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="74d11-401">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="74d11-401">NormalizeNormals</span></span>         | <span data-ttu-id="74d11-402">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-402">bool</span></span>   | <span data-ttu-id="74d11-403">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-403">True or False.</span></span> <span data-ttu-id="74d11-404">Stessi valori di D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="74d11-404">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="74d11-405">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="74d11-405">PatchSegments</span></span>            | <span data-ttu-id="74d11-406">float</span><span class="sxs-lookup"><span data-stu-id="74d11-406">float</span></span>  | <span data-ttu-id="74d11-407">Stessi valori di nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="74d11-407">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="74d11-408">PointScale \_</span><span class="sxs-lookup"><span data-stu-id="74d11-408">PointScale\_A</span></span>            | <span data-ttu-id="74d11-409">float</span><span class="sxs-lookup"><span data-stu-id="74d11-409">float</span></span>  | <span data-ttu-id="74d11-410">Gli stessi valori di D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="74d11-410">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="74d11-411">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="74d11-411">PointScale\_B</span></span>            | <span data-ttu-id="74d11-412">float</span><span class="sxs-lookup"><span data-stu-id="74d11-412">float</span></span>  | <span data-ttu-id="74d11-413">Stessi valori di D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="74d11-413">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="74d11-414">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="74d11-414">PointScale\_C</span></span>            | <span data-ttu-id="74d11-415">float</span><span class="sxs-lookup"><span data-stu-id="74d11-415">float</span></span>  | <span data-ttu-id="74d11-416">Stessi valori di D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="74d11-416">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="74d11-417">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-417">PointScaleEnable</span></span>         | <span data-ttu-id="74d11-418">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-418">bool</span></span>   | <span data-ttu-id="74d11-419">Stessi valori di D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-419">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="74d11-420">PointSize</span><span class="sxs-lookup"><span data-stu-id="74d11-420">PointSize</span></span>                | <span data-ttu-id="74d11-421">float</span><span class="sxs-lookup"><span data-stu-id="74d11-421">float</span></span>  | <span data-ttu-id="74d11-422">Stessi valori di D3DRS \_ POINTSIZE.</span><span class="sxs-lookup"><span data-stu-id="74d11-422">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="74d11-423">PointSize \_ min</span><span class="sxs-lookup"><span data-stu-id="74d11-423">PointSize\_Min</span></span>           | <span data-ttu-id="74d11-424">float</span><span class="sxs-lookup"><span data-stu-id="74d11-424">float</span></span>  | <span data-ttu-id="74d11-425">Gli stessi valori di D3DRS \_ POINTSIZE \_ min.</span><span class="sxs-lookup"><span data-stu-id="74d11-425">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="74d11-426">PointSize \_ Max</span><span class="sxs-lookup"><span data-stu-id="74d11-426">PointSize\_Max</span></span>           | <span data-ttu-id="74d11-427">float</span><span class="sxs-lookup"><span data-stu-id="74d11-427">float</span></span>  | <span data-ttu-id="74d11-428">Gli stessi valori di D3DRS \_ POINTSIZE \_ Max senza il \_ prefisso D3DRS.</span><span class="sxs-lookup"><span data-stu-id="74d11-428">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="74d11-429">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-429">PointSpriteEnable</span></span>        | <span data-ttu-id="74d11-430">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-430">bool</span></span>   | <span data-ttu-id="74d11-431">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-431">True or False.</span></span> <span data-ttu-id="74d11-432">Stessi valori di D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-432">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="74d11-433">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-433">RangeFogEnable</span></span>           | <span data-ttu-id="74d11-434">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-434">bool</span></span>   | <span data-ttu-id="74d11-435">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-435">True or False.</span></span> <span data-ttu-id="74d11-436">Stessi valori di D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-436">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="74d11-437">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="74d11-437">SpecularEnable</span></span>           | <span data-ttu-id="74d11-438">bool</span><span class="sxs-lookup"><span data-stu-id="74d11-438">bool</span></span>   | <span data-ttu-id="74d11-439">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="74d11-439">True or False.</span></span> <span data-ttu-id="74d11-440">Stessi valori di D3DRS \_ SPECULARENABLE.</span><span class="sxs-lookup"><span data-stu-id="74d11-440">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="74d11-441">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="74d11-441">SpecularMaterialSource</span></span>   | <span data-ttu-id="74d11-442">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-442">dword</span></span>  | <span data-ttu-id="74d11-443">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="74d11-443">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="74d11-444">Vedere D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="74d11-444">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="74d11-445">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="74d11-445">TweenFactor</span></span>              | <span data-ttu-id="74d11-446">float</span><span class="sxs-lookup"><span data-stu-id="74d11-446">float</span></span>  | <span data-ttu-id="74d11-447">Stessi valori di D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="74d11-447">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="74d11-448">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="74d11-448">VertexBlend</span></span>              | <span data-ttu-id="74d11-449">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-449">dword</span></span>  | <span data-ttu-id="74d11-450">Gli stessi valori di [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) senza il \_ prefisso D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="74d11-450">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="74d11-451">Vedere D3DRS \_ VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="74d11-451">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="74d11-452">Esempio:</span><span class="sxs-lookup"><span data-stu-id="74d11-452">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="74d11-453">In questo modo, il colore di ambiente float4<0.7 f, 0,0 f, 0,0 f, 1.0 f>, impostare la modalità di abbattimento della superficie in senso antiorario e impostare il colore di nebbia su rosso.</span><span class="sxs-lookup"><span data-stu-id="74d11-453">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="74d11-454">Stati campionatore</span><span class="sxs-lookup"><span data-stu-id="74d11-454">Sampler States</span></span>

<span data-ttu-id="74d11-455">Uno stato del campionatore rappresenta un oggetto campionatore.</span><span class="sxs-lookup"><span data-stu-id="74d11-455">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="74d11-456">State</span><span class="sxs-lookup"><span data-stu-id="74d11-456">State</span></span>   | <span data-ttu-id="74d11-457">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-457">Type</span></span>    | <span data-ttu-id="74d11-458">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-458">Values</span></span>                              |
| <span data-ttu-id="74d11-459">Campionatore</span><span class="sxs-lookup"><span data-stu-id="74d11-459">Sampler</span></span> | <span data-ttu-id="74d11-460">campionatore</span><span class="sxs-lookup"><span data-stu-id="74d11-460">sampler</span></span> | <span data-ttu-id="74d11-461">**Null** o un blocco di stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="74d11-461">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="74d11-462">Stati fase campionatore</span><span class="sxs-lookup"><span data-stu-id="74d11-462">Sampler Stage States</span></span>

<span data-ttu-id="74d11-463">Gli Stati della fase del campionatore vengono usati per campionare le trame.</span><span class="sxs-lookup"><span data-stu-id="74d11-463">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="74d11-464">Stato campionatore determina i tipi di filtro e le modalità di indirizzamento della trama.</span><span class="sxs-lookup"><span data-stu-id="74d11-464">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d11-465">Stato campionatore</span><span class="sxs-lookup"><span data-stu-id="74d11-465">Sampler State</span></span>       | <span data-ttu-id="74d11-466">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-466">Type</span></span>                         | <span data-ttu-id="74d11-467">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-467">Values</span></span>                                                                                                                            |
| <span data-ttu-id="74d11-468">Indirizzo \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-468">AddressU\[16\]</span></span>      | <span data-ttu-id="74d11-469">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-469">dword</span></span>                        | <span data-ttu-id="74d11-470">Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="74d11-470">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="74d11-471">Vedere D3DSAMP \_ .</span><span class="sxs-lookup"><span data-stu-id="74d11-471">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="74d11-472">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-472">AddressV\[16\]</span></span>      | <span data-ttu-id="74d11-473">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-473">dword</span></span>                        | <span data-ttu-id="74d11-474">Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="74d11-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="74d11-475">Vedere D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="74d11-475">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="74d11-476">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-476">AddressW\[16\]</span></span>      | <span data-ttu-id="74d11-477">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-477">dword</span></span>                        | <span data-ttu-id="74d11-478">Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="74d11-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="74d11-479">Vedere D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="74d11-479">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="74d11-480">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-480">BorderColor\[16\]</span></span>   | [<span data-ttu-id="74d11-481">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="74d11-481">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="74d11-482">Gli stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il \_ prefisso D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="74d11-482">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="74d11-483">Vedere D3DSAMP \_ BorderColor.</span><span class="sxs-lookup"><span data-stu-id="74d11-483">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="74d11-484">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-484">MagFilter\[16\]</span></span>     | <span data-ttu-id="74d11-485">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-485">dword</span></span>                        | <span data-ttu-id="74d11-486">Gli stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il \_ prefisso D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="74d11-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="74d11-487">Vedere D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="74d11-487">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="74d11-488">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-488">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="74d11-489">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-489">dword</span></span>                        | <span data-ttu-id="74d11-490">Gli stessi valori di D3DSAMP \_ MAXANISOTROPY senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="74d11-490">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="74d11-491">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-491">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="74d11-492">INT</span><span class="sxs-lookup"><span data-stu-id="74d11-492">int</span></span>                          | <span data-ttu-id="74d11-493">Gli stessi valori di D3DSAMP \_ MAXMIPLEVEL senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="74d11-493">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="74d11-494">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-494">MinFilter\[16\]</span></span>     | <span data-ttu-id="74d11-495">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-495">dword</span></span>                        | <span data-ttu-id="74d11-496">Gli stessi valori di D3DSAMP \_ MINFILTER senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="74d11-496">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="74d11-497">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-497">MipFilter\[16\]</span></span>     | <span data-ttu-id="74d11-498">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-498">dword</span></span>                        | <span data-ttu-id="74d11-499">Gli stessi valori di D3DSAMP \_ MIPFILTER senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="74d11-499">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="74d11-500">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="74d11-500">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="74d11-501">float</span><span class="sxs-lookup"><span data-stu-id="74d11-501">float</span></span>                        | <span data-ttu-id="74d11-502">Gli stessi valori di D3DSAMP \_ MIPMAPLODBIAS senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="74d11-502">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="74d11-503">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="74d11-503">SRGBTexture</span></span>         | <span data-ttu-id="74d11-504">float</span><span class="sxs-lookup"><span data-stu-id="74d11-504">float</span></span>                        | <span data-ttu-id="74d11-505">Stesso valore di D3DSAMP \_ SRGBTEXTURE senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="74d11-505">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                  |



 

<span data-ttu-id="74d11-506">Esempio:</span><span class="sxs-lookup"><span data-stu-id="74d11-506">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="74d11-507">Questo blocca i valori di UVW in modo che siano compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="74d11-507">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="74d11-508">Stati shader</span><span class="sxs-lookup"><span data-stu-id="74d11-508">Shader States</span></span>

<span data-ttu-id="74d11-509">Sono presenti solo due stati Effect shader: uno associato a un oggetto vertex shader e l'altro associato a un oggetto pixel shader.</span><span class="sxs-lookup"><span data-stu-id="74d11-509">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="74d11-510">Stato dello shader</span><span class="sxs-lookup"><span data-stu-id="74d11-510">Shader State</span></span> | <span data-ttu-id="74d11-511">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-511">Type</span></span>         | <span data-ttu-id="74d11-512">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-512">Values</span></span>                                                                      |
| <span data-ttu-id="74d11-513">PixelShader</span><span class="sxs-lookup"><span data-stu-id="74d11-513">PixelShader</span></span>  | <span data-ttu-id="74d11-514">PixelShader</span><span class="sxs-lookup"><span data-stu-id="74d11-514">pixelshader</span></span>  | <span data-ttu-id="74d11-515">**Null**, un blocco di assembly, una destinazione di compilazione o un parametro pixel shader.</span><span class="sxs-lookup"><span data-stu-id="74d11-515">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="74d11-516">VertexShader</span><span class="sxs-lookup"><span data-stu-id="74d11-516">VertexShader</span></span> | <span data-ttu-id="74d11-517">vertexshader</span><span class="sxs-lookup"><span data-stu-id="74d11-517">vertexshader</span></span> | <span data-ttu-id="74d11-518">**Null**, un blocco di assembly, una destinazione di compilazione o un parametro pixel shader.</span><span class="sxs-lookup"><span data-stu-id="74d11-518">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="74d11-519">Esempio:</span><span class="sxs-lookup"><span data-stu-id="74d11-519">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="74d11-520">Questa operazione compilerà VSTexture, un vertex shader definito in precedenza nel file con estensione FX, al vertex shader versione 1,1, quindi imposterà lo shader compilato come vertex shader.</span><span class="sxs-lookup"><span data-stu-id="74d11-520">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="74d11-521">Il pixel shader viene assegnato a **null**.</span><span class="sxs-lookup"><span data-stu-id="74d11-521">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="74d11-522">Stati costanti shader</span><span class="sxs-lookup"><span data-stu-id="74d11-522">Shader Constant States</span></span>

<span data-ttu-id="74d11-523">Gli stati costanti dello shader vengono usati per accedere ai parametri costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="74d11-523">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="74d11-524">Stato costante shader</span><span class="sxs-lookup"><span data-stu-id="74d11-524">Shader Constant State</span></span> | <span data-ttu-id="74d11-525">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-525">Type</span></span>            | <span data-ttu-id="74d11-526">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-526">Values</span></span>                                       |
| <span data-ttu-id="74d11-527">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="74d11-527">PixelShaderConstant</span></span>   | <span data-ttu-id="74d11-528">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-528">float\[m\[n\]\]</span></span> | <span data-ttu-id="74d11-529">matrice m x n di float; m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-529">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="74d11-530">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="74d11-530">PixelShaderConstant1</span></span>  | <span data-ttu-id="74d11-531">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-531">float4</span></span>          | <span data-ttu-id="74d11-532">Un float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-532">One 4D float.</span></span>                                |
| <span data-ttu-id="74d11-533">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="74d11-533">PixelShaderConstant2</span></span>  | <span data-ttu-id="74d11-534">float4x2</span><span class="sxs-lookup"><span data-stu-id="74d11-534">float4x2</span></span>        | <span data-ttu-id="74d11-535">Due float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-535">Two 4D floats.</span></span>                               |
| <span data-ttu-id="74d11-536">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="74d11-536">PixelShaderConstant3</span></span>  | <span data-ttu-id="74d11-537">float4x3</span><span class="sxs-lookup"><span data-stu-id="74d11-537">float4x3</span></span>        | <span data-ttu-id="74d11-538">Tre float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-538">Three 4D floats.</span></span>                             |
| <span data-ttu-id="74d11-539">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="74d11-539">PixelShaderConstant4</span></span>  | <span data-ttu-id="74d11-540">float4x4</span><span class="sxs-lookup"><span data-stu-id="74d11-540">float4x4</span></span>        | <span data-ttu-id="74d11-541">Quattro float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-541">Four 4D floats.</span></span>                              |
| <span data-ttu-id="74d11-542">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="74d11-542">PixelShaderConstantB</span></span>  | <span data-ttu-id="74d11-543">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-543">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="74d11-544">matrice m x n di bool; m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-544">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="74d11-545">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="74d11-545">PixelShaderConstantI</span></span>  | <span data-ttu-id="74d11-546">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-546">int\[m\[n\]\]</span></span>   | <span data-ttu-id="74d11-547">matrice m x n di int.</span><span class="sxs-lookup"><span data-stu-id="74d11-547">m x n array of ints.</span></span> <span data-ttu-id="74d11-548">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-548">m and n are optional.</span></span>   |
| <span data-ttu-id="74d11-549">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="74d11-549">PixelShaderConstantF</span></span>  | <span data-ttu-id="74d11-550">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-550">float\[m\[n\]\]</span></span> | <span data-ttu-id="74d11-551">matrice m x n di float.</span><span class="sxs-lookup"><span data-stu-id="74d11-551">m x n array of floats.</span></span> <span data-ttu-id="74d11-552">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-552">m and n are optional.</span></span> |
| <span data-ttu-id="74d11-553">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="74d11-553">VertexShaderConstant</span></span>  | <span data-ttu-id="74d11-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="74d11-555">matrice m x n di float.</span><span class="sxs-lookup"><span data-stu-id="74d11-555">m x n array of floats.</span></span> <span data-ttu-id="74d11-556">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-556">m and n are optional.</span></span> |
| <span data-ttu-id="74d11-557">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="74d11-557">VertexShaderConstant1</span></span> | <span data-ttu-id="74d11-558">float4</span><span class="sxs-lookup"><span data-stu-id="74d11-558">float4</span></span>          | <span data-ttu-id="74d11-559">Un float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-559">One 4D float.</span></span>                                |
| <span data-ttu-id="74d11-560">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="74d11-560">VertexShaderConstant2</span></span> | <span data-ttu-id="74d11-561">float4x2</span><span class="sxs-lookup"><span data-stu-id="74d11-561">float4x2</span></span>        | <span data-ttu-id="74d11-562">Due float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-562">Two 4D floats.</span></span>                               |
| <span data-ttu-id="74d11-563">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="74d11-563">VertexShaderConstant3</span></span> | <span data-ttu-id="74d11-564">float4x3</span><span class="sxs-lookup"><span data-stu-id="74d11-564">float4x3</span></span>        | <span data-ttu-id="74d11-565">Tre float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-565">Three 4D floats.</span></span>                             |
| <span data-ttu-id="74d11-566">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="74d11-566">VertexShaderConstant4</span></span> | <span data-ttu-id="74d11-567">float4x4</span><span class="sxs-lookup"><span data-stu-id="74d11-567">float4x4</span></span>        | <span data-ttu-id="74d11-568">Quattro float 4D.</span><span class="sxs-lookup"><span data-stu-id="74d11-568">Four 4D floats.</span></span>                              |
| <span data-ttu-id="74d11-569">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="74d11-569">VertexShaderConstantB</span></span> | <span data-ttu-id="74d11-570">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-570">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="74d11-571">matrice m x n di bool.</span><span class="sxs-lookup"><span data-stu-id="74d11-571">m x n array of bools.</span></span> <span data-ttu-id="74d11-572">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-572">m and n are optional.</span></span>  |
| <span data-ttu-id="74d11-573">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="74d11-573">VertexShaderConstantI</span></span> | <span data-ttu-id="74d11-574">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-574">int\[m\[n\]\]</span></span>   | <span data-ttu-id="74d11-575">matrice m x n di int.</span><span class="sxs-lookup"><span data-stu-id="74d11-575">m x n array of ints.</span></span> <span data-ttu-id="74d11-576">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-576">m and n are optional.</span></span>   |
| <span data-ttu-id="74d11-577">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="74d11-577">VertexShaderConstantF</span></span> | <span data-ttu-id="74d11-578">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="74d11-578">float\[m\[n\]\]</span></span> | <span data-ttu-id="74d11-579">matrice m x n di float.</span><span class="sxs-lookup"><span data-stu-id="74d11-579">m x n array of floats.</span></span> <span data-ttu-id="74d11-580">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74d11-580">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="74d11-581">Stati di trama</span><span class="sxs-lookup"><span data-stu-id="74d11-581">Texture States</span></span>

<span data-ttu-id="74d11-582">Gli Stati di trama inizializzano le trame usate da multitexture Blender.</span><span class="sxs-lookup"><span data-stu-id="74d11-582">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="74d11-583">Stato trama</span><span class="sxs-lookup"><span data-stu-id="74d11-583">Texture State</span></span> | <span data-ttu-id="74d11-584">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-584">Type</span></span>    | <span data-ttu-id="74d11-585">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-585">Values</span></span>                            |
| <span data-ttu-id="74d11-586">Trama \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-586">Texture\[8\]</span></span>  | <span data-ttu-id="74d11-587">trama</span><span class="sxs-lookup"><span data-stu-id="74d11-587">texture</span></span> | <span data-ttu-id="74d11-588">**Null** o un parametro texture.</span><span class="sxs-lookup"><span data-stu-id="74d11-588">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="74d11-589">Stati della fase trama</span><span class="sxs-lookup"><span data-stu-id="74d11-589">Texture Stage States</span></span>

<span data-ttu-id="74d11-590">Gli Stati della fase trama configurano le trame e le fasi di trama in Blender multitexture.</span><span class="sxs-lookup"><span data-stu-id="74d11-590">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d11-591">Stato della fase trama</span><span class="sxs-lookup"><span data-stu-id="74d11-591">Texture Stage State</span></span>        | <span data-ttu-id="74d11-592">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-592">Type</span></span>  | <span data-ttu-id="74d11-593">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-593">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="74d11-594">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-594">AlphaOp\[8\]</span></span>               | <span data-ttu-id="74d11-595">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-595">dword</span></span> | <span data-ttu-id="74d11-596">Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il \_ prefisso D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="74d11-596">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="74d11-597">Vedere D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="74d11-597">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="74d11-598">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-598">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="74d11-599">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-599">dword</span></span> | <span data-ttu-id="74d11-600">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="74d11-600">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="74d11-601">Vedere D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="74d11-601">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="74d11-602">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-602">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="74d11-603">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-603">dword</span></span> | <span data-ttu-id="74d11-604">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="74d11-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="74d11-605">Vedere D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="74d11-605">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="74d11-606">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-606">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="74d11-607">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-607">dword</span></span> | <span data-ttu-id="74d11-608">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="74d11-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="74d11-609">Vedere D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="74d11-609">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="74d11-610">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-610">ColorArg0\[8\]</span></span>             | <span data-ttu-id="74d11-611">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-611">dword</span></span> | <span data-ttu-id="74d11-612">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="74d11-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="74d11-613">Vedere D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="74d11-613">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="74d11-614">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-614">ColorArg1\[8\]</span></span>             | <span data-ttu-id="74d11-615">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-615">dword</span></span> | <span data-ttu-id="74d11-616">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="74d11-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="74d11-617">Vedere D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="74d11-617">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="74d11-618">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-618">ColorArg2\[8\]</span></span>             | <span data-ttu-id="74d11-619">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-619">dword</span></span> | <span data-ttu-id="74d11-620">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="74d11-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="74d11-621">Vedere D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="74d11-621">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="74d11-622">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-622">ColorOp\[8\]</span></span>               | <span data-ttu-id="74d11-623">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-623">dword</span></span> | <span data-ttu-id="74d11-624">Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il \_ prefisso D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="74d11-624">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="74d11-625">Vedere D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="74d11-625">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="74d11-626">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-626">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="74d11-627">float</span><span class="sxs-lookup"><span data-stu-id="74d11-627">float</span></span> | <span data-ttu-id="74d11-628">Gli stessi valori di D3DTSS \_ BUMPENVLSCALE senza il \_ prefisso D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="74d11-628">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="74d11-629">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-629">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="74d11-630">float</span><span class="sxs-lookup"><span data-stu-id="74d11-630">float</span></span> | <span data-ttu-id="74d11-631">Gli stessi valori di D3DTSS \_ BUMPENVLOFFSET senza il \_ prefisso D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="74d11-631">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="74d11-632">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-632">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="74d11-633">float</span><span class="sxs-lookup"><span data-stu-id="74d11-633">float</span></span> | <span data-ttu-id="74d11-634">Stessi valori di D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="74d11-634">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="74d11-635">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-635">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="74d11-636">float</span><span class="sxs-lookup"><span data-stu-id="74d11-636">float</span></span> | <span data-ttu-id="74d11-637">Stessi valori di D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="74d11-637">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="74d11-638">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-638">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="74d11-639">float</span><span class="sxs-lookup"><span data-stu-id="74d11-639">float</span></span> | <span data-ttu-id="74d11-640">Stessi valori di D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="74d11-640">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="74d11-641">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-641">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="74d11-642">float</span><span class="sxs-lookup"><span data-stu-id="74d11-642">float</span></span> | <span data-ttu-id="74d11-643">Stessi valori di D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="74d11-643">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="74d11-644">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-644">ResultArg\[8\]</span></span>             | <span data-ttu-id="74d11-645">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-645">dword</span></span> | <span data-ttu-id="74d11-646">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="74d11-646">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="74d11-647">Vedere D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="74d11-647">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="74d11-648">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-648">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="74d11-649">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-649">dword</span></span> | <span data-ttu-id="74d11-650">Gli stessi valori di D3DTSS \_ TEXCOORDINDEX senza il \_ prefisso D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="74d11-650">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="74d11-651">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-651">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="74d11-652">dword</span><span class="sxs-lookup"><span data-stu-id="74d11-652">dword</span></span> | <span data-ttu-id="74d11-653">Stessi valori dei valori [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) senza il \_ prefisso D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="74d11-653">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="74d11-654">Vedere D3DTSS \_ TEXTURETRANSFORMFLAGS.</span><span class="sxs-lookup"><span data-stu-id="74d11-654">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="74d11-655">Stati di trasformazione</span><span class="sxs-lookup"><span data-stu-id="74d11-655">Transform States</span></span>

<span data-ttu-id="74d11-656">Impostare gli Stati di trasformazione per inizializzare matrici di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="74d11-656">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="74d11-657">Gli effetti utilizzano matrici trasposte per migliorare l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="74d11-657">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="74d11-658">È possibile fornire matrici trasposte a un effetto oppure un effetto trasmetterà automaticamente le matrici prima di utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="74d11-658">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74d11-659">Stato trasformazione</span><span class="sxs-lookup"><span data-stu-id="74d11-659">Transform State</span></span>       | <span data-ttu-id="74d11-660">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d11-660">Type</span></span>     | <span data-ttu-id="74d11-661">Valori</span><span class="sxs-lookup"><span data-stu-id="74d11-661">Values</span></span>                                                                                                                          |
| <span data-ttu-id="74d11-662">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="74d11-662">ProjectionTransform</span></span>   | <span data-ttu-id="74d11-663">float4x4</span><span class="sxs-lookup"><span data-stu-id="74d11-663">float4x4</span></span> | <span data-ttu-id="74d11-664">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="74d11-664">A 4x4 matrix of floats.</span></span> <span data-ttu-id="74d11-665">Stessi valori della \_ proiezione D3DTS senza il \_ prefisso D3DTS.</span><span class="sxs-lookup"><span data-stu-id="74d11-665">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="74d11-666">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="74d11-666">TextureTransform\[8\]</span></span> | <span data-ttu-id="74d11-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="74d11-667">float4x4</span></span> | <span data-ttu-id="74d11-668">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="74d11-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="74d11-669">Gli stessi valori di [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) senza il \_ prefisso D3DTS.</span><span class="sxs-lookup"><span data-stu-id="74d11-669">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="74d11-670">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="74d11-670">ViewTransform</span></span>         | <span data-ttu-id="74d11-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="74d11-671">float4x4</span></span> | <span data-ttu-id="74d11-672">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="74d11-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="74d11-673">Gli stessi valori della \_ vista D3DTS senza il \_ prefisso D3DTS.</span><span class="sxs-lookup"><span data-stu-id="74d11-673">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="74d11-674">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="74d11-674">WorldTransform</span></span>        | <span data-ttu-id="74d11-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="74d11-675">float4x4</span></span> | <span data-ttu-id="74d11-676">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="74d11-676">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="74d11-677">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74d11-677">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74d11-678">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="74d11-678">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
