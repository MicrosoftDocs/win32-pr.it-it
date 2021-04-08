---
description: Imposta il peso della traccia. Il peso viene usato per determinare come unire più tracce.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: 'Metodo ID3DXAnimationController:: SetTrackWeight (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762364"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a><span data-ttu-id="b48e1-104">Metodo ID3DXAnimationController:: SetTrackWeight</span><span class="sxs-lookup"><span data-stu-id="b48e1-104">ID3DXAnimationController::SetTrackWeight method</span></span>

<span data-ttu-id="b48e1-105">Imposta il peso della traccia.</span><span class="sxs-lookup"><span data-stu-id="b48e1-105">Sets the track weight.</span></span> <span data-ttu-id="b48e1-106">Il peso viene usato per determinare come unire più tracce.</span><span class="sxs-lookup"><span data-stu-id="b48e1-106">The weight is used to determine how to blend multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48e1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b48e1-107">Syntax</span></span>


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a><span data-ttu-id="b48e1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b48e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b48e1-109">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b48e1-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b48e1-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b48e1-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b48e1-111">Identificatore della traccia su cui impostare il peso.</span><span class="sxs-lookup"><span data-stu-id="b48e1-111">Identifier of the track to set the weight on.</span></span>

</dd> <dt>

<span data-ttu-id="b48e1-112">*Peso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b48e1-112">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b48e1-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b48e1-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b48e1-114">Valore del peso.</span><span class="sxs-lookup"><span data-stu-id="b48e1-114">Weight value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b48e1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b48e1-115">Return value</span></span>

<span data-ttu-id="b48e1-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b48e1-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b48e1-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b48e1-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b48e1-118">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b48e1-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48e1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b48e1-119">Requirements</span></span>



| <span data-ttu-id="b48e1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b48e1-120">Requirement</span></span> | <span data-ttu-id="b48e1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b48e1-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b48e1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b48e1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b48e1-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b48e1-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b48e1-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="b48e1-124">Library</span></span><br/> | <dl> <span data-ttu-id="b48e1-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b48e1-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b48e1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b48e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48e1-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="b48e1-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
