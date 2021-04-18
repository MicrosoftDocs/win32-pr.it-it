---
description: Applica il set di animazioni alla traccia specificata.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: 'Metodo ID3DXAnimationController:: SetTrackAnimationSet (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dce979e48ed118dc257c147b27615f7bbc89231
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323284"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a><span data-ttu-id="1cd04-103">Metodo ID3DXAnimationController:: SetTrackAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1cd04-103">ID3DXAnimationController::SetTrackAnimationSet method</span></span>

<span data-ttu-id="1cd04-104">Applica il set di animazioni alla traccia specificata.</span><span class="sxs-lookup"><span data-stu-id="1cd04-104">Applies the animation set to the specified track.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd04-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cd04-105">Syntax</span></span>


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="1cd04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cd04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd04-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cd04-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd04-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cd04-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cd04-109">Identificatore della traccia a cui viene applicato il set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="1cd04-109">Identifier of the track to which the animation set is applied.</span></span>

</dd> <dt>

<span data-ttu-id="1cd04-110">*pAnimSet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cd04-110">*pAnimSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd04-111">Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span><span class="sxs-lookup"><span data-stu-id="1cd04-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)**</span></span>

<span data-ttu-id="1cd04-112">Puntatore al set di animazioni [**ID3DXAnimationSet**](id3dxanimationset.md) da aggiungere alla traccia.</span><span class="sxs-lookup"><span data-stu-id="1cd04-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set to be added to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd04-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cd04-113">Return value</span></span>

<span data-ttu-id="1cd04-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1cd04-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1cd04-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1cd04-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1cd04-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1cd04-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd04-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cd04-117">Remarks</span></span>

<span data-ttu-id="1cd04-118">Questo metodo imposta il set di animazioni sulla traccia specificata per la combinazione.</span><span class="sxs-lookup"><span data-stu-id="1cd04-118">This method sets the animation set to the specified track for mixing.</span></span> <span data-ttu-id="1cd04-119">Il set di animazioni per ogni traccia viene mescolato in base al peso e alla velocità della traccia quando viene chiamato [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) .</span><span class="sxs-lookup"><span data-stu-id="1cd04-119">The animation set for each track is blended according to the track weight and speed when [**AdvanceTime**](id3dxanimationcontroller--advancetime.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd04-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cd04-120">Requirements</span></span>



| <span data-ttu-id="1cd04-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cd04-121">Requirement</span></span> | <span data-ttu-id="1cd04-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1cd04-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd04-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cd04-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1cd04-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cd04-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1cd04-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cd04-125">Library</span></span><br/> | <dl> <span data-ttu-id="1cd04-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cd04-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1cd04-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cd04-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cd04-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="1cd04-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
