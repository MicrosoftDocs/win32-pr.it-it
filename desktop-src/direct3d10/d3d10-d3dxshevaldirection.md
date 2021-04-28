---
description: 'Funzione D3DXSHEvalDirection (D3DX10.h): valuta le funzioni di base armoniche sferiche (SH) da un vettore di direzione di input.'
ms.assetid: c86973cc-c5b0-4358-b7eb-5c31f38b5b5a
title: Funzione D3DXSHEvalDirection (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirection
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7fa1f94d65ca8096a0398d71ca2f562b643d47a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108589"
---
# <a name="d3dxshevaldirection-function-d3dx10h"></a><span data-ttu-id="f8533-103">Funzione D3DXSHEvalDirection (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="f8533-103">D3DXSHEvalDirection function (D3DX10.h)</span></span>

<span data-ttu-id="f8533-104">Valuta le funzioni di base armoniche sferiche (SH) da un vettore di direzione di input.</span><span class="sxs-lookup"><span data-stu-id="f8533-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8533-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8533-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _In_       FLOAT       *pOut,
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="f8533-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8533-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8533-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f8533-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8533-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8533-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8533-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="f8533-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="f8533-110">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="f8533-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f8533-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f8533-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8533-112">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f8533-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8533-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8533-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8533-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="f8533-114">Order of the SH evaluation.</span></span> <span data-ttu-id="f8533-115">Deve essere compreso nell'intervallo tra D3DXSH \_ MINORDER e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="f8533-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="f8533-116">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="f8533-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f8533-117">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="f8533-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8533-118">*pDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f8533-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8533-119">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8533-119">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f8533-120">Vettore di direzione (x, y, z) in cui valutare le funzioni di base sh.</span><span class="sxs-lookup"><span data-stu-id="f8533-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="f8533-121">Deve essere normalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8533-121">Must be normalized.</span></span> <span data-ttu-id="f8533-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f8533-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8533-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8533-123">Return value</span></span>

<span data-ttu-id="f8533-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8533-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8533-125">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="f8533-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="f8533-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f8533-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8533-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8533-127">Remarks</span></span>

<span data-ttu-id="f8533-128">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l I + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="f8533-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="f8533-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="f8533-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="f8533-130">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="f8533-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="f8533-131">Sulla sfera con raggio unità, come illustrato nella figura seguente, la direzione può essere specificata semplicemente con theta, l'angolo sull'asse z nella direzione a destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="f8533-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="f8533-133">Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="f8533-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="f8533-134">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="f8533-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="f8533-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8533-136">Requirements</span></span>



| <span data-ttu-id="f8533-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8533-137">Requirement</span></span> | <span data-ttu-id="f8533-138">Valore</span><span class="sxs-lookup"><span data-stu-id="f8533-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8533-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8533-139">Header</span></span><br/>  | <dl> <span data-ttu-id="f8533-140"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8533-140"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8533-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8533-141">Library</span></span><br/> | <dl> <span data-ttu-id="f8533-142"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8533-142"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8533-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8533-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8533-144">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f8533-144">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
