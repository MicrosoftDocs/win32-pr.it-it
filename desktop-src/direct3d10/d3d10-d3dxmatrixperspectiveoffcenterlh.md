---
description: 'Funzione D3DXMatrixPerspectiveOffCenterLH (D3DX10Math.h): crea una matrice di proiezione prospettica personalizzata e mancino.'
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: Funzione D3DXMatrixPerspectiveOffCenterLH (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1116e24b48c9090739511894d28031ca921ed6ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109049"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a><span data-ttu-id="c97eb-103">Funzione D3DXMatrixPerspectiveOffCenterLH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="c97eb-103">D3DXMatrixPerspectiveOffCenterLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="c97eb-104">Compila una matrice di proiezione prospettica personalizzata e mancino.</span><span class="sxs-lookup"><span data-stu-id="c97eb-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c97eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c97eb-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c97eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c97eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c97eb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c97eb-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c97eb-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c97eb-109">Puntatore alla [**struttura D3DXMATRIX**](d3d10-d3dxmatrix.md) che rappresenta il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c97eb-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97eb-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c97eb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c97eb-112">Valore x minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c97eb-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97eb-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c97eb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c97eb-115">Valore x massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c97eb-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97eb-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c97eb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c97eb-118">Valore y minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c97eb-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97eb-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c97eb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c97eb-121">Valore y massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c97eb-122">*zn* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97eb-123">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c97eb-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c97eb-124">Valore z minimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c97eb-125">*zf* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c97eb-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c97eb-126">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c97eb-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c97eb-127">Valore z massimo del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c97eb-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c97eb-128">Return value</span></span>

<span data-ttu-id="c97eb-129">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c97eb-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c97eb-130">Puntatore a una struttura D3DXMATRIX che è una matrice di proiezione prospettica personalizzata a sinistra.</span><span class="sxs-lookup"><span data-stu-id="c97eb-130">Pointer to a D3DXMATRIX structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c97eb-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="c97eb-131">Remarks</span></span>

<span data-ttu-id="c97eb-132">Tutti i parametri della funzione D3DXMatrixPerspectiveOffCenterLH sono distanze nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="c97eb-132">All the parameters of the D3DXMatrixPerspectiveOffCenterLH function are distances in camera space.</span></span> <span data-ttu-id="c97eb-133">I parametri descrivono le dimensioni del volume della vista.</span><span class="sxs-lookup"><span data-stu-id="c97eb-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c97eb-134">Il valore restituito per questa funzione è lo stesso valore restituito nel parametro pOut.</span><span class="sxs-lookup"><span data-stu-id="c97eb-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c97eb-135">In questo modo, la funzione D3DXMatrixPerspectiveOffCenterLH può essere usata come parametro per un'altra funzione.</span><span class="sxs-lookup"><span data-stu-id="c97eb-135">In this way, the D3DXMatrixPerspectiveOffCenterLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c97eb-136">Questa funzione usa la formula seguente per calcolare la matrice restituita.</span><span class="sxs-lookup"><span data-stu-id="c97eb-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="c97eb-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c97eb-137">Requirements</span></span>



| <span data-ttu-id="c97eb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c97eb-138">Requirement</span></span> | <span data-ttu-id="c97eb-139">Valore</span><span class="sxs-lookup"><span data-stu-id="c97eb-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c97eb-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c97eb-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c97eb-141"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c97eb-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c97eb-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="c97eb-142">Library</span></span><br/> | <dl> <span data-ttu-id="c97eb-143"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c97eb-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c97eb-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c97eb-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c97eb-145">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="c97eb-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
