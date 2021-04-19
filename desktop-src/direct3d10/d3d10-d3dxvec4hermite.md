---
description: Esegue un'interpolazione spline eremita, usando i vettori 4D specificati.
ms.assetid: 8fddcd47-8c8a-4e14-86db-07dd44ec5767
title: Funzione D3DXVec4Hermite (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Hermite
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 49a8f1ea09f055085e9d4befc248203276b85eb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323389"
---
# <a name="d3dxvec4hermite-function-d3dx10mathh"></a><span data-ttu-id="32c74-103">Funzione D3DXVec4Hermite (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="32c74-103">D3DXVec4Hermite function (D3DX10Math.h)</span></span>

<span data-ttu-id="32c74-104">Esegue un'interpolazione spline eremita, usando i vettori 4D specificati.</span><span class="sxs-lookup"><span data-stu-id="32c74-104">Performs a Hermite spline interpolation, using the specified 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c74-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32c74-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Hermite(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pT1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="32c74-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32c74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c74-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="32c74-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="32c74-108">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="32c74-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="32c74-109">Puntatore a [**D3DXVECTOR4**](d3d10-d3dxvector4.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="32c74-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="32c74-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32c74-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c74-111">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="32c74-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="32c74-112">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="32c74-112">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="32c74-113">*pt1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32c74-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c74-114">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="32c74-114">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="32c74-115">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore tangente.</span><span class="sxs-lookup"><span data-stu-id="32c74-115">Pointer to a source D3DXVECTOR4 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="32c74-116">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32c74-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c74-117">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="32c74-117">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="32c74-118">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="32c74-118">Pointer to a source D3DXVECTOR4 structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="32c74-119">*PT2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32c74-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c74-120">Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="32c74-120">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="32c74-121">Puntatore a una struttura D3DXVECTOR4 di origine, un vettore tangente.</span><span class="sxs-lookup"><span data-stu-id="32c74-121">Pointer to a source D3DXVECTOR4 structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="32c74-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32c74-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c74-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32c74-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32c74-124">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="32c74-124">Weighting factor.</span></span> <span data-ttu-id="32c74-125">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="32c74-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c74-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32c74-126">Return value</span></span>

<span data-ttu-id="32c74-127">Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="32c74-127">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="32c74-128">Puntatore a una struttura D3DXVECTOR4 che è il risultato dell'interpolazione della spline eremita.</span><span class="sxs-lookup"><span data-stu-id="32c74-128">Pointer to a D3DXVECTOR4 structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="32c74-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="32c74-129">Remarks</span></span>

<span data-ttu-id="32c74-130">La funzione **D3DXVec4Hermite** esegue l'interpolazione da (PositionA, tangentea) a (PositionB, tangentB) usando l'interpolazione spline eremita.</span><span class="sxs-lookup"><span data-stu-id="32c74-130">The **D3DXVec4Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="32c74-131">L'interpolazione spline è una generalizzazione della spline di Ease-Out.</span><span class="sxs-lookup"><span data-stu-id="32c74-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="32c74-132">La rampa è una funzione di Q (s) con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="32c74-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="32c74-133">Q (s) = come ³ + BS ² + CS + D (e quindi Q '/s = 3As ² + 2B + C)</span><span class="sxs-lookup"><span data-stu-id="32c74-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="32c74-134">a) Q (0) = V1, quindi Q ' (0) = T1</span><span class="sxs-lookup"><span data-stu-id="32c74-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="32c74-135">b) Q (1) = V2, quindi Q ' (1) = T2</span><span class="sxs-lookup"><span data-stu-id="32c74-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="32c74-136">V1 è il contenuto di pV1, V2 nel contenuto di pV2, T1 è il contenuto di pT1 e T2 è il contenuto di pT2.</span><span class="sxs-lookup"><span data-stu-id="32c74-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="32c74-137">Queste proprietà vengono utilizzate per la risoluzione di un oggetto, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="32c74-137">These properties are used to solve for A, B, C, D.</span></span>


```
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```



<span data-ttu-id="32c74-138">Collegare le soluzioni per a, B, C e D per generare Q (s).</span><span class="sxs-lookup"><span data-stu-id="32c74-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>


```
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```



<span data-ttu-id="32c74-139">Il risultato è il seguente:</span><span class="sxs-lookup"><span data-stu-id="32c74-139">This yields:</span></span>

<span data-ttu-id="32c74-140">Q (s) = (2V1-2v2 + T2 + T1) s ³ + (3V2-3V1-2T1-T2) s ² + T1s + V1</span><span class="sxs-lookup"><span data-stu-id="32c74-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="32c74-141">Che può essere ridisposto come segue:</span><span class="sxs-lookup"><span data-stu-id="32c74-141">Which can be rearranged as:</span></span>

<span data-ttu-id="32c74-142">Q (s) = (2S ³-3S ² + 1) V1 + (-2S ³ + 3S ²) V2 + (s ³-2S ² + s) T1 + (s ³-s ²) T2</span><span class="sxs-lookup"><span data-stu-id="32c74-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="32c74-143">Le spline di eremita sono utili per controllare l'animazione perché la curva viene eseguita attraverso tutti i punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="32c74-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="32c74-144">Inoltre, poiché la posizione e la tangente vengono specificate in modo esplicito alle estremità di ogni segmento, è facile creare una curva C2 continua, purché si assicuri che la posizione iniziale e la tangente corrispondano ai valori finali dell'ultimo segmento.</span><span class="sxs-lookup"><span data-stu-id="32c74-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="32c74-145">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="32c74-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="32c74-146">In questo modo, la funzione **D3DXVec4Hermite** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="32c74-146">In this way, the **D3DXVec4Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c74-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32c74-147">Requirements</span></span>



| <span data-ttu-id="32c74-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c74-148">Requirement</span></span> | <span data-ttu-id="32c74-149">Valore</span><span class="sxs-lookup"><span data-stu-id="32c74-149">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32c74-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32c74-150">Header</span></span><br/> | <dl> <span data-ttu-id="32c74-151"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c74-151"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32c74-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32c74-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c74-153">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="32c74-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
