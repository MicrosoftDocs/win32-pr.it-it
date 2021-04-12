---
description: Imposta una chiave evento che modifica l'ora locale di una traccia di animazione.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'Metodo ID3DXAnimationController:: KeyTrackPosition (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355509"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a><span data-ttu-id="a23f3-103">Metodo ID3DXAnimationController:: KeyTrackPosition</span><span class="sxs-lookup"><span data-stu-id="a23f3-103">ID3DXAnimationController::KeyTrackPosition method</span></span>

<span data-ttu-id="a23f3-104">Imposta una chiave evento che modifica l'ora locale di una traccia di animazione.</span><span class="sxs-lookup"><span data-stu-id="a23f3-104">Sets an event key that changes the local time of an animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a23f3-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a><span data-ttu-id="a23f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a23f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a23f3-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f3-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a23f3-109">Identificatore della traccia da modificare.</span><span class="sxs-lookup"><span data-stu-id="a23f3-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="a23f3-110">*NewPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f3-110">*NewPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f3-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f3-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a23f3-112">Nuova ora locale della traccia dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="a23f3-112">New local time of the animation track.</span></span>

</dd> <dt>

<span data-ttu-id="a23f3-113">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f3-113">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f3-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f3-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a23f3-115">Chiave temporale globale.</span><span class="sxs-lookup"><span data-stu-id="a23f3-115">Global time key.</span></span> <span data-ttu-id="a23f3-116">Specifica l'ora globale in cui verrà eseguita la modifica.</span><span class="sxs-lookup"><span data-stu-id="a23f3-116">Specifies the global time when the change will take place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a23f3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a23f3-117">Return value</span></span>

<span data-ttu-id="a23f3-118">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f3-118">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="a23f3-119">Handle di evento per l'evento di combinazione di priorità.</span><span class="sxs-lookup"><span data-stu-id="a23f3-119">Event handle to the priority blend event.</span></span> <span data-ttu-id="a23f3-120">Viene restituito **null** se Track non è valido o se non è disponibile alcun evento free.</span><span class="sxs-lookup"><span data-stu-id="a23f3-120">**NULL** is returned if Track is invalid, or if no free event is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="a23f3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a23f3-121">Requirements</span></span>



| <span data-ttu-id="a23f3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a23f3-122">Requirement</span></span> | <span data-ttu-id="a23f3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a23f3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a23f3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a23f3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a23f3-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a23f3-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a23f3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a23f3-126">Library</span></span><br/> | <dl> <span data-ttu-id="a23f3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a23f3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a23f3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a23f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23f3-129">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="a23f3-129">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
