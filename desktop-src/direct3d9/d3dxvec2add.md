---
description: Aggiunge due vettori 2D.
ms.assetid: 82b2fdf6-1b1f-4768-8c0b-ac8faa77d7ed
title: Funzione D3DXVec2Add (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5087177448b01763bd94acb9b50c27c6cdf38815
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969334"
---
# <a name="d3dxvec2add-function"></a><span data-ttu-id="7a227-103">D3DXVec2Add (funzione)</span><span class="sxs-lookup"><span data-stu-id="7a227-103">D3DXVec2Add function</span></span>

<span data-ttu-id="7a227-104">Aggiunge due vettori 2D.</span><span class="sxs-lookup"><span data-stu-id="7a227-104">Adds two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a227-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a227-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Add(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="7a227-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a227-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a227-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7a227-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a227-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a227-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7a227-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7a227-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7a227-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a227-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a227-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a227-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7a227-112">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="7a227-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7a227-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a227-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a227-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a227-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7a227-115">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="7a227-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a227-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a227-116">Return value</span></span>

<span data-ttu-id="7a227-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a227-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7a227-118">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta la somma dei due vettori.</span><span class="sxs-lookup"><span data-stu-id="7a227-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the sum of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a227-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a227-119">Remarks</span></span>

<span data-ttu-id="7a227-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="7a227-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7a227-121">In questo modo, la funzione **D3DXVec2Add** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="7a227-121">In this way, the **D3DXVec2Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a227-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a227-122">Requirements</span></span>



| <span data-ttu-id="7a227-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a227-123">Requirement</span></span> | <span data-ttu-id="7a227-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7a227-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a227-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a227-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7a227-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a227-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7a227-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a227-127">Library</span></span><br/> | <dl> <span data-ttu-id="7a227-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a227-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a227-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a227-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a227-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7a227-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7a227-131">**D3DXVec2Subtract**</span><span class="sxs-lookup"><span data-stu-id="7a227-131">**D3DXVec2Subtract**</span></span>](d3dxvec2subtract.md)
</dt> <dt>

[<span data-ttu-id="7a227-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="7a227-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




