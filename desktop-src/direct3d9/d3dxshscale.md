---
description: Ridimensiona un vettore armonico sferico (SH); in altre parole, il broncio \[ i \] = PA \[ i \] \* scalare.
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Funzione D3DXSHScale (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1a8cc7c63880876f85969443502db3d5fb3278c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132326"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="f8020-103">Funzione D3DXSHScale (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f8020-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="f8020-104">Ridimensiona un vettore armonico sferico (SH); in altre parole, il broncio \[ i \] = PA \[ i \] \* scalare.</span><span class="sxs-lookup"><span data-stu-id="f8020-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8020-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8020-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="f8020-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8020-107">*broncio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f8020-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8020-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8020-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8020-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="f8020-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="f8020-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="f8020-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f8020-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f8020-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8020-112">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f8020-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8020-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8020-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8020-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="f8020-114">Order of the SH evaluation.</span></span> <span data-ttu-id="f8020-115">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="f8020-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="f8020-116">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="f8020-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f8020-117">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="f8020-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8020-118">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8020-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8020-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8020-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8020-120">Puntatore al vettore SH da scalare.</span><span class="sxs-lookup"><span data-stu-id="f8020-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="f8020-121">*Ridimensiona* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8020-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8020-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8020-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8020-123">Puntatore al valore della scala.</span><span class="sxs-lookup"><span data-stu-id="f8020-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8020-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8020-124">Return value</span></span>

<span data-ttu-id="f8020-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8020-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8020-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="f8020-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8020-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8020-127">Remarks</span></span>

<span data-ttu-id="f8020-128">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="f8020-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="f8020-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="f8020-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="f8020-130">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="f8020-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8020-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8020-131">Requirements</span></span>



| <span data-ttu-id="f8020-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8020-132">Requirement</span></span> | <span data-ttu-id="f8020-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f8020-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8020-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8020-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f8020-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8020-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8020-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8020-136">Library</span></span><br/> | <dl> <span data-ttu-id="f8020-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8020-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8020-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8020-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8020-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="f8020-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f8020-140">Trasferimento Radiance pre-calcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f8020-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
