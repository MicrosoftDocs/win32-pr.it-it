---
description: Restituisce un vettore 2D costituito dai componenti più grandi di due vettori 2D.
ms.assetid: 5eb5141b-d611-4c6b-a3e3-c7ad8f223657
title: Funzione D3DXVec2Maximize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffd5fbc98e653a6bbaffa7d3cec16b13695365b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401955"
---
# <a name="d3dxvec2maximize-function"></a><span data-ttu-id="70e4d-103">D3DXVec2Maximize (funzione)</span><span class="sxs-lookup"><span data-stu-id="70e4d-103">D3DXVec2Maximize function</span></span>

<span data-ttu-id="70e4d-104">Restituisce un vettore 2D costituito dai componenti più grandi di due vettori 2D.</span><span class="sxs-lookup"><span data-stu-id="70e4d-104">Returns a 2D vector that is made up of the largest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e4d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70e4d-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Maximize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="70e4d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="70e4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e4d-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="70e4d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70e4d-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="70e4d-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70e4d-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="70e4d-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="70e4d-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70e4d-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70e4d-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="70e4d-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70e4d-112">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="70e4d-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="70e4d-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70e4d-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70e4d-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="70e4d-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70e4d-115">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="70e4d-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e4d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70e4d-116">Return value</span></span>

<span data-ttu-id="70e4d-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="70e4d-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="70e4d-118">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) costituita dai componenti più grandi dei due vettori.</span><span class="sxs-lookup"><span data-stu-id="70e4d-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e4d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="70e4d-119">Remarks</span></span>

<span data-ttu-id="70e4d-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="70e4d-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="70e4d-121">In questo modo, la funzione **D3DXVec2Maximize** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="70e4d-121">In this way, the **D3DXVec2Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e4d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70e4d-122">Requirements</span></span>



| <span data-ttu-id="70e4d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e4d-123">Requirement</span></span> | <span data-ttu-id="70e4d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="70e4d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70e4d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70e4d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="70e4d-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e4d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="70e4d-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="70e4d-127">Library</span></span><br/> | <dl> <span data-ttu-id="70e4d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70e4d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70e4d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70e4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e4d-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="70e4d-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="70e4d-131">**D3DXVec2Minimize**</span><span class="sxs-lookup"><span data-stu-id="70e4d-131">**D3DXVec2Minimize**</span></span>](d3dxvec2minimize.md)
</dt> </dl>

 

 




