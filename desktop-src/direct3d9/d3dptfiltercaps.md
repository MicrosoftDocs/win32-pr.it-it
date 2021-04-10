---
description: Costanti di filtro della trama.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c122b1260d568a43c69c336059e26a6ecfde2a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049276"
---
# <a name="d3dptfiltercaps"></a><span data-ttu-id="a9631-103">D3DPTFILTERCAPS</span><span class="sxs-lookup"><span data-stu-id="a9631-103">D3DPTFILTERCAPS</span></span>

<span data-ttu-id="a9631-104">Costanti di filtro della trama.</span><span class="sxs-lookup"><span data-stu-id="a9631-104">Texture filtering constants.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9631-105">#definire</span><span class="sxs-lookup"><span data-stu-id="a9631-105">#define</span></span></td>
<td><span data-ttu-id="a9631-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9631-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9631-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span><span class="sxs-lookup"><span data-stu-id="a9631-107">D3DPTFILTERCAPS_CONVOLUTIONMONO</span></span></td>
<td><span data-ttu-id="a9631-108">Il dispositivo supporta il filtro convoluzione monocromatico.</span><span class="sxs-lookup"><span data-stu-id="a9631-108">Device supports monochrome convolution filtering.</span></span> <span data-ttu-id="a9631-109">Questo filtro è rappresentato dal membro D3DTEXF_CONVOLUTIONMONO del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-109">This filter is represented by the D3DTEXF_CONVOLUTIONMONO member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9631-110">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="a9631-110">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="a9631-111">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="a9631-111">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9631-112">D3DPTFILTERCAPS_MAGFPOINT</span><span class="sxs-lookup"><span data-stu-id="a9631-112">D3DPTFILTERCAPS_MAGFPOINT</span></span></td>
<td><span data-ttu-id="a9631-113">Il dispositivo supporta il filtro di esempio per punto per fase per le trame di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="a9631-113">Device supports per-stage point-sample filtering for magnifying textures.</span></span> <span data-ttu-id="a9631-114">Il filtro di ingrandimento Point-Sample è rappresentato dal membro D3DTEXF_POINT del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-114">The point-sample magnification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9631-115">D3DPTFILTERCAPS_MAGFLINEAR</span><span class="sxs-lookup"><span data-stu-id="a9631-115">D3DPTFILTERCAPS_MAGFLINEAR</span></span></td>
<td><span data-ttu-id="a9631-116">Il dispositivo supporta il filtro di interpolazione bilineare per fase per ingrandire mipmap.</span><span class="sxs-lookup"><span data-stu-id="a9631-116">Device supports per-stage bilinear interpolation filtering for magnifying mipmaps.</span></span> <span data-ttu-id="a9631-117">Il filtro mapping MIP di interpolazione bilineare è rappresentato dal membro D3DTEXF_LINEAR del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-117">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9631-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="a9631-118">D3DPTFILTERCAPS_MAGFANISOTROPIC</span></span></td>
<td><span data-ttu-id="a9631-119">Il dispositivo supporta il filtro anisotropico per fase per le trame di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="a9631-119">Device supports per-stage anisotropic filtering for magnifying textures.</span></span> <span data-ttu-id="a9631-120">Il filtro di ingrandimento anisotropico è rappresentato dal membro D3DTEXF_ANISOTROPIC del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-120">The anisotropic magnification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9631-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="a9631-121">D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="a9631-122">Il dispositivo supporta il filtro di esempio piramidale per fase per le trame di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="a9631-122">Device supports per-stage pyramidal sample filtering for magnifying textures.</span></span> <span data-ttu-id="a9631-123">Il filtro di ingrandimento piramidale è rappresentato dal membro D3DTEXF_PYRAMIDALQUAD del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-123">The pyramidal magnifying filter is represented by the D3DTEXF_PYRAMIDALQUAD member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9631-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="a9631-124">D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="a9631-125">Il dispositivo supporta il filtraggio quadruplo per fase per fase per le trame di ingrandimento.</span><span class="sxs-lookup"><span data-stu-id="a9631-125">Device supports per-stage Gaussian quad filtering for magnifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9631-126">D3DPTFILTERCAPS_MINFPOINT</span><span class="sxs-lookup"><span data-stu-id="a9631-126">D3DPTFILTERCAPS_MINFPOINT</span></span></td>
<td><span data-ttu-id="a9631-127">Il dispositivo supporta l'applicazione di filtri di esempio per punto per fase per le trame minimizzazione.</span><span class="sxs-lookup"><span data-stu-id="a9631-127">Device supports per-stage point-sample filtering for minifying textures.</span></span> <span data-ttu-id="a9631-128">Il filtro minification Point-Sample è rappresentato dal membro D3DTEXF_POINT del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-128">The point-sample minification filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9631-129">D3DPTFILTERCAPS_MINFLINEAR</span><span class="sxs-lookup"><span data-stu-id="a9631-129">D3DPTFILTERCAPS_MINFLINEAR</span></span></td>
<td><span data-ttu-id="a9631-130">Il dispositivo supporta il filtro lineare per fase per le trame minimizzazione.</span><span class="sxs-lookup"><span data-stu-id="a9631-130">Device supports per-stage linear filtering for minifying textures.</span></span> <span data-ttu-id="a9631-131">Il filtro minification lineare è rappresentato dal membro D3DTEXF_LINEAR del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-131">The linear minification filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9631-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span><span class="sxs-lookup"><span data-stu-id="a9631-132">D3DPTFILTERCAPS_MINFANISOTROPIC</span></span></td>
<td><span data-ttu-id="a9631-133">Il dispositivo supporta il filtro anisotropico per fase per le trame minimizzazione.</span><span class="sxs-lookup"><span data-stu-id="a9631-133">Device supports per-stage anisotropic filtering for minifying textures.</span></span> <span data-ttu-id="a9631-134">Il filtro minification anisotropico è rappresentato dal membro D3DTEXF_ANISOTROPIC del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-134">The anisotropic minification filter is represented by the D3DTEXF_ANISOTROPIC member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9631-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span><span class="sxs-lookup"><span data-stu-id="a9631-135">D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</span></span></td>
<td><span data-ttu-id="a9631-136">Il dispositivo supporta il filtro di esempio piramidale per fase per le trame minimizzazione.</span><span class="sxs-lookup"><span data-stu-id="a9631-136">Device supports per-stage pyramidal sample filtering for minifying textures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9631-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span><span class="sxs-lookup"><span data-stu-id="a9631-137">D3DPTFILTERCAPS_MINFGAUSSIANQUAD</span></span></td>
<td><span data-ttu-id="a9631-138">Il dispositivo supporta il filtraggio quadruplo per fase per fase per le trame minimizzazione.</span><span class="sxs-lookup"><span data-stu-id="a9631-138">Device supports per-stage Gaussian quad filtering for minifying textures.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9631-139">D3DPTFILTERCAPS_MIPFPOINT</span><span class="sxs-lookup"><span data-stu-id="a9631-139">D3DPTFILTERCAPS_MIPFPOINT</span></span></td>
<td><span data-ttu-id="a9631-140">Il dispositivo supporta l'applicazione di filtri di esempio per punto per fase per mipmap.</span><span class="sxs-lookup"><span data-stu-id="a9631-140">Device supports per-stage point-sample filtering for mipmaps.</span></span> <span data-ttu-id="a9631-141">Il filtro mapping MIP Point-Sample è rappresentato dal membro D3DTEXF_POINT del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-141">The point-sample mipmapping filter is represented by the D3DTEXF_POINT member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9631-142">D3DPTFILTERCAPS_MIPFLINEAR</span><span class="sxs-lookup"><span data-stu-id="a9631-142">D3DPTFILTERCAPS_MIPFLINEAR</span></span></td>
<td><span data-ttu-id="a9631-143">Il dispositivo supporta il filtro di interpolazione bilineare per fase per mipmap.</span><span class="sxs-lookup"><span data-stu-id="a9631-143">Device supports per-stage bilinear interpolation filtering for mipmaps.</span></span> <span data-ttu-id="a9631-144">Il filtro mapping MIP di interpolazione bilineare è rappresentato dal membro D3DTEXF_LINEAR del tipo enumerato <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a9631-144">The bilinear interpolation mipmapping filter is represented by the D3DTEXF_LINEAR member of the <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> enumerated type.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a9631-145">Queste costanti vengono usate dai membri TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps e VertexTextureFilterCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="a9631-145">These constants are used by TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps, and VertexTextureFilterCaps members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a9631-146">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="a9631-146">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a9631-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9631-147">Header</span></span>                   | <span data-ttu-id="a9631-148">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a9631-148">d3d9caps.h</span></span> |
| <span data-ttu-id="a9631-149">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="a9631-149">Minimum operating system</span></span> | <span data-ttu-id="a9631-150">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a9631-150">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a9631-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9631-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9631-152">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="a9631-152">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
