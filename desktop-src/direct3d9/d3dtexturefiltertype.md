---
description: Definisce le modalità di filtro della trama per una fase della trama.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumerazione D3DTEXTUREFILTERTYPE (D3D9Types. h)
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
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322306"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="45b8a-103">Enumerazione D3DTEXTUREFILTERTYPE</span><span class="sxs-lookup"><span data-stu-id="45b8a-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="45b8a-104">Definisce le modalità di filtro della trama per una fase della trama.</span><span class="sxs-lookup"><span data-stu-id="45b8a-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45b8a-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="45b8a-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="45b8a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="45b8a-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ None**</span><span class="sxs-lookup"><span data-stu-id="45b8a-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-108">Se usato con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), Disabilita mapping MIP.</span><span class="sxs-lookup"><span data-stu-id="45b8a-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="45b8a-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**Punto di D3DTEXF \_**</span><span class="sxs-lookup"><span data-stu-id="45b8a-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-110">Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), specifica che il filtro punti deve essere usato rispettivamente come ingrandimento della trama o filtro minification.</span><span class="sxs-lookup"><span data-stu-id="45b8a-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="45b8a-111">Se usato con **D3DSAMP \_ MIPFILTER**, Abilita mapping MIP e specifica che il rasterizzatore sceglie il colore dal Texel del livello MIP più vicino.</span><span class="sxs-lookup"><span data-stu-id="45b8a-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="45b8a-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ lineare**</span><span class="sxs-lookup"><span data-stu-id="45b8a-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-113">Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), specifica che è necessario usare il filtro lineare come ingrandimento della trama o filtro minification rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="45b8a-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="45b8a-114">Se usato con **D3DSAMP \_ MIPFILTER**, Abilita il filtro mapping MIP e trilineare; specifica che l'rasterizzazione Interpola tra i due livelli MIP più vicini.</span><span class="sxs-lookup"><span data-stu-id="45b8a-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="45b8a-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotropico**</span><span class="sxs-lookup"><span data-stu-id="45b8a-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-116">Se usato con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), specifica che il filtro di trama anisotropico viene usato rispettivamente come ingrandimento della trama o filtro minification.</span><span class="sxs-lookup"><span data-stu-id="45b8a-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="45b8a-117">Compensa la distorsione causata dalla differenza nell'angolo tra il poligono di trama e il piano dello schermo.</span><span class="sxs-lookup"><span data-stu-id="45b8a-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="45b8a-118">L'uso di con **D3DSAMP \_ MIPFILTER** non è definito.</span><span class="sxs-lookup"><span data-stu-id="45b8a-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="45b8a-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**\_PYRAMIDALQUAD D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="45b8a-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-120">Un filtro tenda da 4 campioni usato come ingrandimento della trama o filtro minification.</span><span class="sxs-lookup"><span data-stu-id="45b8a-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="45b8a-121">L'uso di con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.</span><span class="sxs-lookup"><span data-stu-id="45b8a-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="45b8a-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**\_GAUSSIANQUAD D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="45b8a-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-123">Un filtro di controllo gaussiana di 4 campioni usato come ingrandimento della trama o filtro minification.</span><span class="sxs-lookup"><span data-stu-id="45b8a-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="45b8a-124">L'uso di con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.</span><span class="sxs-lookup"><span data-stu-id="45b8a-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="45b8a-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**\_CONVOLUTIONMONO D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="45b8a-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-126">Filtro di convoluzione per le trame monocromatiche.</span><span class="sxs-lookup"><span data-stu-id="45b8a-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="45b8a-127">Vedere [D3DFMT \_ a1](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="45b8a-127">See [D3DFMT\_A1](d3dformat.md).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b8a-128">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="45b8a-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="45b8a-129">Questo flag è disponibile solo in Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="45b8a-129">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

<span data-ttu-id="45b8a-130">L'uso di con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) non è definito.</span><span class="sxs-lookup"><span data-stu-id="45b8a-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="45b8a-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="45b8a-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="45b8a-132">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="45b8a-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="45b8a-133">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="45b8a-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="45b8a-134">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="45b8a-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45b8a-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="45b8a-135">Remarks</span></span>

<span data-ttu-id="45b8a-136">D3DTEXTUREFILTERTYPE viene usato da [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) insieme a [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) per definire le modalità di filtro della trama per una fase della trama.</span><span class="sxs-lookup"><span data-stu-id="45b8a-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="45b8a-137">Per verificare se un formato supporta tipi di filtro di trama diversi dal punto di D3DTEXF \_ (che è sempre supportato), chiamare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con il \_ filtro query D3DUSAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="45b8a-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="45b8a-138">Impostare il filtro di ingrandimento di una fase trama chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il \_ valore D3DSAMP MAGFILTER come secondo parametro e un membro di questa enumerazione come terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="45b8a-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="45b8a-139">Impostare il filtro minification della fase della trama chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il \_ valore D3DSAMP MINFILTER come secondo parametro e un membro di questa enumerazione come terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="45b8a-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="45b8a-140">Impostare il filtro di trama per usare i livelli between-mipmap chiamando [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con il \_ valore D3DSAMP MIPFILTER come secondo parametro e un membro di questa enumerazione come terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="45b8a-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="45b8a-141">Non tutte le modalità di filtro valide per un dispositivo verranno applicate alle mappe del volume.</span><span class="sxs-lookup"><span data-stu-id="45b8a-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="45b8a-142">In generale, \_ \_ i filtri di ingrandimento lineari D3DTEXF Point e D3DTEXF sono supportati per le mappe dei volumi.</span><span class="sxs-lookup"><span data-stu-id="45b8a-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="45b8a-143">Se \_ è impostato D3DPTEXTURECAPS MIPVOLUMEMAP, i filtri D3DTEXF \_ Point mipmap Filter e D3DTEXF \_ Point e D3DTEXF \_ Linear minification saranno supportati per le mappe del volume.</span><span class="sxs-lookup"><span data-stu-id="45b8a-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="45b8a-144">Il dispositivo può supportare o meno il filtro D3DTEXF \_ lineare mipmap per mappe del volume.</span><span class="sxs-lookup"><span data-stu-id="45b8a-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="45b8a-145">I dispositivi che supportano il filtro anisotropico per le mappe 2D non supportano necessariamente il filtro anisotropico per le mappe del volume.</span><span class="sxs-lookup"><span data-stu-id="45b8a-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="45b8a-146">Tuttavia, le applicazioni che abilitano il filtro anisotropico riceveranno il migliore filtro disponibile (probabilmente lineare) se il filtro anisotropico non è supportato.</span><span class="sxs-lookup"><span data-stu-id="45b8a-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b8a-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45b8a-147">Requirements</span></span>



| <span data-ttu-id="45b8a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b8a-148">Requirement</span></span> | <span data-ttu-id="45b8a-149">Valore</span><span class="sxs-lookup"><span data-stu-id="45b8a-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45b8a-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45b8a-150">Header</span></span><br/> | <dl> <span data-ttu-id="45b8a-151"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="45b8a-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b8a-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45b8a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b8a-153">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="45b8a-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="45b8a-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="45b8a-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="45b8a-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="45b8a-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="45b8a-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="45b8a-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="45b8a-157">**IDirect3DDevice9:: SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="45b8a-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
