---
description: Imposta la combinazione di chiavi di evento per la traccia di animazione specificata.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'Metodo ID3DXAnimationController:: KeyPriorityBlend (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354259"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a><span data-ttu-id="45db4-103">Metodo ID3DXAnimationController:: KeyPriorityBlend</span><span class="sxs-lookup"><span data-stu-id="45db4-103">ID3DXAnimationController::KeyPriorityBlend method</span></span>

<span data-ttu-id="45db4-104">Imposta la combinazione di chiavi di evento per la traccia di animazione specificata.</span><span class="sxs-lookup"><span data-stu-id="45db4-104">Sets blending event keys for the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="45db4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45db4-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a><span data-ttu-id="45db4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45db4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45db4-107">*NewBlendWeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45db4-107">*NewBlendWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45db4-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45db4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45db4-109">Numero compreso tra 0 e 1 utilizzato per unire le tracce.</span><span class="sxs-lookup"><span data-stu-id="45db4-109">Number between 0 and 1 that is used to blend tracks together.</span></span>

</dd> <dt>

<span data-ttu-id="45db4-110">*StartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45db4-110">*StartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45db4-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45db4-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45db4-112">Tempo globale per l'avvio di Blend.</span><span class="sxs-lookup"><span data-stu-id="45db4-112">Global time to start the blend.</span></span>

</dd> <dt>

<span data-ttu-id="45db4-113">*Durata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45db4-113">*Duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45db4-114">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="45db4-114">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="45db4-115">Durata dell'ora globale della Blend.</span><span class="sxs-lookup"><span data-stu-id="45db4-115">Global time duration of the blend.</span></span>

</dd> <dt>

<span data-ttu-id="45db4-116">*Transizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45db4-116">*Transition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45db4-117">Tipo: **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**</span><span class="sxs-lookup"><span data-stu-id="45db4-117">Type: **[**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md)**</span></span>

<span data-ttu-id="45db4-118">Specifica il tipo di transizione usato per la durata della Blend.</span><span class="sxs-lookup"><span data-stu-id="45db4-118">Specifies the transition type used for the duration of the blend.</span></span> <span data-ttu-id="45db4-119">Vedere [**D3DXTRANSITION \_ Type**](./d3dxtransition-type.md).</span><span class="sxs-lookup"><span data-stu-id="45db4-119">See [**D3DXTRANSITION\_TYPE**](./d3dxtransition-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45db4-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45db4-120">Return value</span></span>

<span data-ttu-id="45db4-121">Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="45db4-121">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="45db4-122">Handle di evento per l'evento di combinazione di priorità.</span><span class="sxs-lookup"><span data-stu-id="45db4-122">Event handle to the priority blend event.</span></span> <span data-ttu-id="45db4-123">Se uno o più parametri di input non sono validi oppure non è disponibile alcun evento libero, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="45db4-123">**NULL** is returned if one or more of the input parameters is invalid, or no free event is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="45db4-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="45db4-124">Remarks</span></span>

<span data-ttu-id="45db4-125">Il controller di animazione si combina in tre fasi: le tracce con priorità bassa vengono combinate per prime, le tracce con priorità alta vengono mescolate secondo e i risultati di entrambe le operazioni vengono combinati.</span><span class="sxs-lookup"><span data-stu-id="45db4-125">The animation controller blends in three phases: low priority tracks are blended first, high priority tracks are blended second, and then the results of both are blended.</span></span>

## <a name="requirements"></a><span data-ttu-id="45db4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45db4-126">Requirements</span></span>



| <span data-ttu-id="45db4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="45db4-127">Requirement</span></span> | <span data-ttu-id="45db4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="45db4-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45db4-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45db4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="45db4-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="45db4-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="45db4-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="45db4-131">Library</span></span><br/> | <dl> <span data-ttu-id="45db4-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45db4-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45db4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45db4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45db4-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="45db4-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="45db4-135">**SetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="45db4-135">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
