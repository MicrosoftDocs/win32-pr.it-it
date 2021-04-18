---
description: Calcola il prodotto scalare di due vettori a sferica armonica (SH).
ms.assetid: 30f0e858-4c31-4b25-9979-754d996a7d48
title: Funzione D3DXSHDot (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20f0896168dae0e2a779625c683777938c8e2df2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323197"
---
# <a name="d3dxshdot-function-d3dx10h"></a><span data-ttu-id="b3fbd-103">Funzione D3DXSHDot (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="b3fbd-103">D3DXSHDot function (D3DX10.h)</span></span>

<span data-ttu-id="b3fbd-104">Calcola il prodotto scalare di due vettori a sferica armonica (SH).</span><span class="sxs-lookup"><span data-stu-id="b3fbd-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3fbd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3fbd-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="b3fbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3fbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3fbd-107">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b3fbd-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fbd-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3fbd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3fbd-109">Ordine della valutazione dell'armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="b3fbd-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="b3fbd-110">Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="b3fbd-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b3fbd-111">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="b3fbd-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b3fbd-112">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="b3fbd-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b3fbd-113">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3fbd-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fbd-114">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3fbd-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b3fbd-115">Puntatore al primo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="b3fbd-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="b3fbd-116">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3fbd-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3fbd-117">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3fbd-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b3fbd-118">Puntatore al secondo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="b3fbd-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3fbd-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3fbd-119">Return value</span></span>

<span data-ttu-id="b3fbd-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3fbd-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3fbd-121">Coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="b3fbd-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3fbd-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3fbd-122">Remarks</span></span>

<span data-ttu-id="b3fbd-123">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="b3fbd-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="b3fbd-124">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="b3fbd-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="b3fbd-125">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="b3fbd-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3fbd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3fbd-126">Requirements</span></span>



| <span data-ttu-id="b3fbd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3fbd-127">Requirement</span></span> | <span data-ttu-id="b3fbd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b3fbd-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fbd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3fbd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b3fbd-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3fbd-130"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3fbd-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3fbd-131">Library</span></span><br/> | <dl> <span data-ttu-id="b3fbd-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3fbd-132"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3fbd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3fbd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fbd-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="b3fbd-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
