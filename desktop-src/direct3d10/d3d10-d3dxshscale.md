---
description: Ridimensiona un vettore armonico sferico (SH); in altre parole, il broncio \[ i \] = PA \[ i \] \* scalare.
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: Funzione D3DXSHScale (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHScale
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7aa7ee66b29c7d9816708a8625bb568426a62b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323329"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="5829e-103">Funzione D3DXSHScale (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="5829e-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="5829e-104">Ridimensiona un vettore armonico sferico (SH); in altre parole, il broncio \[ i \] = PA \[ i \] \* scalare.</span><span class="sxs-lookup"><span data-stu-id="5829e-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="5829e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5829e-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="5829e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5829e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5829e-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5829e-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5829e-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5829e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5829e-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="5829e-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="5829e-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="5829e-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5829e-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5829e-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5829e-112">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5829e-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5829e-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5829e-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5829e-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="5829e-114">Order of the SH evaluation.</span></span> <span data-ttu-id="5829e-115">Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="5829e-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="5829e-116">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="5829e-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="5829e-117">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="5829e-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="5829e-118">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5829e-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5829e-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5829e-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5829e-120">Puntatore al vettore SH da scalare.</span><span class="sxs-lookup"><span data-stu-id="5829e-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="5829e-121">*Ridimensiona* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5829e-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5829e-122">Tipo: **const [**float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5829e-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5829e-123">Puntatore al valore della scala.</span><span class="sxs-lookup"><span data-stu-id="5829e-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5829e-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5829e-124">Return value</span></span>

<span data-ttu-id="5829e-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5829e-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5829e-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="5829e-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="5829e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="5829e-127">Remarks</span></span>

<span data-ttu-id="5829e-128">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="5829e-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="5829e-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="5829e-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="5829e-130">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="5829e-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="5829e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5829e-131">Requirements</span></span>



| <span data-ttu-id="5829e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5829e-132">Requirement</span></span> | <span data-ttu-id="5829e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5829e-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5829e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5829e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5829e-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5829e-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5829e-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="5829e-136">Library</span></span><br/> | <dl> <span data-ttu-id="5829e-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5829e-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5829e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5829e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5829e-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="5829e-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
