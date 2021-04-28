---
description: 'Funzione D3DXVec2TransformNormal (D3DX10Math.h): trasforma la normale vettore 2D in base alla matrice specificata.'
ms.assetid: fc238bb1-155f-4018-9c92-16352726920d
title: Funzione D3DXVec2TransformNormal (D3DX10Math.h)
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
ms.openlocfilehash: 403562ab779ebf532e1c1ebcec4ce21a2beadd7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108299"
---
# <a name="d3dxvec2transformnormal-function-d3dx10mathh"></a><span data-ttu-id="f5c1f-103">Funzione D3DXVec2TransformNormal (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="f5c1f-103">D3DXVec2TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="f5c1f-104">Trasforma la normale del vettore 2D in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-104">Transforms the 2D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c1f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5c1f-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormal(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f5c1f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5c1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c1f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f5c1f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c1f-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5c1f-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="f5c1f-109">Puntatore [**all'oggetto D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f5c1f-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f5c1f-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c1f-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5c1f-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="f5c1f-112">Puntatore alla struttura D3DXVECTOR2 di origine.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> <dt>

<span data-ttu-id="f5c1f-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f5c1f-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c1f-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5c1f-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f5c1f-115">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c1f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5c1f-116">Return value</span></span>

<span data-ttu-id="f5c1f-117">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5c1f-117">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="f5c1f-118">Puntatore a una struttura D3DXVECTOR2 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-118">Pointer to a D3DXVECTOR2 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c1f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5c1f-119">Remarks</span></span>

<span data-ttu-id="f5c1f-120">Questa funzione trasforma il vettore (pV->x, pV->y, 0, 0) dalla matrice a cui punta pM.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-120">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="f5c1f-121">Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="f5c1f-122">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f5c1f-123">In questo modo, la **funzione D3DXVec2TransformNormal** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="f5c1f-123">In this way, the **D3DXVec2TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c1f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5c1f-124">Requirements</span></span>



| <span data-ttu-id="f5c1f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c1f-125">Requirement</span></span> | <span data-ttu-id="f5c1f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f5c1f-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c1f-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5c1f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f5c1f-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c1f-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f5c1f-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5c1f-129">Library</span></span><br/> | <dl> <span data-ttu-id="f5c1f-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5c1f-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5c1f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5c1f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c1f-132">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f5c1f-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
