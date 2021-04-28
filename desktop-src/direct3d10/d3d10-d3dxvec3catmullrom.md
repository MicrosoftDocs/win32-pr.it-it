---
description: "Funzione D3DXVec3CatmullRom (D3DX10Math.h): esegue un'interpolazione Catmull-Rom, usando i vettori 3D specificati."
ms.assetid: 324bd4b5-b0df-4dd3-b370-3c365c9f2db1
title: Funzione D3DXVec3CatmullRom (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: a09d61e9c43624f441975eca1a131a82f8092587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108219"
---
# <a name="d3dxvec3catmullrom-function-d3dx10mathh"></a><span data-ttu-id="ea8cb-103">Funzione D3DXVec3CatmullRom (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="ea8cb-103">D3DXVec3CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="ea8cb-104">Esegue un Catmull-Rom interpolazione, usando i vettori 3D specificati.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-104">Performs a Catmull-Rom interpolation, using the specified 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea8cb-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3CatmullRom(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV0,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="ea8cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea8cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8cb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ea8cb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8cb-108">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea8cb-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea8cb-109">Puntatore a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cb-110">*pV0* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea8cb-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8cb-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea8cb-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea8cb-112">Puntatore a una struttura D3DXVECTOR3 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-112">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cb-113">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea8cb-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8cb-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea8cb-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea8cb-115">Puntatore a una struttura D3DXVECTOR3 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-115">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cb-116">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea8cb-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8cb-117">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea8cb-117">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea8cb-118">Puntatore a una struttura D3DXVECTOR3 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-118">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cb-119">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea8cb-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8cb-120">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea8cb-120">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea8cb-121">Puntatore a una struttura D3DXVECTOR3 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-121">Pointer to a source D3DXVECTOR3 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="ea8cb-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea8cb-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8cb-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea8cb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea8cb-124">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-124">Weighting factor.</span></span> <span data-ttu-id="ea8cb-125">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8cb-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea8cb-126">Return value</span></span>

<span data-ttu-id="ea8cb-127">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea8cb-127">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ea8cb-128">Puntatore a una struttura D3DXVECTOR3 che rappresenta il risultato dellCatmull-Rom interpolazione.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-128">Pointer to a D3DXVECTOR3 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8cb-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea8cb-129">Remarks</span></span>

<span data-ttu-id="ea8cb-130">Dati quattro punti (p1, p2, p3, p4), trovare una funzione Q(s) in modo che:</span><span class="sxs-lookup"><span data-stu-id="ea8cb-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="ea8cb-131">La Catmull-Rom spline può essere derivata dalla spline hermite impostando:</span><span class="sxs-lookup"><span data-stu-id="ea8cb-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="ea8cb-132">dove:</span><span class="sxs-lookup"><span data-stu-id="ea8cb-132">where:</span></span>

<span data-ttu-id="ea8cb-133">v1 è il contenuto di pV0.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="ea8cb-134">v2 è il contenuto di pV1.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="ea8cb-135">p3 è il contenuto di pV2.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="ea8cb-136">p4 è il contenuto di pV3.</span><span class="sxs-lookup"><span data-stu-id="ea8cb-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="ea8cb-137">Uso dell'equazione spline hermite:</span><span class="sxs-lookup"><span data-stu-id="ea8cb-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="ea8cb-138">e sostituendo v1, v2, t1, t2 produce:</span><span class="sxs-lookup"><span data-stu-id="ea8cb-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



<span data-ttu-id="ea8cb-139">Questa operazione può essere ridisposta nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ea8cb-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="ea8cb-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea8cb-140">Requirements</span></span>



| <span data-ttu-id="ea8cb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea8cb-141">Requirement</span></span> | <span data-ttu-id="ea8cb-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ea8cb-142">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8cb-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea8cb-143">Header</span></span><br/> | <dl> <span data-ttu-id="ea8cb-144"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8cb-144"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8cb-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea8cb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8cb-146">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="ea8cb-146">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
