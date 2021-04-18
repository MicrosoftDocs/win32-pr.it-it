---
description: Imposta il peso della combinazione di priorità per la traccia di animazione specificata.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'Metodo ID3DXAnimationController:: SetTrackPriority (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 32f1f8cce4641203782b0a84840d2986780da26a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323642"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a><span data-ttu-id="38c64-103">Metodo ID3DXAnimationController:: SetTrackPriority</span><span class="sxs-lookup"><span data-stu-id="38c64-103">ID3DXAnimationController::SetTrackPriority method</span></span>

<span data-ttu-id="38c64-104">Imposta il peso della combinazione di priorità per la traccia di animazione specificata.</span><span class="sxs-lookup"><span data-stu-id="38c64-104">Sets the priority blending weight for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="38c64-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38c64-105">Syntax</span></span>


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a><span data-ttu-id="38c64-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="38c64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c64-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38c64-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c64-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38c64-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38c64-109">Identificatore di traccia.</span><span class="sxs-lookup"><span data-stu-id="38c64-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="38c64-110">*Priorità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="38c64-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c64-111">Tipo: **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**</span><span class="sxs-lookup"><span data-stu-id="38c64-111">Type: **[**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md)**</span></span>

<span data-ttu-id="38c64-112">Tenere traccia della priorità.</span><span class="sxs-lookup"><span data-stu-id="38c64-112">Track priority.</span></span> <span data-ttu-id="38c64-113">Questo parametro deve essere impostato su una delle costanti dal [**\_ tipo D3DXPRIORITY**](./d3dxpriority-type.md).</span><span class="sxs-lookup"><span data-stu-id="38c64-113">This parameter should be set to one of the constants from [**D3DXPRIORITY\_TYPE**](./d3dxpriority-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c64-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38c64-114">Return value</span></span>

<span data-ttu-id="38c64-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38c64-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38c64-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38c64-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="38c64-117">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="38c64-117">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="38c64-118">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="38c64-118">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="38c64-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38c64-119">Requirements</span></span>



| <span data-ttu-id="38c64-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="38c64-120">Requirement</span></span> | <span data-ttu-id="38c64-121">Valore</span><span class="sxs-lookup"><span data-stu-id="38c64-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38c64-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38c64-122">Header</span></span><br/>  | <dl> <span data-ttu-id="38c64-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="38c64-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="38c64-124">Library</span></span><br/> | <dl> <span data-ttu-id="38c64-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38c64-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38c64-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38c64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c64-127">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="38c64-127">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
