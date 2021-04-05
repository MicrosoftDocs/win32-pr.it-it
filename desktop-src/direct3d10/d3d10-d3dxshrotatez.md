---
description: Ruota il vettore armonico sferico (SH) nell'asse z in base all'angolo specificato.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: Funzione D3DXSHRotateZ (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0348dd8dfed9b100f64c53427ca2b77dd48ccded
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969430"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a><span data-ttu-id="53f9f-103">Funzione D3DXSHRotateZ (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="53f9f-103">D3DXSHRotateZ function (D3DX10.h)</span></span>

<span data-ttu-id="53f9f-104">Ruota il vettore armonico sferico (SH) nell'asse z in base all'angolo specificato.</span><span class="sxs-lookup"><span data-stu-id="53f9f-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f9f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53f9f-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="53f9f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="53f9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f9f-107">*broncio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f9f-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9f-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53f9f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53f9f-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="53f9f-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="53f9f-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="53f9f-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="53f9f-111">Questo puntatore non deve avere alias con pIn.</span><span class="sxs-lookup"><span data-stu-id="53f9f-111">This pointer should not alias with pIn.</span></span> <span data-ttu-id="53f9f-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="53f9f-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53f9f-113">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="53f9f-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9f-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53f9f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53f9f-115">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="53f9f-115">Order of the SH evaluation.</span></span> <span data-ttu-id="53f9f-116">Deve essere compreso tra D3DXSH \_ MINORDER \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="53f9f-116">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="53f9f-117">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="53f9f-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="53f9f-118">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="53f9f-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="53f9f-119">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f9f-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9f-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53f9f-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53f9f-121">Angolo di rotazione, in radianti.</span><span class="sxs-lookup"><span data-stu-id="53f9f-121">Rotation angle in radians.</span></span> <span data-ttu-id="53f9f-122">La rotazione viene eseguita intorno all'asse z.</span><span class="sxs-lookup"><span data-stu-id="53f9f-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="53f9f-123">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53f9f-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f9f-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="53f9f-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53f9f-125">Puntatore ai coefficienti SH ruotati.</span><span class="sxs-lookup"><span data-stu-id="53f9f-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f9f-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53f9f-126">Return value</span></span>

<span data-ttu-id="53f9f-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53f9f-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53f9f-128">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="53f9f-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f9f-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="53f9f-129">Remarks</span></span>

<span data-ttu-id="53f9f-130">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="53f9f-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="53f9f-131">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="53f9f-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="53f9f-132">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="53f9f-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f9f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53f9f-133">Requirements</span></span>



| <span data-ttu-id="53f9f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f9f-134">Requirement</span></span> | <span data-ttu-id="53f9f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="53f9f-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53f9f-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53f9f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="53f9f-137"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f9f-137"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="53f9f-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="53f9f-138">Library</span></span><br/> | <dl> <span data-ttu-id="53f9f-139"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53f9f-139"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f9f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53f9f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f9f-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="53f9f-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
