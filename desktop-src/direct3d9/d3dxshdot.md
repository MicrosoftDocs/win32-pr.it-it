---
description: Funzione D3DXSHDot (D3dx9math.h) - Calcola il prodotto del punto di due vettori armonici sferici (SH).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Funzione D3DXSHDot (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87f88c7c7b80871a68084607cb99621199dfcc0a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093929"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a><span data-ttu-id="12547-103">Funzione D3DXSHDot (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="12547-103">D3DXSHDot function (D3dx9math.h)</span></span>

<span data-ttu-id="12547-104">Calcola il prodotto del punto di due vettori armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="12547-104">Computes the dot product of two spherical harmonic (SH) vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="12547-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12547-105">Syntax</span></span>


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="12547-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12547-107">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="12547-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12547-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12547-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12547-109">Ordine della valutazione armonica sferica (SH).</span><span class="sxs-lookup"><span data-stu-id="12547-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="12547-110">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="12547-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="12547-111">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="12547-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="12547-112">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="12547-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="12547-113">*pA* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="12547-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12547-114">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="12547-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12547-115">Puntatore al primo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="12547-115">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="12547-116">*pB* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="12547-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12547-117">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="12547-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="12547-118">Puntatore al secondo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="12547-118">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12547-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12547-119">Return value</span></span>

<span data-ttu-id="12547-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12547-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12547-121">Coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="12547-121">SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="12547-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="12547-122">Remarks</span></span>

<span data-ttu-id="12547-123">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="12547-123">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="12547-124">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="12547-124">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="12547-125">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="12547-125">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="12547-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12547-126">Requirements</span></span>



| <span data-ttu-id="12547-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="12547-127">Requirement</span></span> | <span data-ttu-id="12547-128">Valore</span><span class="sxs-lookup"><span data-stu-id="12547-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12547-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12547-129">Header</span></span><br/>  | <dl> <span data-ttu-id="12547-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="12547-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="12547-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="12547-131">Library</span></span><br/> | <dl> <span data-ttu-id="12547-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="12547-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12547-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12547-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12547-134">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="12547-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="12547-135">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="12547-135">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
