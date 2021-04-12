---
description: Restituisce un handle di evento a un evento di combinazione di priorità attualmente in esecuzione.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'Metodo ID3DXAnimationController:: GetCurrentPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df8b52a5bd5267cf88eaf101a0589000099dd600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355794"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a><span data-ttu-id="f878d-103">Metodo ID3DXAnimationController:: GetCurrentPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="f878d-103">ID3DXAnimationController::GetCurrentPriorityBlend method</span></span>

<span data-ttu-id="f878d-104">Restituisce un handle di evento a un evento di combinazione di priorità attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f878d-104">Returns an event handle to a priority blend event that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="f878d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f878d-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="f878d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f878d-106">Parameters</span></span>

<span data-ttu-id="f878d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f878d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f878d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f878d-108">Return value</span></span>

<span data-ttu-id="f878d-109">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="f878d-109">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="f878d-110">Handle dell'evento per l'evento di combinazione di priorità attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f878d-110">Event handle to the currently running priority blend event.</span></span> <span data-ttu-id="f878d-111">Se non è attualmente in esecuzione alcun evento di Blend di priorità, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="f878d-111">**NULL** is returned if no priority blend event is currently running.</span></span>

## <a name="requirements"></a><span data-ttu-id="f878d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f878d-112">Requirements</span></span>



| <span data-ttu-id="f878d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f878d-113">Requirement</span></span> | <span data-ttu-id="f878d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f878d-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f878d-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f878d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f878d-116"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f878d-116"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f878d-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="f878d-117">Library</span></span><br/> | <dl> <span data-ttu-id="f878d-118"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f878d-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f878d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f878d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f878d-120">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="f878d-120">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




