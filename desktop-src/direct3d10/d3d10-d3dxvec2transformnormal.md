---
description: Trasforma il vettore 2D normale in base alla matrice specificata.
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: Funzione D3DXVec2TransformNormal (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4043a8f5a57f14be3e8506dc257690ef581835d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969370"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="6a821-103">Funzione D3DXVec2TransformNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6a821-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="6a821-104">Trasforma il vettore 2D normale in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="6a821-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a821-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a821-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="6a821-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a821-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6a821-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a821-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a821-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="6a821-109">Puntatore a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6a821-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a821-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a821-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a821-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a821-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="6a821-112">Puntatore alla struttura D3DXVECTOR2 di origine.</span><span class="sxs-lookup"><span data-stu-id="6a821-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="6a821-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a821-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a821-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a821-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6a821-115">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="6a821-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a821-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a821-116">Return value</span></span>

<span data-ttu-id="6a821-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a821-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="6a821-118">Puntatore a una struttura D3DXVECTOR2 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="6a821-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a821-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a821-119">Remarks</span></span>

<span data-ttu-id="6a821-120">Questa funzione trasforma il vettore (pV->x, pV->y, 0, 0) dalla matrice a cui fa riferimento il pM.</span><span class="sxs-lookup"><span data-stu-id="6a821-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="6a821-121">Se si vuole trasformare un normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="6a821-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="6a821-122">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="6a821-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6a821-123">In questo modo, la funzione **D3DXVec2TransformNormal** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="6a821-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a821-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a821-124">Requirements</span></span>



| <span data-ttu-id="6a821-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a821-125">Requirement</span></span> | <span data-ttu-id="6a821-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6a821-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a821-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a821-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6a821-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a821-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a821-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a821-129">Library</span></span><br/> | <dl> <span data-ttu-id="6a821-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a821-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a821-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a821-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a821-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="6a821-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
