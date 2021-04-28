---
description: 'Funzione D3DXFillCubeTextureTX: usa una funzione HLSL (High Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.'
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: Funzione D3DXFillCubeTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c6d054900f3f4c4710e22c54759161800137c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107669"
---
# <a name="d3dxfillcubetexturetx-function"></a><span data-ttu-id="ca5d4-103">Funzione D3DXFillCubeTextureTX</span><span class="sxs-lookup"><span data-stu-id="ca5d4-103">D3DXFillCubeTextureTX function</span></span>

<span data-ttu-id="ca5d4-104">Usa una funzione HLSL (High-Level Shader Language) compilata per riempire ogni texel di ogni livello mipmap di una trama.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5d4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca5d4-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="ca5d4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca5d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca5d4-107">*pTexture* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ca5d4-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5d4-108">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="ca5d4-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="ca5d4-109">Puntatore a [**un oggetto IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) che rappresenta la trama da riempire.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="ca5d4-110">*pTextureShader* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ca5d4-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca5d4-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="ca5d4-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="ca5d4-112">Puntatore a un oggetto shader con trama [**ID3DXTextureShader.**](id3dxtextureshader.md)</span><span class="sxs-lookup"><span data-stu-id="ca5d4-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca5d4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca5d4-113">Return value</span></span>

<span data-ttu-id="ca5d4-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca5d4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca5d4-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ca5d4-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca5d4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca5d4-117">Remarks</span></span>

<span data-ttu-id="ca5d4-118">La destinazione della trama deve essere una funzione HLSL che accetta contiene la semantica seguente:</span><span class="sxs-lookup"><span data-stu-id="ca5d4-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="ca5d4-119">Un parametro di input deve usare una semantica POSITION.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="ca5d4-120">Un parametro di input deve usare una semantica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="ca5d4-121">La funzione deve restituire un parametro che usa la semantica COLOR.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="ca5d4-122">I parametri di input possono essere in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="ca5d4-122">The input parameters can be in any order.</span></span> <span data-ttu-id="ca5d4-123">Per un esempio, vedere [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="ca5d4-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5d4-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca5d4-124">Requirements</span></span>



| <span data-ttu-id="ca5d4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5d4-125">Requirement</span></span> | <span data-ttu-id="ca5d4-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ca5d4-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5d4-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca5d4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ca5d4-128"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="ca5d4-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ca5d4-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca5d4-129">Library</span></span><br/> | <dl> <span data-ttu-id="ca5d4-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca5d4-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ca5d4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca5d4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5d4-132">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ca5d4-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="ca5d4-133">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="ca5d4-133">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
