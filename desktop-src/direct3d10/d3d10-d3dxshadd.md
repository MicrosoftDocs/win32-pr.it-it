---
description: Aggiunge due vettori ad armonica sferica (SH); in altre parole, broncio \[ i \] = PA i \[ \] + PB \[ i \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Funzione D3DXSHAdd (D3DX10. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1750b473764daf030160adc42d258a1f911f5f16
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235155"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="d29c8-103">Funzione D3DXSHAdd (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="d29c8-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="d29c8-104">Aggiunge due vettori ad armonica sferica (SH); in altre parole, broncio \[ i \] = PA i \[ \] + PB \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="d29c8-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="d29c8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d29c8-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="d29c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d29c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d29c8-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d29c8-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d29c8-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d29c8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d29c8-109">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="d29c8-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="d29c8-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="d29c8-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d29c8-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d29c8-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d29c8-112">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d29c8-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d29c8-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d29c8-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d29c8-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="d29c8-114">Order of the SH evaluation.</span></span> <span data-ttu-id="d29c8-115">Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="d29c8-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d29c8-116">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="d29c8-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="d29c8-117">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="d29c8-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d29c8-118">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d29c8-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d29c8-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d29c8-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d29c8-120">Puntatore al primo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="d29c8-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="d29c8-121">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d29c8-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d29c8-122">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d29c8-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d29c8-123">Puntatore al secondo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="d29c8-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d29c8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d29c8-124">Return value</span></span>

<span data-ttu-id="d29c8-125">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d29c8-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d29c8-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="d29c8-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="d29c8-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="d29c8-127">Remarks</span></span>

<span data-ttu-id="d29c8-128">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="d29c8-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="d29c8-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="d29c8-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="d29c8-130">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="d29c8-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="d29c8-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d29c8-131">Requirements</span></span>



| <span data-ttu-id="d29c8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d29c8-132">Requirement</span></span> | <span data-ttu-id="d29c8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d29c8-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d29c8-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d29c8-134">Header</span></span><br/>  | <dl> <span data-ttu-id="d29c8-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d29c8-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d29c8-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="d29c8-136">Library</span></span><br/> | <dl> <span data-ttu-id="d29c8-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d29c8-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d29c8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d29c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d29c8-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="d29c8-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
