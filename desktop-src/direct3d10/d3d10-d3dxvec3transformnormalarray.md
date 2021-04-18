---
description: Trasforma una matrice (x, y, z, 0) in base a una matrice specificata.
ms.assetid: 7f0a41ce-bd3a-4e35-9a5d-8178a4e7bd44
title: Funzione D3DXVec3TransformNormalArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: facb5591becd27d3fff283e8d531118ca433d5d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322390"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="0a30d-103">Funzione D3DXVec3TransformNormalArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0a30d-103">D3DXVec3TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="0a30d-104">Trasforma una matrice (x, y, z, 0) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="0a30d-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a30d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a30d-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="0a30d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a30d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a30d-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0a30d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a30d-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a30d-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0a30d-109">Puntatore alla matrice [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0a30d-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0a30d-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a30d-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a30d-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a30d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a30d-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="0a30d-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0a30d-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a30d-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a30d-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a30d-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0a30d-115">Puntatore alla matrice D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="0a30d-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="0a30d-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a30d-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a30d-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a30d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a30d-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="0a30d-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="0a30d-119">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a30d-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a30d-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0a30d-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0a30d-121">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="0a30d-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0a30d-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a30d-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a30d-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a30d-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a30d-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="0a30d-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a30d-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a30d-125">Return value</span></span>

<span data-ttu-id="0a30d-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a30d-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="0a30d-127">Puntatore a una matrice D3DXVECTOR3 che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="0a30d-127">Pointer to a D3DXVECTOR3 array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a30d-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a30d-128">Remarks</span></span>

<span data-ttu-id="0a30d-129">Questa funzione trasforma il vettore (pV->x, pV->y, pV->z, 0) dalla matrice a cui punta il pM.</span><span class="sxs-lookup"><span data-stu-id="0a30d-129">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="0a30d-130">Se si vuole trasformare un normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="0a30d-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="0a30d-131">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="0a30d-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0a30d-132">In questo modo, la funzione **D3DXVec3TransformNormalArray** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="0a30d-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a30d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a30d-133">Requirements</span></span>



| <span data-ttu-id="0a30d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a30d-134">Requirement</span></span> | <span data-ttu-id="0a30d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0a30d-135">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a30d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a30d-136">Header</span></span><br/> | <dl> <span data-ttu-id="0a30d-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a30d-137"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a30d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a30d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a30d-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0a30d-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
