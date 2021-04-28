---
description: "Funzione D3DXVec2CatmullRom (D3dx9math.h): esegue un'interpolazione Catmull-Rom, usando i vettori 2D specificati."
ms.assetid: dacda32d-b4c4-4d8b-9d20-9a4bb1d3ce6c
title: Funzione D3DXVec2CatmullRom (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c734727f3f2f44c9094885e0e743f605f16c91d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114319"
---
# <a name="d3dxvec2catmullrom-function-d3dx9mathh"></a><span data-ttu-id="df8f7-103">Funzione D3DXVec2CatmullRom (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="df8f7-103">D3DXVec2CatmullRom function (D3dx9math.h)</span></span>

<span data-ttu-id="df8f7-104">Esegue unCatmull-Rom interpolazione, usando i vettori 2D specificati.</span><span class="sxs-lookup"><span data-stu-id="df8f7-104">Performs a Catmull-Rom interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df8f7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="df8f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df8f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df8f7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="df8f7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df8f7-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="df8f7-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="df8f7-109">Puntatore alla [**struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="df8f7-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="df8f7-110">*pV0* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="df8f7-110">*pV0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8f7-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="df8f7-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="df8f7-112">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="df8f7-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="df8f7-113">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="df8f7-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8f7-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="df8f7-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="df8f7-115">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="df8f7-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="df8f7-116">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="df8f7-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8f7-117">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="df8f7-117">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="df8f7-118">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="df8f7-118">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="df8f7-119">*pV3* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="df8f7-119">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8f7-120">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="df8f7-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="df8f7-121">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="df8f7-121">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="df8f7-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df8f7-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df8f7-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df8f7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df8f7-124">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="df8f7-124">Weighting factor.</span></span> <span data-ttu-id="df8f7-125">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="df8f7-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df8f7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df8f7-126">Return value</span></span>

<span data-ttu-id="df8f7-127">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="df8f7-127">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="df8f7-128">Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) che è il risultato dellCatmull-Rom interpolazione.</span><span class="sxs-lookup"><span data-stu-id="df8f7-128">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the Catmull-Rom interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="df8f7-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="df8f7-129">Remarks</span></span>

<span data-ttu-id="df8f7-130">Dati quattro punti (p1, p2, p3, p4), trovare una funzione Q(s) in modo che:</span><span class="sxs-lookup"><span data-stu-id="df8f7-130">Given four points (p1, p2, p3, p4), find a function Q(s) such that:</span></span>


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



<span data-ttu-id="df8f7-131">La Catmull-Rom spline può essere derivata dalla spline Hermite impostando:</span><span class="sxs-lookup"><span data-stu-id="df8f7-131">The Catmull-Rom spline can be derived from the Hermite spline by setting:</span></span>


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



<span data-ttu-id="df8f7-132">dove:</span><span class="sxs-lookup"><span data-stu-id="df8f7-132">where:</span></span>

<span data-ttu-id="df8f7-133">v1 è il contenuto di pV0.</span><span class="sxs-lookup"><span data-stu-id="df8f7-133">v1 is the contents of pV0.</span></span>

<span data-ttu-id="df8f7-134">v2 è il contenuto di pV1.</span><span class="sxs-lookup"><span data-stu-id="df8f7-134">v2 is the contents of pV1.</span></span>

<span data-ttu-id="df8f7-135">p3 è il contenuto di pV2.</span><span class="sxs-lookup"><span data-stu-id="df8f7-135">p3 is the contents of pV2.</span></span>

<span data-ttu-id="df8f7-136">p4 è il contenuto di pV3.</span><span class="sxs-lookup"><span data-stu-id="df8f7-136">p4 is the contents of pV3.</span></span>

<span data-ttu-id="df8f7-137">Uso dell'equazione spline Hermite:</span><span class="sxs-lookup"><span data-stu-id="df8f7-137">Using the Hermite spline equation:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



<span data-ttu-id="df8f7-138">e la sostituzione di v1, v2, t1, t2 produce:</span><span class="sxs-lookup"><span data-stu-id="df8f7-138">and substituting for v1, v2, t1, t2 yields:</span></span>


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



<span data-ttu-id="df8f7-139">Questo può essere riorganizzato come:</span><span class="sxs-lookup"><span data-stu-id="df8f7-139">This can be rearranged as:</span></span>


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a><span data-ttu-id="df8f7-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df8f7-140">Requirements</span></span>



| <span data-ttu-id="df8f7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="df8f7-141">Requirement</span></span> | <span data-ttu-id="df8f7-142">Valore</span><span class="sxs-lookup"><span data-stu-id="df8f7-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df8f7-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df8f7-143">Header</span></span><br/>  | <dl> <span data-ttu-id="df8f7-144"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="df8f7-144"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="df8f7-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="df8f7-145">Library</span></span><br/> | <dl> <span data-ttu-id="df8f7-146"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="df8f7-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df8f7-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df8f7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df8f7-148">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="df8f7-148">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="df8f7-149">**D3DXVec3CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="df8f7-149">**D3DXVec3CatmullRom**</span></span>](d3dxvec3catmullrom.md)
</dt> <dt>

[<span data-ttu-id="df8f7-150">**D3DXVec4CatmullRom**</span><span class="sxs-lookup"><span data-stu-id="df8f7-150">**D3DXVec4CatmullRom**</span></span>](d3dxvec4catmullrom.md)
</dt> </dl>

 

 
