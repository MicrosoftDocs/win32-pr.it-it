---
description: Imposta il peso della combinazione di priorità usato dal controller di animazione.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'Metodo ID3DXAnimationController:: SetPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323285"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a><span data-ttu-id="c5532-103">Metodo ID3DXAnimationController:: SetPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="c5532-103">ID3DXAnimationController::SetPriorityBlend method</span></span>

<span data-ttu-id="c5532-104">Imposta il peso della combinazione di priorità usato dal controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="c5532-104">Sets the priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5532-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5532-105">Syntax</span></span>


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a><span data-ttu-id="c5532-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5532-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5532-107">*BlendWeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5532-107">*BlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5532-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5532-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5532-109">Peso della combinazione di priorità usato dal controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="c5532-109">Priority blending weight used by the animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5532-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5532-110">Return value</span></span>

<span data-ttu-id="c5532-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5532-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5532-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5532-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c5532-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c5532-113">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5532-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5532-114">Remarks</span></span>

<span data-ttu-id="c5532-115">Il peso della Blend viene usato per unire le tracce con priorità alta e bassa.</span><span class="sxs-lookup"><span data-stu-id="c5532-115">The blend weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5532-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5532-116">Requirements</span></span>



| <span data-ttu-id="c5532-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5532-117">Requirement</span></span> | <span data-ttu-id="c5532-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c5532-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5532-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5532-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c5532-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5532-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c5532-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5532-121">Library</span></span><br/> | <dl> <span data-ttu-id="c5532-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5532-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5532-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5532-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5532-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c5532-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="c5532-125">**GetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="c5532-125">**GetPriorityBlend**</span></span>](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
