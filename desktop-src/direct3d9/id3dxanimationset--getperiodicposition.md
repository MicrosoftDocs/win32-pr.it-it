---
description: Restituisce la posizione dell'ora nell'intervallo di tempo locale di un set di animazioni.
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'Metodo ID3DXAnimationSet:: GetPeriodicPosition (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355934"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a><span data-ttu-id="5d661-103">Metodo ID3DXAnimationSet:: GetPeriodicPosition</span><span class="sxs-lookup"><span data-stu-id="5d661-103">ID3DXAnimationSet::GetPeriodicPosition method</span></span>

<span data-ttu-id="5d661-104">Restituisce la posizione dell'ora nell'intervallo di tempo locale di un set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="5d661-104">Returns time position in the local timeframe of an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d661-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d661-105">Syntax</span></span>


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="5d661-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d661-107">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d661-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d661-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d661-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d661-109">Ora locale del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="5d661-109">Local time of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d661-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d661-110">Return value</span></span>

<span data-ttu-id="5d661-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d661-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d661-112">Posizione dell'ora misurata nell'intervallo di tempo del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="5d661-112">Time position as measured in the timeframe of the animation set.</span></span> <span data-ttu-id="5d661-113">Questo valore verrà limitato in base al periodo del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="5d661-113">This value will be bounded by the period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d661-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d661-114">Remarks</span></span>

<span data-ttu-id="5d661-115">La posizione temporale restituita da questo metodo può essere utilizzata come parametro PeriodicPosition di [**ID3DXAnimationSet:: GetSRT**](id3dxanimationset--getsrt.md).</span><span class="sxs-lookup"><span data-stu-id="5d661-115">The time position returned by this method can be used as the PeriodicPosition parameter of [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d661-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d661-116">Requirements</span></span>



| <span data-ttu-id="5d661-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d661-117">Requirement</span></span> | <span data-ttu-id="5d661-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5d661-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d661-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d661-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5d661-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d661-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5d661-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="5d661-121">Library</span></span><br/> | <dl> <span data-ttu-id="5d661-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d661-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d661-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d661-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d661-124">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5d661-124">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
