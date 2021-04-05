---
description: Usa una funzione HLSL (High-Level Shader Language) compilata per riempire ogni Texel di ogni livello di mipmap di una trama.
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: Funzione D3DXFillTextureTX (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3605011f7967edec68d13405b4cabbd9c90d4c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058606"
---
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="b7d0d-103">D3DXFillTextureTX (funzione)</span><span class="sxs-lookup"><span data-stu-id="b7d0d-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="b7d0d-104">Usa una funzione HLSL (High-Level Shader Language) compilata per riempire ogni Texel di ogni livello di mipmap di una trama.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d0d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7d0d-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="b7d0d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7d0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d0d-107">*pTexture* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b7d0d-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d0d-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="b7d0d-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="b7d0d-109">Puntatore a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta la trama da riempire.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="b7d0d-110">*pTextureShader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7d0d-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d0d-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d0d-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="b7d0d-112">Puntatore a un oggetto shader di trama [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d0d-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d0d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7d0d-113">Return value</span></span>

<span data-ttu-id="b7d0d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7d0d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7d0d-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7d0d-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d0d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7d0d-117">Remarks</span></span>

<span data-ttu-id="b7d0d-118">La destinazione della trama deve essere una funzione HLSL che accetta contiene la semantica seguente:</span><span class="sxs-lookup"><span data-stu-id="b7d0d-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="b7d0d-119">Un parametro di input deve usare una semantica di posizione.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="b7d0d-120">Un parametro di input deve usare una semantica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="b7d0d-121">La funzione deve restituire un parametro che usa la semantica del colore.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="b7d0d-122">Di seguito è riportato un esempio di una funzione HLSL:</span><span class="sxs-lookup"><span data-stu-id="b7d0d-122">The following is an example of such an HLSL function:</span></span>


```
float4 TextureGradientFill(
  float2 vTexCoord : POSITION, 
  float2 vTexelSize : PSIZE) : COLOR 
  {
    float r,g, b, xSq,ySq, a;
    xSq = 2.f*vTexCoord.x-1.f; xSq *= xSq;
    ySq = 2.f*vTexCoord.y-1.f; ySq *= ySq;
    a = sqrt(xSq+ySq);
    if (a > 1.0f) {
        a = 1.0f-(a-1.0f);
    }
    else if (a < 0.2f) {
        a = 0.2f;
    }
    r = 1-vTexCoord.x;
    g = 1-vTexCoord.y;
    b = vTexCoord.x;
    return float4(r, g, b, a);
    
  };
```



<span data-ttu-id="b7d0d-123">Si noti che i parametri di input possono essere in qualsiasi ordine, ma è necessario rappresentare entrambe le semantiche di input.</span><span class="sxs-lookup"><span data-stu-id="b7d0d-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d0d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7d0d-124">Requirements</span></span>



| <span data-ttu-id="b7d0d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d0d-125">Requirement</span></span> | <span data-ttu-id="b7d0d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b7d0d-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d0d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7d0d-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b7d0d-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d0d-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b7d0d-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7d0d-129">Library</span></span><br/> | <dl> <span data-ttu-id="b7d0d-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d0d-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b7d0d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7d0d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d0d-132">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b7d0d-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="b7d0d-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="b7d0d-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="b7d0d-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="b7d0d-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
