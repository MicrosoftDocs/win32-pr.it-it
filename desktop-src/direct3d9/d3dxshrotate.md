---
description: 'Funzione D3DXSHRotate (D3dx9math.h): ruota il vettore armonico armonico sferico (SH) in base alla matrice specificata.'
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: Funzione D3DXSHRotate (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f888186fb6d7563a5904d4e6e3f1eabe626afd1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093869"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="063ff-103">Funzione D3DXSHRotate (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="063ff-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="063ff-104">Ruota il vettore armonico armonico (SH) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="063ff-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="063ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="063ff-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="063ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="063ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="063ff-107">*pOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="063ff-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="063ff-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="063ff-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="063ff-109">Puntatore ai coefficienti di output armoniosi sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="063ff-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="063ff-110">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="063ff-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="063ff-111">Questo puntatore non deve creare un alias *con pIn*.</span><span class="sxs-lookup"><span data-stu-id="063ff-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="063ff-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="063ff-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="063ff-113">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="063ff-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063ff-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="063ff-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="063ff-115">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="063ff-115">Order of the SH evaluation.</span></span> <span data-ttu-id="063ff-116">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="063ff-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="063ff-117">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="063ff-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="063ff-118">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="063ff-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="063ff-119">*pMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="063ff-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063ff-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="063ff-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="063ff-121">Puntatore alla matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="063ff-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="063ff-122">La sottomatrici di rotazione deve essere ortogonale, con un determinante unità.</span><span class="sxs-lookup"><span data-stu-id="063ff-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="063ff-123">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="063ff-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="063ff-124">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="063ff-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="063ff-125">Puntatore ai coefficienti SH ruotati.</span><span class="sxs-lookup"><span data-stu-id="063ff-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="063ff-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="063ff-126">Return value</span></span>

<span data-ttu-id="063ff-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="063ff-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="063ff-128">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="063ff-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="063ff-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="063ff-129">Remarks</span></span>

<span data-ttu-id="063ff-130">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l I + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="063ff-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="063ff-131">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="063ff-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="063ff-132">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="063ff-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="063ff-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="063ff-133">Requirements</span></span>



| <span data-ttu-id="063ff-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="063ff-134">Requirement</span></span> | <span data-ttu-id="063ff-135">Valore</span><span class="sxs-lookup"><span data-stu-id="063ff-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="063ff-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="063ff-136">Header</span></span><br/>  | <dl> <span data-ttu-id="063ff-137"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="063ff-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="063ff-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="063ff-138">Library</span></span><br/> | <dl> <span data-ttu-id="063ff-139"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="063ff-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="063ff-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="063ff-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="063ff-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="063ff-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="063ff-142">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="063ff-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
