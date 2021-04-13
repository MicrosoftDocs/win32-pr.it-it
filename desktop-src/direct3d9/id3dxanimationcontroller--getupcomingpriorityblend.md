---
description: Restituisce un handle di evento per l'evento di Blend di priorità successivo pianificato per essere eseguito dopo un evento specificato.
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'Metodo ID3DXAnimationController:: GetUpcomingPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401926"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a><span data-ttu-id="5538a-103">Metodo ID3DXAnimationController:: GetUpcomingPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="5538a-103">ID3DXAnimationController::GetUpcomingPriorityBlend method</span></span>

<span data-ttu-id="5538a-104">Restituisce un handle di evento per l'evento di Blend di priorità successivo pianificato per essere eseguito dopo un evento specificato.</span><span class="sxs-lookup"><span data-stu-id="5538a-104">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="5538a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5538a-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="5538a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5538a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5538a-107">*hEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5538a-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5538a-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="5538a-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="5538a-109">Handle di evento per un evento specificato dopo il quale cercare un evento di combinazione di priorità successivo.</span><span class="sxs-lookup"><span data-stu-id="5538a-109">Event handle to a specified event after which to search for a following priority blend event.</span></span> <span data-ttu-id="5538a-110">Se impostato su **null**, il metodo restituirà l'evento di Blend di priorità pianificato successivo.</span><span class="sxs-lookup"><span data-stu-id="5538a-110">If set to **NULL**, then the method will return the next scheduled priority blend event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5538a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5538a-111">Return value</span></span>

<span data-ttu-id="5538a-112">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="5538a-112">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="5538a-113">Handle di evento per l'evento di Blend di priorità successivo pianificato.</span><span class="sxs-lookup"><span data-stu-id="5538a-113">Event handle to the next scheduled priority blend event.</span></span> <span data-ttu-id="5538a-114">Viene restituito **null** se non è pianificato alcun nuovo evento di Blend di priorità.</span><span class="sxs-lookup"><span data-stu-id="5538a-114">**NULL** is returned if no new priority blend event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="5538a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5538a-115">Remarks</span></span>

<span data-ttu-id="5538a-116">Questo metodo può essere utilizzato in modo iterativo per individuare un evento di Blend di priorità desiderato passando ripetutamente **null** per hEvent.</span><span class="sxs-lookup"><span data-stu-id="5538a-116">This method can be used iteratively to locate a desired priority blend event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="5538a-117">Non scorrere ulteriormente dopo che il metodo ha restituito **null**.</span><span class="sxs-lookup"><span data-stu-id="5538a-117">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5538a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5538a-118">Requirements</span></span>



| <span data-ttu-id="5538a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5538a-119">Requirement</span></span> | <span data-ttu-id="5538a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5538a-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5538a-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5538a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5538a-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5538a-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5538a-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="5538a-123">Library</span></span><br/> | <dl> <span data-ttu-id="5538a-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5538a-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5538a-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5538a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5538a-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="5538a-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




