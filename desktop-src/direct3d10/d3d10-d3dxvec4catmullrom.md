---
description: Esegue un'interpolazione di Catmull-Rom, usando i vettori 4D specificati.
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: Funzione D3DXVec4CatmullRom (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e027272a038f17a77dbeda861d6be909afa2f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969327"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a><span data-ttu-id="a1831-103">Funzione D3DXVec4CatmullRom (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a1831-103">D3DXVec4CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="a1831-104">Esegue un'interpolazione di Catmull-Rom, usando i vettori 4D specificati.</span><span class="sxs-lookup"><span data-stu-id="a1831-104">Performs a Catmull-Rom interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1831-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1831-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="a1831-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1831-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a1831-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1831-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a1831-109">Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1831-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-110">*pV0* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1831-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1831-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a1831-112">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="a1831-112">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-113">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1831-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1831-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a1831-115">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="a1831-115">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1831-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1831-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a1831-118">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="a1831-118">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-119">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1831-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-120">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="a1831-120">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a1831-121">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="a1831-121">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="a1831-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1831-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1831-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1831-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1831-124">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="a1831-124">Weighting factor.</span></span> <span data-ttu-id="a1831-125">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a1831-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1831-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1831-126">Return value</span></span>

<span data-ttu-id="a1831-127">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="a1831-127">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="a1831-128">Puntatore a una struttura D3DXVECTOR4 che è il risultato dell'interpolazione del Catmull-Rom.</span><span class="sxs-lookup"><span data-stu-id="a1831-128">Pointer to a D3DXVECTOR4 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1831-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1831-129">Remarks</span></span>

<span data-ttu-id="a1831-130">Dato quattro punti (P1, P2, P3, P4), trovare una funzione Q (s) in modo che:</span><span class="sxs-lookup"><span data-stu-id="a1831-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="a1831-131">È possibile derivare la spline Catmull-Rom dalla spline eremita impostando:</span><span class="sxs-lookup"><span data-stu-id="a1831-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="a1831-132">dove:</span><span class="sxs-lookup"><span data-stu-id="a1831-132">where:</span></span>

<span data-ttu-id="a1831-133">V1 è il contenuto di pV0.</span><span class="sxs-lookup"><span data-stu-id="a1831-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="a1831-134">V2 nel contenuto di pV1.</span><span class="sxs-lookup"><span data-stu-id="a1831-134">v2 in the contents of pV1.</span></span>

<span data-ttu-id="a1831-135">P3 è il contenuto di pV2.</span><span class="sxs-lookup"><span data-stu-id="a1831-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="a1831-136">P4 è il contenuto di pV3.</span><span class="sxs-lookup"><span data-stu-id="a1831-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="a1831-137">Uso dell'equazione spline eremita:</span><span class="sxs-lookup"><span data-stu-id="a1831-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="a1831-138">e sostituendo V1, V2, T1, T2 restituisce:</span><span class="sxs-lookup"><span data-stu-id="a1831-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="a1831-139">Questo può essere ridisposto come segue:</span><span class="sxs-lookup"><span data-stu-id="a1831-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="a1831-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1831-140">Requirements</span></span>



| <span data-ttu-id="a1831-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1831-141">Requirement</span></span> | <span data-ttu-id="a1831-142">Valore</span><span class="sxs-lookup"><span data-stu-id="a1831-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1831-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1831-143">Header</span></span><br/> | <dl> <span data-ttu-id="a1831-144"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1831-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1831-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1831-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1831-146">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="a1831-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
