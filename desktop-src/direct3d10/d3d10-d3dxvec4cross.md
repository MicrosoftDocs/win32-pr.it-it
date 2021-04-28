---
description: 'Funzione D3DXVec4Cross (D3DX10Math.h): determina il prodotto incrociato in quattro dimensioni.'
ms.assetid: 4f728fbd-cf5a-4d2e-ba4f-487616d83f6d
title: Funzione D3DXVec4Cross (D3DX10Math.h)
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
ms.openlocfilehash: e52cc1adb1e48f65599b1bf7179f7953823f1e1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102949"
---
# <a name="d3dxvec4cross-function-d3dx10mathh"></a><span data-ttu-id="dc873-103">Funzione D3DXVec4Cross (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="dc873-103">D3DXVec4Cross function (D3DX10Math.h)</span></span>

<span data-ttu-id="dc873-104">Determina il prodotto incrociato in quattro dimensioni.</span><span class="sxs-lookup"><span data-stu-id="dc873-104">Determines the cross-product in four dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc873-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc873-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Cross(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="dc873-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc873-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dc873-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc873-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc873-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="dc873-109">Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dc873-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dc873-110">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dc873-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc873-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc873-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="dc873-112">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="dc873-112">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="dc873-113">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dc873-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc873-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc873-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="dc873-115">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="dc873-115">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="dc873-116">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dc873-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc873-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc873-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="dc873-118">Puntatore a una struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="dc873-118">Pointer to a source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc873-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc873-119">Return value</span></span>

<span data-ttu-id="dc873-120">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc873-120">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="dc873-121">Puntatore a una struttura D3DXVECTOR4 che rappresenta il prodotto incrociato.</span><span class="sxs-lookup"><span data-stu-id="dc873-121">Pointer to a D3DXVECTOR4 structure that is the cross product.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc873-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc873-122">Remarks</span></span>

<span data-ttu-id="dc873-123">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="dc873-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="dc873-124">In questo modo, la funzione D3DXVec4Cross può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="dc873-124">In this way, the D3DXVec4Cross function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc873-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc873-125">Requirements</span></span>



| <span data-ttu-id="dc873-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc873-126">Requirement</span></span> | <span data-ttu-id="dc873-127">Valore</span><span class="sxs-lookup"><span data-stu-id="dc873-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc873-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc873-128">Header</span></span><br/> | <dl> <span data-ttu-id="dc873-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="dc873-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc873-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc873-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc873-131">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="dc873-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
