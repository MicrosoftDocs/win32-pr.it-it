---
description: Trasforma il vettore (x, y, z,1) in base a una matrice specificata.
ms.assetid: 88b26d94-2550-4126-bf91-b06391ec5c75
title: Funzione D3DXVec3Transform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 6db2e2ad4279863ba68f709f02f86796552e0463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969443"
---
# <a name="d3dxvec3transform-function-d3dx10mathh"></a><span data-ttu-id="6f9ca-103">Funzione D3DXVec3Transform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6f9ca-103">D3DXVec3Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="6f9ca-104">Trasforma il vettore (x, y, z,1) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="6f9ca-104">Transforms vector (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f9ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f9ca-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6f9ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f9ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f9ca-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6f9ca-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9ca-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f9ca-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6f9ca-109">Puntatore alla struttura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6f9ca-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6f9ca-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f9ca-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9ca-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f9ca-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="6f9ca-112">Puntatore all'origine [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="6f9ca-112">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="6f9ca-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f9ca-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f9ca-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f9ca-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6f9ca-115">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="6f9ca-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f9ca-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6f9ca-116">Return value</span></span>

<span data-ttu-id="6f9ca-117">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f9ca-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="6f9ca-118">Puntatore a una struttura D3DXVECTOR4 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="6f9ca-118">Pointer to a D3DXVECTOR4 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f9ca-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f9ca-119">Remarks</span></span>

<span data-ttu-id="6f9ca-120">Questa funzione trasforma il vettore, pV (x, y, z, 1), dal pM della matrice.</span><span class="sxs-lookup"><span data-stu-id="6f9ca-120">This function transforms the vector, pV (x, y, z, 1), by the matrix pM.</span></span>

<span data-ttu-id="6f9ca-121">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="6f9ca-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6f9ca-122">In questo modo, la funzione D3DXVec3Transform può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="6f9ca-122">In this way, the D3DXVec3Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f9ca-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f9ca-123">Requirements</span></span>



| <span data-ttu-id="6f9ca-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f9ca-124">Requirement</span></span> | <span data-ttu-id="6f9ca-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6f9ca-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f9ca-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f9ca-126">Header</span></span><br/> | <dl> <span data-ttu-id="6f9ca-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f9ca-127"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f9ca-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f9ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f9ca-129">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6f9ca-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
