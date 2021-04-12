---
description: Clona, o copia, un controller di animazione.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'Metodo ID3DXAnimationController:: CloneAnimationController (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355799"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a><span data-ttu-id="e10fb-103">Metodo ID3DXAnimationController:: CloneAnimationController</span><span class="sxs-lookup"><span data-stu-id="e10fb-103">ID3DXAnimationController::CloneAnimationController method</span></span>

<span data-ttu-id="e10fb-104">Clona, o copia, un controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="e10fb-104">Clones, or copies, an animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e10fb-105">Syntax</span></span>


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="e10fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e10fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10fb-107">*MaxNumAnimationOutputs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10fb-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10fb-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e10fb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e10fb-109">Numero massimo di output di animazione che il controller può supportare.</span><span class="sxs-lookup"><span data-stu-id="e10fb-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="e10fb-110">*MaxNumAnimationSets* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10fb-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10fb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e10fb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e10fb-112">Numero massimo di set di animazioni che il controller può supportare.</span><span class="sxs-lookup"><span data-stu-id="e10fb-112">Maximum number of animation sets the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="e10fb-113">*MaxNumTracks* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10fb-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10fb-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e10fb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e10fb-115">Numero massimo di tracce che il controller può supportare.</span><span class="sxs-lookup"><span data-stu-id="e10fb-115">Maximum number of tracks the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="e10fb-116">*MaxNumEvents* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10fb-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10fb-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e10fb-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e10fb-118">Numero massimo di eventi che il controller può supportare.</span><span class="sxs-lookup"><span data-stu-id="e10fb-118">Maximum number of events the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="e10fb-119">*ppAnimController* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e10fb-119">*ppAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e10fb-120">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="e10fb-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="e10fb-121">Indirizzo di un puntatore al controller di animazione [**ID3DXAnimationController**](id3dxanimationcontroller.md) clonato.</span><span class="sxs-lookup"><span data-stu-id="e10fb-121">Address of a pointer to the cloned [**ID3DXAnimationController**](id3dxanimationcontroller.md) animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10fb-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e10fb-122">Return value</span></span>

<span data-ttu-id="e10fb-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e10fb-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e10fb-124">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e10fb-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e10fb-125">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="e10fb-125">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10fb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e10fb-126">Requirements</span></span>



| <span data-ttu-id="e10fb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e10fb-127">Requirement</span></span> | <span data-ttu-id="e10fb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e10fb-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e10fb-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e10fb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e10fb-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e10fb-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e10fb-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="e10fb-131">Library</span></span><br/> | <dl> <span data-ttu-id="e10fb-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e10fb-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e10fb-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e10fb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10fb-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e10fb-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
