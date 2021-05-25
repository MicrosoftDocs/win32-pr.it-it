---
description: Flag di funzionalità primitive del driver vari.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4ace0b9070d158769e22e02a759545b1bf7785
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343136"
---
# <a name="d3dpmisccaps"></a><span data-ttu-id="aaac2-103">D3DPMISCCAPS</span><span class="sxs-lookup"><span data-stu-id="aaac2-103">D3DPMISCCAPS</span></span>

<span data-ttu-id="aaac2-104">Flag di funzionalità primitive del driver vari.</span><span class="sxs-lookup"><span data-stu-id="aaac2-104">Miscellaneous driver primitive capability flags.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aaac2-105">#Definire</span><span class="sxs-lookup"><span data-stu-id="aaac2-105">#define</span></span></td>
<td><span data-ttu-id="aaac2-106">Valore</span><span class="sxs-lookup"><span data-stu-id="aaac2-106">Value</span></span></td>
<td><span data-ttu-id="aaac2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aaac2-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-108">D3DPMISCCAPS_MASKZ</span><span class="sxs-lookup"><span data-stu-id="aaac2-108">D3DPMISCCAPS_MASKZ</span></span></td>
<td><span data-ttu-id="aaac2-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="aaac2-109">0x00000002L</span></span></td>
<td><span data-ttu-id="aaac2-110">Il dispositivo può abilitare e disabilitare la modifica del buffer di profondità nelle operazioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="aaac2-110">Device can enable and disable modification of the depth buffer on pixel operations.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-111">D3DPMISCCAPS_CULLNONE</span><span class="sxs-lookup"><span data-stu-id="aaac2-111">D3DPMISCCAPS_CULLNONE</span></span></td>
<td><span data-ttu-id="aaac2-112">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="aaac2-112">0x00000010L</span></span></td>
<td><span data-ttu-id="aaac2-113">Il driver non esegue il culling del triangolo.</span><span class="sxs-lookup"><span data-stu-id="aaac2-113">The driver does not perform triangle culling.</span></span> <span data-ttu-id="aaac2-114">Corrisponde al membro D3DCULL_NONE del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerato D3DCULL.</strong></a></span><span class="sxs-lookup"><span data-stu-id="aaac2-114">This corresponds to the D3DCULL_NONE member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-115">D3DPMISCCAPS_CULLCW</span><span class="sxs-lookup"><span data-stu-id="aaac2-115">D3DPMISCCAPS_CULLCW</span></span></td>
<td><span data-ttu-id="aaac2-116">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="aaac2-116">0x00000020L</span></span></td>
<td><span data-ttu-id="aaac2-117">Il driver supporta l'culling triangolare in senso orario attraverso D3DRS_CULLMODE stato.</span><span class="sxs-lookup"><span data-stu-id="aaac2-117">The driver supports clockwise triangle culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="aaac2-118">Si applica solo alle primitive di triangolo. Questo flag corrisponde al D3DCULL_CW del <a href="/windows/desktop/direct3d9/d3dcull"><strong>tipo enumerato D3DCULL.</strong></a></span><span class="sxs-lookup"><span data-stu-id="aaac2-118">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-119">D3DPMISCCAPS_CULLCCW</span><span class="sxs-lookup"><span data-stu-id="aaac2-119">D3DPMISCCAPS_CULLCCW</span></span></td>
<td><span data-ttu-id="aaac2-120">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="aaac2-120">0x00000040L</span></span></td>
<td><span data-ttu-id="aaac2-121">Il driver supporta l'culling in senso antiorario attraverso lo D3DRS_CULLMODE stato.</span><span class="sxs-lookup"><span data-stu-id="aaac2-121">The driver supports counterclockwise culling through the D3DRS_CULLMODE state.</span></span> <span data-ttu-id="aaac2-122">Si applica solo alle primitive di triangolo. Questo flag corrisponde al D3DCULL_CCW del tipo <a href="/windows/desktop/direct3d9/d3dcull"><strong>enumerato D3DCULL.</strong></a></span><span class="sxs-lookup"><span data-stu-id="aaac2-122">(This applies only to triangle primitives.) This flag corresponds to the D3DCULL_CCW member of the <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-123">D3DPMISCCAPS_COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="aaac2-123">D3DPMISCCAPS_COLORWRITEENABLE</span></span></td>
<td><span data-ttu-id="aaac2-124">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="aaac2-124">0x00000100L</span></span></td>
<td><span data-ttu-id="aaac2-125">Il dispositivo supporta le scritture per canale per il buffer dei colori di destinazione del rendering tramite lo D3DRS_COLORWRITEENABLE stato.</span><span class="sxs-lookup"><span data-stu-id="aaac2-125">Device supports per-channel writes for the render-target color buffer through the D3DRS_COLORWRITEENABLE state.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span><span class="sxs-lookup"><span data-stu-id="aaac2-126">D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</span></span></td>
<td><span data-ttu-id="aaac2-127">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="aaac2-127">0x00000200L</span></span></td>
<td><span data-ttu-id="aaac2-128">Il dispositivo ritaglia correttamente i punti di ridimensionamento maggiori di 1,0 ai piani di ritaglio definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="aaac2-128">Device correctly clips scaled points of size greater than 1.0 to user-defined clipping planes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-129">D3DPMISCCAPS_CLIPTLVERTS</span><span class="sxs-lookup"><span data-stu-id="aaac2-129">D3DPMISCCAPS_CLIPTLVERTS</span></span></td>
<td><span data-ttu-id="aaac2-130">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="aaac2-130">0x00000200L</span></span></td>
<td><span data-ttu-id="aaac2-131">Clip del dispositivo dopo la trasformazione delle primitive dei vertici.</span><span class="sxs-lookup"><span data-stu-id="aaac2-131">Device clips post-transformed vertex primitives.</span></span> <span data-ttu-id="aaac2-132">Specificare D3DUSAGE_DONOTCLIP quando la pipeline non deve eseguire alcun ritaglio.</span><span class="sxs-lookup"><span data-stu-id="aaac2-132">Specify D3DUSAGE_DONOTCLIP when the pipeline should not do any clipping.</span></span> <span data-ttu-id="aaac2-133">In questo caso, potrebbe essere necessario eseguire un ritaglio software aggiuntivo in fase di disegno, che richiede che il vertex buffer sia nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="aaac2-133">For this case, additional software clipping may need to be performed at draw time, requiring the vertex buffer to be in system memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-134">D3DPMISCCAPS_TSSARGTEMP</span><span class="sxs-lookup"><span data-stu-id="aaac2-134">D3DPMISCCAPS_TSSARGTEMP</span></span></td>
<td><span data-ttu-id="aaac2-135">0x00000400L</span><span class="sxs-lookup"><span data-stu-id="aaac2-135">0x00000400L</span></span></td>
<td><span data-ttu-id="aaac2-136">Il dispositivo supporta <a href="d3dta.md">D3DTA per</a> il registro temporaneo.</span><span class="sxs-lookup"><span data-stu-id="aaac2-136">Device supports <a href="d3dta.md">D3DTA</a> for temporary register.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-137">D3DPMISCCAPS_BLENDOP</span><span class="sxs-lookup"><span data-stu-id="aaac2-137">D3DPMISCCAPS_BLENDOP</span></span></td>
<td><span data-ttu-id="aaac2-138">0x00000800L</span><span class="sxs-lookup"><span data-stu-id="aaac2-138">0x00000800L</span></span></td>
<td><span data-ttu-id="aaac2-139">Il dispositivo supporta operazioni di alpha blending diverse da D3DBLENDOP_ADD.</span><span class="sxs-lookup"><span data-stu-id="aaac2-139">Device supports alpha-blending operations other than D3DBLENDOP_ADD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-140">D3DPMISCCAPS_NULLREFERENCE</span><span class="sxs-lookup"><span data-stu-id="aaac2-140">D3DPMISCCAPS_NULLREFERENCE</span></span></td>
<td><span data-ttu-id="aaac2-141">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="aaac2-141">0x00000100L</span></span></td>
<td><span data-ttu-id="aaac2-142">Dispositivo di riferimento di cui non viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="aaac2-142">A reference device that does not render.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span><span class="sxs-lookup"><span data-stu-id="aaac2-143">D3DPMISCCAPS_INDEPENDENTWRITEMASKS</span></span></td>
<td><span data-ttu-id="aaac2-144">0x00004000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-144">0x00004000L</span></span></td>
<td><span data-ttu-id="aaac2-145">Il dispositivo supporta maschere di scrittura indipendenti per più trame di elementi o più destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="aaac2-145">Device supports independent write masks for multiple element textures or multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-146">D3DPMISCCAPS_PERSTAGECONSTANT</span><span class="sxs-lookup"><span data-stu-id="aaac2-146">D3DPMISCCAPS_PERSTAGECONSTANT</span></span></td>
<td><span data-ttu-id="aaac2-147">0x00008000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-147">0x00008000L</span></span></td>
<td><span data-ttu-id="aaac2-148">Il dispositivo supporta costanti per fase.</span><span class="sxs-lookup"><span data-stu-id="aaac2-148">Device supports per-stage constants.</span></span> <span data-ttu-id="aaac2-149">Vedere D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aaac2-149">See D3DTSS_CONSTANT in <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span><span class="sxs-lookup"><span data-stu-id="aaac2-150">D3DPMISCCAPS_POSTBLENDSRGBCONVERT</span></span></td>
<td><span data-ttu-id="aaac2-151">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-151">0x00200000L</span></span></td>
<td><span data-ttu-id="aaac2-152">Il dispositivo supporta la conversione in sRGB dopo la fusione.</span><span class="sxs-lookup"><span data-stu-id="aaac2-152">Device supports conversion to sRGB after blending.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aaac2-153">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="aaac2-153">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="aaac2-154">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="aaac2-154">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span><span class="sxs-lookup"><span data-stu-id="aaac2-155">D3DPMISCCAPS_FOGANDSPECULARALPHA</span></span></td>
<td><span data-ttu-id="aaac2-156">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-156">0x00010000L</span></span></td>
<td><span data-ttu-id="aaac2-157">Il dispositivo supporta alfa separati e speculari.</span><span class="sxs-lookup"><span data-stu-id="aaac2-157">Device supports separate fog and specular alpha.</span></span> <span data-ttu-id="aaac2-158">Molti dispositivi usano il canale alfa speculare per archiviare il fattore di rischio.</span><span class="sxs-lookup"><span data-stu-id="aaac2-158">Many devices use the specular alpha channel to store the fog factor.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="aaac2-159">D3DPMISCCAPS_SEPARATEALPHABLEND</span></span></td>
<td><span data-ttu-id="aaac2-160">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-160">0x00020000L</span></span></td>
<td><span data-ttu-id="aaac2-161">Il dispositivo supporta impostazioni di blend separate per il canale alfa.</span><span class="sxs-lookup"><span data-stu-id="aaac2-161">Device supports separate blend settings for the alpha channel.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span><span class="sxs-lookup"><span data-stu-id="aaac2-162">D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</span></span></td>
<td><span data-ttu-id="aaac2-163">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-163">0x00040000L</span></span></td>
<td><span data-ttu-id="aaac2-164">Il dispositivo supporta diverse profondità di bit per più destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="aaac2-164">Device supports different bit depths for multiple render targets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aaac2-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span><span class="sxs-lookup"><span data-stu-id="aaac2-165">D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</span></span></td>
<td><span data-ttu-id="aaac2-166">0x00080000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-166">0x00080000L</span></span></td>
<td><span data-ttu-id="aaac2-167">Il dispositivo supporta le operazioni post-pixel shader per più destinazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="aaac2-167">Device supports post-pixel shader operations for multiple render targets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aaac2-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span><span class="sxs-lookup"><span data-stu-id="aaac2-168">D3DPMISCCAPS_FOGVERTEXCLAMPED</span></span></td>
<td><span data-ttu-id="aaac2-169">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="aaac2-169">0x00100000L</span></span></td>
<td><span data-ttu-id="aaac2-170">Fattore di fusione della nebbia per vertice delle piascie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaac2-170">Device clamps fog blend factor per vertex.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="aaac2-171">Queste costanti vengono usate dal membro PrimitiveMiscCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="aaac2-171">These constants are used by the PrimitiveMiscCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="aaac2-172">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="aaac2-172">Constant Information</span></span>



| <span data-ttu-id="aaac2-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaac2-173">Requirement</span></span>                         |  <span data-ttu-id="aaac2-174">Valore</span><span class="sxs-lookup"><span data-stu-id="aaac2-174">Value</span></span>          |
|--------------------------|------------|
| <span data-ttu-id="aaac2-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aaac2-175">Header</span></span>                   | <span data-ttu-id="aaac2-176">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="aaac2-176">d3d9caps.h</span></span> |
| <span data-ttu-id="aaac2-177">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="aaac2-177">Minimum operating system</span></span> | <span data-ttu-id="aaac2-178">Windows 98</span><span class="sxs-lookup"><span data-stu-id="aaac2-178">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aaac2-179">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aaac2-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaac2-180">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="aaac2-180">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
