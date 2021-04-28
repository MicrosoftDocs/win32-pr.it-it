---
description: 'Funzione D3DXVec2TransformNormalArray (D3DX10Math.h): trasforma una matrice (x, y, 0, 0) da una determinata matrice.'
ms.assetid: a53f998a-f2a5-4e4b-bc1c-c1f46284d78b
title: Funzione D3DXVec2TransformNormalArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformNormalArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b4e18fc2bb8c62bb86947b9eab35daae9d0242ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108279"
---
# <a name="d3dxvec2transformnormalarray-function-d3dx10mathh"></a><span data-ttu-id="467b2-103">Funzione D3DXVec2TransformNormalArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="467b2-103">D3DXVec2TransformNormalArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="467b2-104">Trasforma una matrice (x, y, 0, 0) in base a una matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="467b2-104">Transforms an array (x, y, 0, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="467b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="467b2-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformNormalArray(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR2 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="467b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="467b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="467b2-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="467b2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="467b2-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="467b2-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="467b2-109">Puntatore a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="467b2-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="467b2-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="467b2-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="467b2-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="467b2-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="467b2-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="467b2-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="467b2-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="467b2-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="467b2-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="467b2-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="467b2-115">Puntatore alla matrice D3DXVECTOR2 di origine.</span><span class="sxs-lookup"><span data-stu-id="467b2-115">Pointer to the source D3DXVECTOR2 array.</span></span>

</dd> <dt>

<span data-ttu-id="467b2-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="467b2-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="467b2-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="467b2-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="467b2-118">Stride tra vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="467b2-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="467b2-119">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="467b2-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="467b2-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="467b2-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="467b2-121">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="467b2-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="467b2-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="467b2-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="467b2-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="467b2-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="467b2-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="467b2-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="467b2-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="467b2-125">Return value</span></span>

<span data-ttu-id="467b2-126">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="467b2-126">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="467b2-127">Puntatore a una struttura D3DXVECTOR2 che rappresenta la matrice trasformata.</span><span class="sxs-lookup"><span data-stu-id="467b2-127">Pointer to a D3DXVECTOR2 structure that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="467b2-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="467b2-128">Remarks</span></span>

<span data-ttu-id="467b2-129">Questa funzione trasforma il vettore (pV->x, pV->y, 0, 0) dalla matrice a cui punta pM.</span><span class="sxs-lookup"><span data-stu-id="467b2-129">This function transforms the vector (pV->x, pV->y, 0, 0) by the matrix pointed to by pM.</span></span>

<span data-ttu-id="467b2-130">Se si vuole trasformare una normale, la matrice passata a questa funzione deve essere la trasposizione dell'inverso della matrice da usare per trasformare un punto.</span><span class="sxs-lookup"><span data-stu-id="467b2-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="467b2-131">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="467b2-131">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="467b2-132">In questo modo, la **funzione D3DXVec2TransformNormalArray** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="467b2-132">In this way, the **D3DXVec2TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="467b2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="467b2-133">Requirements</span></span>



| <span data-ttu-id="467b2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="467b2-134">Requirement</span></span> | <span data-ttu-id="467b2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="467b2-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="467b2-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="467b2-136">Header</span></span><br/>  | <dl> <span data-ttu-id="467b2-137"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="467b2-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="467b2-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="467b2-138">Library</span></span><br/> | <dl> <span data-ttu-id="467b2-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="467b2-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="467b2-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="467b2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467b2-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="467b2-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
