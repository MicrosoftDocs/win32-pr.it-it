---
description: Costanti di filtro delle trame.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343086"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="cfe1f-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="cfe1f-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="cfe1f-104">Costanti di filtro delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cfe1f-105">#Definire</span><span class="sxs-lookup"><span data-stu-id="cfe1f-105">#define</span></span></td>
<td><span data-ttu-id="cfe1f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfe1f-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfe1f-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="cfe1f-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="cfe1f-108">Il dispositivo supporta il filtro convoluzione monocromatica.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="cfe1f-109">Questo filtro è rappresentato dal D3DTEXF_CONVOLUTIONMONO del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cfe1f-110">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="cfe1f-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="cfe1f-111">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfe1f-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="cfe1f-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="cfe1f-113">Il dispositivo supporta il filtro per campione di punti per fase per la ingrandimento delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="cfe1f-114">Il filtro di ingrandimento del campione di punti è rappresentato dal D3DTEXF_POINT del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfe1f-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="cfe1f-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="cfe1f-116">Il dispositivo supporta il filtro di interpolazione bilineare per fase per ingrandire le mipmap.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="cfe1f-117">Il filtro mipmapping di interpolazione bilineare è rappresentato dal D3DTEXF_LINEAR del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfe1f-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="cfe1f-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="cfe1f-119">Il dispositivo supporta il filtro anisotropo per fase per la ingrandimento delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="cfe1f-120">Il filtro di ingrandimento anisotropo è rappresentato dal D3DTEXF_ANISOTROPIC del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfe1f-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="cfe1f-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="cfe1f-122">Il dispositivo supporta il filtro dei campioni piramidali per fase per l'ingrandimento delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="cfe1f-123">Il filtro di ingrandimento piramidale è rappresentato dal D3DTEXF_PYRAMIDALQUAD membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfe1f-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="cfe1f-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="cfe1f-125">Il dispositivo supporta il filtro quad gaussiano per fase per le trame di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfe1f-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="cfe1f-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="cfe1f-127">Il dispositivo supporta il filtro per campione di punti per fase per la minificazione delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="cfe1f-128">Il filtro di minificazione del campione di punti è rappresentato dal D3DTEXF_POINT membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfe1f-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="cfe1f-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="cfe1f-130">Il dispositivo supporta il filtro lineare per fase per la minificazione delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="cfe1f-131">Il filtro di minificazione lineare è rappresentato dal D3DTEXF_LINEAR membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfe1f-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="cfe1f-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="cfe1f-133">Il dispositivo supporta il filtro anisotropo per fase per la minificazione delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="cfe1f-134">Il filtro di minificazione anisotrop è rappresentato dal D3DTEXF_ANISOTROPIC membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfe1f-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="cfe1f-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="cfe1f-136">Il dispositivo supporta il filtro dei campioni piramidali per fase per la minificazione delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfe1f-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="cfe1f-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="cfe1f-138">Il dispositivo supporta il filtro quad gaussiano per fase per la minificazione delle trame.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cfe1f-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="cfe1f-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="cfe1f-140">Il dispositivo supporta il filtro per campione di punti per fase per le mipmap.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="cfe1f-141">Il filtro mipmapping di esempio di punti è rappresentato dal D3DTEXF_POINT membro del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cfe1f-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="cfe1f-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="cfe1f-143">Il dispositivo supporta il filtro di interpolazione bilineare per fase per le mipmap.</span><span class="sxs-lookup"><span data-stu-id="cfe1f-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="cfe1f-144">Il filtro mipmapping di interpolazione bilineare è rappresentato dal D3DTEXF_LINEAR del tipo <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>enumerato D3DTEXTUREFILTERTYPE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="cfe1f-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cfe1f-145">Queste costanti vengono usate dai membri TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps e VertexTextureFilterCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="cfe1f-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="cfe1f-146">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="cfe1f-146">Constant Information</span></span>



|  <span data-ttu-id="cfe1f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfe1f-147">Requirement</span></span>                        | <span data-ttu-id="cfe1f-148">Valore</span><span class="sxs-lookup"><span data-stu-id="cfe1f-148">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="cfe1f-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfe1f-149">Header</span></span>                   | <span data-ttu-id="cfe1f-150">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="cfe1f-150">d3d9caps.h</span></span> |
| <span data-ttu-id="cfe1f-151">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="cfe1f-151">Minimum operating system</span></span> | <span data-ttu-id="cfe1f-152">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cfe1f-152">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cfe1f-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cfe1f-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfe1f-154">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="cfe1f-154">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
