---
description: Funzione D3DXSHAdd (D3DX10.h) - Aggiunge due vettori armonici armonici (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .
ms.assetid: dbfea12b-c110-42a7-84b6-0dff3d958032
title: Funzione D3DXSHAdd (D3DX10.h)
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
ms.openlocfilehash: 8d39940fef4ad611ea530d95efea29c74266d22a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108659"
---
# <a name="d3dxshadd-function-d3dx10h"></a><span data-ttu-id="2cb3d-103">Funzione D3DXSHAdd (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="2cb3d-103">D3DXSHAdd function (D3DX10.h)</span></span>

<span data-ttu-id="2cb3d-104">Aggiunge due vettori armoniosi sferici (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .</span><span class="sxs-lookup"><span data-stu-id="2cb3d-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb3d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cb3d-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="2cb3d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cb3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cb3d-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2cb3d-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb3d-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cb3d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2cb3d-109">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="2cb3d-110">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="2cb3d-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2cb3d-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2cb3d-112">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2cb3d-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb3d-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2cb3d-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2cb3d-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-114">Order of the SH evaluation.</span></span> <span data-ttu-id="2cb3d-115">Deve essere compreso nell'intervallo tra D3DXSH \_ MINORDER e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="2cb3d-116">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="2cb3d-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="2cb3d-117">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="2cb3d-118">*pA* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2cb3d-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb3d-119">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cb3d-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2cb3d-120">Puntatore al primo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="2cb3d-121">*pB* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2cb3d-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cb3d-122">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2cb3d-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2cb3d-123">Puntatore al secondo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cb3d-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cb3d-124">Return value</span></span>

<span data-ttu-id="2cb3d-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2cb3d-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2cb3d-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cb3d-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cb3d-127">Remarks</span></span>

<span data-ttu-id="2cb3d-128">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l I + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="2cb3d-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="2cb3d-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="2cb3d-130">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="2cb3d-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb3d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cb3d-131">Requirements</span></span>



| <span data-ttu-id="2cb3d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb3d-132">Requirement</span></span> | <span data-ttu-id="2cb3d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2cb3d-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb3d-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cb3d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2cb3d-135"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2cb3d-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cb3d-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="2cb3d-136">Library</span></span><br/> | <dl> <span data-ttu-id="2cb3d-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cb3d-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cb3d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cb3d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb3d-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="2cb3d-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
