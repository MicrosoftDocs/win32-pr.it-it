---
description: Ruota il vettore armonico sferico (SH) per la matrice specificata.
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: Funzione D3DXSHRotate (D3DX10. h)
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
ms.openlocfilehash: 1cdff4a74cb92943db2bd6dc9f207dbac2208afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323331"
---
# <a name="d3dxshrotate-function-d3dx10h"></a><span data-ttu-id="15fe4-103">Funzione D3DXSHRotate (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="15fe4-103">D3DXSHRotate function (D3DX10.h)</span></span>

<span data-ttu-id="15fe4-104">Ruota il vettore armonico sferico (SH) per la matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="15fe4-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fe4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15fe4-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="15fe4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15fe4-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15fe4-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fe4-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="15fe4-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15fe4-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="15fe4-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="15fe4-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="15fe4-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="15fe4-111">Questo puntatore non deve avere alias con pIn.</span><span class="sxs-lookup"><span data-stu-id="15fe4-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="15fe4-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="15fe4-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="15fe4-113">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="15fe4-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fe4-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15fe4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15fe4-115">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="15fe4-115">Order of the SH evaluation.</span></span> <span data-ttu-id="15fe4-116">Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="15fe4-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="15fe4-117">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="15fe4-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="15fe4-118">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="15fe4-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="15fe4-119">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15fe4-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fe4-120">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="15fe4-120">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="15fe4-121">Puntatore alla matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="15fe4-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="15fe4-122">La sottomatrice di rotazione deve essere ortogonale, con un determinante di unità.</span><span class="sxs-lookup"><span data-stu-id="15fe4-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="15fe4-123">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15fe4-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fe4-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="15fe4-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15fe4-125">Puntatore ai coefficienti SH ruotati.</span><span class="sxs-lookup"><span data-stu-id="15fe4-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15fe4-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15fe4-126">Return value</span></span>

<span data-ttu-id="15fe4-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="15fe4-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15fe4-128">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="15fe4-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="15fe4-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="15fe4-129">Remarks</span></span>

<span data-ttu-id="15fe4-130">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="15fe4-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="15fe4-131">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="15fe4-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="15fe4-132">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="15fe4-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="15fe4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15fe4-133">Requirements</span></span>



| <span data-ttu-id="15fe4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="15fe4-134">Requirement</span></span> | <span data-ttu-id="15fe4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="15fe4-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15fe4-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15fe4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="15fe4-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="15fe4-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="15fe4-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="15fe4-138">Library</span></span><br/> | <dl> <span data-ttu-id="15fe4-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15fe4-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15fe4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15fe4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fe4-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="15fe4-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
