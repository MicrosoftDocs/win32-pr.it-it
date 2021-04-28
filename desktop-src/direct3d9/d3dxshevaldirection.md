---
description: 'Funzione D3DXSHEvalDirection (D3dx9math.h): valuta le funzioni di base armoniche sferiche (SH) da un vettore di direzione di input.'
ms.assetid: f30ba32c-d6b0-4e4e-b5cd-839ed7821855
title: Funzione D3DXSHEvalDirection (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e02f0f3d8770b4b703f275de3225eacb301a7843
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093962"
---
# <a name="d3dxshevaldirection-function-d3dx9mathh"></a><span data-ttu-id="207bf-103">Funzione D3DXSHEvalDirection (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="207bf-103">D3DXSHEvalDirection function (D3dx9math.h)</span></span>

<span data-ttu-id="207bf-104">Valuta le funzioni di base armoniche sferiche (SH) da un vettore di direzione di input.</span><span class="sxs-lookup"><span data-stu-id="207bf-104">Evaluates the spherical harmonic (SH) basis functions from an input direction vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="207bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="207bf-105">Syntax</span></span>


```C++
FLOAT* D3DXSHEvalDirection(
  _Out_       FLOAT       *pOut,
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir
);
```



## <a name="parameters"></a><span data-ttu-id="207bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="207bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="207bf-107">*pOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="207bf-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="207bf-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="207bf-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="207bf-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="207bf-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="207bf-110">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="207bf-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="207bf-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="207bf-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="207bf-112">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="207bf-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207bf-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="207bf-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="207bf-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="207bf-114">Order of the SH evaluation.</span></span> <span data-ttu-id="207bf-115">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="207bf-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="207bf-116">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="207bf-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="207bf-117">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="207bf-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="207bf-118">*pDir* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="207bf-118">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207bf-119">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="207bf-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="207bf-120">Vettore di direzione (x, y, z) in cui valutare le funzioni di base sh.</span><span class="sxs-lookup"><span data-stu-id="207bf-120">(x, y, z) direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="207bf-121">Deve essere normalizzato.</span><span class="sxs-lookup"><span data-stu-id="207bf-121">Must be normalized.</span></span> <span data-ttu-id="207bf-122">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="207bf-122">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="207bf-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="207bf-123">Return value</span></span>

<span data-ttu-id="207bf-124">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="207bf-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="207bf-125">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="207bf-125">Pointer to SH output coefficients.</span></span> <span data-ttu-id="207bf-126">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="207bf-126">See Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="207bf-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="207bf-127">Remarks</span></span>

<span data-ttu-id="207bf-128">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l I + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="207bf-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="207bf-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="207bf-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="207bf-130">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="207bf-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

<span data-ttu-id="207bf-131">Sulla sfera con raggio dell'unità, come illustrato nella figura seguente, la direzione può essere specificata [](coordinate-systems.md)semplicemente con theta, l'angolo verso l'asse z nella direzione a destra e phi, l'angolo da z.</span><span class="sxs-lookup"><span data-stu-id="207bf-131">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![illustrazione di una sfera con raggio unità](images/spherical-coordinates.png)

<span data-ttu-id="207bf-133">Le equazioni seguenti mostrano la relazione tra le coordinate cartesiane (x, y, z) e sferiche (theta, phi) sulla sfera unità.</span><span class="sxs-lookup"><span data-stu-id="207bf-133">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="207bf-134">L'angolo theta varia nell'intervallo da 0 a 2 pi greco, mentre phi varia da 0 a pi greco.</span><span class="sxs-lookup"><span data-stu-id="207bf-134">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equazioni della relazione tra coordinate cartesiane e sferiche](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="207bf-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="207bf-136">Requirements</span></span>



| <span data-ttu-id="207bf-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="207bf-137">Requirement</span></span> | <span data-ttu-id="207bf-138">Valore</span><span class="sxs-lookup"><span data-stu-id="207bf-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="207bf-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="207bf-139">Header</span></span><br/>  | <dl> <span data-ttu-id="207bf-140"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="207bf-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="207bf-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="207bf-141">Library</span></span><br/> | <dl> <span data-ttu-id="207bf-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="207bf-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="207bf-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="207bf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207bf-144">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="207bf-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="207bf-145">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="207bf-145">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
