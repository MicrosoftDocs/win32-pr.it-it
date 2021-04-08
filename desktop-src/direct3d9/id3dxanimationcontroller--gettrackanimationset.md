---
description: Ottiene il set di animazioni per la traccia specificata.
ms.assetid: d40669ac-c391-4912-82d6-28c366a0f1dc
title: 'Metodo ID3DXAnimationController:: GetTrackAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7ba397fb876d94aa48f635785737ab0448ecef6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969424"
---
# <a name="id3dxanimationcontrollergettrackanimationset-method"></a><span data-ttu-id="1c08a-103">Metodo ID3DXAnimationController:: GetTrackAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1c08a-103">ID3DXAnimationController::GetTrackAnimationSet method</span></span>

<span data-ttu-id="1c08a-104">Ottiene il set di animazioni per la traccia specificata.</span><span class="sxs-lookup"><span data-stu-id="1c08a-104">Gets the animation set for the given track.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c08a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c08a-105">Syntax</span></span>


```C++
HRESULT GetTrackAnimationSet(
  [in]  UINT               Track,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="1c08a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c08a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c08a-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c08a-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c08a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c08a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c08a-109">Identificatore di traccia.</span><span class="sxs-lookup"><span data-stu-id="1c08a-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1c08a-110">*ppAnimSet* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c08a-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c08a-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c08a-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="1c08a-112">Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) per la traccia specificata.</span><span class="sxs-lookup"><span data-stu-id="1c08a-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set for the given track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c08a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c08a-113">Return value</span></span>

<span data-ttu-id="1c08a-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c08a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c08a-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1c08a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1c08a-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1c08a-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c08a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c08a-117">Requirements</span></span>



| <span data-ttu-id="1c08a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c08a-118">Requirement</span></span> | <span data-ttu-id="1c08a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1c08a-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c08a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c08a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1c08a-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c08a-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1c08a-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c08a-122">Library</span></span><br/> | <dl> <span data-ttu-id="1c08a-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c08a-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c08a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c08a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c08a-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="1c08a-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
