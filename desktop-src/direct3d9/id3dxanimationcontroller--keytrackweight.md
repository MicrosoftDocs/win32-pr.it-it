---
description: Imposta una chiave evento che modifica il peso di una traccia di animazione. Il peso viene usato come moltiplicatore quando si combinano più tracce.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'Metodo ID3DXAnimationController:: KeyTrackWeight (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323293"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a><span data-ttu-id="c4bdf-103">Metodo ID3DXAnimationController:: KeyTrackWeight</span><span class="sxs-lookup"><span data-stu-id="c4bdf-103">ID3DXAnimationController::KeyTrackWeight method</span></span>

<span data-ttu-id="c4bdf-104">Imposta una chiave evento che modifica il peso di una traccia di animazione. Il peso viene usato come moltiplicatore quando si combinano più tracce.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-104">Sets an event key that changes the weight of an animation track. The weight is used as a multiplier when combining multiple tracks together.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bdf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4bdf-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="c4bdf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4bdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4bdf-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bdf-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bdf-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4bdf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4bdf-109">Identificatore della traccia da modificare.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="c4bdf-110">*NewWeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bdf-110">*NewWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bdf-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4bdf-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4bdf-112">Nuovo peso della traccia.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-112">New weight of the track.</span></span>

</dd> <dt>

<span data-ttu-id="c4bdf-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bdf-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bdf-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4bdf-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4bdf-115">Chiave temporale globale.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-115">Global time key.</span></span> <span data-ttu-id="c4bdf-116">Specifica l'ora globale in cui verrà eseguita la modifica.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-116">Specifies the global time when the change will take place.</span></span>

</dd> <dt>

<span data-ttu-id="c4bdf-117">*Durata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bdf-117">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bdf-118">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4bdf-118">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4bdf-119">Tempo di transizione, che specifica il tempo necessario per il completamento della transizione senza problemi.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-119">Transition time, which specifies how long the smooth transition will take to complete.</span></span>

</dd> <dt>

<span data-ttu-id="c4bdf-120">*Transizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bdf-120">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bdf-121">Tipo: **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="c4bdf-121">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="c4bdf-122">Specifica il tipo di transizione utilizzato per la transizione tra pesi.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-122">Specifies the transition type used for transitioning between weights.</span></span> <span data-ttu-id="c4bdf-123">Vedere [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="c4bdf-123">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4bdf-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4bdf-124">Return value</span></span>

<span data-ttu-id="c4bdf-125">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="c4bdf-125">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="c4bdf-126">Handle di evento per l'evento di combinazione di priorità.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-126">Event handle to the priority blend event.</span></span> <span data-ttu-id="c4bdf-127">Se uno o più parametri di input non sono validi oppure non è disponibile alcun evento libero, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="c4bdf-127">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4bdf-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4bdf-128">Remarks</span></span>

<span data-ttu-id="c4bdf-129">Il peso viene usato come un moltiplicatore per determinare la quantità di questa traccia da unire insieme ad altre tracce.</span><span class="sxs-lookup"><span data-stu-id="c4bdf-129">The weight is used like a multiplier to determine how much of this track to blend together with other tracks.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4bdf-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4bdf-130">Requirements</span></span>



| <span data-ttu-id="c4bdf-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4bdf-131">Requirement</span></span> | <span data-ttu-id="c4bdf-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c4bdf-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bdf-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4bdf-133">Header</span></span><br/>  | <dl> <span data-ttu-id="c4bdf-134"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4bdf-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c4bdf-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4bdf-135">Library</span></span><br/> | <dl> <span data-ttu-id="c4bdf-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4bdf-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4bdf-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4bdf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4bdf-138">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="c4bdf-138">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
