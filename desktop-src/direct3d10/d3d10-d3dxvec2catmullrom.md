---
description: "Funzione D3DXVec2CatmullRom (D3DX10Math.h): esegue un'interpolazione Catmull-Rom, usando i vettori 2D specificati."
ms.assetid: 8ec1abfa-0fa9-486a-b86d-bbb8f1d63849
title: Funzione D3DXVec2CatmullRom (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CatmullRom
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41b61d9488e09b72c73cba885d836c6451631c56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108409"
---
# <a name="d3dxvec2catmullrom-function-d3dx10mathh"></a><span data-ttu-id="bac52-103">Funzione D3DXVec2CatmullRom (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="bac52-103">D3DXVec2CatmullRom function (D3DX10Math.h)</span></span>

<span data-ttu-id="bac52-104">Esegue un Catmull-Rom interpolazione, usando i vettori 2D specificati.</span><span class="sxs-lookup"><span data-stu-id="bac52-104">Performs a Catmull-Rom interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bac52-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2CatmullRom(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV0,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="bac52-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bac52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bac52-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bac52-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bac52-108">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bac52-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bac52-109">Puntatore a [**D3DXVECTOR2**](d3d10-d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bac52-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bac52-110">*pV0* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bac52-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac52-111">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bac52-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bac52-112">Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="bac52-112">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="bac52-113">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bac52-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac52-114">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bac52-114">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bac52-115">Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="bac52-115">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="bac52-116">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bac52-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac52-117">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bac52-117">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bac52-118">Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="bac52-118">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="bac52-119">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="bac52-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac52-120">Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bac52-120">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bac52-121">Puntatore a una struttura D3DXVECTOR2 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="bac52-121">Pointer to a source D3DXVECTOR2 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="bac52-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bac52-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bac52-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bac52-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bac52-124">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="bac52-124">Weighting factor.</span></span> <span data-ttu-id="bac52-125">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="bac52-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bac52-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bac52-126">Return value</span></span>

<span data-ttu-id="bac52-127">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bac52-127">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bac52-128">Puntatore a una struttura D3DXVECTOR2 che rappresenta il risultato dellCatmull-Rom interpolazione.</span><span class="sxs-lookup"><span data-stu-id="bac52-128">Pointer to a D3DXVECTOR2 structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="bac52-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="bac52-129">Remarks</span></span>

<span data-ttu-id="bac52-130">Dati quattro punti (p1, p2, p3, p4), trovare una funzione Q(s) in modo che:</span><span class="sxs-lookup"><span data-stu-id="bac52-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="bac52-131">La Catmull-Rom spline può essere derivata dalla spline hermite impostando:</span><span class="sxs-lookup"><span data-stu-id="bac52-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="bac52-132">dove:</span><span class="sxs-lookup"><span data-stu-id="bac52-132">where:</span></span>

<span data-ttu-id="bac52-133">v1 è il contenuto di pV0.</span><span class="sxs-lookup"><span data-stu-id="bac52-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="bac52-134">v2 è il contenuto di pV1.</span><span class="sxs-lookup"><span data-stu-id="bac52-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="bac52-135">p3 è il contenuto di pV2.</span><span class="sxs-lookup"><span data-stu-id="bac52-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="bac52-136">p4 è il contenuto di pV3.</span><span class="sxs-lookup"><span data-stu-id="bac52-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="bac52-137">Uso dell'equazione spline hermite:</span><span class="sxs-lookup"><span data-stu-id="bac52-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="bac52-138">e sostituendo v1, v2, t1, t2 produce:</span><span class="sxs-lookup"><span data-stu-id="bac52-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



<span data-ttu-id="bac52-139">Questa operazione può essere ridisposta nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="bac52-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="bac52-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bac52-140">Requirements</span></span>



| <span data-ttu-id="bac52-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bac52-141">Requirement</span></span> | <span data-ttu-id="bac52-142">Valore</span><span class="sxs-lookup"><span data-stu-id="bac52-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bac52-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bac52-143">Header</span></span><br/>  | <dl> <span data-ttu-id="bac52-144"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bac52-144"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bac52-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="bac52-145">Library</span></span><br/> | <dl> <span data-ttu-id="bac52-146"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bac52-146"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bac52-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bac52-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac52-148">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="bac52-148">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
