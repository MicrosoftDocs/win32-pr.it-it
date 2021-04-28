---
description: 'Funzione D3DXSHScale (D3DX10.h): ridimensiona un vettore sferico aricale (SH). in altre parole, pOut \[ i \] = pA i \[ \] \* Scale.'
ms.assetid: e323d238-f635-4780-982d-8798ba178f31
title: Funzione D3DXSHScale (D3DX10.h)
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
ms.openlocfilehash: 0fab96575e5542eaaed725a88f9ba52c3289a4ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108499"
---
# <a name="d3dxshscale-function-d3dx10h"></a><span data-ttu-id="db6b9-103">Funzione D3DXSHScale (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="db6b9-103">D3DXSHScale function (D3DX10.h)</span></span>

<span data-ttu-id="db6b9-104">Ridimensiona un vettore sferico aricale (SH). in altre parole, pOut \[ i \] = pA i \[ \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="db6b9-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db6b9-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_ const FLOAT *pIn,
  _In_ const FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="db6b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db6b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6b9-107">*pOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="db6b9-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6b9-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="db6b9-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db6b9-109">Puntatore ai coefficienti di output sferici armonici (SH).</span><span class="sxs-lookup"><span data-stu-id="db6b9-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="db6b9-110">La valutazione genera coefficienti Di ordine.</span><span class="sxs-lookup"><span data-stu-id="db6b9-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="db6b9-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="db6b9-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="db6b9-112">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="db6b9-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6b9-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db6b9-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db6b9-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="db6b9-114">Order of the SH evaluation.</span></span> <span data-ttu-id="db6b9-115">Deve essere compreso nell'intervallo da D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="db6b9-115">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="db6b9-116">La valutazione genera coefficienti Di ordine.</span><span class="sxs-lookup"><span data-stu-id="db6b9-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="db6b9-117">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="db6b9-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="db6b9-118">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="db6b9-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6b9-119">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="db6b9-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db6b9-120">Puntatore al vettore SH da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="db6b9-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="db6b9-121">*Scalabilità* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="db6b9-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6b9-122">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="db6b9-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="db6b9-123">Puntatore al valore della scala.</span><span class="sxs-lookup"><span data-stu-id="db6b9-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6b9-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db6b9-124">Return value</span></span>

<span data-ttu-id="db6b9-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="db6b9-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="db6b9-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="db6b9-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="db6b9-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="db6b9-127">Remarks</span></span>

<span data-ttu-id="db6b9-128">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="db6b9-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="db6b9-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="db6b9-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="db6b9-130">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="db6b9-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6b9-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db6b9-131">Requirements</span></span>



| <span data-ttu-id="db6b9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="db6b9-132">Requirement</span></span> | <span data-ttu-id="db6b9-133">Valore</span><span class="sxs-lookup"><span data-stu-id="db6b9-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db6b9-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db6b9-134">Header</span></span><br/>  | <dl> <span data-ttu-id="db6b9-135"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="db6b9-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="db6b9-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="db6b9-136">Library</span></span><br/> | <dl> <span data-ttu-id="db6b9-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="db6b9-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db6b9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db6b9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6b9-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="db6b9-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
