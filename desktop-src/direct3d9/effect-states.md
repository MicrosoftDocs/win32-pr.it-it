---
description: Gli Stati degli effetti vengono utilizzati per inizializzare gli Stati della pipeline in preparazione all'elaborazione dei vertici e dei pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Stati degli effetti (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314764"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="28203-103">Stati degli effetti (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="28203-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="28203-104">Gli Stati degli effetti vengono utilizzati per inizializzare gli Stati della pipeline in preparazione all'elaborazione dei vertici e dei pixel.</span><span class="sxs-lookup"><span data-stu-id="28203-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="28203-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="28203-105">Where:</span></span>

-   <span data-ttu-id="28203-106">stato dell'effetto, simile agli Stati tradizionali della pipeline della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="28203-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="28203-107">Di seguito è riportato un elenco completo di Stati.</span><span class="sxs-lookup"><span data-stu-id="28203-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="28203-108">\[\[ \] indice \] di -Indice integer facoltativo.</span><span class="sxs-lookup"><span data-stu-id="28203-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="28203-109">L'indice identifica un determinato stato all'interno di una matrice di Stati di effetto.</span><span class="sxs-lookup"><span data-stu-id="28203-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="28203-110">Le parentesi esterne indicano che un indice è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="28203-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="28203-111">Se viene utilizzato un indice, assicurarsi di utilizzare le parentesi interne.</span><span class="sxs-lookup"><span data-stu-id="28203-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="28203-112">espressione di assegnazione dello stato di espressione.</span><span class="sxs-lookup"><span data-stu-id="28203-112">expression - State assignment expression.</span></span> <span data-ttu-id="28203-113">Vedere [espressioni (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="28203-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="28203-114">Ogni stato ha un tipo di dati nativo.</span><span class="sxs-lookup"><span data-stu-id="28203-114">Each state has a native data type.</span></span> <span data-ttu-id="28203-115">Si tratta del tipo di dati in cui lo stato prevede che i valori siano presenti quando vengono assegnati dall'effetto.</span><span class="sxs-lookup"><span data-stu-id="28203-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="28203-116">Di seguito sono elencati i tipi di dati previsti da ogni stato.</span><span class="sxs-lookup"><span data-stu-id="28203-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="28203-117">Si noti che l'interfaccia Effect tenterà di eseguire il cast dei valori nel tipo appropriato il prima possibile.</span><span class="sxs-lookup"><span data-stu-id="28203-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="28203-118">È possibile eseguire il cast dei valori letterali in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="28203-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="28203-119">Quando vengono chiamati i metodi set appropriati, è necessario eseguire il cast delle variabili non letterali, ad esempio le variabili regolari.</span><span class="sxs-lookup"><span data-stu-id="28203-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="28203-120">Ad esempio, l'interfaccia Effect eseguirà il cast dei valori impostati utilizzando SetValue, [**SetValue**](id3dxbaseeffect--setvalue.md)e altre funzioni [**simili, se**](id3dxbaseeffect--setbool.md)necessario.</span><span class="sxs-lookup"><span data-stu-id="28203-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="28203-121">Per prestazioni ottimali, assicurarsi che i valori passati all'interfaccia effetto siano già del tipo corretto e che non sia necessario eseguire il cast.</span><span class="sxs-lookup"><span data-stu-id="28203-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="28203-122">Se il runtime non è in grado di eseguire il cast di un valore, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="28203-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="28203-123">Gli Stati degli effetti possono essere suddivisi nelle categorie seguenti:</span><span class="sxs-lookup"><span data-stu-id="28203-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="28203-124">Stati leggeri</span><span class="sxs-lookup"><span data-stu-id="28203-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="28203-125">Stati del materiale</span><span class="sxs-lookup"><span data-stu-id="28203-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="28203-126">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="28203-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="28203-127">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="28203-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="28203-128">Stati di rendering della pipe del vertice</span><span class="sxs-lookup"><span data-stu-id="28203-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="28203-129">Stati campionatore</span><span class="sxs-lookup"><span data-stu-id="28203-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="28203-130">Stati fase campionatore</span><span class="sxs-lookup"><span data-stu-id="28203-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="28203-131">Stati shader</span><span class="sxs-lookup"><span data-stu-id="28203-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="28203-132">Stati costanti shader</span><span class="sxs-lookup"><span data-stu-id="28203-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="28203-133">Stati di trama</span><span class="sxs-lookup"><span data-stu-id="28203-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="28203-134">Stati della fase trama</span><span class="sxs-lookup"><span data-stu-id="28203-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="28203-135">Stati di trasformazione</span><span class="sxs-lookup"><span data-stu-id="28203-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="28203-136">Stati leggeri</span><span class="sxs-lookup"><span data-stu-id="28203-136">Light States</span></span>

<span data-ttu-id="28203-137">Per garantire prestazioni ottimali per l'applicazione di un effetto, è necessario specificare nel file degli effetti tutti i componenti di una luce o di un materiale.</span><span class="sxs-lookup"><span data-stu-id="28203-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="28203-138">Gli Stati che non vengono dichiarati sono impostati su un valore predefinito perché non è possibile impostare gli Stati di luce singolarmente da Direct3D.</span><span class="sxs-lookup"><span data-stu-id="28203-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28203-139">Stato chiaro</span><span class="sxs-lookup"><span data-stu-id="28203-139">Light State</span></span>            | <span data-ttu-id="28203-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-140">Type</span></span>   | <span data-ttu-id="28203-141">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="28203-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="28203-143">float4</span><span class="sxs-lookup"><span data-stu-id="28203-143">float4</span></span> | <span data-ttu-id="28203-144">Vedere il membro di ambiente di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="28203-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="28203-146">float</span><span class="sxs-lookup"><span data-stu-id="28203-146">float</span></span>  | <span data-ttu-id="28203-147">Vedere il membro Attenuation0 di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="28203-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="28203-149">float</span><span class="sxs-lookup"><span data-stu-id="28203-149">float</span></span>  | <span data-ttu-id="28203-150">Vedere il membro Attenuation1 di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="28203-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="28203-152">float</span><span class="sxs-lookup"><span data-stu-id="28203-152">float</span></span>  | <span data-ttu-id="28203-153">Vedere il membro Attenuation2 di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="28203-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="28203-155">float4</span><span class="sxs-lookup"><span data-stu-id="28203-155">float4</span></span> | <span data-ttu-id="28203-156">Vedere il membro Diffusion di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="28203-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="28203-158">float3</span><span class="sxs-lookup"><span data-stu-id="28203-158">float3</span></span> | <span data-ttu-id="28203-159">Vedere il membro direction di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="28203-160">N Alleggeribile \[\]</span><span class="sxs-lookup"><span data-stu-id="28203-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="28203-161">bool</span><span class="sxs-lookup"><span data-stu-id="28203-161">bool</span></span>   | <span data-ttu-id="28203-162">**True** o **false**.</span><span class="sxs-lookup"><span data-stu-id="28203-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="28203-163">Vedere l'argomento bEnable in [**schiarente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="28203-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="28203-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="28203-165">float</span><span class="sxs-lookup"><span data-stu-id="28203-165">float</span></span>  | <span data-ttu-id="28203-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="28203-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="28203-167">Vedere il membro di interruzione di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="28203-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="28203-169">float</span><span class="sxs-lookup"><span data-stu-id="28203-169">float</span></span>  | <span data-ttu-id="28203-170">Vedere il membro Phi di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="28203-171">Posizioneilluminazione \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="28203-172">float3</span><span class="sxs-lookup"><span data-stu-id="28203-172">float3</span></span> | <span data-ttu-id="28203-173">Vedere il membro Position di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="28203-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-174">LightRange\[n\]</span></span>        | <span data-ttu-id="28203-175">float</span><span class="sxs-lookup"><span data-stu-id="28203-175">float</span></span>  | <span data-ttu-id="28203-176">Vedere il membro di intervallo di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="28203-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="28203-178">float4</span><span class="sxs-lookup"><span data-stu-id="28203-178">float4</span></span> | <span data-ttu-id="28203-179">Vedere il membro speculare di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="28203-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="28203-181">float</span><span class="sxs-lookup"><span data-stu-id="28203-181">float</span></span>  | <span data-ttu-id="28203-182">Vedere il membro theta di [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="28203-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="28203-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="28203-183">LightType\[n\]</span></span>         | <span data-ttu-id="28203-184">dword</span><span class="sxs-lookup"><span data-stu-id="28203-184">dword</span></span>  | <span data-ttu-id="28203-185">Stesso valore della matrice di un massimo di n valori [**D3DLIGHTTYPE**](./d3dlighttype.md) senza il \_ prefisso D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="28203-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="28203-186">Esempio:</span><span class="sxs-lookup"><span data-stu-id="28203-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="28203-187">Questa operazione consentirà di accendere il tipo, impostare la posizione della luce su float3<10.0 f, 1.0 f, 23.0 f> e impostare il colore di ambiente su float4<0.7 f, 0,0 f, 0,0 f, 1.0 f>.</span><span class="sxs-lookup"><span data-stu-id="28203-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="28203-188">Stati del materiale</span><span class="sxs-lookup"><span data-stu-id="28203-188">Material States</span></span>

<span data-ttu-id="28203-189">Gli Stati che non vengono dichiarati sono impostati su un valore predefinito perché non è possibile impostare gli Stati del materiale singolarmente tramite Direct3D.</span><span class="sxs-lookup"><span data-stu-id="28203-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="28203-190">Stato del materiale</span><span class="sxs-lookup"><span data-stu-id="28203-190">Material State</span></span>   | <span data-ttu-id="28203-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-191">Type</span></span>   | <span data-ttu-id="28203-192">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-192">Values</span></span>                                         |
| <span data-ttu-id="28203-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="28203-193">MaterialAmbient</span></span>  | <span data-ttu-id="28203-194">float4</span><span class="sxs-lookup"><span data-stu-id="28203-194">float4</span></span> | <span data-ttu-id="28203-195">Stesso valore di [ **ambiente**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="28203-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="28203-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="28203-196">MaterialDiffuse</span></span>  | <span data-ttu-id="28203-197">float4</span><span class="sxs-lookup"><span data-stu-id="28203-197">float4</span></span> | <span data-ttu-id="28203-198">Stesso valore di [ **Diffusion**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="28203-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="28203-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="28203-199">MaterialEmissive</span></span> | <span data-ttu-id="28203-200">float4</span><span class="sxs-lookup"><span data-stu-id="28203-200">float4</span></span> | <span data-ttu-id="28203-201">Stesso valore di [ **emissivo**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="28203-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="28203-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="28203-202">MaterialPower</span></span>    | <span data-ttu-id="28203-203">float</span><span class="sxs-lookup"><span data-stu-id="28203-203">float</span></span>  | <span data-ttu-id="28203-204">Stesso valore di [ **Power**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="28203-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="28203-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="28203-205">MaterialSpecular</span></span> | <span data-ttu-id="28203-206">float4</span><span class="sxs-lookup"><span data-stu-id="28203-206">float4</span></span> | <span data-ttu-id="28203-207">Stesso valore di [ **speculare**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="28203-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="28203-208">Esempio:</span><span class="sxs-lookup"><span data-stu-id="28203-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="28203-209">Il colore di diffusione verrà impostato su float4<0.7 f, 0,0 f, 0,0 f, 1.0 f> e apporterà la potenza del materiale 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="28203-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="28203-210">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="28203-210">Render States</span></span>

<span data-ttu-id="28203-211">Esistono due tipi di Stati di rendering:</span><span class="sxs-lookup"><span data-stu-id="28203-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="28203-212">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="28203-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="28203-213">Stati di rendering della pipe del vertice</span><span class="sxs-lookup"><span data-stu-id="28203-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="28203-214">Stati di rendering della pipe pixel</span><span class="sxs-lookup"><span data-stu-id="28203-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="28203-215">Gli Stati di rendering dei file degli effetti hanno nomi simili agli Stati della pipeline della funzione fissa, spesso con il prefisso rimosso.</span><span class="sxs-lookup"><span data-stu-id="28203-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28203-216">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="28203-216">Render State</span></span></td>
<td><span data-ttu-id="28203-217">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-217">Type</span></span></td>
<td><span data-ttu-id="28203-218">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="28203-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="28203-220">bool</span><span class="sxs-lookup"><span data-stu-id="28203-220">bool</span></span></td>
<td><span data-ttu-id="28203-221">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-221">True or False.</span></span> <span data-ttu-id="28203-222">Gli stessi valori di D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="28203-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="28203-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="28203-224">dword</span><span class="sxs-lookup"><span data-stu-id="28203-224">dword</span></span></td>
<td><span data-ttu-id="28203-225">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="28203-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="28203-226">Vedere D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="28203-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="28203-227">AlphaRef</span></span></td>
<td><span data-ttu-id="28203-228">dword</span><span class="sxs-lookup"><span data-stu-id="28203-228">dword</span></span></td>
<td><span data-ttu-id="28203-229">Stessi valori di D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="28203-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="28203-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="28203-231">dword</span><span class="sxs-lookup"><span data-stu-id="28203-231">dword</span></span></td>
<td><span data-ttu-id="28203-232">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-232">True or False.</span></span> <span data-ttu-id="28203-233">Vedere D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="28203-234">BlendOp</span></span></td>
<td><span data-ttu-id="28203-235">dword</span><span class="sxs-lookup"><span data-stu-id="28203-235">dword</span></span></td>
<td><span data-ttu-id="28203-236">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> senza il prefisso D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="28203-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="28203-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="28203-238">dword</span><span class="sxs-lookup"><span data-stu-id="28203-238">dword</span></span></td>
<td><span data-ttu-id="28203-239">Combinazione bit per bit di rosso | VERDE | BLU | Alfa.</span><span class="sxs-lookup"><span data-stu-id="28203-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="28203-240">Vedere D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="28203-241">DepthBias</span></span></td>
<td><span data-ttu-id="28203-242">float</span><span class="sxs-lookup"><span data-stu-id="28203-242">float</span></span></td>
<td><span data-ttu-id="28203-243">Stessi valori di D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="28203-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="28203-244">DestBlend</span></span></td>
<td><span data-ttu-id="28203-245">dword</span><span class="sxs-lookup"><span data-stu-id="28203-245">dword</span></span></td>
<td><span data-ttu-id="28203-246">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="28203-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="28203-247">DitherEnable</span></span></td>
<td><span data-ttu-id="28203-248">bool</span><span class="sxs-lookup"><span data-stu-id="28203-248">bool</span></span></td>
<td><span data-ttu-id="28203-249">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-249">True or False.</span></span> <span data-ttu-id="28203-250">Stessi valori di D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="28203-251">FillMode</span></span></td>
<td><span data-ttu-id="28203-252">dword</span><span class="sxs-lookup"><span data-stu-id="28203-252">dword</span></span></td>
<td><span data-ttu-id="28203-253">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> senza il prefisso D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="28203-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="28203-254">LastPixel</span></span></td>
<td><span data-ttu-id="28203-255">dword</span><span class="sxs-lookup"><span data-stu-id="28203-255">dword</span></span></td>
<td><span data-ttu-id="28203-256">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-256">True or False.</span></span> <span data-ttu-id="28203-257">Vedere D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="28203-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-258">MODOOMBRA</span><span class="sxs-lookup"><span data-stu-id="28203-258">ShadeMode</span></span></td>
<td><span data-ttu-id="28203-259">dword</span><span class="sxs-lookup"><span data-stu-id="28203-259">dword</span></span></td>
<td><span data-ttu-id="28203-260">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> senza il prefisso D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="28203-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="28203-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="28203-262">float</span><span class="sxs-lookup"><span data-stu-id="28203-262">float</span></span></td>
<td><span data-ttu-id="28203-263">Stessi valori di D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="28203-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="28203-264">SrcBlend</span></span></td>
<td><span data-ttu-id="28203-265">dword</span><span class="sxs-lookup"><span data-stu-id="28203-265">dword</span></span></td>
<td><span data-ttu-id="28203-266">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> senza il prefisso D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="28203-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="28203-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="28203-268">bool</span><span class="sxs-lookup"><span data-stu-id="28203-268">bool</span></span></td>
<td><span data-ttu-id="28203-269">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-269">True or False.</span></span> <span data-ttu-id="28203-270">Stessi valori di D3DRS_SRGBWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="28203-271">StencilEnable</span></span></td>
<td><span data-ttu-id="28203-272">bool</span><span class="sxs-lookup"><span data-stu-id="28203-272">bool</span></span></td>
<td><span data-ttu-id="28203-273">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-273">True or False.</span></span> <span data-ttu-id="28203-274">Stessi valori di D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="28203-275">StencilFail</span></span></td>
<td><span data-ttu-id="28203-276">dword</span><span class="sxs-lookup"><span data-stu-id="28203-276">dword</span></span></td>
<td><span data-ttu-id="28203-277">Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="28203-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="28203-278">Vedere D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="28203-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="28203-279">StencilFunc</span></span></td>
<td><span data-ttu-id="28203-280">dword</span><span class="sxs-lookup"><span data-stu-id="28203-280">dword</span></span></td>
<td><span data-ttu-id="28203-281">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="28203-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="28203-282">Vedere D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="28203-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-283">StencilMask</span><span class="sxs-lookup"><span data-stu-id="28203-283">StencilMask</span></span></td>
<td><span data-ttu-id="28203-284">dword</span><span class="sxs-lookup"><span data-stu-id="28203-284">dword</span></span></td>
<td><span data-ttu-id="28203-285">Stessi valori di D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="28203-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="28203-286">StencilPass</span></span></td>
<td><span data-ttu-id="28203-287">dword</span><span class="sxs-lookup"><span data-stu-id="28203-287">dword</span></span></td>
<td><span data-ttu-id="28203-288">Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="28203-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="28203-289">Vedere D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="28203-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="28203-290">StencilRef</span></span></td>
<td><span data-ttu-id="28203-291">INT</span><span class="sxs-lookup"><span data-stu-id="28203-291">int</span></span></td>
<td><span data-ttu-id="28203-292">Stessi valori di D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="28203-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="28203-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="28203-294">dword</span><span class="sxs-lookup"><span data-stu-id="28203-294">dword</span></span></td>
<td><span data-ttu-id="28203-295">Stessi valori di D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="28203-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="28203-296">StencilZFail</span></span></td>
<td><span data-ttu-id="28203-297">dword</span><span class="sxs-lookup"><span data-stu-id="28203-297">dword</span></span></td>
<td><span data-ttu-id="28203-298">Gli stessi valori di <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> senza il prefisso D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="28203-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="28203-299">Vedere D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="28203-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="28203-300">TextureFactor</span></span></td>
<td><span data-ttu-id="28203-301">dword</span><span class="sxs-lookup"><span data-stu-id="28203-301">dword</span></span></td>
<td><span data-ttu-id="28203-302">Stessi valori di <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="28203-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="28203-303">Stessi valori di D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="28203-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-304">Wrap0-Wrap15</span><span class="sxs-lookup"><span data-stu-id="28203-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="28203-305">dword</span><span class="sxs-lookup"><span data-stu-id="28203-305">dword</span></span></td>
<td><span data-ttu-id="28203-306">I valori corrispondono ai valori utilizzati da D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="28203-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="28203-307">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="28203-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="28203-308">COORD0 (che corrisponde a D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="28203-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="28203-309">COORD1 (che corrisponde a D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="28203-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="28203-310">COORD2 (che corrisponde a D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="28203-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="28203-311">COORD3 (che corrisponde a D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="28203-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="28203-312">U (che corrisponde a D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="28203-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="28203-313">V (che corrisponde a D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="28203-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="28203-314">W (che corrisponde a D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="28203-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="28203-315">ZEnable</span></span></td>
<td><span data-ttu-id="28203-316">dword</span><span class="sxs-lookup"><span data-stu-id="28203-316">dword</span></span></td>
<td><span data-ttu-id="28203-317">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> senza il prefisso D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="28203-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28203-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="28203-318">ZFunc</span></span></td>
<td><span data-ttu-id="28203-319">dword</span><span class="sxs-lookup"><span data-stu-id="28203-319">dword</span></span></td>
<td><span data-ttu-id="28203-320">Gli stessi valori di <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> senza il prefisso D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="28203-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="28203-321">Vedere D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="28203-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28203-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="28203-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="28203-323">bool</span><span class="sxs-lookup"><span data-stu-id="28203-323">bool</span></span></td>
<td><span data-ttu-id="28203-324">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-324">True or False.</span></span> <span data-ttu-id="28203-325">Vedere D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="28203-326">Esempio:</span><span class="sxs-lookup"><span data-stu-id="28203-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="28203-327">In questo modo verrà abilitata la fusione alfa e verrà eseguito il rendering di tutte le geometrie in wireframe.</span><span class="sxs-lookup"><span data-stu-id="28203-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="28203-328">Stati di rendering della pipe del vertice</span><span class="sxs-lookup"><span data-stu-id="28203-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="28203-329">Gli Stati di rendering dei file degli effetti hanno nomi simili agli Stati della pipeline della funzione fissa, spesso con il prefisso rimosso.</span><span class="sxs-lookup"><span data-stu-id="28203-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28203-330">Stato di rendering</span><span class="sxs-lookup"><span data-stu-id="28203-330">Render State</span></span>             | <span data-ttu-id="28203-331">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-331">Type</span></span>   | <span data-ttu-id="28203-332">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-332">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="28203-333">Di ambiente</span><span class="sxs-lookup"><span data-stu-id="28203-333">Ambient</span></span>                  | <span data-ttu-id="28203-334">float4</span><span class="sxs-lookup"><span data-stu-id="28203-334">float4</span></span> | <span data-ttu-id="28203-335">Stessi valori dell' \_ ambiente D3DRS.</span><span class="sxs-lookup"><span data-stu-id="28203-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="28203-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="28203-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="28203-337">dword</span><span class="sxs-lookup"><span data-stu-id="28203-337">dword</span></span>  | <span data-ttu-id="28203-338">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="28203-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="28203-339">Vedere D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="28203-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="28203-340">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="28203-340">Clipping</span></span>                 | <span data-ttu-id="28203-341">bool</span><span class="sxs-lookup"><span data-stu-id="28203-341">bool</span></span>   | <span data-ttu-id="28203-342">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-342">True or False.</span></span> <span data-ttu-id="28203-343">Stessi valori del \_ ritaglio D3DRS.</span><span class="sxs-lookup"><span data-stu-id="28203-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="28203-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="28203-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="28203-345">dword</span><span class="sxs-lookup"><span data-stu-id="28203-345">dword</span></span>  | <span data-ttu-id="28203-346">Combinazione bit per bit di macro D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="28203-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="28203-347">Vedere [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="28203-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="28203-348">ColorVertex</span></span>              | <span data-ttu-id="28203-349">bool</span><span class="sxs-lookup"><span data-stu-id="28203-349">bool</span></span>   | <span data-ttu-id="28203-350">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-350">True or False.</span></span> <span data-ttu-id="28203-351">Stessi valori di D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="28203-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="28203-352">CullMode</span><span class="sxs-lookup"><span data-stu-id="28203-352">CullMode</span></span>                 | <span data-ttu-id="28203-353">dword</span><span class="sxs-lookup"><span data-stu-id="28203-353">dword</span></span>  | <span data-ttu-id="28203-354">Gli stessi valori di [**D3DCULL**](./d3dcull.md) senza il \_ prefisso D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="28203-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="28203-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="28203-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="28203-356">dword</span><span class="sxs-lookup"><span data-stu-id="28203-356">dword</span></span>  | <span data-ttu-id="28203-357">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="28203-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="28203-358">Vedere D3DRS \_ DIFFUSEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="28203-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="28203-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="28203-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="28203-360">dword</span><span class="sxs-lookup"><span data-stu-id="28203-360">dword</span></span>  | <span data-ttu-id="28203-361">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="28203-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="28203-362">Vedere D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="28203-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="28203-363">FogColor</span><span class="sxs-lookup"><span data-stu-id="28203-363">FogColor</span></span>                 | <span data-ttu-id="28203-364">dword</span><span class="sxs-lookup"><span data-stu-id="28203-364">dword</span></span>  | <span data-ttu-id="28203-365">Stessi valori di [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="28203-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="28203-366">Vedere D3DRS \_ FogColor.</span><span class="sxs-lookup"><span data-stu-id="28203-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="28203-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="28203-367">FogDensity</span></span>               | <span data-ttu-id="28203-368">float</span><span class="sxs-lookup"><span data-stu-id="28203-368">float</span></span>  | <span data-ttu-id="28203-369">Stessi valori di D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="28203-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="28203-370">FogEnable</span><span class="sxs-lookup"><span data-stu-id="28203-370">FogEnable</span></span>                | <span data-ttu-id="28203-371">bool</span><span class="sxs-lookup"><span data-stu-id="28203-371">bool</span></span>   | <span data-ttu-id="28203-372">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-372">True or False.</span></span> <span data-ttu-id="28203-373">Stessi valori di D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="28203-374">FogEnd</span><span class="sxs-lookup"><span data-stu-id="28203-374">FogEnd</span></span>                   | <span data-ttu-id="28203-375">float</span><span class="sxs-lookup"><span data-stu-id="28203-375">float</span></span>  | <span data-ttu-id="28203-376">Stessi valori di D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="28203-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="28203-377">FogStart</span><span class="sxs-lookup"><span data-stu-id="28203-377">FogStart</span></span>                 | <span data-ttu-id="28203-378">float</span><span class="sxs-lookup"><span data-stu-id="28203-378">float</span></span>  | <span data-ttu-id="28203-379">Stessi valori di D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="28203-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="28203-380">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="28203-380">FogTableMode</span></span>             | <span data-ttu-id="28203-381">dword</span><span class="sxs-lookup"><span data-stu-id="28203-381">dword</span></span>  | <span data-ttu-id="28203-382">Stessi valori di [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="28203-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="28203-383">Vedere D3DRS \_ FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="28203-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="28203-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="28203-384">FogVertexMode</span></span>            | <span data-ttu-id="28203-385">dword</span><span class="sxs-lookup"><span data-stu-id="28203-385">dword</span></span>  | <span data-ttu-id="28203-386">Gli stessi valori di [**D3DFOGMODE**](./d3dfogmode.md) senza il \_ prefisso D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="28203-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="28203-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="28203-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="28203-388">bool</span><span class="sxs-lookup"><span data-stu-id="28203-388">bool</span></span>   | <span data-ttu-id="28203-389">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-389">True or False.</span></span> <span data-ttu-id="28203-390">Stessi valori di D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="28203-391">Luce</span><span class="sxs-lookup"><span data-stu-id="28203-391">Lighting</span></span>                 | <span data-ttu-id="28203-392">bool</span><span class="sxs-lookup"><span data-stu-id="28203-392">bool</span></span>   | <span data-ttu-id="28203-393">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-393">True or False.</span></span> <span data-ttu-id="28203-394">Stessi valori dell' \_ illuminazione D3DRS.</span><span class="sxs-lookup"><span data-stu-id="28203-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="28203-395">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="28203-395">LocalViewer</span></span>              | <span data-ttu-id="28203-396">bool</span><span class="sxs-lookup"><span data-stu-id="28203-396">bool</span></span>   | <span data-ttu-id="28203-397">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-397">True or False.</span></span> <span data-ttu-id="28203-398">Stessi valori di D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="28203-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="28203-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="28203-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="28203-400">bool</span><span class="sxs-lookup"><span data-stu-id="28203-400">bool</span></span>   | <span data-ttu-id="28203-401">Stessi valori di D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="28203-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="28203-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="28203-402">MultiSampleMask</span></span>          | <span data-ttu-id="28203-403">dword</span><span class="sxs-lookup"><span data-stu-id="28203-403">dword</span></span>  | <span data-ttu-id="28203-404">Stessi valori di D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="28203-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="28203-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="28203-405">NormalizeNormals</span></span>         | <span data-ttu-id="28203-406">bool</span><span class="sxs-lookup"><span data-stu-id="28203-406">bool</span></span>   | <span data-ttu-id="28203-407">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-407">True or False.</span></span> <span data-ttu-id="28203-408">Stessi valori di D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="28203-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="28203-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="28203-409">PatchSegments</span></span>            | <span data-ttu-id="28203-410">float</span><span class="sxs-lookup"><span data-stu-id="28203-410">float</span></span>  | <span data-ttu-id="28203-411">Stessi valori di nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="28203-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="28203-412">PointScale \_</span><span class="sxs-lookup"><span data-stu-id="28203-412">PointScale\_A</span></span>            | <span data-ttu-id="28203-413">float</span><span class="sxs-lookup"><span data-stu-id="28203-413">float</span></span>  | <span data-ttu-id="28203-414">Gli stessi valori di D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="28203-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="28203-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="28203-415">PointScale\_B</span></span>            | <span data-ttu-id="28203-416">float</span><span class="sxs-lookup"><span data-stu-id="28203-416">float</span></span>  | <span data-ttu-id="28203-417">Stessi valori di D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="28203-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="28203-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="28203-418">PointScale\_C</span></span>            | <span data-ttu-id="28203-419">float</span><span class="sxs-lookup"><span data-stu-id="28203-419">float</span></span>  | <span data-ttu-id="28203-420">Stessi valori di D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="28203-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="28203-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="28203-421">PointScaleEnable</span></span>         | <span data-ttu-id="28203-422">bool</span><span class="sxs-lookup"><span data-stu-id="28203-422">bool</span></span>   | <span data-ttu-id="28203-423">Stessi valori di D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="28203-424">PointSize</span><span class="sxs-lookup"><span data-stu-id="28203-424">PointSize</span></span>                | <span data-ttu-id="28203-425">float</span><span class="sxs-lookup"><span data-stu-id="28203-425">float</span></span>  | <span data-ttu-id="28203-426">Stessi valori di D3DRS \_ POINTSIZE.</span><span class="sxs-lookup"><span data-stu-id="28203-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="28203-427">PointSize \_ min</span><span class="sxs-lookup"><span data-stu-id="28203-427">PointSize\_Min</span></span>           | <span data-ttu-id="28203-428">float</span><span class="sxs-lookup"><span data-stu-id="28203-428">float</span></span>  | <span data-ttu-id="28203-429">Gli stessi valori di D3DRS \_ POINTSIZE \_ min.</span><span class="sxs-lookup"><span data-stu-id="28203-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="28203-430">PointSize \_ Max</span><span class="sxs-lookup"><span data-stu-id="28203-430">PointSize\_Max</span></span>           | <span data-ttu-id="28203-431">float</span><span class="sxs-lookup"><span data-stu-id="28203-431">float</span></span>  | <span data-ttu-id="28203-432">Gli stessi valori di D3DRS \_ POINTSIZE \_ Max senza il \_ prefisso D3DRS.</span><span class="sxs-lookup"><span data-stu-id="28203-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="28203-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="28203-433">PointSpriteEnable</span></span>        | <span data-ttu-id="28203-434">bool</span><span class="sxs-lookup"><span data-stu-id="28203-434">bool</span></span>   | <span data-ttu-id="28203-435">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-435">True or False.</span></span> <span data-ttu-id="28203-436">Stessi valori di D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="28203-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="28203-437">RangeFogEnable</span></span>           | <span data-ttu-id="28203-438">bool</span><span class="sxs-lookup"><span data-stu-id="28203-438">bool</span></span>   | <span data-ttu-id="28203-439">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-439">True or False.</span></span> <span data-ttu-id="28203-440">Stessi valori di D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="28203-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="28203-441">SpecularEnable</span></span>           | <span data-ttu-id="28203-442">bool</span><span class="sxs-lookup"><span data-stu-id="28203-442">bool</span></span>   | <span data-ttu-id="28203-443">Vero o falso.</span><span class="sxs-lookup"><span data-stu-id="28203-443">True or False.</span></span> <span data-ttu-id="28203-444">Stessi valori di D3DRS \_ SPECULARENABLE.</span><span class="sxs-lookup"><span data-stu-id="28203-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="28203-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="28203-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="28203-446">dword</span><span class="sxs-lookup"><span data-stu-id="28203-446">dword</span></span>  | <span data-ttu-id="28203-447">Gli stessi valori di [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) senza il \_ prefisso D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="28203-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="28203-448">Vedere D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="28203-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="28203-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="28203-449">TweenFactor</span></span>              | <span data-ttu-id="28203-450">float</span><span class="sxs-lookup"><span data-stu-id="28203-450">float</span></span>  | <span data-ttu-id="28203-451">Stessi valori di D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="28203-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="28203-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="28203-452">VertexBlend</span></span>              | <span data-ttu-id="28203-453">dword</span><span class="sxs-lookup"><span data-stu-id="28203-453">dword</span></span>  | <span data-ttu-id="28203-454">Gli stessi valori di [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) senza il \_ prefisso D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="28203-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="28203-455">Vedere D3DRS \_ VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="28203-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="28203-456">Esempio:</span><span class="sxs-lookup"><span data-stu-id="28203-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="28203-457">In questo modo, il colore di ambiente float4<0.7 f, 0,0 f, 0,0 f, 1.0 f>, impostare la modalità di abbattimento della superficie in senso antiorario e impostare il colore di nebbia su rosso.</span><span class="sxs-lookup"><span data-stu-id="28203-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="28203-458">Stati campionatore</span><span class="sxs-lookup"><span data-stu-id="28203-458">Sampler States</span></span>

<span data-ttu-id="28203-459">Uno stato del campionatore rappresenta un oggetto campionatore.</span><span class="sxs-lookup"><span data-stu-id="28203-459">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="28203-460">State</span><span class="sxs-lookup"><span data-stu-id="28203-460">State</span></span>   | <span data-ttu-id="28203-461">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-461">Type</span></span>    | <span data-ttu-id="28203-462">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-462">Values</span></span>                              |
| <span data-ttu-id="28203-463">Campionatore</span><span class="sxs-lookup"><span data-stu-id="28203-463">Sampler</span></span> | <span data-ttu-id="28203-464">campionatore</span><span class="sxs-lookup"><span data-stu-id="28203-464">sampler</span></span> | <span data-ttu-id="28203-465">**Null** o un blocco di stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="28203-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="28203-466">Stati fase campionatore</span><span class="sxs-lookup"><span data-stu-id="28203-466">Sampler Stage States</span></span>

<span data-ttu-id="28203-467">Gli Stati della fase del campionatore vengono usati per campionare le trame.</span><span class="sxs-lookup"><span data-stu-id="28203-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="28203-468">Stato campionatore determina i tipi di filtro e le modalità di indirizzamento della trama.</span><span class="sxs-lookup"><span data-stu-id="28203-468">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28203-469">Stato campionatore</span><span class="sxs-lookup"><span data-stu-id="28203-469">Sampler State</span></span>       | <span data-ttu-id="28203-470">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-470">Type</span></span>                         | <span data-ttu-id="28203-471">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-471">Values</span></span>                                                                                                                            |
| <span data-ttu-id="28203-472">Indirizzo \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-472">AddressU\[16\]</span></span>      | <span data-ttu-id="28203-473">dword</span><span class="sxs-lookup"><span data-stu-id="28203-473">dword</span></span>                        | <span data-ttu-id="28203-474">Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="28203-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="28203-475">Vedere D3DSAMP \_ .</span><span class="sxs-lookup"><span data-stu-id="28203-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="28203-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-476">AddressV\[16\]</span></span>      | <span data-ttu-id="28203-477">dword</span><span class="sxs-lookup"><span data-stu-id="28203-477">dword</span></span>                        | <span data-ttu-id="28203-478">Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="28203-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="28203-479">Vedere D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="28203-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="28203-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-480">AddressW\[16\]</span></span>      | <span data-ttu-id="28203-481">dword</span><span class="sxs-lookup"><span data-stu-id="28203-481">dword</span></span>                        | <span data-ttu-id="28203-482">Gli stessi valori di [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) senza il \_ prefisso D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="28203-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="28203-483">Vedere D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="28203-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="28203-484">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="28203-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="28203-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="28203-486">Gli stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il \_ prefisso D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="28203-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="28203-487">Vedere D3DSAMP \_ BorderColor.</span><span class="sxs-lookup"><span data-stu-id="28203-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="28203-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="28203-489">dword</span><span class="sxs-lookup"><span data-stu-id="28203-489">dword</span></span>                        | <span data-ttu-id="28203-490">Gli stessi valori di [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) senza il \_ prefisso D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="28203-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="28203-491">Vedere D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="28203-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="28203-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="28203-493">dword</span><span class="sxs-lookup"><span data-stu-id="28203-493">dword</span></span>                        | <span data-ttu-id="28203-494">Gli stessi valori di D3DSAMP \_ MAXANISOTROPY senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="28203-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="28203-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="28203-496">INT</span><span class="sxs-lookup"><span data-stu-id="28203-496">int</span></span>                          | <span data-ttu-id="28203-497">Gli stessi valori di D3DSAMP \_ MAXMIPLEVEL senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="28203-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="28203-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="28203-499">dword</span><span class="sxs-lookup"><span data-stu-id="28203-499">dword</span></span>                        | <span data-ttu-id="28203-500">Gli stessi valori di D3DSAMP \_ MINFILTER senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="28203-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="28203-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="28203-502">dword</span><span class="sxs-lookup"><span data-stu-id="28203-502">dword</span></span>                        | <span data-ttu-id="28203-503">Gli stessi valori di D3DSAMP \_ MIPFILTER senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="28203-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="28203-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="28203-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="28203-505">float</span><span class="sxs-lookup"><span data-stu-id="28203-505">float</span></span>                        | <span data-ttu-id="28203-506">Gli stessi valori di D3DSAMP \_ MIPMAPLODBIAS senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="28203-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="28203-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="28203-507">SRGBTexture</span></span>         | <span data-ttu-id="28203-508">bool</span><span class="sxs-lookup"><span data-stu-id="28203-508">bool</span></span>                         | <span data-ttu-id="28203-509">Stesso valore di D3DSAMP \_ SRGBTEXTURE senza il \_ prefisso D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="28203-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="28203-510">Esempio:</span><span class="sxs-lookup"><span data-stu-id="28203-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="28203-511">Questo blocca i valori di UVW in modo che siano compresi tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="28203-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="28203-512">Stati shader</span><span class="sxs-lookup"><span data-stu-id="28203-512">Shader States</span></span>

<span data-ttu-id="28203-513">Sono presenti solo due stati Effect shader: uno associato a un oggetto vertex shader e l'altro associato a un oggetto pixel shader.</span><span class="sxs-lookup"><span data-stu-id="28203-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="28203-514">Stato dello shader</span><span class="sxs-lookup"><span data-stu-id="28203-514">Shader State</span></span> | <span data-ttu-id="28203-515">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-515">Type</span></span>         | <span data-ttu-id="28203-516">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-516">Values</span></span>                                                                      |
| <span data-ttu-id="28203-517">PixelShader</span><span class="sxs-lookup"><span data-stu-id="28203-517">PixelShader</span></span>  | <span data-ttu-id="28203-518">PixelShader</span><span class="sxs-lookup"><span data-stu-id="28203-518">pixelshader</span></span>  | <span data-ttu-id="28203-519">**Null**, un blocco di assembly, una destinazione di compilazione o un parametro pixel shader.</span><span class="sxs-lookup"><span data-stu-id="28203-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="28203-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="28203-520">VertexShader</span></span> | <span data-ttu-id="28203-521">vertexshader</span><span class="sxs-lookup"><span data-stu-id="28203-521">vertexshader</span></span> | <span data-ttu-id="28203-522">**Null**, un blocco di assembly, una destinazione di compilazione o un parametro pixel shader.</span><span class="sxs-lookup"><span data-stu-id="28203-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="28203-523">Esempio:</span><span class="sxs-lookup"><span data-stu-id="28203-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="28203-524">Questa operazione compilerà VSTexture, un vertex shader definito in precedenza nel file con estensione FX, al vertex shader versione 1,1, quindi imposterà lo shader compilato come vertex shader.</span><span class="sxs-lookup"><span data-stu-id="28203-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="28203-525">Il pixel shader viene assegnato a **null**.</span><span class="sxs-lookup"><span data-stu-id="28203-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="28203-526">Stati costanti shader</span><span class="sxs-lookup"><span data-stu-id="28203-526">Shader Constant States</span></span>

<span data-ttu-id="28203-527">Gli stati costanti dello shader vengono usati per accedere ai parametri costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="28203-527">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="28203-528">Stato costante shader</span><span class="sxs-lookup"><span data-stu-id="28203-528">Shader Constant State</span></span> | <span data-ttu-id="28203-529">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-529">Type</span></span>            | <span data-ttu-id="28203-530">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-530">Values</span></span>                                       |
| <span data-ttu-id="28203-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="28203-531">PixelShaderConstant</span></span>   | <span data-ttu-id="28203-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="28203-533">matrice m x n di float; m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="28203-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="28203-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="28203-535">float4</span><span class="sxs-lookup"><span data-stu-id="28203-535">float4</span></span>          | <span data-ttu-id="28203-536">Un float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-536">One 4D float.</span></span>                                |
| <span data-ttu-id="28203-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="28203-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="28203-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="28203-538">float4x2</span></span>        | <span data-ttu-id="28203-539">Due float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="28203-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="28203-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="28203-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="28203-541">float4x3</span></span>        | <span data-ttu-id="28203-542">Tre float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="28203-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="28203-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="28203-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="28203-544">float4x4</span></span>        | <span data-ttu-id="28203-545">Quattro float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="28203-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="28203-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="28203-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="28203-548">matrice m x n di bool; m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="28203-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="28203-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="28203-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="28203-551">matrice m x n di int.</span><span class="sxs-lookup"><span data-stu-id="28203-551">m x n array of ints.</span></span> <span data-ttu-id="28203-552">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-552">m and n are optional.</span></span>   |
| <span data-ttu-id="28203-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="28203-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="28203-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="28203-555">matrice m x n di float.</span><span class="sxs-lookup"><span data-stu-id="28203-555">m x n array of floats.</span></span> <span data-ttu-id="28203-556">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-556">m and n are optional.</span></span> |
| <span data-ttu-id="28203-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="28203-557">VertexShaderConstant</span></span>  | <span data-ttu-id="28203-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="28203-559">matrice m x n di float.</span><span class="sxs-lookup"><span data-stu-id="28203-559">m x n array of floats.</span></span> <span data-ttu-id="28203-560">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-560">m and n are optional.</span></span> |
| <span data-ttu-id="28203-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="28203-561">VertexShaderConstant1</span></span> | <span data-ttu-id="28203-562">float4</span><span class="sxs-lookup"><span data-stu-id="28203-562">float4</span></span>          | <span data-ttu-id="28203-563">Un float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-563">One 4D float.</span></span>                                |
| <span data-ttu-id="28203-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="28203-564">VertexShaderConstant2</span></span> | <span data-ttu-id="28203-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="28203-565">float4x2</span></span>        | <span data-ttu-id="28203-566">Due float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="28203-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="28203-567">VertexShaderConstant3</span></span> | <span data-ttu-id="28203-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="28203-568">float4x3</span></span>        | <span data-ttu-id="28203-569">Tre float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="28203-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="28203-570">VertexShaderConstant4</span></span> | <span data-ttu-id="28203-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="28203-571">float4x4</span></span>        | <span data-ttu-id="28203-572">Quattro float 4D.</span><span class="sxs-lookup"><span data-stu-id="28203-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="28203-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="28203-573">VertexShaderConstantB</span></span> | <span data-ttu-id="28203-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="28203-575">matrice m x n di bool.</span><span class="sxs-lookup"><span data-stu-id="28203-575">m x n array of bools.</span></span> <span data-ttu-id="28203-576">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-576">m and n are optional.</span></span>  |
| <span data-ttu-id="28203-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="28203-577">VertexShaderConstantI</span></span> | <span data-ttu-id="28203-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="28203-579">matrice m x n di int.</span><span class="sxs-lookup"><span data-stu-id="28203-579">m x n array of ints.</span></span> <span data-ttu-id="28203-580">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-580">m and n are optional.</span></span>   |
| <span data-ttu-id="28203-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="28203-581">VertexShaderConstantF</span></span> | <span data-ttu-id="28203-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="28203-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="28203-583">matrice m x n di float.</span><span class="sxs-lookup"><span data-stu-id="28203-583">m x n array of floats.</span></span> <span data-ttu-id="28203-584">m e n sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="28203-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="28203-585">Stati di trama</span><span class="sxs-lookup"><span data-stu-id="28203-585">Texture States</span></span>

<span data-ttu-id="28203-586">Gli Stati di trama inizializzano le trame usate da multitexture Blender.</span><span class="sxs-lookup"><span data-stu-id="28203-586">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="28203-587">Stato trama</span><span class="sxs-lookup"><span data-stu-id="28203-587">Texture State</span></span> | <span data-ttu-id="28203-588">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-588">Type</span></span>    | <span data-ttu-id="28203-589">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-589">Values</span></span>                            |
| <span data-ttu-id="28203-590">Trama \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-590">Texture\[8\]</span></span>  | <span data-ttu-id="28203-591">trama</span><span class="sxs-lookup"><span data-stu-id="28203-591">texture</span></span> | <span data-ttu-id="28203-592">**Null** o un parametro texture.</span><span class="sxs-lookup"><span data-stu-id="28203-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="28203-593">Stati della fase trama</span><span class="sxs-lookup"><span data-stu-id="28203-593">Texture Stage States</span></span>

<span data-ttu-id="28203-594">Gli Stati della fase trama configurano le trame e le fasi di trama in Blender multitexture.</span><span class="sxs-lookup"><span data-stu-id="28203-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28203-595">Stato della fase trama</span><span class="sxs-lookup"><span data-stu-id="28203-595">Texture Stage State</span></span>        | <span data-ttu-id="28203-596">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-596">Type</span></span>  | <span data-ttu-id="28203-597">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-597">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="28203-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="28203-599">dword</span><span class="sxs-lookup"><span data-stu-id="28203-599">dword</span></span> | <span data-ttu-id="28203-600">Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il \_ prefisso D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="28203-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="28203-601">Vedere D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="28203-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="28203-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="28203-603">dword</span><span class="sxs-lookup"><span data-stu-id="28203-603">dword</span></span> | <span data-ttu-id="28203-604">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="28203-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="28203-605">Vedere D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="28203-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="28203-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="28203-607">dword</span><span class="sxs-lookup"><span data-stu-id="28203-607">dword</span></span> | <span data-ttu-id="28203-608">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="28203-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="28203-609">Vedere D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="28203-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="28203-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="28203-611">dword</span><span class="sxs-lookup"><span data-stu-id="28203-611">dword</span></span> | <span data-ttu-id="28203-612">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="28203-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="28203-613">Vedere D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="28203-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="28203-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="28203-615">dword</span><span class="sxs-lookup"><span data-stu-id="28203-615">dword</span></span> | <span data-ttu-id="28203-616">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="28203-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="28203-617">Vedere D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="28203-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="28203-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="28203-619">dword</span><span class="sxs-lookup"><span data-stu-id="28203-619">dword</span></span> | <span data-ttu-id="28203-620">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="28203-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="28203-621">Vedere D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="28203-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="28203-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="28203-623">dword</span><span class="sxs-lookup"><span data-stu-id="28203-623">dword</span></span> | <span data-ttu-id="28203-624">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="28203-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="28203-625">Vedere D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="28203-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="28203-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="28203-627">dword</span><span class="sxs-lookup"><span data-stu-id="28203-627">dword</span></span> | <span data-ttu-id="28203-628">Uguale a [**D3DTEXTUREOP**](./d3dtextureop.md) senza il \_ prefisso D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="28203-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="28203-629">Vedere D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="28203-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="28203-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="28203-631">float</span><span class="sxs-lookup"><span data-stu-id="28203-631">float</span></span> | <span data-ttu-id="28203-632">Gli stessi valori di D3DTSS \_ BUMPENVLSCALE senza il \_ prefisso D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="28203-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="28203-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="28203-634">float</span><span class="sxs-lookup"><span data-stu-id="28203-634">float</span></span> | <span data-ttu-id="28203-635">Gli stessi valori di D3DTSS \_ BUMPENVLOFFSET senza il \_ prefisso D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="28203-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="28203-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="28203-637">float</span><span class="sxs-lookup"><span data-stu-id="28203-637">float</span></span> | <span data-ttu-id="28203-638">Stessi valori di D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="28203-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="28203-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="28203-640">float</span><span class="sxs-lookup"><span data-stu-id="28203-640">float</span></span> | <span data-ttu-id="28203-641">Stessi valori di D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="28203-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="28203-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="28203-643">float</span><span class="sxs-lookup"><span data-stu-id="28203-643">float</span></span> | <span data-ttu-id="28203-644">Stessi valori di D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="28203-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="28203-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="28203-646">float</span><span class="sxs-lookup"><span data-stu-id="28203-646">float</span></span> | <span data-ttu-id="28203-647">Stessi valori di D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="28203-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="28203-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="28203-649">dword</span><span class="sxs-lookup"><span data-stu-id="28203-649">dword</span></span> | <span data-ttu-id="28203-650">Uguale a [D3DTA](d3dta.md) senza il \_ prefisso D3DTA.</span><span class="sxs-lookup"><span data-stu-id="28203-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="28203-651">Vedere D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="28203-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="28203-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="28203-653">dword</span><span class="sxs-lookup"><span data-stu-id="28203-653">dword</span></span> | <span data-ttu-id="28203-654">Gli stessi valori di D3DTSS \_ TEXCOORDINDEX senza il \_ prefisso D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="28203-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="28203-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="28203-656">dword</span><span class="sxs-lookup"><span data-stu-id="28203-656">dword</span></span> | <span data-ttu-id="28203-657">Stessi valori dei valori [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) senza il \_ prefisso D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="28203-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="28203-658">Vedere D3DTSS \_ TEXTURETRANSFORMFLAGS.</span><span class="sxs-lookup"><span data-stu-id="28203-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="28203-659">Stati di trasformazione</span><span class="sxs-lookup"><span data-stu-id="28203-659">Transform States</span></span>

<span data-ttu-id="28203-660">Impostare gli Stati di trasformazione per inizializzare matrici di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="28203-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="28203-661">Gli effetti utilizzano matrici trasposte per migliorare l'efficienza.</span><span class="sxs-lookup"><span data-stu-id="28203-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="28203-662">È possibile fornire matrici trasposte a un effetto oppure un effetto trasmetterà automaticamente le matrici prima di utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="28203-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28203-663">Stato trasformazione</span><span class="sxs-lookup"><span data-stu-id="28203-663">Transform State</span></span>       | <span data-ttu-id="28203-664">Tipo</span><span class="sxs-lookup"><span data-stu-id="28203-664">Type</span></span>     | <span data-ttu-id="28203-665">Valori</span><span class="sxs-lookup"><span data-stu-id="28203-665">Values</span></span>                                                                                                                          |
| <span data-ttu-id="28203-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="28203-666">ProjectionTransform</span></span>   | <span data-ttu-id="28203-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="28203-667">float4x4</span></span> | <span data-ttu-id="28203-668">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="28203-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="28203-669">Stessi valori della \_ proiezione D3DTS senza il \_ prefisso D3DTS.</span><span class="sxs-lookup"><span data-stu-id="28203-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="28203-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="28203-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="28203-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="28203-671">float4x4</span></span> | <span data-ttu-id="28203-672">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="28203-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="28203-673">Gli stessi valori di [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) senza il \_ prefisso D3DTS.</span><span class="sxs-lookup"><span data-stu-id="28203-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="28203-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="28203-674">ViewTransform</span></span>         | <span data-ttu-id="28203-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="28203-675">float4x4</span></span> | <span data-ttu-id="28203-676">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="28203-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="28203-677">Gli stessi valori della \_ vista D3DTS senza il \_ prefisso D3DTS.</span><span class="sxs-lookup"><span data-stu-id="28203-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="28203-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="28203-678">WorldTransform</span></span>        | <span data-ttu-id="28203-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="28203-679">float4x4</span></span> | <span data-ttu-id="28203-680">Matrice 4x4 di float.</span><span class="sxs-lookup"><span data-stu-id="28203-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="28203-681">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28203-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28203-682">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="28203-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
