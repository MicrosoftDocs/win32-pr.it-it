---
description: "Funzione D3DXVec2Hermite (D3dx9math.h): esegue un'interpolazione spline hermite usando i vettori 2D specificati."
ms.assetid: 30eb9490-bc01-4449-adfb-1c552e8ad3e7
title: Funzione D3DXVec2Hermite (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Hermite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88073e23826362e1f9a753f411ac89ac1e272fc6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097989"
---
# <a name="d3dxvec2hermite-function-d3dx9mathh"></a><span data-ttu-id="abbd7-103">Funzione D3DXVec2Hermite (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="abbd7-103">D3DXVec2Hermite function (D3dx9math.h)</span></span>

<span data-ttu-id="abbd7-104">Esegue un'interpolazione spline hermite, usando i vettori 2D specificati.</span><span class="sxs-lookup"><span data-stu-id="abbd7-104">Performs a Hermite spline interpolation, using the specified 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="abbd7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abbd7-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Hermite(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pT1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pT2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="abbd7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="abbd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abbd7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="abbd7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="abbd7-108">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="abbd7-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="abbd7-109">Puntatore alla [**struttura D3DXVECTOR2**](d3dxvector2.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="abbd7-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="abbd7-110">*pV1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="abbd7-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbd7-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="abbd7-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="abbd7-112">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="abbd7-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="abbd7-113">*pT1* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="abbd7-113">*pT1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbd7-114">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="abbd7-114">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="abbd7-115">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore tangente.</span><span class="sxs-lookup"><span data-stu-id="abbd7-115">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="abbd7-116">*pV2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="abbd7-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbd7-117">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="abbd7-117">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="abbd7-118">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore di posizione.</span><span class="sxs-lookup"><span data-stu-id="abbd7-118">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a position vector.</span></span>

</dd> <dt>

<span data-ttu-id="abbd7-119">*pT2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="abbd7-119">*pT2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbd7-120">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="abbd7-120">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="abbd7-121">Puntatore a una [**struttura D3DXVECTOR2 di**](d3dxvector2.md) origine, un vettore tangente.</span><span class="sxs-lookup"><span data-stu-id="abbd7-121">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure, a tangent vector.</span></span>

</dd> <dt>

<span data-ttu-id="abbd7-122">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abbd7-122">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abbd7-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="abbd7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="abbd7-124">Fattore di ponderazione.</span><span class="sxs-lookup"><span data-stu-id="abbd7-124">Weighting factor.</span></span> <span data-ttu-id="abbd7-125">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="abbd7-125">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abbd7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abbd7-126">Return value</span></span>

<span data-ttu-id="abbd7-127">Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="abbd7-127">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="abbd7-128">Puntatore a [**una struttura D3DXVECTOR2**](d3dxvector2.md) che è il risultato dell'interpolazione spline hermite.</span><span class="sxs-lookup"><span data-stu-id="abbd7-128">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the Hermite spline interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="abbd7-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="abbd7-129">Remarks</span></span>

<span data-ttu-id="abbd7-130">La **funzione D3DXVec2Hermite** interpola da (positionA, tangentA) a (positionB, tangentB) usando l'interpolazione spline hermite.</span><span class="sxs-lookup"><span data-stu-id="abbd7-130">The **D3DXVec2Hermite** function interpolates from (positionA, tangentA) to (positionB, tangentB) using Hermite spline interpolation.</span></span>

<span data-ttu-id="abbd7-131">L'interpolazione spline è una generalizzazione della spline ease-in e ease-out.</span><span class="sxs-lookup"><span data-stu-id="abbd7-131">The spline interpolation is a generalization of the ease-in, ease-out spline.</span></span> <span data-ttu-id="abbd7-132">La rampa è una funzione di Q(s) con le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="abbd7-132">The ramp is a function of Q(s) with the following properties.</span></span>

<span data-ttu-id="abbd7-133">Q(s) = As³ + Bs² + Cs + D (e quindi, Q(s) = 3As² + 2Bs + C)</span><span class="sxs-lookup"><span data-stu-id="abbd7-133">Q(s) = As³ + Bs² + Cs + D (and therefore, Q'(s) = 3As² + 2Bs + C)</span></span>

<span data-ttu-id="abbd7-134">a) Q(0) = v1, quindi Q'(0) = t1</span><span class="sxs-lookup"><span data-stu-id="abbd7-134">a) Q(0) = v1, so Q'(0) = t1</span></span>

<span data-ttu-id="abbd7-135">b) Q(1) = v2, quindi Q'(1) = t2</span><span class="sxs-lookup"><span data-stu-id="abbd7-135">b) Q(1) = v2, so Q'(1) = t2</span></span>

<span data-ttu-id="abbd7-136">v1 è il contenuto di pV1, v2 nel contenuto di pV2, t1 è il contenuto di pT1 e t2 è il contenuto di pT2.</span><span class="sxs-lookup"><span data-stu-id="abbd7-136">v1 is the contents of pV1, v2 in the contents of pV2, t1 is the contents of pT1, and t2 is the contents of pT2.</span></span>

<span data-ttu-id="abbd7-137">Queste proprietà vengono usate per risolvere A, B, C, D.</span><span class="sxs-lookup"><span data-stu-id="abbd7-137">These properties are used to solve for A, B, C, D.</span></span>

``` syntax
D = v1  (from a)
C = t1  (from a)
3A + 2B = t2 - t-1 (substituting for C)
A + B = v2 - v1 - t1 (substituting for C and D)
```

<span data-ttu-id="abbd7-138">Collegare le soluzioni per A, B, C e D per generare domande e risposte.</span><span class="sxs-lookup"><span data-stu-id="abbd7-138">Plug in the solutions for A,B,C and D to generate Q(s).</span></span>

``` syntax
A = 2v1 - 2v2 + t2 + t1 
B = 3v2 - 3v1 - 2t1 - t2
C = t1 
D = v1
```

<span data-ttu-id="abbd7-139">Il risultato è il seguente:</span><span class="sxs-lookup"><span data-stu-id="abbd7-139">This yields:</span></span>

<span data-ttu-id="abbd7-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span><span class="sxs-lookup"><span data-stu-id="abbd7-140">Q(s) = (2v1 - 2v2 + t2 + t1)s³ + (3v2 - 3v1 - 2t1 - t2)s² + t1s + v1</span></span>

<span data-ttu-id="abbd7-141">Che può essere ridisporto come:</span><span class="sxs-lookup"><span data-stu-id="abbd7-141">Which can be rearranged as:</span></span>

<span data-ttu-id="abbd7-142">Q(s) = (2s² - 3s² + 1)v1 + (-2s² + 3s²)v2 + (s³ - 2s² + s)t1 + (s² - s²)t2</span><span class="sxs-lookup"><span data-stu-id="abbd7-142">Q(s) = (2s³ - 3s² + 1)v1 + (-2s³ + 3s²)v2 + (s³ - 2s² + s)t1 + (s³ - s²)t2</span></span>

<span data-ttu-id="abbd7-143">Le spline ermeti sono utili per controllare l'animazione perché la curva attraversa tutti i punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="abbd7-143">Hermite splines are useful for controlling animation because the curve runs through all the control points.</span></span> <span data-ttu-id="abbd7-144">Inoltre, poiché la posizione e la tangente vengono specificate in modo esplicito alle estremità di ogni segmento, è facile creare una curva continua C2, purché la posizione iniziale e la tangente corrispondano ai valori finali dell'ultimo segmento.</span><span class="sxs-lookup"><span data-stu-id="abbd7-144">Also, because the position and tangent are explicitly specified at the ends of each segment, it is easy to create a C2 continuous curve as long as you make sure that your starting position and tangent match the ending values of the last segment.</span></span>

<span data-ttu-id="abbd7-145">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="abbd7-145">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="abbd7-146">In questo modo, la **funzione D3DXVec2Hermite** può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="abbd7-146">In this way, the **D3DXVec2Hermite** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="abbd7-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abbd7-147">Requirements</span></span>



| <span data-ttu-id="abbd7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="abbd7-148">Requirement</span></span> | <span data-ttu-id="abbd7-149">Valore</span><span class="sxs-lookup"><span data-stu-id="abbd7-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abbd7-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abbd7-150">Header</span></span><br/>  | <dl> <span data-ttu-id="abbd7-151"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="abbd7-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="abbd7-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="abbd7-152">Library</span></span><br/> | <dl> <span data-ttu-id="abbd7-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="abbd7-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="abbd7-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abbd7-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abbd7-155">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="abbd7-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
