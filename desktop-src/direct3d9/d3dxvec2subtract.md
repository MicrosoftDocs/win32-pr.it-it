---
description: Sottrae due vettori 2D.
ms.assetid: e5a693e9-b143-41d5-923d-3f3f71461a42
title: Funzione D3DXVec2Subtract (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c12f41da7594f3eff9743eed7a1b0780f36c5fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530883"
---
# <a name="d3dxvec2subtract-function"></a><span data-ttu-id="7d6bb-103">D3DXVec2Subtract (funzione)</span><span class="sxs-lookup"><span data-stu-id="7d6bb-103">D3DXVec2Subtract function</span></span>

<span data-ttu-id="7d6bb-104">Sottrae due vettori 2D.</span><span class="sxs-lookup"><span data-stu-id="7d6bb-104">Subtracts two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6bb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d6bb-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Subtract(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="7d6bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d6bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d6bb-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7d6bb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6bb-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d6bb-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7d6bb-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7d6bb-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7d6bb-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d6bb-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6bb-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d6bb-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7d6bb-112">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="7d6bb-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7d6bb-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d6bb-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d6bb-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d6bb-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7d6bb-115">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="7d6bb-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d6bb-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d6bb-116">Return value</span></span>

<span data-ttu-id="7d6bb-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d6bb-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="7d6bb-118">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta la differenza di due vettori.</span><span class="sxs-lookup"><span data-stu-id="7d6bb-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the difference of two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d6bb-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d6bb-119">Remarks</span></span>

<span data-ttu-id="7d6bb-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="7d6bb-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7d6bb-121">In questo modo, la funzione **D3DXVec2Subtract** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="7d6bb-121">In this way, the **D3DXVec2Subtract** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d6bb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d6bb-122">Requirements</span></span>



| <span data-ttu-id="7d6bb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d6bb-123">Requirement</span></span> | <span data-ttu-id="7d6bb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7d6bb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6bb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d6bb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7d6bb-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d6bb-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7d6bb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d6bb-127">Library</span></span><br/> | <dl> <span data-ttu-id="7d6bb-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d6bb-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d6bb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d6bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d6bb-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="7d6bb-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7d6bb-131">**D3DXVec2Add**</span><span class="sxs-lookup"><span data-stu-id="7d6bb-131">**D3DXVec2Add**</span></span>](d3dxvec2add.md)
</dt> <dt>

[<span data-ttu-id="7d6bb-132">**D3DXVec2Scale**</span><span class="sxs-lookup"><span data-stu-id="7d6bb-132">**D3DXVec2Scale**</span></span>](d3dxvec2scale.md)
</dt> </dl>

 

 




