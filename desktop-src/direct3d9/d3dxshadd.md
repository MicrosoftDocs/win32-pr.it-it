---
description: 'Funzione D3DXSHAdd (D3dx9math.h): aggiunge due vettori sferici aricali (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .'
ms.assetid: 12775c90-ed9d-4931-a449-2571816dd079
title: Funzione D3DXSHAdd (D3dx9math.h)
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
ms.openlocfilehash: 7333d1803b9f7ea7b056ff78ffd053bd6086184b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117959"
---
# <a name="d3dxshadd-function-d3dx9mathh"></a><span data-ttu-id="1d560-103">Funzione D3DXSHAdd (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1d560-103">D3DXSHAdd function (D3dx9math.h)</span></span>

<span data-ttu-id="1d560-104">Aggiunge due vettori sferici aricali (SH). in altre parole, pOut \[ i \] = pA i + \[ \] pB i \[ \] .</span><span class="sxs-lookup"><span data-stu-id="1d560-104">Adds two spherical harmonic (SH) vectors; in other words, pOut\[i\] = pA\[i\] + pB\[i\].</span></span>

## <a name="syntax"></a><span data-ttu-id="1d560-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d560-105">Syntax</span></span>


```C++
FLOAT* D3DXSHAdd(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pA,
  _In_  const FLOAT *pB
);
```



## <a name="parameters"></a><span data-ttu-id="1d560-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d560-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d560-107">*pOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1d560-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d560-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d560-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d560-109">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="1d560-109">Pointer to SH output coefficients.</span></span> <span data-ttu-id="1d560-110">La valutazione genera coefficienti Di ordine.</span><span class="sxs-lookup"><span data-stu-id="1d560-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1d560-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1d560-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1d560-112">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1d560-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d560-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d560-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d560-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="1d560-114">Order of the SH evaluation.</span></span> <span data-ttu-id="1d560-115">Deve essere compreso nell'intervallo [da D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="1d560-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1d560-116">La valutazione genera coefficienti Di ordine.</span><span class="sxs-lookup"><span data-stu-id="1d560-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1d560-117">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="1d560-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1d560-118">*pA* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1d560-118">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d560-119">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1d560-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d560-120">Puntatore al primo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="1d560-120">Pointer to the first SH vector.</span></span>

</dd> <dt>

<span data-ttu-id="1d560-121">*pB* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1d560-121">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d560-122">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1d560-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d560-123">Puntatore al secondo vettore SH.</span><span class="sxs-lookup"><span data-stu-id="1d560-123">Pointer to the second SH vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d560-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d560-124">Return value</span></span>

<span data-ttu-id="1d560-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d560-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1d560-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="1d560-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d560-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d560-127">Remarks</span></span>

<span data-ttu-id="1d560-128">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="1d560-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="1d560-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="1d560-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="1d560-130">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="1d560-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d560-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d560-131">Requirements</span></span>



| <span data-ttu-id="1d560-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d560-132">Requirement</span></span> | <span data-ttu-id="1d560-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1d560-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d560-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d560-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1d560-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1d560-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1d560-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="1d560-136">Library</span></span><br/> | <dl> <span data-ttu-id="1d560-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d560-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d560-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d560-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d560-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="1d560-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1d560-140">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1d560-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
