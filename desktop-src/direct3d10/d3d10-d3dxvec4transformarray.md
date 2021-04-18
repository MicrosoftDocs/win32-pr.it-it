---
description: Trasforma una matrice (x, y, z, w) in base a una matrice specificata.
ms.assetid: afd5cccb-e22f-4726-a84e-9eac1c1c277f
title: Funzione D3DXVec4TransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 5571fb19786e19a61c85741bcf6d4acb5231e977
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323184"
---
# <a name="d3dxvec4transformarray-function-d3dx10mathh"></a><span data-ttu-id="20bbd-103">Funzione D3DXVec4TransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="20bbd-103">D3DXVec4TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="20bbd-104">Trasforma una matrice (x, y, z, w) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="20bbd-104">Transforms an array (x, y, z, w) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20bbd-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR4 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="20bbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20bbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20bbd-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="20bbd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20bbd-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="20bbd-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="20bbd-109">Puntatore alla matrice [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="20bbd-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="20bbd-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20bbd-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bbd-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20bbd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20bbd-112">Stride tra i vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="20bbd-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="20bbd-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20bbd-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bbd-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="20bbd-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="20bbd-115">Puntatore alla matrice D3DXVECTOR4 di origine.</span><span class="sxs-lookup"><span data-stu-id="20bbd-115">Pointer to the source D3DXVECTOR4 array.</span></span>

</dd> <dt>

<span data-ttu-id="20bbd-116">*VStride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20bbd-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bbd-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20bbd-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20bbd-118">Stride tra i vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="20bbd-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="20bbd-119">*PM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20bbd-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bbd-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="20bbd-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="20bbd-121">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) di origine.</span><span class="sxs-lookup"><span data-stu-id="20bbd-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="20bbd-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20bbd-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bbd-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="20bbd-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="20bbd-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="20bbd-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20bbd-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20bbd-125">Return value</span></span>

<span data-ttu-id="20bbd-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="20bbd-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="20bbd-127">Puntatore a una struttura [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="20bbd-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="20bbd-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="20bbd-128">Remarks</span></span>

<span data-ttu-id="20bbd-129">Questa funzione trasforma la matrice pV (x, y, z, w) dalle pM della matrice.</span><span class="sxs-lookup"><span data-stu-id="20bbd-129">This function transforms the array pV (x, y, z, w) by the matrix pM.</span></span>

<span data-ttu-id="20bbd-130">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="20bbd-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="20bbd-131">In questo modo, la funzione **D3DXVec4TransformArray** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="20bbd-131">In this way, the **D3DXVec4TransformArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bbd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20bbd-132">Requirements</span></span>



| <span data-ttu-id="20bbd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="20bbd-133">Requirement</span></span> | <span data-ttu-id="20bbd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="20bbd-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20bbd-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20bbd-135">Header</span></span><br/> | <dl> <span data-ttu-id="20bbd-136"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="20bbd-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bbd-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20bbd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bbd-138">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="20bbd-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
