---
description: Determina il prodotto incrociato in quattro dimensioni.
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: Funzione D3DXVec4Cross (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Cross
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e3e2a612740a207ea4dc44243ce24ebbab7fc08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323186"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="be484-103">Funzione D3DXVec4Cross (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="be484-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="be484-104">Determina il prodotto incrociato in quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="be484-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="be484-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be484-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="be484-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be484-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be484-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="be484-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be484-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="be484-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="be484-109">Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="be484-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="be484-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be484-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be484-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="be484-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="be484-112">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="be484-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="be484-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be484-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be484-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="be484-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="be484-115">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="be484-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="be484-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be484-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be484-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="be484-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="be484-118">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="be484-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be484-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be484-119">Return value</span></span>

<span data-ttu-id="be484-120">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="be484-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="be484-121">Puntatore a una struttura D3DXVECTOR4 che rappresenta il prodotto incrociato.</span><span class="sxs-lookup"><span data-stu-id="be484-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="be484-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="be484-122">Remarks</span></span>

<span data-ttu-id="be484-123">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="be484-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="be484-124">In questo modo, la funzione D3DXVec4Cross può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="be484-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be484-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be484-125">Requirements</span></span>



| <span data-ttu-id="be484-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="be484-126">Requirement</span></span> | <span data-ttu-id="be484-127">Valore</span><span class="sxs-lookup"><span data-stu-id="be484-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be484-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="be484-128">Header</span></span><br/> | <dl> <span data-ttu-id="be484-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="be484-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be484-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be484-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be484-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="be484-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
