---
description: Rimuove un evento specificato da una traccia di animazione, impedendo l'esecuzione dell'evento.
ms.assetid: 658ffe91-44ba-4bde-b78c-c545dff27ab1
title: 'Metodo ID3DXAnimationController:: UnkeyEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac0c9d6a643337c43a5cadd5bcfe0b090cd39a00
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355944"
---
# <a name="id3dxanimationcontrollerunkeyevent-method"></a><span data-ttu-id="d4407-103">Metodo ID3DXAnimationController:: UnkeyEvent</span><span class="sxs-lookup"><span data-stu-id="d4407-103">ID3DXAnimationController::UnkeyEvent method</span></span>

<span data-ttu-id="d4407-104">Rimuove un evento specificato da una traccia di animazione, impedendo l'esecuzione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="d4407-104">Removes a specified event from an animation track, preventing the execution of the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4407-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4407-105">Syntax</span></span>


```C++
HRESULT UnkeyEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="d4407-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4407-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4407-107">*hEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4407-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4407-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="d4407-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="d4407-109">Handle di evento per l'evento da rimuovere dalla traccia dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="d4407-109">Event handle to the event to be removed from the animation track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4407-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4407-110">Return value</span></span>

<span data-ttu-id="d4407-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4407-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4407-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4407-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4407-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d4407-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4407-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4407-114">Requirements</span></span>



| <span data-ttu-id="d4407-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4407-115">Requirement</span></span> | <span data-ttu-id="d4407-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d4407-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4407-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4407-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d4407-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4407-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d4407-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4407-119">Library</span></span><br/> | <dl> <span data-ttu-id="d4407-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4407-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4407-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4407-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4407-122">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="d4407-122">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




