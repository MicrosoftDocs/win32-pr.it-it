---
description: Restituisce un handle di evento all'evento successivo pianificato in modo che venga eseguito dopo un evento specificato in una traccia di animazione.
ms.assetid: 616b2de1-6107-4d18-ad2e-de2ef4560aee
title: 'Metodo ID3DXAnimationController:: GetUpcomingTrackEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f863ce918f25c6b0975010f71a63f067c01f7345
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969310"
---
# <a name="id3dxanimationcontrollergetupcomingtrackevent-method"></a><span data-ttu-id="01e9d-103">Metodo ID3DXAnimationController:: GetUpcomingTrackEvent</span><span class="sxs-lookup"><span data-stu-id="01e9d-103">ID3DXAnimationController::GetUpcomingTrackEvent method</span></span>

<span data-ttu-id="01e9d-104">Restituisce un handle di evento all'evento successivo pianificato in modo che venga eseguito dopo un evento specificato in una traccia di animazione.</span><span class="sxs-lookup"><span data-stu-id="01e9d-104">Returns an event handle to the next event scheduled to occur after a specified event on an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e9d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01e9d-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingTrackEvent(
  [in] UINT            Track,
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="01e9d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="01e9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01e9d-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e9d-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e9d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01e9d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01e9d-109">Identificatore di traccia.</span><span class="sxs-lookup"><span data-stu-id="01e9d-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="01e9d-110">*hEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01e9d-110">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01e9d-111">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="01e9d-111">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="01e9d-112">Handle di evento per un evento specificato dopo il quale cercare un evento successivo.</span><span class="sxs-lookup"><span data-stu-id="01e9d-112">Event handle to a specified event after which to search for a following event.</span></span> <span data-ttu-id="01e9d-113">Se impostato su **null**, il metodo restituirà l'evento pianificato successivo.</span><span class="sxs-lookup"><span data-stu-id="01e9d-113">If set to **NULL**, then the method will return the next scheduled event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01e9d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01e9d-114">Return value</span></span>

<span data-ttu-id="01e9d-115">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="01e9d-115">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="01e9d-116">Handle di evento per l'evento successivo pianificato per l'esecuzione nella traccia specificata. Se non è pianificato alcun nuovo evento, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="01e9d-116">Event handle to the next event scheduled to run on the specified track. **NULL** is returned if no new event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="01e9d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="01e9d-117">Remarks</span></span>

<span data-ttu-id="01e9d-118">Questo metodo può essere utilizzato in modo iterativo per individuare un evento desiderato passando ripetutamente **null** per hEvent.</span><span class="sxs-lookup"><span data-stu-id="01e9d-118">This method can be used iteratively to locate a desired event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="01e9d-119">Non scorrere ulteriormente dopo che il metodo ha restituito **null**.</span><span class="sxs-lookup"><span data-stu-id="01e9d-119">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01e9d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01e9d-120">Requirements</span></span>



| <span data-ttu-id="01e9d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e9d-121">Requirement</span></span> | <span data-ttu-id="01e9d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="01e9d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01e9d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01e9d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="01e9d-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="01e9d-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="01e9d-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="01e9d-125">Library</span></span><br/> | <dl> <span data-ttu-id="01e9d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01e9d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01e9d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01e9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e9d-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="01e9d-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
