---
description: Ottiene una descrizione di un evento di animazione specificato.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'Metodo ID3DXAnimationController:: GetEventDesc (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323507"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a><span data-ttu-id="c4b6a-103">Metodo ID3DXAnimationController:: GetEventDesc</span><span class="sxs-lookup"><span data-stu-id="c4b6a-103">ID3DXAnimationController::GetEventDesc method</span></span>

<span data-ttu-id="c4b6a-104">Ottiene una descrizione di un evento di animazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c4b6a-104">Gets a description of a specified animation event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b6a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4b6a-105">Syntax</span></span>


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="c4b6a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4b6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4b6a-107">*hEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4b6a-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b6a-108">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="c4b6a-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="c4b6a-109">Handle di evento per un evento di animazione da descrivere.</span><span class="sxs-lookup"><span data-stu-id="c4b6a-109">Event handle to an animation event to describe.</span></span>

</dd> <dt>

<span data-ttu-id="c4b6a-110">*pDesc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c4b6a-110">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b6a-111">Tipo: **[ **LPD3DXEVENT \_ desc**](d3dxevent-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="c4b6a-111">Type: **[**LPD3DXEVENT\_DESC**](d3dxevent-desc.md)**</span></span>

<span data-ttu-id="c4b6a-112">Puntatore a una struttura [**D3DXEVENT \_ desc**](d3dxevent-desc.md) che contiene una descrizione dell'evento di animazione.</span><span class="sxs-lookup"><span data-stu-id="c4b6a-112">Pointer to a [**D3DXEVENT\_DESC**](d3dxevent-desc.md) structure that contains a description of the animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4b6a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4b6a-113">Return value</span></span>

<span data-ttu-id="c4b6a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4b6a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4b6a-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4b6a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c4b6a-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c4b6a-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4b6a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4b6a-117">Requirements</span></span>



| <span data-ttu-id="c4b6a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4b6a-118">Requirement</span></span> | <span data-ttu-id="c4b6a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c4b6a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b6a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4b6a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c4b6a-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4b6a-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c4b6a-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4b6a-122">Library</span></span><br/> | <dl> <span data-ttu-id="c4b6a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4b6a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4b6a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4b6a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4b6a-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c4b6a-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




