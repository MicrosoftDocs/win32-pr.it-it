---
description: 'Funzione D3DXVec3TransformNormalArray (D3DX10Math.h): trasforma una matrice (x, y, z, 0) da una determinata matrice.'
ms.assetid: 7f0a41ce-bd3a-4e35-9a5d-8178a4e7bd44
title: Funzione D3DXVec3TransformNormalArray (D3DX10Math.h)
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
ms.openlocfilehash: d391717056d1cd8a6957a6647612ed8b1ca65e41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103049"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="656f2-103">Funzione D3DXVec3TransformNormalArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="656f2-103">D3DXVec3TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="656f2-104">Trasforma una matrice (x, y, z, 0) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="656f2-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="656f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="656f2-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="656f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="656f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656f2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="656f2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="656f2-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="656f2-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="656f2-109">Puntatore alla [**matrice D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="656f2-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="656f2-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="656f2-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656f2-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656f2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656f2-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="656f2-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="656f2-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="656f2-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656f2-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="656f2-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="656f2-115">Puntatore alla matrice D3DXVECTOR3 di origine.</span><span class="sxs-lookup"><span data-stu-id="656f2-115">Pointer to the source D3DXVECTOR3 array.</span></span>

</dd> <dt>

<span data-ttu-id="656f2-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="656f2-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656f2-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656f2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656f2-118">Stride tra vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="656f2-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="656f2-119">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="656f2-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656f2-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="656f2-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="656f2-121">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="656f2-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="656f2-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="656f2-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="656f2-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="656f2-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="656f2-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="656f2-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656f2-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="656f2-125">Return value</span></span>

<span data-ttu-id="656f2-126">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="656f2-126">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="656f2-127">Puntatore a una matrice D3DXVECTOR3 che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="656f2-127">Pointer to a D3DXVECTOR3 array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="656f2-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="656f2-128">Remarks</span></span>

<span data-ttu-id="656f2-129">Questa funzione trasforma il vettore (pV->x, pV->y, pV->z, 0) dalla matrice a cui punta pM.</span><span class="sxs-lookup"><span data-stu-id="656f2-129">This function transforms the vector (pV->x, pV->y, pV->z, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="656f2-130">Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="656f2-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="656f2-131">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="656f2-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="656f2-132">In questo modo, la **funzione D3DXVec3TransformNormalArray** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="656f2-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="656f2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="656f2-133">Requirements</span></span>



| <span data-ttu-id="656f2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="656f2-134">Requirement</span></span> | <span data-ttu-id="656f2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="656f2-135">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="656f2-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="656f2-136">Header</span></span><br/> | <dl> <span data-ttu-id="656f2-137"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="656f2-137"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656f2-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="656f2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656f2-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="656f2-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
