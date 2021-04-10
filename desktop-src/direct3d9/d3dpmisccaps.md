---
description: Flag di funzionalità primitive del driver varie.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225732"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="0e797-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="0e797-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="0e797-104">Flag di funzionalità primitive del driver varie.</span><span class="sxs-lookup"><span data-stu-id="0e797-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e797-105">#definire</span><span class="sxs-lookup"><span data-stu-id="0e797-105">#define</span></span></td>
<td><span data-ttu-id="0e797-106">Valore</span><span class="sxs-lookup"><span data-stu-id="0e797-106">Value</span></span></td>
<td><span data-ttu-id="0e797-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e797-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="0e797-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="0e797-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="0e797-109">0x00000002L</span></span></td>
<td><span data-ttu-id="0e797-110">Il dispositivo può abilitare e disabilitare la modifica del buffer di profondità sulle operazioni pixel.</span><span class="sxs-lookup"><span data-stu-id="0e797-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="0e797-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="0e797-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="0e797-112">0x00000010L</span></span></td>
<td><span data-ttu-id="0e797-113">Il driver non esegue l'abbattimento dei triangoli.</span><span class="sxs-lookup"><span data-stu-id="0e797-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="0e797-114">Corrisponde al membro D3DCULL_NONE del tipo enumerato <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0e797-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="0e797-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="0e797-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="0e797-116">0x00000020L</span></span></td>
<td><span data-ttu-id="0e797-117">Il driver supporta l'abbattimento di triangolo in senso orario attraverso lo stato D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="0e797-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="0e797-118">(Si applica solo alle primitive triangolari). Questo flag corrisponde al membro D3DCULL_CW del tipo enumerato <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0e797-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="0e797-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="0e797-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="0e797-120">0x00000040L</span></span></td>
<td><span data-ttu-id="0e797-121">Il driver supporta l'eliminazione in senso antiorario tramite lo stato D3DRS_CULLMODE.</span><span class="sxs-lookup"><span data-stu-id="0e797-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="0e797-122">(Si applica solo alle primitive triangolari). Questo flag corrisponde al membro D3DCULL_CCW del tipo enumerato <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="0e797-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="0e797-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="0e797-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="0e797-124">0x00000100L</span></span></td>
<td><span data-ttu-id="0e797-125">Il dispositivo supporta le Scritture per canale per il buffer dei colori della destinazione di rendering tramite lo stato D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="0e797-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="0e797-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="0e797-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="0e797-127">0x00000200L</span></span></td>
<td><span data-ttu-id="0e797-128">Il dispositivo Ritaglia correttamente i punti ridimensionati di dimensioni maggiori di 1,0 ai piani di ritaglio definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0e797-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="0e797-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="0e797-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="0e797-130">0x00000200L</span></span></td>
<td><span data-ttu-id="0e797-131">I clip del dispositivo vengono ritagliate primitive dei vertici.</span><span class="sxs-lookup"><span data-stu-id="0e797-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="0e797-132">Specificare D3DUSAGE_DONOTCLIP quando la pipeline non deve eseguire alcun ritaglio.</span><span class="sxs-lookup"><span data-stu-id="0e797-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="0e797-133">In tal caso, potrebbe essere necessario eseguire il ritaglio software aggiuntivo in fase di estrazione, in modo che il buffer dei vertici si trovi nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="0e797-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="0e797-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="0e797-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="0e797-135">0x00000400L</span></span></td>
<td><span data-ttu-id="0e797-136">Il dispositivo supporta <a href="d3dta.md">D3DTA</a> per il registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="0e797-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="0e797-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="0e797-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="0e797-138">0x00000800L</span></span></td>
<td><span data-ttu-id="0e797-139">Il dispositivo supporta operazioni di fusione alfa diverse da D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="0e797-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="0e797-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="0e797-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="0e797-141">0x00000100L</span></span></td>
<td><span data-ttu-id="0e797-142">Dispositivo di riferimento che non esegue il rendering.</span><span class="sxs-lookup"><span data-stu-id="0e797-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="0e797-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="0e797-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="0e797-144">0x00004000L</span></span></td>
<td><span data-ttu-id="0e797-145">Il dispositivo supporta maschere di scrittura indipendenti per più trame di elementi o più destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="0e797-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="0e797-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="0e797-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="0e797-147">0x00008000L</span></span></td>
<td><span data-ttu-id="0e797-148">Il dispositivo supporta le costanti per fase.</span><span class="sxs-lookup"><span data-stu-id="0e797-148">Device supports per-stage constants.</span></span> <span data-ttu-id="0e797-149">Vedere D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0e797-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="0e797-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="0e797-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="0e797-151">0x00200000L</span></span></td>
<td><span data-ttu-id="0e797-152">Il dispositivo supporta la conversione a sRGB dopo la fusione.</span><span class="sxs-lookup"><span data-stu-id="0e797-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0e797-153">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="0e797-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="0e797-154">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="0e797-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="0e797-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="0e797-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="0e797-156">0x00010000L</span></span></td>
<td><span data-ttu-id="0e797-157">Il dispositivo supporta la nebbia separata e l'alfa speculare.</span><span class="sxs-lookup"><span data-stu-id="0e797-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="0e797-158">Molti dispositivi usano il canale alfa speculare per archiviare il fattore di nebbia.</span><span class="sxs-lookup"><span data-stu-id="0e797-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="0e797-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="0e797-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="0e797-160">0x00020000L</span></span></td>
<td><span data-ttu-id="0e797-161">Il dispositivo supporta impostazioni di Blend separate per il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="0e797-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="0e797-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="0e797-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="0e797-163">0x00040000L</span></span></td>
<td><span data-ttu-id="0e797-164">Il dispositivo supporta profondità di bit diverse per più destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="0e797-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0e797-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="0e797-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="0e797-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="0e797-166">0x00080000L</span></span></td>
<td><span data-ttu-id="0e797-167">Il dispositivo supporta operazioni post-pixel shader per più destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="0e797-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0e797-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="0e797-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="0e797-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="0e797-169">0x00100000L</span></span></td>
<td><span data-ttu-id="0e797-170">I dispositivi bloccano il fattore di Blend di nebbia per vertice.</span><span class="sxs-lookup"><span data-stu-id="0e797-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0e797-171">Queste costanti vengono usate dal membro PrimitiveMiscCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="0e797-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="0e797-172">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="0e797-172">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="0e797-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e797-173">Header</span></span>                   | <span data-ttu-id="0e797-174">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="0e797-174">d3d9caps.h</span></span> |
| <span data-ttu-id="0e797-175">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="0e797-175">Minimum operating system</span></span> | <span data-ttu-id="0e797-176">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0e797-176">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0e797-177">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e797-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e797-178">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="0e797-178">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
