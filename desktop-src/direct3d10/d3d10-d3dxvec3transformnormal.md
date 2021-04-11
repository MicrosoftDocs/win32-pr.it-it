---
description: Trasforma il vettore 3D normale dalla matrice specificata.
ms.assetid: 8068b80f-6222-4f23-8b1c-2ff5592fa898
title: Funzione D3DXVec3TransformNormal (D3DX10Math. h)
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
ms.openlocfilehash: 602f366d3d7ccbcd37804226323d5584eed034f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355299"
---
# <a name="d3dxvec3transformnormal-function-d3dx10mathh"></a><span data-ttu-id="b6649-103">Funzione D3DXVec3TransformNormal (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b6649-103">D3DXVec3TransformNormal function (D3DX10Math.h)</span></span>

<span data-ttu-id="b6649-104">Trasforma il vettore 3D normale dalla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="b6649-104">Transforms the 3D vector normal by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6649-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6649-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormal(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b6649-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6649-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6649-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b6649-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6649-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6649-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b6649-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b6649-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b6649-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6649-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6649-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b6649-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b6649-112">Puntatore alla struttura D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="b6649-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> <dt>

<span data-ttu-id="b6649-113">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6649-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6649-114">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b6649-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b6649-115">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="b6649-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6649-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6649-116">Return value</span></span>

<span data-ttu-id="b6649-117">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6649-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b6649-118">Puntatore a una struttura D3DXVECTOR3 che rappresenta il vettore trasformato.</span><span class="sxs-lookup"><span data-stu-id="b6649-118">Pointer to a D3DXVECTOR3 structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6649-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6649-119">Remarks</span></span>

<span data-ttu-id="b6649-120">Questa funzione trasforma il vettore (pV->x, pV->y, pV->z, 0) dalla matrice a cui punta il pM.</span><span class="sxs-lookup"><span data-stu-id="b6649-120">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="b6649-121">Se si vuole trasformare un normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="b6649-121">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="b6649-122">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="b6649-122">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b6649-123">In questo modo, la funzione **D3DXVec3TransformNormal** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="b6649-123">In this way, the **D3DXVec3TransformNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6649-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6649-124">Requirements</span></span>



| <span data-ttu-id="b6649-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6649-125">Requirement</span></span> | <span data-ttu-id="b6649-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b6649-126">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6649-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6649-127">Header</span></span><br/> | <dl> <span data-ttu-id="b6649-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6649-128"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6649-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6649-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6649-130">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b6649-130">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
