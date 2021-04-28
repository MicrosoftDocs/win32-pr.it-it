---
description: 'Funzione D3DXSHRotate (D3DX10.h): ruota il vettore armonico armonico sferico (SH) in base alla matrice specificata.'
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: Funzione D3DXSHRotate (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2f2af3fe59c57ba32bc03bb59233bec72722bbb5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108539"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="fad37-103">Funzione D3DXSHRotate (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="fad37-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="fad37-104">Ruota il vettore armonico armonico (SH) in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="fad37-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fad37-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="fad37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fad37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad37-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fad37-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad37-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fad37-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fad37-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="fad37-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="fad37-110">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="fad37-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fad37-111">Questo puntatore non deve essere associato a pIn.</span><span class="sxs-lookup"><span data-stu-id="fad37-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="fad37-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="fad37-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fad37-113">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fad37-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad37-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fad37-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fad37-115">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="fad37-115">Order of the SH evaluation.</span></span> <span data-ttu-id="fad37-116">Deve essere compreso nell'intervallo tra D3DXSH \_ MINORDER e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="fad37-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="fad37-117">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="fad37-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="fad37-118">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="fad37-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="fad37-119">*pMatrix* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fad37-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad37-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fad37-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fad37-121">Puntatore alla matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="fad37-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="fad37-122">La sottomatrici di rotazione deve essere ortogonale, con un determinante unità.</span><span class="sxs-lookup"><span data-stu-id="fad37-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="fad37-123">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fad37-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad37-124">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="fad37-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fad37-125">Puntatore ai coefficienti SH ruotati.</span><span class="sxs-lookup"><span data-stu-id="fad37-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad37-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fad37-126">Return value</span></span>

<span data-ttu-id="fad37-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fad37-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fad37-128">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="fad37-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad37-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="fad37-129">Remarks</span></span>

<span data-ttu-id="fad37-130">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="fad37-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="fad37-131">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="fad37-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="fad37-132">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="fad37-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="fad37-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fad37-133">Requirements</span></span>



| <span data-ttu-id="fad37-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad37-134">Requirement</span></span> | <span data-ttu-id="fad37-135">Valore</span><span class="sxs-lookup"><span data-stu-id="fad37-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fad37-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fad37-136">Header</span></span><br/>  | <dl> <span data-ttu-id="fad37-137"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="fad37-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="fad37-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="fad37-138">Library</span></span><br/> | <dl> <span data-ttu-id="fad37-139"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fad37-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad37-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fad37-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad37-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="fad37-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
