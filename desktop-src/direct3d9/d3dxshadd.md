---
description: Aggiunge due vettori ad armonica sferica (SH); in altre parole, broncio \[ i \] = PA i \[ \] + PB \[ i \] .
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Funzione D3DXSHAdd (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b8f65a14cf745e8b378728d4fa6e0a234284d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322480"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="0938b-103">Funzione D3DXSHAdd (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0938b-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="0938b-104">Aggiunge due vettori ad armonica sferica (SH); in altre parole, broncio \[ i \] = PA i \[ \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="0938b-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="0938b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0938b-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="0938b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0938b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0938b-107">*broncio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0938b-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0938b-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0938b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0938b-109">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="0938b-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="0938b-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="0938b-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0938b-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="0938b-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0938b-112">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0938b-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0938b-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0938b-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0938b-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="0938b-114">Order of the SH evaluation.</span></span> <span data-ttu-id="0938b-115">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="0938b-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="0938b-116">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="0938b-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="0938b-117">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="0938b-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="0938b-118">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0938b-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0938b-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0938b-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0938b-120">Puntatore al primo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="0938b-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="0938b-121">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0938b-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0938b-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0938b-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0938b-123">Puntatore al secondo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="0938b-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0938b-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0938b-124">Return value</span></span>

<span data-ttu-id="0938b-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0938b-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0938b-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="0938b-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="0938b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0938b-127">Remarks</span></span>

<span data-ttu-id="0938b-128">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="0938b-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="0938b-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="0938b-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="0938b-130">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="0938b-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="0938b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0938b-131">Requirements</span></span>



| <span data-ttu-id="0938b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0938b-132">Requirement</span></span> | <span data-ttu-id="0938b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0938b-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0938b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0938b-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0938b-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0938b-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0938b-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="0938b-136">Library</span></span><br/> | <dl> <span data-ttu-id="0938b-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0938b-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0938b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0938b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0938b-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="0938b-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="0938b-140">Trasferimento Radiance pre-calcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0938b-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
