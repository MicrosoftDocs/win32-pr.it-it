---
description: Ruota il vettore armonico sferico (SH) nell'asse z in base all'angolo specificato.
ms.assetid: 1f471183-4c8e-4fa8-9a42-f6cc2bb1b0f2
title: Funzione D3DXSHRotateZ (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac13cff212aaabdd8a9586b88e3152779bcfaf85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401957"
---
# <a name="d3dxshrotatez-function-d3dx9mathh"></a><span data-ttu-id="76aab-103">Funzione D3DXSHRotateZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="76aab-103">D3DXSHRotateZ function (D3dx9math.h)</span></span>

<span data-ttu-id="76aab-104">Ruota il vettore armonico sferico (SH) nell'asse z in base all'angolo specificato.</span><span class="sxs-lookup"><span data-stu-id="76aab-104">Rotates the spherical harmonic (SH) vector in the z-axis by the given angle.</span></span>

## <a name="syntax"></a><span data-ttu-id="76aab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76aab-105">Syntax</span></span>


```C++
FLOAT* D3DXSHRotateZ(
  _Out_       FLOAT *pOut,
  _In_        UINT  Order,
  _In_        FLOAT Angle,
  _In_  const FLOAT *pIn
);
```



## <a name="parameters"></a><span data-ttu-id="76aab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="76aab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76aab-107">*broncio* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76aab-107">*pOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76aab-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="76aab-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76aab-109">Puntatore ai coefficienti di output armonici sferici (SH).</span><span class="sxs-lookup"><span data-stu-id="76aab-109">Pointer to Spherical harmonic (SH) output coefficients.</span></span> <span data-ttu-id="76aab-110">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="76aab-110">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="76aab-111">Questo puntatore non deve avere alias con *pin*.</span><span class="sxs-lookup"><span data-stu-id="76aab-111">This pointer should not alias with *pIn*.</span></span> <span data-ttu-id="76aab-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="76aab-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="76aab-113">*Ordine* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="76aab-113">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76aab-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76aab-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76aab-115">Ordine della valutazione SH.</span><span class="sxs-lookup"><span data-stu-id="76aab-115">Order of the SH evaluation.</span></span> <span data-ttu-id="76aab-116">Deve essere compreso tra [D3DXSH \_ MINORDER](other-d3dx-constants.md) \_ e D3DXSH MAXORDER, inclusi.</span><span class="sxs-lookup"><span data-stu-id="76aab-116">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="76aab-117">La valutazione genera coefficienti Order ².</span><span class="sxs-lookup"><span data-stu-id="76aab-117">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="76aab-118">Il livello della valutazione è Order-1.</span><span class="sxs-lookup"><span data-stu-id="76aab-118">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="76aab-119">*Angolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76aab-119">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76aab-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76aab-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76aab-121">Angolo di rotazione, in radianti.</span><span class="sxs-lookup"><span data-stu-id="76aab-121">Rotation angle in radians.</span></span> <span data-ttu-id="76aab-122">La rotazione viene eseguita intorno all'asse z.</span><span class="sxs-lookup"><span data-stu-id="76aab-122">The rotation is performed around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="76aab-123">*Aggiungi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76aab-123">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76aab-124">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="76aab-124">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76aab-125">Puntatore ai coefficienti SH ruotati.</span><span class="sxs-lookup"><span data-stu-id="76aab-125">Pointer to rotated SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76aab-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76aab-126">Return value</span></span>

<span data-ttu-id="76aab-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="76aab-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="76aab-128">Puntatore ai coefficienti di output SH.</span><span class="sxs-lookup"><span data-stu-id="76aab-128">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="76aab-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="76aab-129">Remarks</span></span>

<span data-ttu-id="76aab-130">Ogni coefficiente della funzione di base YLM viene archiviato in corrispondenza della posizione di memoria l ² + m + l, dove:</span><span class="sxs-lookup"><span data-stu-id="76aab-130">Each coefficient of the basis function Yₗₘ is stored at memory location l² + m + l, where:</span></span>

-   <span data-ttu-id="76aab-131">l è il grado della funzione di base.</span><span class="sxs-lookup"><span data-stu-id="76aab-131">l is the degree of the basis function.</span></span>
-   <span data-ttu-id="76aab-132">m è l'indice della funzione di base per il valore l specificato e viene compreso tra-l e l, inclusi.</span><span class="sxs-lookup"><span data-stu-id="76aab-132">m is the basis function index for the given l value and ranges from -l to l, inclusive.</span></span>

## <a name="requirements"></a><span data-ttu-id="76aab-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76aab-133">Requirements</span></span>



| <span data-ttu-id="76aab-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="76aab-134">Requirement</span></span> | <span data-ttu-id="76aab-135">Valore</span><span class="sxs-lookup"><span data-stu-id="76aab-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76aab-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76aab-136">Header</span></span><br/>  | <dl> <span data-ttu-id="76aab-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="76aab-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="76aab-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="76aab-138">Library</span></span><br/> | <dl> <span data-ttu-id="76aab-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76aab-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76aab-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76aab-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76aab-141">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="76aab-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="76aab-142">Trasferimento Radiance pre-calcolato (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="76aab-142">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
