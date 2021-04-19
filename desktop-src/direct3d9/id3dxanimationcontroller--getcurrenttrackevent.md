---
description: Restituisce un handle di evento per l'evento attualmente in esecuzione sulla traccia di animazione specificata.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'Metodo ID3DXAnimationController:: GetCurrentTrackEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323174"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a><span data-ttu-id="e8b13-103">Metodo ID3DXAnimationController:: GetCurrentTrackEvent</span><span class="sxs-lookup"><span data-stu-id="e8b13-103">ID3DXAnimationController::GetCurrentTrackEvent method</span></span>

<span data-ttu-id="e8b13-104">Restituisce un handle di evento per l'evento attualmente in esecuzione sulla traccia di animazione specificata.</span><span class="sxs-lookup"><span data-stu-id="e8b13-104">Returns an event handle to the event currently running on the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b13-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8b13-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a><span data-ttu-id="e8b13-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8b13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8b13-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8b13-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b13-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8b13-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8b13-109">Identificatore di traccia.</span><span class="sxs-lookup"><span data-stu-id="e8b13-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e8b13-110">*EventType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8b13-110">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b13-111">Tipo: **[ **D3DXEVENT \_**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e8b13-111">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

<span data-ttu-id="e8b13-112">Tipo di evento su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="e8b13-112">Type of event to query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8b13-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8b13-113">Return value</span></span>

<span data-ttu-id="e8b13-114">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="e8b13-114">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="e8b13-115">Handle di evento per l'evento attualmente in esecuzione nella traccia specificata. Se non è in esecuzione alcun evento nella traccia specificata, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="e8b13-115">Event handle to the event currently running on the specified track. **NULL** is returned if no event is running on the specified track.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b13-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8b13-116">Requirements</span></span>



| <span data-ttu-id="e8b13-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8b13-117">Requirement</span></span> | <span data-ttu-id="e8b13-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e8b13-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b13-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8b13-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e8b13-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b13-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e8b13-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8b13-121">Library</span></span><br/> | <dl> <span data-ttu-id="e8b13-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8b13-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e8b13-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8b13-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b13-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e8b13-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
