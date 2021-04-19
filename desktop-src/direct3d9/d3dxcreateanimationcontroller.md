---
description: Crea un oggetto controller di animazione.
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: Funzione D3DXCreateAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322612"
---
# <a name="d3dxcreateanimationcontroller-function"></a><span data-ttu-id="e4dc7-103">D3DXCreateAnimationController (funzione)</span><span class="sxs-lookup"><span data-stu-id="e4dc7-103">D3DXCreateAnimationController function</span></span>

<span data-ttu-id="e4dc7-104">Crea un oggetto controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-104">Creates an animation controller object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4dc7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4dc7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="e4dc7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4dc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4dc7-107">*MaxNumAnimationOutputs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4dc7-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4dc7-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4dc7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4dc7-109">Numero massimo di output di animazione che il controller può supportare.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="e4dc7-110">*MaxNumAnimationSets* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4dc7-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4dc7-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4dc7-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4dc7-112">Numero massimo di set di animazioni che è possibile combinare.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-112">Maximum number of animation sets that can be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="e4dc7-113">*MaxNumTracks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4dc7-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4dc7-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4dc7-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4dc7-115">Numero massimo di set di animazioni che è possibile combinare simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-115">Maximum number of animation sets that can be mixed simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="e4dc7-116">*MaxNumEvents* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4dc7-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4dc7-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4dc7-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4dc7-118">Numero massimo di eventi in attesa che il controller supporterà.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-118">Maximum number of outstanding events that the controller will support.</span></span>

</dd> <dt>

<span data-ttu-id="e4dc7-119">*ppAnimController* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e4dc7-119">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4dc7-120">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4dc7-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="e4dc7-121">Puntatore all'oggetto controller di animazione creato.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-121">Pointer to the animation controller object created.</span></span> <span data-ttu-id="e4dc7-122">Vedere [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="e4dc7-122">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4dc7-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4dc7-123">Return value</span></span>

<span data-ttu-id="e4dc7-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4dc7-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4dc7-125">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e4dc7-126">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-126">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4dc7-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4dc7-127">Remarks</span></span>

<span data-ttu-id="e4dc7-128">Un controller di animazione controlla un mixer di animazioni.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-128">An animation controller controls an animation mixer.</span></span> <span data-ttu-id="e4dc7-129">Il controller aggiunge metodi per modificare i parametri di fusione nel tempo per consentire transizioni senza problemi.</span><span class="sxs-lookup"><span data-stu-id="e4dc7-129">The controller adds methods to modify blending parameters over time to enable smooth transitions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4dc7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4dc7-130">Requirements</span></span>



| <span data-ttu-id="e4dc7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4dc7-131">Requirement</span></span> | <span data-ttu-id="e4dc7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e4dc7-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4dc7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4dc7-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e4dc7-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4dc7-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e4dc7-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4dc7-135">Library</span></span><br/> | <dl> <span data-ttu-id="e4dc7-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4dc7-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4dc7-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4dc7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4dc7-138">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="e4dc7-138">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
