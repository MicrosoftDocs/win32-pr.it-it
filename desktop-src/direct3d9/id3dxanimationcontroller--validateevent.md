---
description: Verifica se un handle di evento specificato è valido e se l'evento di animazione non è stato ancora completato.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'Metodo ID3DXAnimationController:: ValidateEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323634"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a><span data-ttu-id="c84cc-103">Metodo ID3DXAnimationController:: ValidateEvent</span><span class="sxs-lookup"><span data-stu-id="c84cc-103">ID3DXAnimationController::ValidateEvent method</span></span>

<span data-ttu-id="c84cc-104">Verifica se un handle di evento specificato è valido e se l'evento di animazione non è stato ancora completato.</span><span class="sxs-lookup"><span data-stu-id="c84cc-104">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c84cc-105">Syntax</span></span>


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="c84cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c84cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c84cc-107">*hEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c84cc-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84cc-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="c84cc-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="c84cc-109">Handle di evento per un evento di animazione.</span><span class="sxs-lookup"><span data-stu-id="c84cc-109">Event handle to an animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c84cc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c84cc-110">Return value</span></span>

<span data-ttu-id="c84cc-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c84cc-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c84cc-112">Restituisce \_ OK se l'handle dell'evento è valido e l'evento non è stato ancora completato.</span><span class="sxs-lookup"><span data-stu-id="c84cc-112">Returns S\_OK if the event handle is valid and the event has not yet completed.</span></span>

<span data-ttu-id="c84cc-113">Restituisce E ha \_ esito negativo se l'handle dell'evento non è valido e/o l'evento è stato completato.</span><span class="sxs-lookup"><span data-stu-id="c84cc-113">Returns E\_FAIL if the event handle is invalid and/or the event has completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="c84cc-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c84cc-114">Remarks</span></span>

<span data-ttu-id="c84cc-115">Il metodo indicherà che un handle di evento è valido anche se l'evento è in esecuzione ma non è stato ancora completato.</span><span class="sxs-lookup"><span data-stu-id="c84cc-115">The method will indicate that an event handle is valid even if the event is running but has not yet completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84cc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c84cc-116">Requirements</span></span>



| <span data-ttu-id="c84cc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84cc-117">Requirement</span></span> | <span data-ttu-id="c84cc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c84cc-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c84cc-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c84cc-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c84cc-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c84cc-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c84cc-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="c84cc-121">Library</span></span><br/> | <dl> <span data-ttu-id="c84cc-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c84cc-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c84cc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c84cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84cc-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c84cc-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




