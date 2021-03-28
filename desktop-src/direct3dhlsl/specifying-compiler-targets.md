---
title: Specifica delle destinazioni del compilatore
description: Qui sono elencate le destinazioni per i vari profili supportati da D3DCompile \ functions e dal compilatore HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399660"
---
# <a name="specifying-compiler-targets"></a><span data-ttu-id="f1ffd-103">Specifica delle destinazioni del compilatore</span><span class="sxs-lookup"><span data-stu-id="f1ffd-103">Specifying Compiler Targets</span></span>

<span data-ttu-id="f1ffd-104">È necessario specificare la destinazione dello shader, ovvero il set di funzionalità shader, per la compilazione quando si chiama la funzione [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)o [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="f1ffd-104">You need to specify the shader target — set of shader features — to compile against when you call the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2), or [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function.</span></span> <span data-ttu-id="f1ffd-105">Qui sono elencate le destinazioni per i vari profili supportati dalle funzioni **D3DCompile \*** e dal compilatore HLSL.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-105">Here we list the targets for various profiles that the **D3DCompile\*** functions and the HLSL compiler support.</span></span>

-   [<span data-ttu-id="f1ffd-106">Livelli di funzionalità Direct3D 11,0 e 11,1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-106">Direct3D 11.0 and 11.1 feature levels</span></span>](#direct3d-110-and-111-feature-levels)
-   [<span data-ttu-id="f1ffd-107">Livello funzionalità Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-107">Direct3D 10.1 feature level</span></span>](#direct3d-101-feature-level)
-   [<span data-ttu-id="f1ffd-108">Livello funzionalità Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-108">Direct3D 10.0 feature level</span></span>](#direct3d-100-feature-level)
-   [<span data-ttu-id="f1ffd-109">Livelli di funzionalità Direct3D 9,1, 9,2 e 9,3</span><span class="sxs-lookup"><span data-stu-id="f1ffd-109">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>](#direct3d-91-92-and-93-feature-levels)
-   [<span data-ttu-id="f1ffd-110">Modello di shader Direct3D 9 Legacy 3,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-110">Legacy Direct3D 9 Shader Model 3.0</span></span>](#legacy-direct3d-9-shader-model-30)
-   [<span data-ttu-id="f1ffd-111">Modello di shader Direct3D 9 Legacy 2,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-111">Legacy Direct3D 9 Shader Model 2.0</span></span>](#legacy-direct3d-9-shader-model-20)
-   [<span data-ttu-id="f1ffd-112">Modello 1. x legacy Direct3D 9 shader</span><span class="sxs-lookup"><span data-stu-id="f1ffd-112">Legacy Direct3D 9 Shader Model 1.x</span></span>](#legacy-direct3d-9-shader-model-1x)
-   [<span data-ttu-id="f1ffd-113">Effetti legacy</span><span class="sxs-lookup"><span data-stu-id="f1ffd-113">Legacy Effects</span></span>](#legacy-effects)
-   [<span data-ttu-id="f1ffd-114">Note</span><span class="sxs-lookup"><span data-stu-id="f1ffd-114">Notes</span></span>](#notes)
-   [<span data-ttu-id="f1ffd-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1ffd-115">Related topics</span></span>](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a><span data-ttu-id="f1ffd-116">Livelli di funzionalità Direct3D 11,0 e 11,1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-116">Direct3D 11.0 and 11.1 feature levels</span></span>

<span data-ttu-id="f1ffd-117">Di seguito sono riportate le destinazioni dello shader supportate dai [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 11,0 e 11,1.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-117">Here are the shader targets that Direct3D 11.0 and 11.1 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>



| <span data-ttu-id="f1ffd-118">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-118">Target</span></span>   | <span data-ttu-id="f1ffd-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-119">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ffd-120">cs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-120">cs\_5\_0</span></span> | <span data-ttu-id="f1ffd-121">DirectCompute 5,0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-121">DirectCompute 5.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))</span></span>                              |
| <span data-ttu-id="f1ffd-122">DS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-122">ds\_5\_0</span></span> | [<span data-ttu-id="f1ffd-123">Domain shader</span><span class="sxs-lookup"><span data-stu-id="f1ffd-123">Domain shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| <span data-ttu-id="f1ffd-124">GS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-124">gs\_5\_0</span></span> | <span data-ttu-id="f1ffd-125">[Geometria Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-125">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="f1ffd-126">HS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-126">hs\_5\_0</span></span> | [<span data-ttu-id="f1ffd-127">Hull shader</span><span class="sxs-lookup"><span data-stu-id="f1ffd-127">Hull shader</span></span>](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| <span data-ttu-id="f1ffd-128">PS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-128">ps\_5\_0</span></span> | <span data-ttu-id="f1ffd-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-129">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="f1ffd-130">vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-130">vs\_5\_0</span></span> | <span data-ttu-id="f1ffd-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-131">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-101-feature-level"></a><span data-ttu-id="f1ffd-132">Livello funzionalità Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-132">Direct3D 10.1 feature level</span></span>

<span data-ttu-id="f1ffd-133">Di seguito sono riportate le destinazioni dello shader supportate dal [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-133">Here are the shader targets that the Direct3D 10.1 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="f1ffd-134">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-134">Target</span></span>   | <span data-ttu-id="f1ffd-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-135">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ffd-136">cs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-136">cs\_4\_1</span></span> | <span data-ttu-id="f1ffd-137">DirectCompute 4,1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="f1ffd-137">DirectCompute 4.1 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="f1ffd-138">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-138">gs\_4\_1</span></span> | <span data-ttu-id="f1ffd-139">[Geometria Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-139">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="f1ffd-140">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-140">ps\_4\_1</span></span> | <span data-ttu-id="f1ffd-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-141">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="f1ffd-142">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-142">vs\_4\_1</span></span> | <span data-ttu-id="f1ffd-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-143">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-100-feature-level"></a><span data-ttu-id="f1ffd-144">Livello funzionalità Direct3D 10,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-144">Direct3D 10.0 feature level</span></span>

<span data-ttu-id="f1ffd-145">Di seguito sono riportate le destinazioni dello shader supportate dal [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-145">Here are the shader targets that the Direct3D 10.0 [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) supports.</span></span>



| <span data-ttu-id="f1ffd-146">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-146">Target</span></span>   | <span data-ttu-id="f1ffd-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-147">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ffd-148">cs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-148">cs\_4\_0</span></span> | <span data-ttu-id="f1ffd-149">DirectCompute 4,0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹</span><span class="sxs-lookup"><span data-stu-id="f1ffd-149">DirectCompute 4.0 ([compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹</span></span>                             |
| <span data-ttu-id="f1ffd-150">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-150">gs\_4\_0</span></span> | <span data-ttu-id="f1ffd-151">[Geometria Shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-151">[Geometry shader](/previous-versions//bb205146(v=vs.85))</span></span> |
| <span data-ttu-id="f1ffd-152">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-152">ps\_4\_0</span></span> | <span data-ttu-id="f1ffd-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-153">[Pixel shader](/previous-versions//bb205146(v=vs.85))</span></span>          |
| <span data-ttu-id="f1ffd-154">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-154">vs\_4\_0</span></span> | <span data-ttu-id="f1ffd-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1ffd-155">[Vertex shader](/previous-versions//bb205146(v=vs.85))</span></span>       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a><span data-ttu-id="f1ffd-156">Livelli di funzionalità Direct3D 9,1, 9,2 e 9,3</span><span class="sxs-lookup"><span data-stu-id="f1ffd-156">Direct3D 9.1, 9.2, and 9.3 feature levels</span></span>

<span data-ttu-id="f1ffd-157">Di seguito sono riportate le destinazioni dello shader supportate dai [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 e 9,3.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-157">Here are the shader targets that Direct3D 9.1, 9.2 and 9.3 [feature levels](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) support.</span></span>

> [!Note]  
> <span data-ttu-id="f1ffd-158">Quando si usano i \* \_ \_ profili dello \_ shader HLSL a 4 0 di livello \_ 9 \_ , si usano in modo implicito i profili [Shader Model 2. x](dx-graphics-hlsl-sm2.md) per supportare l'hardware compatibile con Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-158">When you use the \*\_4\_0\_level\_9\_x HLSL shader profiles, you implicitly use of the [Shader Model 2.x](dx-graphics-hlsl-sm2.md) profiles to support Direct3D 9 capable hardware.</span></span> <span data-ttu-id="f1ffd-159">I profili Shader Model 2. x supportano un comportamento di controllo di flusso più limitato rispetto ai profili [4. x](dx-graphics-hlsl-sm4.md) e successivi del modello shader.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-159">Shader Model 2.x profiles support more limited flow control behavior than the [Shader Model 4.x](dx-graphics-hlsl-sm4.md) and later profiles.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f1ffd-160">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-160">Target</span></span></th>
<th><span data-ttu-id="f1ffd-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f1ffd-162">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-162">ps_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="f1ffd-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) per 9,1 e 9,2 (limiti simili a ps_2_0)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-163">[Pixel shader](/previous-versions//bb205146(v=vs.85)) for 9.1 and 9.2 (similar limits to ps_2_0)</span></span>
<ul>
<li><span data-ttu-id="f1ffd-164">64 istruzioni di trama aritmetiche e 32</span><span class="sxs-lookup"><span data-stu-id="f1ffd-164">64 arithmetic and 32 texture instructions</span></span></li>
<li><span data-ttu-id="f1ffd-165">12 registri temporanei</span><span class="sxs-lookup"><span data-stu-id="f1ffd-165">12 temporary registers</span></span></li>
<li><span data-ttu-id="f1ffd-166">4 livelli di letture dipendenti</span><span class="sxs-lookup"><span data-stu-id="f1ffd-166">4 levels of dependent reads</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1ffd-167">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="f1ffd-167">ps_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="f1ffd-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> per 9,3 (limiti simili a ps_2_x ² con funzionalità shader aggiuntive)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-168"><a href="/previous-versions//bb205146(v=vs.85)">Pixel shader</a> for 9.3 (similar limits to ps_2_x² with additional shader features)</span></span>
<ul>
<li><span data-ttu-id="f1ffd-169">512 istruzioni</span><span class="sxs-lookup"><span data-stu-id="f1ffd-169">512 instructions</span></span></li>
<li><span data-ttu-id="f1ffd-170">32 registri temporanei</span><span class="sxs-lookup"><span data-stu-id="f1ffd-170">32 temporary registers</span></span></li>
<li><span data-ttu-id="f1ffd-171">Controllo di flusso statico (profondità massima di 4)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-171">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="f1ffd-172">Controllo dinamico del flusso (profondità massima di 24)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-172">Dynamic flow control (max depth of 24)</span></span></li>
<li><span data-ttu-id="f1ffd-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="f1ffd-173">D3DPS20CAPS_ARBITRARYSWIZZLE</span></span></li>
<li><span data-ttu-id="f1ffd-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="f1ffd-174">D3DPS20CAPS_GRADIENTINSTRUCTIONS</span></span></li>
<li><span data-ttu-id="f1ffd-175">D3DPS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="f1ffd-175">D3DPS20CAPS_PREDICATION</span></span></li>
<li><span data-ttu-id="f1ffd-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="f1ffd-176">D3DPS20CAPS_NODEPENDENTREADLIMIT</span></span></li>
<li><span data-ttu-id="f1ffd-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="f1ffd-177">D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f1ffd-178">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-178">vs_4_0_level_9_1</span></span></td>
<td><span data-ttu-id="f1ffd-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> per 9,1 e 9,2 (simile a VS_2_0)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-179"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.1 and 9.2 (similar to vs_2_0)</span></span>
<ul>
<li><span data-ttu-id="f1ffd-180">256 istruzioni</span><span class="sxs-lookup"><span data-stu-id="f1ffd-180">256 instructions</span></span></li>
<li><span data-ttu-id="f1ffd-181">12 registri temporanei</span><span class="sxs-lookup"><span data-stu-id="f1ffd-181">12 temporary registers</span></span></li>
<li><span data-ttu-id="f1ffd-182">Controllo di flusso statico (profondità massima di 1)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-182">Static flow control (max depth of 1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f1ffd-183">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="f1ffd-183">vs_4_0_level_9_3</span></span></td>
<td><span data-ttu-id="f1ffd-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> per 9,3 (simile a vs_2_a ² con funzionalità e istanze shader aggiuntive)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-184"><a href="/previous-versions//bb205146(v=vs.85)">Vertex shader</a> for 9.3 (similar to vs_2_a² with additional shader features and instancing)</span></span>
<ul>
<li><span data-ttu-id="f1ffd-185">256 istruzioni</span><span class="sxs-lookup"><span data-stu-id="f1ffd-185">256 instructions</span></span></li>
<li><span data-ttu-id="f1ffd-186">32 registri temporanei</span><span class="sxs-lookup"><span data-stu-id="f1ffd-186">32 temporary registers</span></span></li>
<li><span data-ttu-id="f1ffd-187">Controllo di flusso statico (profondità massima di 4)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-187">Static flow control (max depth of 4)</span></span></li>
<li><span data-ttu-id="f1ffd-188">D3DVS20CAPS_PREDICATION</span><span class="sxs-lookup"><span data-stu-id="f1ffd-188">D3DVS20CAPS_PREDICATION</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a><span data-ttu-id="f1ffd-189">Modello di shader Direct3D 9 Legacy 3,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-189">Legacy Direct3D 9 Shader Model 3.0</span></span>

<span data-ttu-id="f1ffd-190">Di seguito sono riportate le destinazioni shader per il modello di shader Direct3D 9 Legacy 3,0 ³.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-190">Here are the shader targets for legacy Direct3D 9 shader model 3.0³.</span></span>



| <span data-ttu-id="f1ffd-191">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-191">Target</span></span>    | <span data-ttu-id="f1ffd-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-192">Description</span></span>                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ffd-193">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-193">ps\_3\_0</span></span>  | <span data-ttu-id="f1ffd-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-194">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>               |
| <span data-ttu-id="f1ffd-195">PS \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1ffd-195">ps\_3\_sw</span></span> | <span data-ttu-id="f1ffd-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3,0 (software)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-196">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span>    |
| <span data-ttu-id="f1ffd-197">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-197">vs\_3\_0</span></span>  | <span data-ttu-id="f1ffd-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-198">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0</span></span>            |
| <span data-ttu-id="f1ffd-199">Visual Studio \_ 3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1ffd-199">vs\_3\_sw</span></span> | <span data-ttu-id="f1ffd-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3,0 (software)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-200">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 3.0 (software)</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-20"></a><span data-ttu-id="f1ffd-201">Modello di shader Direct3D 9 Legacy 2,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-201">Legacy Direct3D 9 Shader Model 2.0</span></span>

<span data-ttu-id="f1ffd-202">Di seguito sono riportate le destinazioni shader per il modello di shader Direct3D 9 Legacy 2,0 ³.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-202">Here are the shader targets for legacy Direct3D 9 shader model 2.0³.</span></span>



| <span data-ttu-id="f1ffd-203">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-203">Target</span></span>    | <span data-ttu-id="f1ffd-204">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-204">Description</span></span>                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ffd-205">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-205">ps\_2\_0</span></span>  | <span data-ttu-id="f1ffd-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-206">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>             |
| <span data-ttu-id="f1ffd-207">PS \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="f1ffd-207">ps\_2\_a</span></span>  | <span data-ttu-id="f1ffd-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="f1ffd-208">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>              |
| <span data-ttu-id="f1ffd-209">PS \_ 2 \_ b</span><span class="sxs-lookup"><span data-stu-id="f1ffd-209">ps\_2\_b</span></span>  | <span data-ttu-id="f1ffd-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2B</span><span class="sxs-lookup"><span data-stu-id="f1ffd-210">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2b</span></span>              |
| <span data-ttu-id="f1ffd-211">PS \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1ffd-211">ps\_2\_sw</span></span> | <span data-ttu-id="f1ffd-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2,0 software</span><span class="sxs-lookup"><span data-stu-id="f1ffd-212">[Pixel shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span>    |
| <span data-ttu-id="f1ffd-213">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-213">vs\_2\_0</span></span>  | <span data-ttu-id="f1ffd-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-214">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0</span></span>          |
| <span data-ttu-id="f1ffd-215">vs \_ 2 \_ a</span><span class="sxs-lookup"><span data-stu-id="f1ffd-215">vs\_2\_a</span></span>  | <span data-ttu-id="f1ffd-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span><span class="sxs-lookup"><span data-stu-id="f1ffd-216">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2a</span></span>           |
| <span data-ttu-id="f1ffd-217">vs \_ 2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1ffd-217">vs\_2\_sw</span></span> | <span data-ttu-id="f1ffd-218">Software [vertex shader](/previous-versions//bb205146(v=vs.85)) 2,0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-218">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 2.0 software</span></span> |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a><span data-ttu-id="f1ffd-219">Modello 1. x legacy Direct3D 9 shader</span><span class="sxs-lookup"><span data-stu-id="f1ffd-219">Legacy Direct3D 9 Shader Model 1.x</span></span>

<span data-ttu-id="f1ffd-220">Di seguito sono riportate le destinazioni dello shader per la versione 1. x precedente di Direct3D 9 shader ⁴.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-220">Here are the shader targets for legacy Direct3D 9 shader model 1.x⁴.</span></span>



| <span data-ttu-id="f1ffd-221">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-221">Target</span></span>   | <span data-ttu-id="f1ffd-222">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-222">Description</span></span>                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ffd-223">TX \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-223">tx\_1\_0</span></span> | <span data-ttu-id="f1ffd-224">Profilo shader texture che usa le funzioni ⁵ di D3DX9 legacy [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) e [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx)</span><span class="sxs-lookup"><span data-stu-id="f1ffd-224">Texture shader profile that legacy D3DX9⁵ functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) and [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use</span></span> |
| <span data-ttu-id="f1ffd-225">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-225">vs\_1\_1</span></span> | <span data-ttu-id="f1ffd-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1,1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-226">[Vertex shader](/previous-versions//bb205146(v=vs.85)) 1.1</span></span>                                                            |



 

## <a name="legacy-effects"></a><span data-ttu-id="f1ffd-227">Effetti legacy</span><span class="sxs-lookup"><span data-stu-id="f1ffd-227">Legacy Effects</span></span>

<span data-ttu-id="f1ffd-228">Ecco le destinazioni degli effetti degli effetti legacy.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-228">Here are the effect targets for legacy effects.</span></span>



| <span data-ttu-id="f1ffd-229">Destinazione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-229">Target</span></span>   | <span data-ttu-id="f1ffd-230">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ffd-230">Description</span></span>                               |
|----------|-------------------------------------------|
| <span data-ttu-id="f1ffd-231">FX \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-231">fx\_2\_0</span></span> | <span data-ttu-id="f1ffd-232">Effetti (FX) per Direct3D 9 in D3DX9 ⁵</span><span class="sxs-lookup"><span data-stu-id="f1ffd-232">Effects (FX) for Direct3D 9 in D3DX9⁵</span></span>     |
| <span data-ttu-id="f1ffd-233">FX \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-233">fx\_4\_0</span></span> | <span data-ttu-id="f1ffd-234">Effetti (FX) per Direct3D 10,0 in D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="f1ffd-234">Effects (FX) for Direct3D 10.0 in D3DX10⁵</span></span> |
| <span data-ttu-id="f1ffd-235">FX \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f1ffd-235">fx\_4\_1</span></span> | <span data-ttu-id="f1ffd-236">Effetti (FX) per Direct3D 10,1 in D3DX10 ⁵</span><span class="sxs-lookup"><span data-stu-id="f1ffd-236">Effects (FX) for Direct3D 10.1 in D3DX10⁵</span></span> |
| <span data-ttu-id="f1ffd-237">FX \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1ffd-237">fx\_5\_0</span></span> | <span data-ttu-id="f1ffd-238">Effetti (FX) per Direct3D 11 ⁵</span><span class="sxs-lookup"><span data-stu-id="f1ffd-238">Effects (FX) for Direct3D 11⁵</span></span>             |



 

## <a name="notes"></a><span data-ttu-id="f1ffd-239">Note</span><span class="sxs-lookup"><span data-stu-id="f1ffd-239">Notes</span></span>

<span data-ttu-id="f1ffd-240">Di seguito sono riportate alcune note a cui fanno riferimento le sezioni precedenti:</span><span class="sxs-lookup"><span data-stu-id="f1ffd-240">Here are some notes that the preceding sections refer to:</span></span>

1.  <span data-ttu-id="f1ffd-241">i dispositivi con [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 e 10,1 possono facoltativamente supportare DirectCompute.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-241">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 and 10.1 devices can optionally support DirectCompute.</span></span> <span data-ttu-id="f1ffd-242">Per verificare il supporto, utilizzare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con le [**\_ \_ \_ \_ \_ Opzioni hardware della funzionalità d3d11 D3D10 X**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="f1ffd-242">To verify support, use [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).</span></span>
2.  <span data-ttu-id="f1ffd-243">il [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 richiede in modo efficace l'hardware che soddisfa i requisiti per il [3,0 modello di shader Direct3D 9 legacy](#legacy-direct3d-9-shader-model-30), ma questo livello di funzionalità non usa \_ destinazioni vs 3 \_ 0 o PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-243">[feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 effectively requires hardware that complies with the requirements for [legacy Direct3D 9 shader model 3.0](#legacy-direct3d-9-shader-model-30), but this feature level does not make use of vs\_3\_0 or ps\_3\_0 targets.</span></span>
3.  <span data-ttu-id="f1ffd-244">Usare i modelli di shader Direct3D 9 legacy con l'API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-244">Only use legacy Direct3D 9 shader models with the Direct3D 9 API.</span></span> <span data-ttu-id="f1ffd-245">Usare invece i profili 9. x con l'API Direct3D 10. x e 11. x.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-245">Instead, use the 9.x profiles with the Direct3D 10.x and 11.x API.</span></span>
4.  <span data-ttu-id="f1ffd-246">Le funzioni HLSL shader **D3DCompile \*** correnti non supportano gli shader Legacy 1. x pixel.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-246">The current HLSL shader **D3DCompile\*** functions don't support legacy 1.x pixel shaders.</span></span> <span data-ttu-id="f1ffd-247">L'ultima versione di HLSL per il supporto di queste destinazioni è stata D3DX9 nella versione ottobre 2006 di DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-247">The last version of HLSL to support these targets was D3DX9 in the October 2006 release of the DirectX SDK.</span></span>
5.  <span data-ttu-id="f1ffd-248">Tutte le versioni di D3DX e DirectX SDK sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="f1ffd-248">All versions of D3DX and the DirectX SDK are deprecated.</span></span> <span data-ttu-id="f1ffd-249">Per ulteriori informazioni, vedere [la pagina relativa alla posizione di DirectX SDK](/windows/desktop/directx-sdk--august-2009-).</span><span class="sxs-lookup"><span data-stu-id="f1ffd-249">For more info, see [Where is the DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1ffd-250">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1ffd-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1ffd-251">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="f1ffd-251">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 