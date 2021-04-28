---
description: "Funzione D3DXSHRotateZ (D3dx9math.h): ruota il vettore armonico armonico sferico (SH) nell'asse z in base all'angolo specificato."
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: Funzione D3DXSHRotateZ (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed7db57dc3acedd1e65edab7377b525940ea10e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117849"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="8a159-103">Funzione D3DXSHRotateZ (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8a159-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="8a159-104">Ruota il vettore armonico armonico (SH) nell'asse z in base all'angolo specificato.</span><span class="sxs-lookup"><span data-stu-id="8a159-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a159-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a159-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="8a159-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a159-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a159-107">*pOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="8a159-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a159-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a159-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8a159-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="8a159-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="8a159-110">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="8a159-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="8a159-111">Questo puntatore non deve creare un alias *con pIn*.</span><span class="sxs-lookup"><span data-stu-id="8a159-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="8a159-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="8a159-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8a159-113">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8a159-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a159-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a159-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a159-115">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="8a159-115">Order of the SH evaluation.</span></span> <span data-ttu-id="8a159-116">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="8a159-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="8a159-117">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="8a159-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="8a159-118">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="8a159-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="8a159-119">*Angolo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8a159-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a159-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a159-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a159-121">Angolo di rotazione in radianti.</span><span class="sxs-lookup"><span data-stu-id="8a159-121">Rotation angle in radians.</span></span> <span data-ttu-id="8a159-122">La rotazione viene eseguita intorno all'asse z.</span><span class="sxs-lookup"><span data-stu-id="8a159-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="8a159-123">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8a159-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a159-124">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a159-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8a159-125">Puntatore ai coefficienti SH ruotati.</span><span class="sxs-lookup"><span data-stu-id="8a159-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a159-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a159-126">Return value</span></span>

<span data-ttu-id="8a159-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a159-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8a159-128">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="8a159-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a159-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a159-129">Remarks</span></span>

<span data-ttu-id="8a159-130">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l I + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="8a159-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="8a159-131">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="8a159-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="8a159-132">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="8a159-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a159-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a159-133">Requirements</span></span>



| <span data-ttu-id="8a159-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a159-134">Requirement</span></span> | <span data-ttu-id="8a159-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8a159-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a159-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a159-136">Header</span></span><br/>  | <dl> <span data-ttu-id="8a159-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8a159-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8a159-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a159-138">Library</span></span><br/> | <dl> <span data-ttu-id="8a159-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a159-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a159-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a159-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a159-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="8a159-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8a159-142">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8a159-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
