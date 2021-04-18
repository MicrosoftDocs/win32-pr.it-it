---
description: Ottiene una descrizione del passaggio.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'Metodo ID3DXBaseEffect:: GetPassDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323590"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a><span data-ttu-id="35a1f-103">Metodo ID3DXBaseEffect:: GetPassDesc</span><span class="sxs-lookup"><span data-stu-id="35a1f-103">ID3DXBaseEffect::GetPassDesc method</span></span>

<span data-ttu-id="35a1f-104">Ottiene una descrizione del passaggio.</span><span class="sxs-lookup"><span data-stu-id="35a1f-104">Gets a pass description.</span></span>

## <a name="syntax"></a><span data-ttu-id="35a1f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35a1f-105">Syntax</span></span>


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="35a1f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35a1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35a1f-107">*hPass* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35a1f-107">*hPass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35a1f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="35a1f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="35a1f-109">Handle di pass.</span><span class="sxs-lookup"><span data-stu-id="35a1f-109">Pass handle.</span></span> <span data-ttu-id="35a1f-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="35a1f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="35a1f-111">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35a1f-111">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35a1f-112">Tipo: **[ **D3DXPASS \_ desc**](d3dxpass-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="35a1f-112">Type: **[**D3DXPASS\_DESC**](d3dxpass-desc.md)\***</span></span>

<span data-ttu-id="35a1f-113">Restituisce una descrizione del passaggio specificato.</span><span class="sxs-lookup"><span data-stu-id="35a1f-113">Returns a description of the specified pass.</span></span> <span data-ttu-id="35a1f-114">Vedere [**D3DXPASS \_ desc**](d3dxpass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="35a1f-114">See [**D3DXPASS\_DESC**](d3dxpass-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35a1f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35a1f-115">Return value</span></span>

<span data-ttu-id="35a1f-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35a1f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35a1f-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35a1f-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="35a1f-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="35a1f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a1f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a1f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35a1f-120">Se viene creato un effetto con [D3DXFX \_ non \_ clonabile](d3dxfx.md), questo metodo restituirà puntatori **null** (in [**D3DXPASS \_ desc**](d3dxpass-desc.md)) alle funzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="35a1f-120">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this method will return **NULL** pointers (in [**D3DXPASS\_DESC**](d3dxpass-desc.md)) to the shader functions.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35a1f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35a1f-121">Requirements</span></span>



| <span data-ttu-id="35a1f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="35a1f-122">Requirement</span></span> | <span data-ttu-id="35a1f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="35a1f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a1f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35a1f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="35a1f-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="35a1f-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="35a1f-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="35a1f-126">Library</span></span><br/> | <dl> <span data-ttu-id="35a1f-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35a1f-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="35a1f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35a1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35a1f-129">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="35a1f-129">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




