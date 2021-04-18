---
description: Compila una matrice di proiezione prospettica a sinistra
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: Funzione D3DXMatrixPerspectiveLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 400967b5e4a25244c50dbd6093fa2079700ba4eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323407"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="98499-103">Funzione D3DXMatrixPerspectiveLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="98499-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="98499-104">Compila una matrice di proiezione prospettica a sinistra</span><span class="sxs-lookup"><span data-stu-id="98499-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="98499-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98499-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="98499-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98499-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98499-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="98499-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="98499-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="98499-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="98499-109">Puntatore alla struttura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="98499-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="98499-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98499-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98499-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98499-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98499-112">Larghezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="98499-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="98499-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98499-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98499-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98499-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98499-115">Altezza del volume di visualizzazione nel piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="98499-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="98499-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98499-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98499-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98499-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98499-118">Valore Z del piano di visualizzazione vicino.</span><span class="sxs-lookup"><span data-stu-id="98499-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="98499-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98499-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98499-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98499-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98499-121">Valore Z del piano di visualizzazione lontano.</span><span class="sxs-lookup"><span data-stu-id="98499-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98499-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98499-122">Return value</span></span>

<span data-ttu-id="98499-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="98499-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="98499-124">Puntatore a una struttura D3DXMATRIX che rappresenta una matrice di proiezione prospettica a sinistra.</span><span class="sxs-lookup"><span data-stu-id="98499-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="98499-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="98499-125">Remarks</span></span>

<span data-ttu-id="98499-126">Tutti i parametri della funzione D3DXMatrixPerspectiveLH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="98499-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="98499-127">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="98499-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="98499-128">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro broncio.</span><span class="sxs-lookup"><span data-stu-id="98499-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="98499-129">In questo modo, la funzione D3DXMatrixPerspectiveLH può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="98499-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="98499-130">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="98499-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="98499-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98499-131">Requirements</span></span>



| <span data-ttu-id="98499-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="98499-132">Requirement</span></span> | <span data-ttu-id="98499-133">Valore</span><span class="sxs-lookup"><span data-stu-id="98499-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98499-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98499-134">Header</span></span><br/>  | <dl> <span data-ttu-id="98499-135"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="98499-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="98499-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="98499-136">Library</span></span><br/> | <dl> <span data-ttu-id="98499-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98499-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="98499-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98499-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98499-139">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="98499-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
