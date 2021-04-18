---
description: Compila una matrice di proiezione prospettica personalizzata, a sinistra.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: Funzione D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322129"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="9a04e-103">Funzione D3DXMatrixPerspectiveOffCenterLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9a04e-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="9a04e-104">Compila una matrice di proiezione prospettica personalizzata, a sinistra.</span><span class="sxs-lookup"><span data-stu-id="9a04e-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a04e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a04e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="9a04e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a04e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a04e-107">*broncio* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="9a04e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a04e-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a04e-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9a04e-109">Puntatore alla struttura [**D3DXMATRIX**](d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9a04e-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a04e-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a04e-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a04e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a04e-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a04e-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a04e-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a04e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a04e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a04e-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a04e-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a04e-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a04e-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a04e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a04e-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a04e-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a04e-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a04e-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a04e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a04e-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a04e-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a04e-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a04e-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a04e-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a04e-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="9a04e-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a04e-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a04e-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a04e-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a04e-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a04e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a04e-128">Return value</span></span>

<span data-ttu-id="9a04e-129">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a04e-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9a04e-130">Puntatore a una struttura [**D3DXMATRIX**](d3dxmatrix.md) che è una matrice di proiezione prospettica personalizzata, a sinistra.</span><span class="sxs-lookup"><span data-stu-id="9a04e-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a04e-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a04e-131">Remarks</span></span>

<span data-ttu-id="9a04e-132">Tutti i parametri della funzione **D3DXMatrixPerspectiveOffCenterLH** sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="9a04e-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="9a04e-133">I parametri descrivono le dimensioni del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="9a04e-134">Il valore restituito per questa funzione corrisponde al valore restituito nel parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="9a04e-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9a04e-135">In questo modo, la funzione **D3DXMatrixPerspectiveOffCenterLH** può essere utilizzata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="9a04e-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="9a04e-136">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="9a04e-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="9a04e-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a04e-137">Requirements</span></span>



| <span data-ttu-id="9a04e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a04e-138">Requirement</span></span> | <span data-ttu-id="9a04e-139">Valore</span><span class="sxs-lookup"><span data-stu-id="9a04e-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a04e-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a04e-140">Header</span></span><br/>  | <dl> <span data-ttu-id="9a04e-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a04e-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9a04e-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a04e-142">Library</span></span><br/> | <dl> <span data-ttu-id="9a04e-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a04e-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a04e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a04e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a04e-145">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="9a04e-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9a04e-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="9a04e-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="9a04e-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="9a04e-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="9a04e-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="9a04e-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="9a04e-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="9a04e-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="9a04e-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="9a04e-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
