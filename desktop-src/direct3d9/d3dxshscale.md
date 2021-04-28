---
description: 'Funzione D3DXSHScale (D3dx9math.h): ridimensiona un vettore armonico sferico (SH). in altre parole, pOut \[ i \] = pA i \[ \] \* Scale.'
ms.assetid: e7b08b55-e2e7-4f13-bbee-10b844d3ef91
title: Funzione D3DXSHScale (D3dx9math.h)
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
ms.openlocfilehash: 6a91c3ea1cb49c4c501ab847cb63fe8a39d66665
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093859"
---
# <a name="d3dxshscale-function-d3dx9mathh"></a><span data-ttu-id="c7e22-103">Funzione D3DXSHScale (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c7e22-103">D3DXSHScale function (D3dx9math.h)</span></span>

<span data-ttu-id="c7e22-104">Ridimensiona un vettore armonico sferico (SH). in altre parole, pOut \[ i \] = pA i \[ \] \* Scale.</span><span class="sxs-lookup"><span data-stu-id="c7e22-104">Scales a spherical harmonic (SH) vector; in other words, pOut\[i\] = pA\[i\]\*Scale.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e22-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7e22-105">Syntax</span></span>


```C++
FLOAT* D3DXSHScale(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_  const FLOAT *pIn,
  _In_  const FLOAT *Scale
);
```



## <a name="parameters"></a><span data-ttu-id="c7e22-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7e22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e22-107">*pOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c7e22-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e22-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7e22-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c7e22-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="c7e22-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="c7e22-110">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="c7e22-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c7e22-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="c7e22-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c7e22-112">*Ordine* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c7e22-112">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e22-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7e22-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7e22-114">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="c7e22-114">Order of the SH evaluation.</span></span> <span data-ttu-id="c7e22-115">Deve essere compreso nell'intervallo [tra D3DXSH \_ MINORDER](other-d3dx-constants.md) e D3DXSH \_ MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="c7e22-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c7e22-116">La valutazione genera coefficienti Order².</span><span class="sxs-lookup"><span data-stu-id="c7e22-116">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c7e22-117">Il grado di valutazione è Order - 1.</span><span class="sxs-lookup"><span data-stu-id="c7e22-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c7e22-118">*pIn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c7e22-118">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e22-119">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7e22-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c7e22-120">Puntatore al vettore SH da ridimensionare.</span><span class="sxs-lookup"><span data-stu-id="c7e22-120">Pointer to the SH vector to scale.</span></span>

</dd> <dt>

<span data-ttu-id="c7e22-121">*Ridimensionamento* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c7e22-121">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e22-122">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7e22-122">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c7e22-123">Puntatore al valore di scala.</span><span class="sxs-lookup"><span data-stu-id="c7e22-123">Pointer to the scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e22-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7e22-124">Return value</span></span>

<span data-ttu-id="c7e22-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7e22-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c7e22-126">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="c7e22-126">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e22-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7e22-127">Remarks</span></span>

<span data-ttu-id="c7e22-128">Ogni coefficiente della funzione di base Ylm viene archiviato nella posizione di memoria l I + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="c7e22-128">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="c7e22-129">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="c7e22-129">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="c7e22-130">m è l'indice della funzione di base per il valore l specificato ed è compreso tra -l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="c7e22-130">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e22-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7e22-131">Requirements</span></span>



| <span data-ttu-id="c7e22-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e22-132">Requirement</span></span> | <span data-ttu-id="c7e22-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c7e22-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e22-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7e22-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c7e22-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e22-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c7e22-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="c7e22-136">Library</span></span><br/> | <dl> <span data-ttu-id="c7e22-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7e22-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7e22-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7e22-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e22-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="c7e22-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c7e22-140">Trasferimento di radiance pre-ricalcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c7e22-140">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
