---
description: Cerca la tecnica valida successiva, iniziando dalla tecnica dopo la tecnica specificata.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'Metodo ID3DXEffect:: FindNextValidTechnique (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401971"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a><span data-ttu-id="8bc83-103">Metodo ID3DXEffect:: FindNextValidTechnique</span><span class="sxs-lookup"><span data-stu-id="8bc83-103">ID3DXEffect::FindNextValidTechnique method</span></span>

<span data-ttu-id="8bc83-104">Cerca la tecnica valida successiva, iniziando dalla tecnica dopo la tecnica specificata.</span><span class="sxs-lookup"><span data-stu-id="8bc83-104">Searches for the next valid technique, starting at the technique after the specified technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bc83-105">Syntax</span></span>


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="8bc83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bc83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bc83-107">*hTechnique* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bc83-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc83-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="8bc83-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="8bc83-109">Identificatore univoco di una tecnica.</span><span class="sxs-lookup"><span data-stu-id="8bc83-109">Unique identifier to a technique.</span></span> <span data-ttu-id="8bc83-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8bc83-110">See [Handles (Direct3D 9)](handles.md).</span></span> <span data-ttu-id="8bc83-111">Specificare **null** per questo parametro per trovare la prima tecnica valida.</span><span class="sxs-lookup"><span data-stu-id="8bc83-111">Specify **NULL** for this parameter to find the first valid technique.</span></span>

</dd> <dt>

<span data-ttu-id="8bc83-112">*pTechnique* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8bc83-112">*pTechnique* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc83-113">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span><span class="sxs-lookup"><span data-stu-id="8bc83-113">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***</span></span>

<span data-ttu-id="8bc83-114">Puntatore a un identificatore per la tecnica successiva.</span><span class="sxs-lookup"><span data-stu-id="8bc83-114">Pointer to an identifier for the next technique.</span></span> <span data-ttu-id="8bc83-115">Se si tratta dell'ultima tecnica, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="8bc83-115">**NULL** is returned if this is the last technique.</span></span> <span data-ttu-id="8bc83-116">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="8bc83-116">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bc83-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bc83-117">Return value</span></span>

<span data-ttu-id="8bc83-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8bc83-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8bc83-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8bc83-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8bc83-120">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8bc83-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc83-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bc83-121">Requirements</span></span>



| <span data-ttu-id="8bc83-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bc83-122">Requirement</span></span> | <span data-ttu-id="8bc83-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8bc83-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc83-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bc83-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8bc83-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bc83-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8bc83-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="8bc83-126">Library</span></span><br/> | <dl> <span data-ttu-id="8bc83-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bc83-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8bc83-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bc83-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc83-129">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8bc83-129">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="8bc83-130">**D3DXTECHNIQUE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="8bc83-130">**D3DXTECHNIQUE\_DESC**</span></span>](d3dxtechnique-desc.md)
</dt> <dt>

[<span data-ttu-id="8bc83-131">**ID3DXEffect::ValidateTechnique**</span><span class="sxs-lookup"><span data-stu-id="8bc83-131">**ID3DXEffect::ValidateTechnique**</span></span>](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




