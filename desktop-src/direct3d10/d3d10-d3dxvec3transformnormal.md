---
description: 'Funzione D3DXVec3TransformNormal (D3DX10Math.h): trasforma la normale del vettore 3D in base alla matrice specificata.'
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: Funzione D3DXVec3TransformNormal (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormal
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 0fc1456b89f3e11f2076a8e7b6b960d15e9c7083
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103059"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="80028-103">Funzione D3DXVec3TransformNormal (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="80028-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="80028-104">Trasforma la normale del vettore 3D in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="80028-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="80028-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80028-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="80028-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80028-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80028-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="80028-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80028-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="80028-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="80028-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="80028-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="80028-110">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80028-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80028-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="80028-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="80028-112">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="80028-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="80028-113">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80028-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80028-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="80028-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="80028-115">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="80028-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80028-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80028-116">Return value</span></span>

<span data-ttu-id="80028-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="80028-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="80028-118">Puntatore a una struttura D3DXVECTOR3 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="80028-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="80028-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="80028-119">Remarks</span></span>

<span data-ttu-id="80028-120">Questa funzione trasforma il vettore (pV->x, pV->y, pV->z, 0) dalla matrice a cui punta pM.</span><span class="sxs-lookup"><span data-stu-id="80028-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="80028-121">Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice che si userebbe per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="80028-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="80028-122">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="80028-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="80028-123">In questo modo, la **funzione D3DXVec3TransformNormal** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="80028-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="80028-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80028-124">Requirements</span></span>



| <span data-ttu-id="80028-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80028-125">Requirement</span></span> | <span data-ttu-id="80028-126">Valore</span><span class="sxs-lookup"><span data-stu-id="80028-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80028-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80028-127">Header</span></span><br/> | <dl> <span data-ttu-id="80028-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="80028-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80028-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80028-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80028-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="80028-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
