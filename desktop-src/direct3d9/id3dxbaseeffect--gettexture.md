---
description: Ottiene una trama.
ms.assetid: e009ccc2-4491-4976-9460-7478b2bd34c2
title: 'Metodo ID3DXBaseEffect:: GetTexture (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 25ef71df1f9dcd84bbe6726fd3a13f9ec09eff17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761944"
---
# <a name="id3dxbaseeffectgettexture-method"></a><span data-ttu-id="12631-103">Metodo ID3DXBaseEffect:: GetTexture</span><span class="sxs-lookup"><span data-stu-id="12631-103">ID3DXBaseEffect::GetTexture method</span></span>

<span data-ttu-id="12631-104">Ottiene una trama.</span><span class="sxs-lookup"><span data-stu-id="12631-104">Gets a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="12631-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12631-105">Syntax</span></span>


```C++
HRESULT GetTexture(
  [in]  D3DXHANDLE             hParameter,
  [out] LPDIRECT3DBASETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="12631-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12631-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12631-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12631-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="12631-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="12631-109">Identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="12631-109">Unique identifier.</span></span> <span data-ttu-id="12631-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="12631-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="12631-111">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="12631-111">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12631-112">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="12631-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)\***</span></span>

<span data-ttu-id="12631-113">Restituisce un oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="12631-113">Returns a texture object.</span></span> <span data-ttu-id="12631-114">Vedere [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="12631-114">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12631-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12631-115">Return value</span></span>

<span data-ttu-id="12631-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12631-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12631-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12631-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="12631-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="12631-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="12631-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12631-119">Requirements</span></span>



| <span data-ttu-id="12631-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12631-120">Requirement</span></span> | <span data-ttu-id="12631-121">Valore</span><span class="sxs-lookup"><span data-stu-id="12631-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12631-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12631-122">Header</span></span><br/>  | <dl> <span data-ttu-id="12631-123"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="12631-123"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="12631-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="12631-124">Library</span></span><br/> | <dl> <span data-ttu-id="12631-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12631-125"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="12631-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12631-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12631-127">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="12631-127">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="12631-128">**SetTexture**</span><span class="sxs-lookup"><span data-stu-id="12631-128">**SetTexture**</span></span>](id3dxbaseeffect--settexture.md)
</dt> </dl>

 

 
