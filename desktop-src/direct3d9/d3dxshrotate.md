---
description: Ruota il vettore armonico sferico (SH) per la matrice specificata.
ms.assetid: 9e319725-6cbb-441e-b996-ec2c6f66e5df
title: Funzione D3DXSHRotate (D3dx9math. h)
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
ms.openlocfilehash: 606ef1909237fd9c0277c5d7112284f6b7018e0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322588"
---
# <a name="d3dxshrotate-function-d3dx9mathh"></a><span data-ttu-id="31056-103">Funzione D3DXSHRotate (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="31056-103">D3DXSHRotate function (D3dx9math.h)</span></span>

<span data-ttu-id="31056-104">Ruota il vettore armonico sferico (SH) per la matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="31056-104">Rotates the spherical harmonic (SH) vector by the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="31056-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31056-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotate(
  _Out_       FLOAT      *pOut,
  _In_        UINT       Order,
  _In_  const D3DXMATRIX *pMatrix,
  _In_  const FLOAT      *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="31056-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="31056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31056-107">*broncio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="31056-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31056-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31056-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31056-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="31056-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="31056-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="31056-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="31056-111">Questo puntatore non deve avere alias con *pin*.</span><span class="sxs-lookup"><span data-stu-id="31056-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="31056-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="31056-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="31056-113">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="31056-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31056-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31056-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31056-115">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="31056-115">Order of the SH evaluation.</span></span> <span data-ttu-id="31056-116">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="31056-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="31056-117">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="31056-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="31056-118">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="31056-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="31056-119">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31056-119">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31056-120">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="31056-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="31056-121">Puntatore alla matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="31056-121">Pointer to the rotation matrix.</span></span> <span data-ttu-id="31056-122">La sottomatrice di rotazione deve essere ortogonale, con un determinante di unità.</span><span class="sxs-lookup"><span data-stu-id="31056-122">The rotation sub-matrix must be orthogonal, with a unit determinant.</span></span>

</dd> <dt>

<span data-ttu-id="31056-123">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31056-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31056-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="31056-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31056-125">Puntatore ai coefficienti SH ruotati.</span><span class="sxs-lookup"><span data-stu-id="31056-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31056-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31056-126">Return value</span></span>

<span data-ttu-id="31056-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="31056-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31056-128">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="31056-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="31056-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="31056-129">Remarks</span></span>

<span data-ttu-id="31056-130">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="31056-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="31056-131">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="31056-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="31056-132">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="31056-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="31056-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31056-133">Requirements</span></span>



| <span data-ttu-id="31056-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="31056-134">Requirement</span></span> | <span data-ttu-id="31056-135">Valore</span><span class="sxs-lookup"><span data-stu-id="31056-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31056-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31056-136">Header</span></span><br/>  | <dl> <span data-ttu-id="31056-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="31056-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="31056-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="31056-138">Library</span></span><br/> | <dl> <span data-ttu-id="31056-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31056-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31056-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31056-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31056-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="31056-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="31056-142">Trasferimento Radiance pre-calcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="31056-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
