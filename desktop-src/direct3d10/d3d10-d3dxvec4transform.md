---
description: Trasforma un vettore 4D in base a una matrice specificata.
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: Funzione D3DXVec4Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 56fc6b3041d799cda3e98d459b2523d4b171df10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886275"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="8ed8b-103">Funzione D3DXVec4Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8ed8b-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="8ed8b-104">Trasforma un vettore 4D in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="8ed8b-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed8b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ed8b-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="8ed8b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ed8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed8b-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8ed8b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed8b-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ed8b-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8ed8b-109">Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8ed8b-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8ed8b-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ed8b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed8b-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ed8b-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8ed8b-112">Puntatore alla struttura D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="8ed8b-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ed8b-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ed8b-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed8b-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ed8b-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ed8b-115">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="8ed8b-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ed8b-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ed8b-116">Return value</span></span>

<span data-ttu-id="8ed8b-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ed8b-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="8ed8b-118">Puntatore a una struttura D3DXVECTOR4 che rappresenta il vettore 4D trasformato.</span><span class="sxs-lookup"><span data-stu-id="8ed8b-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed8b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ed8b-119">Remarks</span></span>

<span data-ttu-id="8ed8b-120">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="8ed8b-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8ed8b-121">In questo modo, la funzione D3DXVec4Transform può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="8ed8b-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed8b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ed8b-122">Requirements</span></span>



| <span data-ttu-id="8ed8b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed8b-123">Requirement</span></span> | <span data-ttu-id="8ed8b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8ed8b-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed8b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ed8b-125">Header</span></span><br/> | <dl> <span data-ttu-id="8ed8b-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed8b-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ed8b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ed8b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed8b-128">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8ed8b-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
