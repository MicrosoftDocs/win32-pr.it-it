---
description: Un blocco di stato può essere usato per acquisire solo lo stato del vertice (vedere lo stato di salvataggio e ripristino di blocchi di stato (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Salvataggio degli Stati dei vertici con StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304379"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="84767-103">Salvataggio degli Stati dei vertici con StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="84767-103">Saving Vertex States With a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="84767-104">Un blocco di stato può essere usato per acquisire solo lo stato del vertice (vedere lo stato di [salvataggio e ripristino di blocchi di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="84767-104">A state block can be used to capture only vertex state (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="84767-105">Lo stato seguente è Vertex state:</span><span class="sxs-lookup"><span data-stu-id="84767-105">The following state is vertex state:</span></span>

-   <span data-ttu-id="84767-106">Stato di rendering vertici (vedere [pipeline Vertex: stato di rendering](#vertex-pipeline-render-state)).</span><span class="sxs-lookup"><span data-stu-id="84767-106">Vertex render state (see [Vertex Pipeline: Render State](#vertex-pipeline-render-state)).</span></span>
-   <span data-ttu-id="84767-107">Stato campionatore vertici (vedere [pipeline Vertex: stato campionatore](#vertex-pipeline-sampler-state)).</span><span class="sxs-lookup"><span data-stu-id="84767-107">Vertex sampler state (see [Vertex Pipeline: Sampler State](#vertex-pipeline-sampler-state)).</span></span>
-   <span data-ttu-id="84767-108">Stato trama vertice (vedere [pipeline Vertex: stato trama](#vertex-pipeline-texture-state)).</span><span class="sxs-lookup"><span data-stu-id="84767-108">Vertex texture state (see [Vertex Pipeline: Texture State](#vertex-pipeline-texture-state)).</span></span>
-   <span data-ttu-id="84767-109">I segmenti in modalità NPatch di [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="84767-109">The NPatch mode segments from [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>
-   <span data-ttu-id="84767-110">Ogni luce di [**IDirect3DDevice9:: selight**](/windows/desktop/api), nonché se la luce è abilitata con [**IDirect3DDevice9:: alleggerible**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="84767-110">Each light from [**IDirect3DDevice9::SetLight**](/windows/desktop/api), as well as whether or not the light is enabled with [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>
-   <span data-ttu-id="84767-111">Vertex shader corrente e ognuna delle costanti vertex shader.</span><span class="sxs-lookup"><span data-stu-id="84767-111">The current vertex shader and each of the vertex shader constants.</span></span>
-   <span data-ttu-id="84767-112">Per ogni flusso di vertici, archiviare il valore del divisore da [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="84767-112">For each vertex stream, store the divider value from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="84767-113">Dichiarazione del vertice corrente.</span><span class="sxs-lookup"><span data-stu-id="84767-113">The current vertex declaration.</span></span>

<span data-ttu-id="84767-114">Per acquisire lo stato del vertice con un blocco di stato, specificare D3DSBT \_ VERTEXSTATE quando si chiama [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="84767-114">To capture vertex state with a state block, specify D3DSBT\_VERTEXSTATE when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="vertex-pipeline-render-state"></a><span data-ttu-id="84767-115">Pipeline Vertex: stato di rendering</span><span class="sxs-lookup"><span data-stu-id="84767-115">Vertex Pipeline: Render State</span></span>

<span data-ttu-id="84767-116">Gli Stati di rendering del dispositivo influiscono sul comportamento di quasi tutte le parti della pipeline.</span><span class="sxs-lookup"><span data-stu-id="84767-116">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="84767-117">Gli Stati di rendering vengono impostati chiamando [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="84767-117">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="84767-118">Nella tabella seguente sono inclusi tutti gli Stati di rendering che configurano lo stato dei vertici:</span><span class="sxs-lookup"><span data-stu-id="84767-118">The following table includes all render states that set-up vertex state:</span></span>



| <span data-ttu-id="84767-119">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="84767-119">Render States</span></span>                           | <span data-ttu-id="84767-120">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="84767-120">Default Value</span></span>          |
|-----------------------------------------|------------------------|
| <span data-ttu-id="84767-121">\_CULLMODE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-121">D3DRS\_CULLMODE</span></span>                         | <span data-ttu-id="84767-122">D3DCULL \_ CCW</span><span class="sxs-lookup"><span data-stu-id="84767-122">D3DCULL\_CCW</span></span>           |
| <span data-ttu-id="84767-123">\_FogColor D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-123">D3DRS\_FOGCOLOR</span></span>                         | <span data-ttu-id="84767-124">0</span><span class="sxs-lookup"><span data-stu-id="84767-124">0</span></span>                      |
| <span data-ttu-id="84767-125">\_FOGTABLEMODE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-125">D3DRS\_FOGTABLEMODE</span></span>                     | <span data-ttu-id="84767-126">D3DFOG \_ None</span><span class="sxs-lookup"><span data-stu-id="84767-126">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="84767-127">\_FOGSTART D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-127">D3DRS\_FOGSTART</span></span>                         | <span data-ttu-id="84767-128">0</span><span class="sxs-lookup"><span data-stu-id="84767-128">0</span></span>                      |
| <span data-ttu-id="84767-129">\_FOGEND D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-129">D3DRS\_FOGEND</span></span>                           | <span data-ttu-id="84767-130">1</span><span class="sxs-lookup"><span data-stu-id="84767-130">1</span></span>                      |
| <span data-ttu-id="84767-131">\_FOGDENSITY D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-131">D3DRS\_FOGDENSITY</span></span>                       | <span data-ttu-id="84767-132">1</span><span class="sxs-lookup"><span data-stu-id="84767-132">1</span></span>                      |
| <span data-ttu-id="84767-133">\_RANGEFOGENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-133">D3DRS\_RANGEFOGENABLE</span></span>                   | <span data-ttu-id="84767-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="84767-134">**FALSE**</span></span>              |
| <span data-ttu-id="84767-135">\_Ambiente D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-135">D3DRS\_AMBIENT</span></span>                          | <span data-ttu-id="84767-136">0</span><span class="sxs-lookup"><span data-stu-id="84767-136">0</span></span>                      |
| <span data-ttu-id="84767-137">\_COLORVERTEX D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-137">D3DRS\_COLORVERTEX</span></span>                      | <span data-ttu-id="84767-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="84767-138">**TRUE**</span></span>               |
| <span data-ttu-id="84767-139">\_FOGVERTEXMODE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-139">D3DRS\_FOGVERTEXMODE</span></span>                    | <span data-ttu-id="84767-140">D3DFOG \_ None</span><span class="sxs-lookup"><span data-stu-id="84767-140">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="84767-141">Ritaglio D3DRS \_</span><span class="sxs-lookup"><span data-stu-id="84767-141">D3DRS\_CLIPPING</span></span>                         | <span data-ttu-id="84767-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="84767-142">**TRUE**</span></span>               |
| <span data-ttu-id="84767-143">\_Illuminazione D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-143">D3DRS\_LIGHTING</span></span>                         | <span data-ttu-id="84767-144">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="84767-144">**TRUE**</span></span>               |
| <span data-ttu-id="84767-145">\_LOCALVIEWER D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-145">D3DRS\_LOCALVIEWER</span></span>                      | <span data-ttu-id="84767-146">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="84767-146">**TRUE**</span></span>               |
| <span data-ttu-id="84767-147">\_EMISSIVEMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-147">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>           | <span data-ttu-id="84767-148">\_Materiale D3DMCS</span><span class="sxs-lookup"><span data-stu-id="84767-148">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="84767-149">\_AMBIENTMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-149">D3DRS\_AMBIENTMATERIALSOURCE</span></span>            | <span data-ttu-id="84767-150">\_Materiale D3DMCS</span><span class="sxs-lookup"><span data-stu-id="84767-150">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="84767-151">\_DIFFUSEMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-151">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>            | <span data-ttu-id="84767-152">\_COLOR1 D3DMCS</span><span class="sxs-lookup"><span data-stu-id="84767-152">D3DMCS\_COLOR1</span></span>         |
| <span data-ttu-id="84767-153">\_SPECULARMATERIALSOURCE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-153">D3DRS\_SPECULARMATERIALSOURCE</span></span>           | <span data-ttu-id="84767-154">\_Color2 D3DMCS</span><span class="sxs-lookup"><span data-stu-id="84767-154">D3DMCS\_COLOR2</span></span>         |
| <span data-ttu-id="84767-155">\_VERTEXBLEND D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-155">D3DRS\_VERTEXBLEND</span></span>                      | <span data-ttu-id="84767-156">\_Disabilitazione D3DVBF</span><span class="sxs-lookup"><span data-stu-id="84767-156">D3DVBF\_DISABLE</span></span>        |
| <span data-ttu-id="84767-157">\_CLIPPLANEENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-157">D3DRS\_CLIPPLANEENABLE</span></span>                  | <span data-ttu-id="84767-158">0</span><span class="sxs-lookup"><span data-stu-id="84767-158">0</span></span>                      |
| <span data-ttu-id="84767-159">\_POINTSIZE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-159">D3DRS\_POINTSIZE</span></span>                        | <span data-ttu-id="84767-160">Dipendente dal driver</span><span class="sxs-lookup"><span data-stu-id="84767-160">Driver dependent</span></span>       |
| <span data-ttu-id="84767-161">D3DRS \_ POINTSIZE \_ min</span><span class="sxs-lookup"><span data-stu-id="84767-161">D3DRS\_POINTSIZE\_MIN</span></span>                   | <span data-ttu-id="84767-162">1</span><span class="sxs-lookup"><span data-stu-id="84767-162">1</span></span>                      |
| <span data-ttu-id="84767-163">\_POINTSPRITEENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-163">D3DRS\_POINTSPRITEENABLE</span></span>                | <span data-ttu-id="84767-164">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="84767-164">**FALSE**</span></span>              |
| <span data-ttu-id="84767-165">\_POINTSCALEENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-165">D3DRS\_POINTSCALEENABLE</span></span>                 | <span data-ttu-id="84767-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="84767-166">**FALSE**</span></span>              |
| <span data-ttu-id="84767-167">D3DRS \_ POINTSCALE \_ A</span><span class="sxs-lookup"><span data-stu-id="84767-167">D3DRS\_POINTSCALE\_A</span></span>                    | <span data-ttu-id="84767-168">1</span><span class="sxs-lookup"><span data-stu-id="84767-168">1</span></span>                      |
| <span data-ttu-id="84767-169">D3DRS \_ POINTSCALE \_ B</span><span class="sxs-lookup"><span data-stu-id="84767-169">D3DRS\_POINTSCALE\_B</span></span>                    | <span data-ttu-id="84767-170">0</span><span class="sxs-lookup"><span data-stu-id="84767-170">0</span></span>                      |
| <span data-ttu-id="84767-171">D3DRS \_ POINTSCALE \_ C</span><span class="sxs-lookup"><span data-stu-id="84767-171">D3DRS\_POINTSCALE\_C</span></span>                    | <span data-ttu-id="84767-172">0</span><span class="sxs-lookup"><span data-stu-id="84767-172">0</span></span>                      |
| <span data-ttu-id="84767-173">\_MULTISAMPLEANTIALIAS D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-173">D3DRS\_MULTISAMPLEANTIALIAS</span></span>             | <span data-ttu-id="84767-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="84767-174">**TRUE**</span></span>               |
| <span data-ttu-id="84767-175">\_MULTISAMPLEMASK D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-175">D3DRS\_MULTISAMPLEMASK</span></span>                  | <span data-ttu-id="84767-176">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="84767-176">0xffffffff</span></span>             |
| <span data-ttu-id="84767-177">\_PATCHEDGESTYLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-177">D3DRS\_PATCHEDGESTYLE</span></span>                   | <span data-ttu-id="84767-178">D3DPATCHEDGE \_ discreto</span><span class="sxs-lookup"><span data-stu-id="84767-178">D3DPATCHEDGE\_DISCRETE</span></span> |
| <span data-ttu-id="84767-179">D3DRS \_ POINTSIZE \_ Max</span><span class="sxs-lookup"><span data-stu-id="84767-179">D3DRS\_POINTSIZE\_MAX</span></span>                   | <span data-ttu-id="84767-180">1</span><span class="sxs-lookup"><span data-stu-id="84767-180">1</span></span>                      |
| <span data-ttu-id="84767-181">\_INDEXEDVERTEXBLENDENABLE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-181">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>         | <span data-ttu-id="84767-182">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="84767-182">**FALSE**</span></span>              |
| <span data-ttu-id="84767-183">\_TWEENFACTOR D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-183">D3DRS\_TWEENFACTOR</span></span>                      | <span data-ttu-id="84767-184">0</span><span class="sxs-lookup"><span data-stu-id="84767-184">0</span></span>                      |
| <span data-ttu-id="84767-185">\_POSITIONDEGREE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-185">D3DRS\_POSITIONDEGREE</span></span>                   | <span data-ttu-id="84767-186">\_Cubi D3DDEGREE</span><span class="sxs-lookup"><span data-stu-id="84767-186">D3DDEGREE\_CUBIC</span></span>       |
| <span data-ttu-id="84767-187">\_NORMALDEGREE D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-187">D3DRS\_NORMALDEGREE</span></span>                     | <span data-ttu-id="84767-188">D3DDEGREE \_ lineare</span><span class="sxs-lookup"><span data-stu-id="84767-188">D3DDEGREE\_LINEAR</span></span>      |
| <span data-ttu-id="84767-189">\_MINTESSELLATIONLEVEL D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-189">D3DRS\_MINTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="84767-190">1</span><span class="sxs-lookup"><span data-stu-id="84767-190">1</span></span>                      |
| <span data-ttu-id="84767-191">\_MAXTESSELLATIONLEVEL D3DRS</span><span class="sxs-lookup"><span data-stu-id="84767-191">D3DRS\_MAXTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="84767-192">1</span><span class="sxs-lookup"><span data-stu-id="84767-192">1</span></span>                      |
| <span data-ttu-id="84767-193">D3DRS \_ ADAPTIVETESS \_ X</span><span class="sxs-lookup"><span data-stu-id="84767-193">D3DRS\_ADAPTIVETESS\_X</span></span>                  | <span data-ttu-id="84767-194">0</span><span class="sxs-lookup"><span data-stu-id="84767-194">0</span></span>                      |
| <span data-ttu-id="84767-195">D3DRS \_ ADAPTIVETESS \_ Y</span><span class="sxs-lookup"><span data-stu-id="84767-195">D3DRS\_ADAPTIVETESS\_Y</span></span>                  | <span data-ttu-id="84767-196">0</span><span class="sxs-lookup"><span data-stu-id="84767-196">0</span></span>                      |
| <span data-ttu-id="84767-197">D3DRS \_ ADAPTIVETESS \_ Z</span><span class="sxs-lookup"><span data-stu-id="84767-197">D3DRS\_ADAPTIVETESS\_Z</span></span>                  | <span data-ttu-id="84767-198">1</span><span class="sxs-lookup"><span data-stu-id="84767-198">1</span></span>                      |
| <span data-ttu-id="84767-199">D3DRS \_ ADAPTIVETESS \_ W</span><span class="sxs-lookup"><span data-stu-id="84767-199">D3DRS\_ADAPTIVETESS\_W</span></span>                  | <span data-ttu-id="84767-200">0</span><span class="sxs-lookup"><span data-stu-id="84767-200">0</span></span>                      |
| <span data-ttu-id="84767-201">D3DRS \_ ENABLEADAPTIVETESSELLATION "/></span><span class="sxs-lookup"><span data-stu-id="84767-201">D3DRS\_ENABLEADAPTIVETESSELLATION"/></span></span> | <span data-ttu-id="84767-202">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="84767-202">**FALSE**</span></span>              |



 

## <a name="vertex-pipeline-sampler-state"></a><span data-ttu-id="84767-203">Pipeline Vertex: stato campionatore</span><span class="sxs-lookup"><span data-stu-id="84767-203">Vertex Pipeline: Sampler State</span></span>

<span data-ttu-id="84767-204">Gli Stati del campionatore controllano argomenti correlati al campionamento, ad esempio le modalità di filtro, affiancamento e coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="84767-204">Sampler states control sampling related topics such as filtering, tiling, and texture coordinate address modes.</span></span> <span data-ttu-id="84767-205">Usare [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) per impostare lo stato del campionatore (incluso quello usato nell'unità mosaico per campionare le mappe di spostamento).</span><span class="sxs-lookup"><span data-stu-id="84767-205">Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) to set up the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="84767-206">Gli Stati del campionatore sono stati rinominati con un \_ prefisso "D3DSAMP" per abilitare il rilevamento degli errori in fase di compilazione durante il trasferimento da DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="84767-206">The sampler states have been renamed with a "D3DSAMP\_" prefix to enable compile time error detection when porting from DirectX 8.</span></span>

<span data-ttu-id="84767-207">La tabella seguente include tutti gli Stati del campionatore che configurano lo stato dei vertici:</span><span class="sxs-lookup"><span data-stu-id="84767-207">The following table includes all sampler states that set-up vertex state:</span></span>



| <span data-ttu-id="84767-208">Stati campionatore</span><span class="sxs-lookup"><span data-stu-id="84767-208">Sampler States</span></span>      | <span data-ttu-id="84767-209">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="84767-209">Default Value</span></span> |
|---------------------|---------------|
| <span data-ttu-id="84767-210">\_DMAPOFFSET D3DSAMP</span><span class="sxs-lookup"><span data-stu-id="84767-210">D3DSAMP\_DMAPOFFSET</span></span> | <span data-ttu-id="84767-211">256</span><span class="sxs-lookup"><span data-stu-id="84767-211">256</span></span>           |



 

## <a name="vertex-pipeline-texture-state"></a><span data-ttu-id="84767-212">Pipeline Vertex: stato trama</span><span class="sxs-lookup"><span data-stu-id="84767-212">Vertex Pipeline: Texture State</span></span>

<span data-ttu-id="84767-213">Gli Stati della trama controllano le operazioni di blending del Blender a più trame.</span><span class="sxs-lookup"><span data-stu-id="84767-213">Texture states control texture blending operations of the multi-texture blender.</span></span> <span data-ttu-id="84767-214">Usare [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) per impostare gli Stati della trama.</span><span class="sxs-lookup"><span data-stu-id="84767-214">Use [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) to set-up texture states.</span></span> <span data-ttu-id="84767-215">Usare [**IDirect3DDevice9:: Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per associare una trama a una fase del campionatore.</span><span class="sxs-lookup"><span data-stu-id="84767-215">Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to associate a texture with a sampler stage.</span></span>

<span data-ttu-id="84767-216">La tabella seguente include tutti gli Stati di trama che configurano lo stato dei vertici:</span><span class="sxs-lookup"><span data-stu-id="84767-216">The following table includes all the texture states that set-up vertex state:</span></span>



| <span data-ttu-id="84767-217">Stati di trama</span><span class="sxs-lookup"><span data-stu-id="84767-217">Texture States</span></span>                | <span data-ttu-id="84767-218">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="84767-218">Default Value</span></span>    |
|-------------------------------|------------------|
| <span data-ttu-id="84767-219">\_TEXCOORDINDEX D3DTSS</span><span class="sxs-lookup"><span data-stu-id="84767-219">D3DTSS\_TEXCOORDINDEX</span></span>         | <span data-ttu-id="84767-220">0</span><span class="sxs-lookup"><span data-stu-id="84767-220">0</span></span>                |
| <span data-ttu-id="84767-221">\_TEXTURETRANSFORMFLAGS D3DTSS</span><span class="sxs-lookup"><span data-stu-id="84767-221">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span> | <span data-ttu-id="84767-222">\_Disabilitazione D3DTTFF</span><span class="sxs-lookup"><span data-stu-id="84767-222">D3DTTFF\_DISABLE</span></span> |



 

<span data-ttu-id="84767-223">D3DTSS \_ TEXCOORDINDEX è uno stato di elaborazione Vertex della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="84767-223">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="84767-224">Se viene usato un vertex shader programmabile, questo stato viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="84767-224">If a programmable vertex shader is used, this state is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84767-225">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84767-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84767-226">Stato di salvataggio e ripristino del blocco di stato</span><span class="sxs-lookup"><span data-stu-id="84767-226">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
