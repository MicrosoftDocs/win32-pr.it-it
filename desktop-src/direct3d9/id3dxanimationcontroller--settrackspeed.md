---
description: Imposta la velocità della traccia. La velocità della traccia è simile a un moltiplicatore usato per velocizzare o rallentare la riproduzione della traccia.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'Metodo ID3DXAnimationController:: SetTrackSpeed (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355954"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a><span data-ttu-id="a0f3c-104">Metodo ID3DXAnimationController:: SetTrackSpeed</span><span class="sxs-lookup"><span data-stu-id="a0f3c-104">ID3DXAnimationController::SetTrackSpeed method</span></span>

<span data-ttu-id="a0f3c-105">Imposta la velocità della traccia.</span><span class="sxs-lookup"><span data-stu-id="a0f3c-105">Sets the track speed.</span></span> <span data-ttu-id="a0f3c-106">La velocità della traccia è simile a un moltiplicatore usato per velocizzare o rallentare la riproduzione della traccia.</span><span class="sxs-lookup"><span data-stu-id="a0f3c-106">The track speed is similar to a multiplier that is used to speed up or slow down the playback of the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f3c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0f3c-107">Syntax</span></span>


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a><span data-ttu-id="a0f3c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f3c-109">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f3c-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3c-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3c-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3c-111">Identificatore della traccia su cui impostare la velocità.</span><span class="sxs-lookup"><span data-stu-id="a0f3c-111">Identifier of the track to set the speed on.</span></span>

</dd> <dt>

<span data-ttu-id="a0f3c-112">*Velocità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0f3c-112">*Speed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0f3c-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0f3c-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0f3c-114">Nuova velocità.</span><span class="sxs-lookup"><span data-stu-id="a0f3c-114">New speed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f3c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f3c-115">Return value</span></span>

<span data-ttu-id="a0f3c-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0f3c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0f3c-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0f3c-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a0f3c-118">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a0f3c-118">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f3c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f3c-119">Requirements</span></span>



| <span data-ttu-id="a0f3c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f3c-120">Requirement</span></span> | <span data-ttu-id="a0f3c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a0f3c-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f3c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f3c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a0f3c-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f3c-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a0f3c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0f3c-124">Library</span></span><br/> | <dl> <span data-ttu-id="a0f3c-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0f3c-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0f3c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f3c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f3c-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="a0f3c-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
