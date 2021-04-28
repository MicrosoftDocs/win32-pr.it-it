---
description: 'Funzione D3DXVec3TransformArray (D3DX10Math.h): trasforma una matrice (x, y, z, 1) in base a una determinata matrice.'
ms.assetid: f64c55df-ea93-4c93-be89-eee650e6ecf0
title: Funzione D3DXVec3TransformArray (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: bc38f0ef634763d9a5be85795a897b483431aede
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108119"
---
# <a name="d3dxvec3transformarray-function-d3dx10mathh"></a><span data-ttu-id="2aa30-103">Funzione D3DXVec3TransformArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="2aa30-103">D3DXVec3TransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="2aa30-104">Trasforma una matrice (x, y, z, 1) in base a una determinata matrice.</span><span class="sxs-lookup"><span data-stu-id="2aa30-104">Transforms an array (x, y, z, 1) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aa30-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2aa30-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec3TransformArray(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="2aa30-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2aa30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aa30-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2aa30-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa30-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2aa30-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="2aa30-109">Puntatore alla [**matrice D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2aa30-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2aa30-110">*OutStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2aa30-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa30-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2aa30-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2aa30-112">Stride tra vettori nel flusso di dati di output.</span><span class="sxs-lookup"><span data-stu-id="2aa30-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="2aa30-113">*pV* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2aa30-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa30-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa30-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="2aa30-115">Puntatore alla matrice [**D3DXVECTOR3 di**](d3d10-d3dxvector3.md) origine.</span><span class="sxs-lookup"><span data-stu-id="2aa30-115">Pointer to the source [**D3DXVECTOR3**](d3d10-d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="2aa30-116">*VStride* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2aa30-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa30-117">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2aa30-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2aa30-118">Stride tra vettori nel flusso di dati di input.</span><span class="sxs-lookup"><span data-stu-id="2aa30-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="2aa30-119">*pM* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2aa30-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa30-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2aa30-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2aa30-121">Puntatore alla struttura [**D3DXMATRIX di**](d3d10-d3dxmatrix.md) origine.</span><span class="sxs-lookup"><span data-stu-id="2aa30-121">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2aa30-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aa30-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aa30-123">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2aa30-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2aa30-124">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2aa30-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aa30-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2aa30-125">Return value</span></span>

<span data-ttu-id="2aa30-126">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="2aa30-126">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="2aa30-127">Puntatore a [**una matrice trasformata D3DXVECTOR4.**](d3d10-d3dxvector4.md)</span><span class="sxs-lookup"><span data-stu-id="2aa30-127">Pointer to a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aa30-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="2aa30-128">Remarks</span></span>

<span data-ttu-id="2aa30-129">Questa funzione trasforma la matrice pV (x, y, z, 1) dalla matrice pM.</span><span class="sxs-lookup"><span data-stu-id="2aa30-129">This function transforms the array pV (x, y, z, 1) by the matrix pM.</span></span>

<span data-ttu-id="2aa30-130">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="2aa30-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2aa30-131">In questo modo, la funzione D3DXVec3TransformArray può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="2aa30-131">In this way, the D3DXVec3TransformArray function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa30-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2aa30-132">Requirements</span></span>



| <span data-ttu-id="2aa30-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2aa30-133">Requirement</span></span> | <span data-ttu-id="2aa30-134">Valore</span><span class="sxs-lookup"><span data-stu-id="2aa30-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa30-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2aa30-135">Header</span></span><br/> | <dl> <span data-ttu-id="2aa30-136"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2aa30-136"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2aa30-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2aa30-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2aa30-138">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2aa30-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
