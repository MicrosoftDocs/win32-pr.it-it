---
description: Restituisce un vettore 2D costituito dai componenti più piccoli di due vettori 2D.
ms.assetid: 6944523e-33dd-456e-9cc2-17760d76c548
title: Funzione D3DXVec2Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1914ae9317d686e369f1cb2c7eb36ab54a29845f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322458"
---
# <a name="d3dxvec2minimize-function"></a><span data-ttu-id="a9845-103">D3DXVec2Minimize (funzione)</span><span class="sxs-lookup"><span data-stu-id="a9845-103">D3DXVec2Minimize function</span></span>

<span data-ttu-id="a9845-104">Restituisce un vettore 2D costituito dai componenti più piccoli di due vettori 2D.</span><span class="sxs-lookup"><span data-stu-id="a9845-104">Returns a 2D vector that is made up of the smallest components of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9845-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9845-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Minimize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="a9845-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9845-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9845-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a9845-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9845-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9845-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a9845-109">Puntatore alla struttura [**D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a9845-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a9845-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9845-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9845-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9845-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a9845-112">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a9845-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a9845-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9845-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9845-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9845-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a9845-115">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="a9845-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9845-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9845-116">Return value</span></span>

<span data-ttu-id="a9845-117">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="a9845-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="a9845-118">Puntatore a una struttura [**D3DXVECTOR2**](d3dxvector2.md) costituita dai componenti più piccoli dei due vettori.</span><span class="sxs-lookup"><span data-stu-id="a9845-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is made up of the smallest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9845-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9845-119">Remarks</span></span>

<span data-ttu-id="a9845-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="a9845-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a9845-121">In questo modo, la funzione **D3DXVec2Minimize** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="a9845-121">In this way, the **D3DXVec2Minimize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9845-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9845-122">Requirements</span></span>



| <span data-ttu-id="a9845-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9845-123">Requirement</span></span> | <span data-ttu-id="a9845-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a9845-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9845-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9845-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a9845-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9845-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a9845-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9845-127">Library</span></span><br/> | <dl> <span data-ttu-id="a9845-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9845-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9845-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9845-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9845-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a9845-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a9845-131">**D3DXVec2Maximize**</span><span class="sxs-lookup"><span data-stu-id="a9845-131">**D3DXVec2Maximize**</span></span>](d3dxvec2maximize.md)
</dt> </dl>

 

 




