---
description: Definisce le modalità di filtro trame per una fase di trama.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumerazione D3DTEXTUREFILTERTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343006"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="0d644-103">Enumerazione D3DTEXTUREFILTERTYPE</span><span class="sxs-lookup"><span data-stu-id="0d644-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="0d644-104">Definisce le modalità di filtro trame per una fase di trama.</span><span class="sxs-lookup"><span data-stu-id="0d644-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d644-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d644-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a><span data-ttu-id="0d644-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="0d644-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0d644-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ NONE**</span><span class="sxs-lookup"><span data-stu-id="0d644-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-108">Se usato con [**D3DSAMP \_ MIPFILTER,**](./d3dsamplerstatetype.md)disabilita l'applicazione mipmapping.</span><span class="sxs-lookup"><span data-stu-id="0d644-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="0d644-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**PUNTO D3DTEXF \_**</span><span class="sxs-lookup"><span data-stu-id="0d644-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-110">Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)specifica che il filtro dei punti deve essere usato rispettivamente come filtro di ingrandimento o minificazione della trama.</span><span class="sxs-lookup"><span data-stu-id="0d644-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="0d644-111">Se usato con **D3DSAMP \_ MIPFILTER,** abilita l'applicazione mipmapping e specifica che il rasterizzatore sceglie il colore dal texel del livello mip più vicino.</span><span class="sxs-lookup"><span data-stu-id="0d644-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="0d644-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**LINEARE D3DTEXF \_**</span><span class="sxs-lookup"><span data-stu-id="0d644-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-113">Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)specifica che il filtro lineare deve essere usato rispettivamente come filtro di ingrandimento o minificazione della trama.</span><span class="sxs-lookup"><span data-stu-id="0d644-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="0d644-114">Se usato con **D3DSAMP \_ MIPFILTER,** abilita l'applicazione mipmapping e il filtro trilineare. Specifica che il rasterizzatore interpola tra i due livelli mip più vicini.</span><span class="sxs-lookup"><span data-stu-id="0d644-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="0d644-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROP**</span><span class="sxs-lookup"><span data-stu-id="0d644-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-116">Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)specifica che il filtro trame anisotropo usato rispettivamente come filtro di ingrandimento o minificazione della trama.</span><span class="sxs-lookup"><span data-stu-id="0d644-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="0d644-117">Compensa la distorsione causata dalla differenza di angolo tra il poligono della trama e il piano dello schermo.</span><span class="sxs-lookup"><span data-stu-id="0d644-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="0d644-118">**L'uso con D3DSAMP \_ MIPFILTER** non è definito.</span><span class="sxs-lookup"><span data-stu-id="0d644-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="0d644-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**</span><span class="sxs-lookup"><span data-stu-id="0d644-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-120">Filtro a tent di 4 campioni usato come filtro di ingrandimento o minificazione della trama.</span><span class="sxs-lookup"><span data-stu-id="0d644-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="0d644-121">[**L'uso con D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.</span><span class="sxs-lookup"><span data-stu-id="0d644-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="0d644-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**</span><span class="sxs-lookup"><span data-stu-id="0d644-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-123">Filtro Gaussiano a 4 campioni usato come filtro di ingrandimento o minimicazione della trama.</span><span class="sxs-lookup"><span data-stu-id="0d644-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="0d644-124">[**L'uso con D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.</span><span class="sxs-lookup"><span data-stu-id="0d644-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="0d644-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**</span><span class="sxs-lookup"><span data-stu-id="0d644-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-126">Filtro di convoluzione per trame monocroma.</span><span class="sxs-lookup"><span data-stu-id="0d644-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="0d644-127">Vedere [D3DFMT \_ A1.](d3dformat.md)</span><span class="sxs-lookup"><span data-stu-id="0d644-127">See [D3DFMT\_A1](d3dformat.md).</span></span>

<span data-ttu-id="0d644-128">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="0d644-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="0d644-129">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="0d644-129">This flag is available in Direct3D 9Ex only.</span></span>



 

<span data-ttu-id="0d644-130">[**L'uso con D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.</span><span class="sxs-lookup"><span data-stu-id="0d644-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="0d644-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0d644-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0d644-132">Forza la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0d644-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0d644-133">Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0d644-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0d644-134">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="0d644-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d644-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d644-135">Remarks</span></span>

<span data-ttu-id="0d644-136">D3DTEXTUREFILTERTYPE viene usato da [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) insieme [**a D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) per definire le modalità di filtro della trama per una fase della trama.</span><span class="sxs-lookup"><span data-stu-id="0d644-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="0d644-137">Per verificare se un formato supporta tipi di filtro di trama diversi da D3DTEXF POINT (che è sempre supportato), chiamare \_ [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ QUERY \_ FILTER.</span><span class="sxs-lookup"><span data-stu-id="0d644-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="0d644-138">Impostare il filtro di ingrandimento di una fase della trama chiamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il valore D3DSAMP MAGFILTER come secondo parametro e un membro di questa enumerazione come terzo \_ parametro.</span><span class="sxs-lookup"><span data-stu-id="0d644-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="0d644-139">Impostare il filtro di minificazione di una fase della trama chiamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il valore D3DSAMP MINFILTER come secondo parametro e un membro di questa enumerazione come terzo \_ parametro.</span><span class="sxs-lookup"><span data-stu-id="0d644-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="0d644-140">Impostare il filtro di trama per l'uso tra livelli mipmap chiamando [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il valore MIPFILTER D3DSAMP come secondo parametro e un membro di questa enumerazione come terzo \_ parametro.</span><span class="sxs-lookup"><span data-stu-id="0d644-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="0d644-141">Non tutte le modalità di filtro valide per un dispositivo verranno applicate alle mappe di volume.</span><span class="sxs-lookup"><span data-stu-id="0d644-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="0d644-142">In generale, i filtri di ingrandimento D3DTEXF POINT e \_ D3DTEXF \_ LINEAR saranno supportati per le mappe di volume.</span><span class="sxs-lookup"><span data-stu-id="0d644-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="0d644-143">Se si imposta D3DPTEXTURECAPS \_ MIPVOLUMEMAP, i filtri mipmap D3DTEXF POINT e \_ D3DTEXF POINT e \_ D3DTEXF LINEAR saranno supportati per le mappe \_ di volume.</span><span class="sxs-lookup"><span data-stu-id="0d644-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="0d644-144">Il dispositivo può supportare o meno il filtro mipmap D3DTEXF \_ LINEAR per le mappe dei volumi.</span><span class="sxs-lookup"><span data-stu-id="0d644-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="0d644-145">I dispositivi che supportano il filtro anisotropo per le mappe 2D non supportano necessariamente il filtro anisotropo per le mappe di volume.</span><span class="sxs-lookup"><span data-stu-id="0d644-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="0d644-146">Tuttavia, le applicazioni che abilitano il filtro anisotropo riceveranno il filtro migliore disponibile (probabilmente lineare) se il filtro anisotropo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="0d644-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d644-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d644-147">Requirements</span></span>



| <span data-ttu-id="0d644-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d644-148">Requirement</span></span> | <span data-ttu-id="0d644-149">Valore</span><span class="sxs-lookup"><span data-stu-id="0d644-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d644-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d644-150">Header</span></span><br/> | <dl> <span data-ttu-id="0d644-151"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="0d644-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d644-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d644-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d644-153">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="0d644-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0d644-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="0d644-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="0d644-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="0d644-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="0d644-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="0d644-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="0d644-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="0d644-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
