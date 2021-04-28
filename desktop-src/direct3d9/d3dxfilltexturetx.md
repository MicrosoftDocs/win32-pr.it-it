---
description: 'Funzione D3DXFillTextureTX: usa una funzione HLSL (High Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.'
ms.assetid: 013660ce-865e-4acf-a1ea-670e70377ff5
title: Funzione D3DXFillTextureTX (D3dx9tex.h)
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
ms.openlocfilehash: 419dc0e7b4266a2fe32557c52ed4323b51a25843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107639"
---
# <a name="d3dxfilltexturetx-function"></a><span data-ttu-id="39e64-103">Funzione D3DXFillTextureTX</span><span class="sxs-lookup"><span data-stu-id="39e64-103">D3DXFillTextureTX function</span></span>

<span data-ttu-id="39e64-104">Usa una funzione HLSL (High-Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.</span><span class="sxs-lookup"><span data-stu-id="39e64-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e64-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39e64-105">Syntax</span></span>


```C++
HRESULT D3DXFillTextureTX(
  _Inout_ LPDIRECT3DTEXTURE9  pTexture,
  _In_    LPD3DXTEXTURESHADER pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="39e64-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39e64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e64-107">*pTexture* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="39e64-107">*pTexture* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39e64-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="39e64-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="39e64-109">Puntatore a [**un oggetto IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama da riempire.</span><span class="sxs-lookup"><span data-stu-id="39e64-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="39e64-110">*pTextureShader* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="39e64-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e64-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="39e64-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="39e64-112">Puntatore a un oggetto shader con trama [**ID3DXTextureShader.**](id3dxtextureshader.md)</span><span class="sxs-lookup"><span data-stu-id="39e64-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e64-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39e64-113">Return value</span></span>

<span data-ttu-id="39e64-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39e64-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39e64-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="39e64-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="39e64-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="39e64-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e64-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="39e64-117">Remarks</span></span>

<span data-ttu-id="39e64-118">La destinazione della trama deve essere una funzione HLSL che accetta contiene la semantica seguente:</span><span class="sxs-lookup"><span data-stu-id="39e64-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="39e64-119">Un parametro di input deve usare una semantica POSITION.</span><span class="sxs-lookup"><span data-stu-id="39e64-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="39e64-120">Un parametro di input deve usare una semantica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="39e64-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="39e64-121">La funzione deve restituire un parametro che usa la semantica COLOR.</span><span class="sxs-lookup"><span data-stu-id="39e64-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="39e64-122">Di seguito è riportato un esempio di tale funzione HLSL:</span><span class="sxs-lookup"><span data-stu-id="39e64-122">The following is an example of such an HLSL function:</span></span>


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



<span data-ttu-id="39e64-123">Si noti che i parametri di input possono essere in qualsiasi ordine, ma è necessario rappresentare entrambe le semantiche di input.</span><span class="sxs-lookup"><span data-stu-id="39e64-123">Note that the input parameters can be in any order, but both input semantics must be represented.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e64-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39e64-124">Requirements</span></span>



| <span data-ttu-id="39e64-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e64-125">Requirement</span></span> | <span data-ttu-id="39e64-126">Valore</span><span class="sxs-lookup"><span data-stu-id="39e64-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39e64-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39e64-127">Header</span></span><br/>  | <dl> <span data-ttu-id="39e64-128"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="39e64-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="39e64-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="39e64-129">Library</span></span><br/> | <dl> <span data-ttu-id="39e64-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="39e64-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="39e64-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39e64-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e64-132">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="39e64-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="39e64-133">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="39e64-133">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="39e64-134">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="39e64-134">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
